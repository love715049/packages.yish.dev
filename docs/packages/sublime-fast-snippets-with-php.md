# Sublime fast snippets with php

<svg role="img" width="120" height="120" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><title>Sublime Text icon</title><path 
fill="#272822"
d="M12 20.916h9.523c.598 0 1.094-.339 1.094-.75v-1.921c-.25.251-.646.408-1.094.408H2.479c-.445 0-.841-.157-1.095-.405v1.915c0 .413.49.75 1.095.75H12v.003zM12 22.369h10.443c.859 0 1.557-.516 1.557-1.148 0-.05-.008-.1-.016-.148l-1.605-17.01c-.051-.398-.355-.715-.695-.846L22.9 17.623v2.543c0 .569-.615 1.034-1.381 1.034H2.48c-.758 0-1.377-.469-1.377-1.034v-2.543L2.316 3.217c-.34.133-.645.45-.695.847L.015 21.068c-.012.051-.015.097-.015.15 0 .63.695 1.151 1.556 1.151H12zM21.383 2.965l-.029-.315c0-.021 0-.037-.004-.061l-.006-.07c-.061-.504-.475-.89-1.082-.89H3.735c-.604 0-1.016.384-1.08.885l-.003.076-.003.06-.03.314-1.23 14.661c0 .412.489.75 1.092.75h19.045c.602 0 1.09-.338 1.094-.75l-1.237-14.66zm-5.686 9.306c-.266.698-.878 1.196-1.545 1.5-.725.333-1.535.462-2.332.474-.844.012-1.695-.075-2.517-.27-.416-.094-.847-.207-1.241-.379-.354-.155-.645-.506-.637-.904.008-.404.299-.741.669-.888.387-.154.759-.09 1.137.045.84.29 1.731.411 2.619.381.505-.015 1.39-.285 1.248-1.067-.03-.173-.169-.416-.345-.58-.138-.137-.428-.271-.615-.32-.414-.113-.84-.198-1.26-.289-.846-.186-1.297-.326-2.047-.781-.661-.394-.803-.648-.905-1.24-.133-.775.246-1.389.87-1.859 1.395-1.06 2.732-1.023 4.381-.721.404.075.889.143 1.244.359.35.211.546.637.395 1.033-.141.375-.498.432-.885.39-.416-.044-.586-.154-.979-.228-.822-.15-1.125-.276-1.916-.051-.314.09-.74.389-.58.782.135.325.631.431.927.511.813.217 1.448.467 2.257.705.759.221 1.334.641 1.807 1.309.421.596.511 1.416.256 2.095l-.004-.005-.002-.002z"/></svg>

<p>
<script async defer src="https://buttons.github.io/buttons.js"></script>
<a class="github-button" href="https://github.com/Mombuyish/sublime-fast-snippets-with-php" data-show-count="true" aria-label="Star Mombuyish/sublime-fast-snippets-with-php on GitHub">Star</a>
</p>

Sublime snippets is powerful functions, customize some snippets to create PHP useful method and class.

## Installation

Changing directory to your sublime configure local:

ubuntu:
```
.config/sublime-text-3/Packages/User
```

mac:
```
~/Library/Application Support/Sublime Text 3/Packages/User
```

windows:
```
Sublime Text 3/Packages/User
```

and you can do `git clone`:

```
$ git clone https://github.com/Mombuyish/sublime-fast-snippets-with-php.git
```
or you can also download `.zip` and unzip, put in there.

## Usage

Here is customize shortcuts in sublime.

Support `tab` to previous/next slug.

As you can see, I add new functions , references by PHPStorm.

| shortcut  | function                             |
| --------- |--------------------------------------|
| _c        | build construct method               |
| class     | build class with namespace           |
| aclass    | build abstract class with namespace  |
| echo    | echo  |
| fore    | foreach  |
| forek    | foreach with key  |
| inc    | include  |
| inco    | include_once  |
| prif    | build private method   |
| prisf    | build private static method   |
| prof    | build protected method   |
| prosf    | build protected static method   |
| pubf    | build public method   |
| pubsf    | build public static method   |
| rqr    | require   |
| rqro    | require_once   |
| thr    | throw new...   |


## Notice
Those shortcuts are active `.php` file, Use `<?php` to define the file type.