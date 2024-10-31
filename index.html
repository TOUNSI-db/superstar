<?php
session_start();
require_once '../app/lib/Core.php';
require_once '../vendor/autoload.php';
// Generate a CSRF token if it doesn't exist
if (!isset($_SESSION['csrf_tokens'])) {
    $_SESSION['csrf_tokens'] = [];
}

// Generate a new CSRF token
$token = bin2hex(random_bytes(32));
$_SESSION['csrf_tokens'][$token] = time();
// Remove expired CSRF tokens
$expiryTime = time() - (60 * 60); // Tokens older than 1 hour are considered expired
foreach ($_SESSION['csrf_tokens'] as $key => $value) {
    if ($value < $expiryTime) {
        unset($_SESSION['csrf_tokens'][$key]);
    }
}

$databaseConnection = new DatabaseConnection(SQL_HOST, SQL_DATABASE_AUTH, SQL_USER, SQL_PASSWORD);
$conn = $databaseConnection->getConnection();

$app = new Core($conn,CAPTCHA['secret']);

$result = $app->handleSignUp();
//check account verify
$app->verifyAccount();
//load server status
$app->getServerStatus();
//load rank table

//check if a post request has been issued

?>
<!doctype html>
<html lang="ar" xmlns="http://www.w3.org/1999/xhtml" dir="rtl">
<head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#050d1c">
    <meta name="description" content="سيرفر أمل الشعوب خاص مميز Super Star">
    <meta name="keywords" content="Super Star,rappelz,private server ,mmorpg,أمل الشعوب , سيرفر">
    <meta property="og:title" content="<?php echo TITLE; ?>" />
    <meta property="og:type" content="website">
    <meta property="og:image" content="<?php $app->getLink('assets/imgs/pub.jpg'); ?>">
    <meta property="og:description" content="سيرفر أمل الشعوب خاص مميز Super Star">
    <meta property="og:locale" content="ar">
    <meta http-equiv="Content-Language" content="ar"/>
    <meta charset="UTF-8">
    <link rel="shortcut icon" href="<?php $app->getLink('assets/imgs/favicon.ico'); ?>">
    <link rel="icon" href="<?php $app->getLink('assets/imgs/favicon_32.png'); ?>" sizes="32x32">
    <link rel="icon" href="<?php $app->getLink('assets/imgs/favicon_48.png'); ?>" sizes="48x48">
    <link rel="icon" href="<?php $app->getLink('assets/imgs/favicon_96.png'); ?>" sizes="96x96">
    <link rel="icon" href="<?php $app->getLink('assets/imgs/favicon_144.png'); ?>" sizes="144x144">
    <link rel="apple-touch-icon" href="<?php $app->getLink('assets/imgs/favicon.ico'); ?>" />
    <meta name="msapplication-TileImage" content="<?php $app->getLink('assets/imgs/favicon.ico'); ?>" />
    <title><?php echo TITLE; ?></title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" crossorigin="anonymous">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <link href="<?php $app->getLink('assets/library/awesome/css/all.min.css') ?>" rel="stylesheet" crossorigin="anonymous">
    <link href="<?php $app->getLink('assets/css/main.min.css') ?>" rel="stylesheet" crossorigin="anonymous">
    <link href="<?php $app->getLink('assets/css/ar.min.css') ?>" rel="stylesheet" crossorigin="anonymous">
</head>
<body>
<?php
if ($app->isVerify){
?>
<div class="modal fade" id="staticBackdrop" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="staticBackdropLabel">تأكيد الحساب</h5>
                <button type="button" class="btn-close left" style="margin: 0" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body">
                <div class="alert alert-success my-5" role="alert">
                    <h4 class="alert-heading"><i class="fas fa-check fa-fw fa-lg" aria-hidden="true" style="color: #23c123"></i>
                       مرحبا بك يا نجم !
                    </h4>
                    <p>حسابك الآن فعال وبإمكان الآن الدخول وبدء مغامرتك معنا</p>

                </div>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">موافق</button>
            </div>
        </div>
    </div>
</div>
<?php }?>
<!--main app section-->
<div id="app">
    <div id="main-wrapper">
