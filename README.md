## 1.Install
composer require --prefer-dist lulubin/yii2-helper-qrcode "dev-master"

## 2.Usage
### Controller
```php
namespace app\controllers;
use lulubin\qrcode\QrCode;

class SiteController extends \yii\web\Controller
{
    public function actionQrcode($code_url)
    {
        return QRcode::png($code_url);
    }
}
```

### View
```
<?php 
use yii\helpers\Url;
?>
<img src="<?= Url::to(['/site/qrcode','code_url'=>'https://luluqi.cn'])?>" />
```