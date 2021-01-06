---
title: 应用评分
template: 企业插件
version: 1.5.0
minor: 1.5.X
---

评分插件帮助你提醒用户评价你的应用，立即，之后或者永不。

<native-ent-install plugin-id="app-rate" variables=""></native-ent-install>


## 索引

### 类

* [AppRate](#apprate)

### 接口

* [AppRateCallbacks](#appratecallbacks)
* [AppRateCustomLocale](#appratecustomlocale)
* [AppRatePreferences](#appratepreferences)
* [AppUrls](#appurls)

---

## 类

<a id="apprate"></a>

### AppRate

**AppRate**:

*__名称__*: App Rate

*__描述__*: 评分插件帮助你提醒用户评价你的应用，立即，之后或者永不。

*__用法__*:
 ```typescript
import { AppRate } from '@ionic-enterprise/app-rate/ngx';

constructor(private appRate: AppRate) { }

...
// 设置特定首选项
this.appRate.preferences.storeAppURL = {
  ios: '<app_id>',
  android: 'market://details?id=<package_name>',
  windows: 'ms-windows-store://review/?ProductId=<store_id>'
}

this.appRate.promptForRating(true);

// 或者，重写设定
this.appRate.preferences = {
  usesUntilPrompt: 3,
  storeAppURL: {
   ios: '<app_id>',
   android: 'market://details?id=<package_name>',
   windows: 'ms-windows-store://review/?ProductId=<store_id>'
  }
}

this.appRate.promptForRating(false);
```

*__接口__*: AppRatePreferences AppUrls AppRateCallbacks AppRateCustomLocal

<a id="apprate.preferences"></a>

### 设定

**● preferences**: *[AppRatePreferences](#appratepreferences)*

配置评分插件 参考以下表格设定项

___

<a id="apprate.navigatetoappstore"></a>

### navigateToAppStore

▸ **navigateToAppStore**(): `void`

立即将用户导向应用商店评分页面

**Returns:** `void`

___

<a id="apprate.promptforrating"></a>

### promptForRating

▸ **promptForRating**(immediately: *`boolean`*): `void`

提示用户进行评分

**参数:**

| 名称 | 类型   | 描述       |
| -- | ---- | -------- |
| 立即 | `布尔` | 立即弹出评分提示 |

**Returns:** `void`

___

___

## 接口

<a id="appratecallbacks"></a>

### AppRateCallbacks

**AppRateCallbacks**: 

<a id="appratecallbacks.handlenegativefeedback"></a>

### `<Optional>` handleNegativeFeedback

**● handleNegativeFeedback**: *`Function`*

回调函数 当用户点击了负面反馈，函数被唤起。

___

<a id="appratecallbacks.onbuttonclicked"></a>

### `<Optional>` onButtonClicked

**● onButtonClicked**: *`Function`*

回调函数 当用户点击评价弹窗的按钮时，函数被唤起

___

<a id="appratecallbacks.onratedialogshow"></a>

### `<Optional>` onRateDialogShow

**● onRateDialogShow**: *`Function`*

call back function. called when rate-dialog showing

___

___

<a id="appratecustomlocale"></a>

### AppRateCustomLocale

**AppRateCustomLocale**: 

<a id="appratecustomlocale.appratepromptmessage"></a>

### `<Optional>` appRatePromptMessage

**● appRatePromptMessage**: *`string`*

Feedback prompt message

___

<a id="appratecustomlocale.apprateprompttitle"></a>

### `<Optional>` appRatePromptTitle

**● appRatePromptTitle**: *`string`*

App rate prompt title

___

<a id="appratecustomlocale.cancelbuttonlabel"></a>

### `<Optional>` cancelButtonLabel

**● cancelButtonLabel**: *`string`*

Cancel button label

___

<a id="appratecustomlocale.feedbackpromptmessage"></a>

### `<Optional>` feedbackPromptMessage

**● feedbackPromptMessage**: *`string`*

Feedback prompt message

___

<a id="appratecustomlocale.feedbackprompttitle"></a>

### `<Optional>` feedbackPromptTitle

**● feedbackPromptTitle**: *`string`*

Feedback prompt title

___

<a id="appratecustomlocale.laterbuttonlabel"></a>

### `<Optional>` laterButtonLabel

**● laterButtonLabel**: *`string`*

Later button label

___

<a id="appratecustomlocale.message"></a>

### `<Optional>` message

**● message**: *`string`*

Message

___

<a id="appratecustomlocale.nobuttonlabel"></a>

### `<Optional>` noButtonLabel

**● noButtonLabel**: *`string`*

No button label

___

<a id="appratecustomlocale.ratebuttonlabel"></a>

### `<Optional>` rateButtonLabel

**● rateButtonLabel**: *`string`*

Rate button label

___

<a id="appratecustomlocale.title"></a>

### `<Optional>` title

**● title**: *`string`*

Title

___

<a id="appratecustomlocale.yesbuttonlabel"></a>

### `<Optional>` yesButtonLabel

**● yesButtonLabel**: *`string`*

Yes button label

___

___

<a id="appratepreferences"></a>

### AppRatePreferences

**AppRatePreferences**: 

<a id="appratepreferences.callbacks"></a>

### `<Optional>` callbacks

**● callbacks**: *[AppRateCallbacks](#appratecallbacks)*

Callbacks for events

___

<a id="appratepreferences.customlocale"></a>

### `<Optional>` customLocale

**● customLocale**: *[AppRateCustomLocale](#appratecustomlocale)*

Custom locale object

___

<a id="appratepreferences.displayappname"></a>

### `<Optional>` displayAppName

**● displayAppName**: *`string`*

Custom application title

___

<a id="appratepreferences.inappreview"></a>

### `<Optional>` inAppReview

**● inAppReview**: *`boolean`*

leave app or no when application page opened in app store (now supported only for iOS). Defaults to `false`

___

<a id="appratepreferences.promptagainforeachnewversion"></a>

### `<Optional>` promptAgainForEachNewVersion

**● promptAgainForEachNewVersion**: *`boolean`*

Show dialog again when application version will be updated. Defaults to `true`

___

<a id="appratepreferences.simplemode"></a>

### `<Optional>` simpleMode

**● simpleMode**: *`boolean`*

Simple Mode to display the rate dialog directly and bypass negative feedback filtering flow

___

<a id="appratepreferences.storeappurl"></a>

### `<Optional>` storeAppURL

**● storeAppURL**: *[AppUrls](#appurls)*

App Store URLS

___

<a id="appratepreferences.usecustomratedialog"></a>

### `<Optional>` useCustomRateDialog

**● useCustomRateDialog**: *`boolean`*

use custom view for rate dialog. Defaults to `false`

___

<a id="appratepreferences.uselanguage"></a>

### `<Optional>` useLanguage

**● useLanguage**: *`string`*

Custom BCP 47 language tag

___

<a id="appratepreferences.usesuntilprompt"></a>

### `<Optional>` usesUntilPrompt

**● usesUntilPrompt**: *`number`*

count of runs of application before dialog will be displayed. Defaults to `3`

___

___

<a id="appurls"></a>

### AppUrls

**AppUrls**: 

<a id="appurls.android"></a>

### `<Optional>` android

**● android**: *`string`*

application URL in GooglePlay

___

<a id="appurls.blackberry"></a>

### `<Optional>` blackberry

**● blackberry**: *`string`*

application URL in AppWorld

___

<a id="appurls.ios"></a>

### `<Optional>` ios

**● ios**: *`string`*

application id in AppStore

___

<a id="appurls.windows"></a>

### `<Optional>` windows

**● windows**: *`string`*

application URL in Windows Store

___

<a id="appurls.windows8"></a>

### `<Optional>` windows8

**● windows8**: *`string`*

application URL in WindowsStore

___

___

# Changelog

- 1.5.0
  - [PR #253](https://github.com/pushandplay/cordova-plugin-apprate/pull/253) - Remove iOS rating counter in favor of native approach
  - [PR #252](https://github.com/pushandplay/cordova-plugin-apprate/pull/252) - Postpone initial AppRate.init() until `deviceready`
  - [PR #239](https://github.com/pushandplay/cordova-plugin-apprate/pull/239) - Remove inappbrowser dependency adding support to choose between inappbrowser and safariviewcontroller
  - [PR #244](https://github.com/pushandplay/cordova-plugin-apprate/pull/244) - Use ES5 var instead of ES6 const for better browser compatibility
  - [PR #231](https://github.com/pushandplay/cordova-plugin-apprate/pull/231) - Displaying store view page before it loads for improved UX
  - [PR #228](https://github.com/pushandplay/cordova-plugin-apprate/pull/228) - Add native support for windows platform rating
  - [PR #220](https://github.com/pushandplay/cordova-plugin-apprate/pull/220) - Remove dependency on deprecated cordova-plugin-globalization in favor of browser `Intl` api
  - Various language fixes and improvements
  - [View All Merged PR's](https://github.com/pushandplay/cordova-plugin-apprate/compare/v1.4.0...master)

- 1.4.0
  - [Merged PR's](https://github.com/pushandplay/cordova-plugin-apprate/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Aclosed+merged%3A2017-06-24..2018-06-13)
  - [PR #211](https://github.com/pushandplay/cordova-plugin-apprate/pull/211) - Use NativeStorage for persistance across installs
  - Breaking Change - Instead of directly asking our users to Rate our app, we now handle this flow much better. The first popup will be "Do you like using appName?" If the user says 'Yes' then we ask the user if they would like take a moment and rate our app. If the user says 'NO', We ask the user another question: "Would you mind providing us feedback?" If the user says yes, then we can run a custom callback to handle this such as sending an email. To revert to previous behaviour you can use `simpleMode: true`
  - iOS 9+ now redirects directly to write review
  - iOS 10.3+ now supports In-App Reviews. One limitation to note is you can only prompt the user 3 times per year before it must fallback to the old open review in store. The preference option to disable this feature is called `inAppReview` and defaults to true, this option was previously named `openStoreInApp` and defaulted to false.

- 1.3.0
  - Added a general done callbacks called once we have completed the job, not showing or showing the popup
  - Fix %@ with customLocale
  - Fix bugs with callbacks
  - Fix deep links on ios 9+
  - Locales updates

- 1.2.1
  - Align the version in the package.json and the plugin.xml

- 1.2.0
  - Remove coffeescript to remove barrier of entry to contributions
  - Remove docs generation, just use the readme instead
  - Improve readme
  - Add Windows support from PR #120
  - Fix JSON parse for Android 2.x as per PR #73
  - Remove InAppBrowser dependency
  - Add/Improve Locales

- 1.1.12
  - Bump version to be higher than the previous `cordova-plugin-apprate` on the NPM registry
  - Clean up readme

- 1.1.9
  - Update id to `cordova-plugin-apprate` and update dependencies
  - Add finnish locale