<!--    main navbar section-->
    <div id="main-nav">
        <div id="main-nav-wrapper">
            <div id="nav-drop-down" class="left nav-sep-right">
                <button id="nav-drop-btn" class="nav-drop-menu light-e">المزيد <i class="fas fa-chevron-down fa-fw fa-2xs me-4" aria-hidden="true"></i></button>
                <div id="nav-drop-menu-list" style="display: none">
                    <a href="<?php $app->getLink(''); ?>" class="nav-element-sub light-e"><i class="fas fa-home fa-fw fa-xs" aria-hidden="true"></i> الرئيسية </a>
                    <a href="#download" class="nav-element-sub light-e"><i class="fas fa-download fa-fw fa-xs" aria-hidden="true"></i> تحميل اللعبة </a>
                    <a href="#ranking" class="nav-element-sub light-e"><i class="fas fa-trophy fa-fw fa-xs" aria-hidden="true"></i> أفضل اللاعبين </a>
                    <a href="<?php echo DISCORD; ?>" target="_blank" class="nav-element-sub light-e"><i class="fab fa-discord fa-fw fa-xs" aria-hidden="true"></i> ديسكورد </a>
                    <a href="#signup" class="nav-element-sub light-e"><i class="fas fa-user-plus fa-fw fa-xs mx-1" aria-hidden="true"></i> حساب جديد </a>
                </div>
            </div>
            <div class="nav-logo right light-e nav-sep"></div>
            <a href="<?php $app->getLink(''); ?>" class="nav-element right nav-sep"><i class="fas fa-home fa-fw fa-xs" aria-hidden="true"></i> الرئيسية </a>
            <a href="#download" class="nav-element right nav-sep"><i class="fas fa-download fa-fw fa-xs" aria-hidden="true"></i> تحميل اللعبة </a>
            <a href="#ranking" class="nav-element right nav-sep"><i class="fas fa-trophy fa-fw fa-xs" aria-hidden="true"></i> أفضل اللاعبين </a>
            <a href="<?php echo DISCORD; ?>" target="_blank" class="nav-element right nav-sep"><i class="fab fa-discord fa-fw fa-xs" aria-hidden="true"></i> ديسكورد </a>
            <a href="#signup" class="nav-element-signup left nav-sep-right light-e"><i class="fas fa-user-plus fa-fw fa-xs mx-1" aria-hidden="true"></i> حساب جديد </a>
        </div>
    </div>
    <div id="main-sub-nav">
        <div class="main-status-wrapper left">
            <div class="status-element right">
                <i class="fas fa-power-off fa-fw fa-xs ms-1" aria-hidden="true"></i> حالة السيرفر
                <b class="status-stat me-2" id="server-status" data-status="<?php echo $app->serverStatus; ?>"><?php echo strtoupper($app->serverStatus);?></b>
            </div>
            <div class="main-status-sep right mx-2"></div>
            <div class="status-element right">
                <i class="fas fa-users fa-fw fa-xs ms-1" aria-hidden="true"></i>  عدد المتصلين
                <b class="status-stat me-2" id="server-status" data-status="count"><?php echo $app->playerCount; ?></b>
            </div>
        </div>
    </div>
<!--    Welcome Message Section-->
    <div id="welcome" data-aos="fade-up" data-aos-duration="1500"  data-aos-easing="ease-out-sine">
        <div class="welcome-img right"></div>
        <div class="welcome-content left">
            <h3 class="title-content mb-4">
                حيث للنجوم مكان واحد يجمعهم
            <p class="description-content mb-5">
                <br>
          سيرفر سوبر ستار يقدم
تجربة اللعبة دون الحاجة للشحن ابرز نفسك بين باقية اللاعبين عن طريق		 <br>
             التجربة الفريدة بعالم النجوم	
			
            </p>
            <div id="welcome-links" class="py-5">
                <a href="#signup" class="simple-link left light-e">سجل الآن</a>
                <a href="#download" class="simple-link right light-e">حمل اللعبة</a>
            </div>
        </div>
    </div>
<!--    Download Links Section-->
    <div id="download" class="my-5" data-aos="fade-up" data-aos-duration="1500"  data-aos-easing="ease-out-sine">
        <div class="download-img left"></div>
        <div class="download-content right">
            <h3 class="title-content mb-4">
                <i class="fas fa-download fa-fw fa-xs" aria-hidden="true"></i>
               تحميل اللعبة
            </h3>
            <?php
            foreach (DOWNLOAD_LINKS as $lnk){
                echo '<div class="download-element-wrapper my-5">
                <div class="download-element right">
                    <h3 class="download-head">'.$lnk['title'].'</h3>
                    <p class="download-body">'.$lnk['description'].'</p>
                </div>
                <div class="download-link">
                    <a href="'.$lnk['link'].'" target="_blank" class="main-button left">تحميل</a>
                </div>
            </div>';
            }
            ?>
        </div>
    </div>
