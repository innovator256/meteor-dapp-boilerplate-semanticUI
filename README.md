# meteor-dapp-boilerplate

A starting point for decentralized MeteorJS applications. Includes Ethereum.js, iron-router, Official Semantic UI Integration for Meteor, Font Awesome, LESS and more.

** Modification Based off of [SilentCicero's](https://github.com/SilentCicero/meteor-dapp-boilerplate) which is based on [Differential's meteor-boilerplate](https://github.com/Differential/meteor-boilerplate) and [Ethereum's meteor-dapp-wallet](https://github.com/ethereum/meteor-dapp-wallet). Please note that this boilerplate is still in Alpha.

* [Alpha](#alpha)
* [Included Packages](#included-packages)
* [Installation](#installation)
* [Deployment](#deployment)
* [File Structure](#file-structure)
* [Official Semantic UI and Less](#bootstrap-and-less)
* [Favicons and Touch Icons](#favicons-and-touch-icons)
* [Private Network](#private-network)
* [Unit Testing](#unit-testing)
* [License](#license)

## <a name="included-packages"></a> Included Packages

* Collections:
  * [dburles:collection-helpers](https://github.com/dburles/meteor-collection-helpers)
  * [matb33:collection-hooks](https://github.com/matb33/meteor-collection-hooks)
  * [reywood:publish-composite](https://github.com/englue/meteor-publish-composite)
  * [frozeman:persistent-minimongo](https://github.com/frozeman/meteor-persistent-minimongo)
* Router:
  * [iron:router](https://github.com/EventedMind/iron-router)
  * [zimme:iron-router-active](https://github.com/zimme/meteor-iron-router-active)
  * [yasinuslu:blaze-meta](https://github.com/yasinuslu/blaze-meta)
* [Theming and style]
  * [Official Semantic UI](http://semantic-ui.com/)
  * [Font Awesome](http://fontawesome.io)

* [Ethereum](http://ethereum.org)
  * [ethereum:elements](https://github.com/ethereum/meteor-package-elements)
  * [ethereum:tools](https://github.com/ethereum/meteor-package-tools)
  * [ethereum:js](https://github.com/ethereum/ethereum.js)
  * [ethereum:accounts](https://github.com/ethereum/meteor-package-accounts/)
  * [ethereum:blocks](https://github.com/ethereum/meteor-package-blocks/)
* Numbers:
  * [3stack:bignumber](https://github.com/MikeMcl/bignumber.js/)
  * [chance.js](http://chancejs.com/)
* Language:
  * [tap:i18n](https://github.com/TAPevents/tap-i18n)
* Unit Testing:
  * [mike:mocha](https://github.com/mad-eye/meteor-mocha-web/)
* Misc:
  * [Moment.js](http://momentjs.com/)
  * [chuangbo:cookie](https://github.com/chuangbo/meteor-cookie)
  * [Underscore.js](http://underscorejs.org/)
  * [Underscore.string](http://epeli.github.io/underscore.string/)
  * [frozeman:storage](https://github.com/frozeman/meteor-storage)
  * [frozeman:template-var](https://github.com/frozeman/meteor-template-var)
  * [frozeman:reactive-timer](https://github.com/frozeman/meteor-reactive-timer)


## <a name="installation"></a> Installation

Clone this repo

    $ git clone gitUrl ***

Create an account with geth (create a passphrase):

    $ geth account new

Start a local geth node instace (then hit 'enter' to promt passphrase input):

    $ geth --rpc --rpcaddr="0.0.0.0" --rpccorsdomain="*" --mine --unlock=0 --verbosity=5 --maxpeers=0 --minerthreads="4"

Start the app using Meteor

    $ cd meteor-dapp-boilerplate-semanticUI/app
    $ meteor
##<a name="Hosted-Alpha"></a>Hosted Alpha     

----
[meteor-semanticui-dapp Demo](meteor-semanticui-dapp-boilerplate.meteor.com) 

## <a name="file-structure"></a> File Structure

This file structure is largley modification of SilentCicero's boilerplate which in turn is based on Differentials boilerplate, but with client-only directories. Client-only files are stored in the `client` directory. The `public` directory is for publicly accessible assets such as images and fonts. The `i18n` directory is for language files.

## <a name="Semantic-ui-and-less"></a> Semantic-ui and LESS

Since flemay:less-autoprefixer compiles LESS files you don't need any other less package.

please see [Semantic-UI-Meteor docummentatio](https://github.com/Semantic-Org/Semantic-UI-Meteor) for file structure and other important directions


## <a name="favicons-and-touch-icons"></a> Favicons and Touch Icons

Upload your image to http://realfavicongenerator.net/ and place the resulting images in `public/images/favicons`

## <a name="private-network"></a> Private Network

If you would like to test your dApp with a local private Ethereum node, a `test-genesis.json` file is provided in the `app` folder. This is an example command line to run your own private network:

    $ geth --rpc --rpccorsdomain "*" --genesis test-genesis.json --networkid 1234 --mine --unlock 0

## <a name="unit-testing"></a> Unit Testing

All tests are stored in the `app/tests` directory. By default the [Mocha](https://mochajs.org/) testing framework is not installed, but some example tests are provided with this boilerplate. In order to activate Mocha/Velocity you must edit `app/.meteor/packages` and uncomment `#mike:mocha` to `mike:mocha`. A testing button will appear on the top right hand corner of your dApp. Remember to remove the mocha package for deployment and production.

Add Mocha/Velocity

    $ meteor add mike:mocha

Remove Mocha/Velocity

    $ meteor remove mike:mocha

Please refer to this page for more on unit testing in Meteor: https://velocity.readme.io/

## <a name="license"></a> License

Released under the MIT License, see LICENSE file.
