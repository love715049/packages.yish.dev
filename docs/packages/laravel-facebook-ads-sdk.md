# LaravelFacebookAdsSdk
::: warning
This package was not maintenance.
:::

**update! facebook ads api 3.1 !**

<p>
<script async defer src="https://buttons.github.io/buttons.js"></script>
<a class="github-button" href="https://github.com/Mombuyish/LaravelFacebookAdsSdk" data-show-count="true" aria-label="Star Mombuyish/LaravelFacebookAdsSdk on GitHub">Star</a>
</p>

# Installation
``` bash
$ composer require yish/laravel-facebook-php-ads-sdk
```

## app.php
``` php
//Provider
Yish\LaravelFacebookAdsSdk\FacebookAdsServiceProvider::class,

//Facade
'FacebookAds' => Yish\LaravelFacebookAdsSdk\Facades\LaravelFacebookAdsSdk::class,
```

## config publish
``` bash
$ php artisan vendor:publish
```
.env
``` bash
FB_APP_ID=
FB_APP_SECRET=
```


# functions
Reference `FacebookAds\Object\Fields\AdAccountFields` consts.
``` php
FacebookAds::getAdAccountList($facebookToken, ['ACCOUNT_ID', 'BUSINESS']);
```
or you can do on string for one.
``` php
FacebookAds::getAdAccountList($facebookToken, 'ACCOUNT_ID');
```

Reference `FacebookAds\Object\Fields\CampaignFields` consts.
``` php
FacebookAds::getCampaignList($facebookToken, $account_id, ['OBJECTIVE', 'NAME']);
```
or you can do on string for one.
``` php
FacebookAds::getCampaignList($facebookToken, $account_id, 'OBJECTIVE');
```

Reference `FacebookAds\Object\Fields\AdInsightsFields` consts.

By default.
``` php
//DEFAULT:$parameters = ['IMPRESSIONS', 'SPEND'], $preset = 'last_30_days', $time_range = null, $amount = 50
FacebookAds::getInsightList($userFbToken, $type, $ids);
```
Example:
``` php
FacebookAds::getInsightList($userFbToken, $type, $ids, 'last_month');
FacebookAds::getInsightList($userFbToken, $type, $ids, null, ['2015-01-01', '2015-03-01']);

//Note
date_preset: his field is ignored if time_range or time_ranges is specified.
FacebookAds::getInsightList($userFbToken, $type, $ids, 'last_month', ['2015-01-01', '2015-03-01']); //you will get '2015-01-01', '2015-03-01' data.
```
or you can do on string for one.
``` php
FacebookAds::getInsightList($userFbToken, $type, $ids, 'COST_PER_UNIQUE_CLICK');
$type = [
    'adaccount',
    'campaign',
    'adset',
    'ad',
];

//$preset @see https://developers.facebook.com/docs/marketing-api/reference/ad-campaign/insights/
```

# Exceptions
I add `LaravelFacebookAdsSdkException` to handle exceptions.
You can handle it in `App\Exceptions` handler.php
``` php
if ( $e instanceof LaravelFacebookAdsSdkException ) {
    return respond($e->getMessage(), $e->getCode());
}
```

# Transform
Transform AdAccount status you can call this:
``` php
FacebookAds::transAdAccountStatus($adaccount_status);
```
[reference](https://developers.facebook.com/docs/marketing-api/reference/ad-account/#Reading)
::: tip
//account_status, Status of the account 
* 1 = ACTIVE
* 2 = DISABLED
* 3 = UNSETTLED
* ....
:::

Transform DisableReason  status you can call this:
``` php
FacebookAds::transDisableReason($disable_reason);
```
[reference](https://developers.facebook.com/docs/marketing-api/reference/ad-account/#Reading)
::: tip
* 0 = NONE
* 1 = ADS_INTEGRITY_POLICY
* 2 = ADS_IP_REVIEW
* 3 = RISK_PAYMENT
* 4 = GRAY_ACCOUNT_SHUT_DOWN
* 5 = ADS_AFC_REVIEW
:::