<!--    Signup section -->
    <div id="signup" class="my-5" data-aos-anchor-placement="top-center" data-aos="fade-up" data-aos-duration="1500"  data-aos-easing="ease-out-sine">
        <h3 class="title-content mb-4">
            <i class="fas fa-user-plus fa-fw fa-xs" aria-hidden="true"></i>
           إنشاء حساب جديد
        </h3>
        <div id="signup-wrapper">
            <?php
            $alertDisplay = isset($result['head']) ? 'block' : 'none';
            $usernameDisplay = isset($result['username']) ? '' : $app->username ;
            $emailDisplay = isset($result['email']) ? '':$app->email;
            $passwordDisplay = isset($result['password']) ? '' : $app->password;
            $usernameError = isset($result['username']) ? 'on':'';
            $emailError = isset($result['email']) ? 'on':'';
            $passwordError = isset($result['password']) ? 'on':'';
            $rePasswordError = isset($result['re-password']) ? 'on':'';
            $reCaptchaError = isset($result['re-captcha']) ? 'is-invalid':'';
            if (isset($result['success'])){
                $usernameDisplay ='';
                $emailDisplay = '';
                $passwordDisplay = '';
            }
            if (!isset($result['success'])){
            ?>
            <p class="middle-message my-4">
              قم بملء البينات أسفله لإتمام عملية تسجيلك معنا
            </p>
            <div id="system-alert" class="my-4">
                <div class="alert alert-danger" style="display: <?php echo $alertDisplay; ?>" role="alert">
                    <?php
                    $temp = ['head','username','email','password','re-password','re-captcha'];
                    foreach ($temp as $val){
                        if (isset($result[$val])){
                            echo $result[$val].'<br>';
                        }
                    }
                    ?>
                </div>
            </div>
            <div id="main-form">
                <form action="#signup" method="POST">
                    <input type="hidden" name="csrf_token" value="<?php echo $token; ?>">
                <div class="main-input my-5" data-error="<?php echo $usernameError; ?>">
                    <label for="username"><i class="fas fa-user fa-fw fa-xs" aria-hidden="true"></i>
                        إسم المستخدم
                    </label>
                    <input type="text" id="username" name="username" placeholder="" value="<?php echo $usernameDisplay; ?>" required>
                </div>
                <div class="main-input my-5" data-error="<?php echo $emailError; ?>">
                    <label for="email"><i class="fas fa-envelope fa-fw fa-xs" aria-hidden="true"></i>
                      البريد الإكتروني
                    </label>
                    <input type="email" id="email" name="email" placeholder="" value="<?php echo $emailDisplay; ?>" required>
                </div>
                <div class="main-input my-5" data-error="<?php echo $passwordError; ?>">
                    <label for="password"><i class="fas fa-lock fa-fw fa-xs" aria-hidden="true"></i>
                       كلمة المرور
                    </label>
                    <input type="password" id="password" name="password" placeholder="" value="<?php echo $passwordDisplay; ?>" required>
                </div>
                <div class="main-input my-5" data-error="<?php echo $rePasswordError; ?>">
                    <label for="re_password"><i class="fas fa-lock-alt fa-fw fa-xs" aria-hidden="true"></i>
                       تأكيد كلمة المرور
                    </label>
                    <input type="password" id="re_password" name="re_password" placeholder="">
                </div>
                <div class="main-check my-5">
                    <div class="cf-turnstile" data-language="ar" data-size="normal" data-theme="dark" data-sitekey="<?php echo CAPTCHA['public']; ?>" data-callback="javascriptCallback"></div>
                </div>

                <div class="main-btn">
                    <button class="main-button" style="margin: 0 auto">تسجيل</button>
                </div>
                </form>
            </div>
                <?php
            }else{
                ?>
                <div class="alert alert-success my-5" role="alert">
                    <h4 class="alert-heading"><i class="fas fa-check fa-fw fa-lg" aria-hidden="true" style="color: #23c123"></i>
                    تم إنشاء حسابك !
                    </h4>
                    <p>لقد قمنا بإنشاء حسابك بنجاح ، تحتاج الآن إلى تأكيد حسابك كي تتمكن من الدخول معنا .</p>
                    <hr>
                    <p class="mb-0">تم إرسال رسالة خاصة إلى البريد : <b><?php echo $app->email; ?></b> الرجاء الضغط على الرابط المرفق ليتم التحقق من حسابك .</p>
                </div>
                <?php
            }
            ?>
        </div>
    </div>
<!--    Ranking Section-->
    <div id="ranking" data-aos="fade-up" data-aos-duration="1500"  data-aos-easing="ease-out-sine">
        <h3 class="title-content mb-4 ms-5 right">
            <i class="fas fa-user-plus fa-fw fa-xs" aria-hidden="true"></i>
            ترتيب اللاعبين
        </h3>
        <button class="rank-btn right" rank-select="on">اللفل</button>
        <button class="rank-btn right" rank-select="off">النمط</button>

        <div class="rank-table my-5">
            <ul class="rank-head">
                <li class="rank-id right">#</li>
                <li class="rank-name right">الإسم</li>
                <li class="rank-job right" style="line-height: 60px!important;height: 60px!important;">الإختصاص</li>
                <li class="rank-level right">المستوى</li>
                <li class="rank-status right">الحالة</li>
            </ul>
            <?php
            $rLv = $app->getPlayers();
            foreach($rLv as $rnk=>$lv){
                $clr =  ($rnk % 2 == 0) ? "off" : "on";
                $currRnk = $rnk + 1;
                echo '
                <ul class="rank-body" alternate-style="'.$clr.'">
                <li class="rank-id right">'.$currRnk.'</li>
                <li class="rank-name right">'.$lv->name.'</li>
                <li class="rank-job right"><div class="rank-icn ms-2" style="background-image: url('.$app->getLink('assets/imgs/jobs/'.$lv->job.'.jpg',false).')"></div> '.GAME_JOBS[$lv->job].' </li>
                <li class="rank-level right">'.$lv->lv.'</li>
                <li class="rank-status right" data-status="'.strtolower($lv->stat).'"><i class="fas fa-power-off fa-fw" aria-hidden="true"></i></li>
            </ul>
                ';
            }
            ?>

        </div>
        <div class="rank-table my-5" style="display: none">
            <ul class="rank-head">
                <li class="rank-id right">#</li>
                <li class="rank-name right">الإسم</li>
                <li class="rank-job right" style="line-height: 60px!important;height: 60px!important;">الإختصاص</li>
                <li class="rank-level right">نقاط النمط</li>
                <li class="rank-status right">الحالة</li>
            </ul>
            <?php
            $rLv = $app->getPlayers('pk');
            foreach($rLv as $rnk=>$lv){
                $clr =  ($rnk % 2 == 0) ? "off" : "on";
                $currRnk = $rnk + 1;
                echo '
                <ul class="rank-body" alternate-style="'.$clr.'">
                <li class="rank-id right">'.$currRnk.'</li>
                <li class="rank-name right">'.$lv->name.'</li>
                <li class="rank-job right"><div class="rank-icn ms-2" style="background-image: url('.$app->getLink('assets/imgs/jobs/'.$lv->job.'.jpg',false).')"></div> '.GAME_JOBS[$lv->job].' </li>
                <li class="rank-level right">'.$lv->pkc.'</li>
                <li class="rank-status right" data-status="'.strtolower($lv->stat).'"><i class="fas fa-power-off fa-fw" aria-hidden="true"></i></li>
            </ul>
                ';
            }
            ?>
        </div>
    </div>
<!--    footer-->
    <footer id="footer" class="my-5">
        <div id="footer-logo">

        </div>
    </footer>
    </div>
</div>





<!--SCRIPT LINKS PUTS IN HERE-->
<script src="https://challenges.cloudflare.com/turnstile/v0/api.js"></script>
<script src="https://code.jquery.com/jquery-3.7.1.min.js" integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4" crossorigin="anonymous"></script>
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
<script>
    AOS.init();
    $(document).ready(function (){
        $("#staticBackdrop").modal('show');

        $(".rank-btn").on('click',function (){
            if ($(this).attr('rank-select') == 'on'){return true;}
            $(".rank-btn").attr('rank-select','off');
            $(this).attr('rank-select','on')
            $(".rank-table").fadeToggle();
        });
        $("#nav-drop-btn").on("click",function (){
            $("#nav-drop-menu-list").slideToggle('slow');
        });
        $('body').on('click',function(event){
            if((!$(event.target).is('#nav-drop-down')) && (!$(event.target).is("#nav-drop-btn"))){
            console.log(event.target);
              $("#nav-drop-menu-list").slideUp('slow');
            }
        });
    });
</script>
</body>
</html>