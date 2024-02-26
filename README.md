<!DOCTYPE html>
<html lang="en-US">
<head>
  <meta charset="utf-8">
  <!-- Created using Storyline 3 - http://www.articulate.com  -->
  <!-- version: 3.12.24693.0 -->
  <title>&quot;CILLUBA&quot;oke</title>
  <meta http-equiv="x-ua-compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no, shrink-to-fit=no, minimal-ui" />
  <meta name="apple-mobile-web-app-capable" content="yes" />
  <style>
    html, body { height: 100%; padding: 0; margin: 0 }
    #app { height: 100%; width: 100%; }
  </style>
  
  <script>window.THREE = { };</script>
</head>
<body style="background: #FFFFFF" class="cs-HTML theme-classic">
  <!-- 360 -->
  <script>!function(e){function n(e,i){return e.test(i)}function i(e){var i=e||navigator.userAgent,o=i.split("[FBAN");if(void 0!==o[1]&&(i=o[0]),this.apple={phone:n(t,i),ipod:n(d,i),tablet:!n(t,i)&&n(s,i),device:n(t,i)||n(d,i)||n(s,i)},this.amazon={phone:n(h,i),tablet:!n(h,i)&&n(a,i),device:n(h,i)||n(a,i)},this.android={phone:n(h,i)||n(b,i),tablet:!n(h,i)&&!n(b,i)&&(n(a,i)||n(r,i)),device:n(h,i)||n(a,i)||n(b,i)||n(r,i)},this.windows={phone:n(l,i),tablet:n(p,i),device:n(l,i)||n(p,i)},this.other={blackberry:n(f,i),blackberry10:n(u,i),opera:n(c,i),firefox:n(A,i),chrome:n(w,i),device:n(f,i)||n(u,i)||n(c,i)||n(A,i)||n(w,i)},this.seven_inch=n(v,i),this.any=this.apple.device||this.android.device||this.windows.device||this.other.device||this.seven_inch,this.phone=this.apple.phone||this.android.phone||this.windows.phone,this.tablet=this.apple.tablet||this.android.tablet||this.windows.tablet,"undefined"==typeof window)return this}function o(){var e=new i;return e.Class=i,e}var t=/iPhone/i,d=/iPod/i,s=/iPad/i,b=/(?=.*\bAndroid\b)(?=.*\bMobile\b)/i,r=/Android/i,h=/(?=.*\bAndroid\b)(?=.*\bSD4930UR\b)/i,a=/(?=.*\bAndroid\b)(?=.*\b(?:KFOT|KFTT|KFJWI|KFJWA|KFSOWI|KFTHWI|KFTHWA|KFAPWI|KFAPWA|KFARWI|KFASWI|KFSAWI|KFSAWA)\b)/i,l=/IEMobile/i,p=/(?=.*\bWindows\b)(?=.*\bARM\b)/i,f=/BlackBerry/i,u=/BB10/i,c=/Opera Mini/i,w=/(CriOS|Chrome)(?=.*\bMobile\b)/i,A=/(?=.*\bFirefox\b)(?=.*\bMobile\b)/i,v=new RegExp("(?:Nexus 7|BNTV250|Kindle Fire|Silk|GT-P1000)","i");"undefined"!=typeof module&&module.exports&&"undefined"==typeof window?module.exports=i:"undefined"!=typeof module&&module.exports&&"undefined"!=typeof window?module.exports=o():"function"==typeof define&&define.amd?define("isMobile",[],e.isMobile=o()):e.isMobile=o()}(this);
    window.isMobile.apple.tablet = window.isMobile.apple.tablet ||
      (navigator.platform === 'MacIntel' && navigator.maxTouchPoints > 1);
    window.isMobile.apple.device = window.isMobile.apple.device || window.isMobile.apple.tablet;
    window.isMobile.tablet = window.isMobile.tablet || window.isMobile.apple.tablet;
    window.isMobile.any = window.isMobile.any || window.isMobile.apple.tablet;
  </script>

  <div id="focus-sink" aria-hidden="true" tabIndex="-1"></div>

  <div id="preso"></div>
  <script>
    window.DS = {};
    window.globals = {
      DATA_PATH_BASE: '',
      HAS_FRAME: true,
      HAS_SLIDE: true,

      lmsPresent: false,
      tinCanPresent: false,
      cmi5Present: false,
      aoSupport: false,
      scale: 'noscale',
      captureRc: false,
      browserSize: 'optimal',
      bgColor: '#FFFFFF',
      features: 'AccessibleText,SettingsControl,TextStyleHyperlinks',
      themeName: 'classic',
      preloaderColor: '#FFFFFF',
      suppressAnalytics: false,
      productChannel: 'perpetual',
      publishSource: 'storyline',
      aid: '',
      cid: '14d9a369-7cdd-43c9-b36a-d968af47c05e',
      playerVersion: '3.12.24693.0',
      maxIosVideoElements: 5,

      
      parseParams: function(qs) {
        if (window.globals.parsedParams != null) {
          return window.globals.parsedParams;
        }
        qs = (qs || window.location.search.substr(1)).split('+').join(' ');
        var params = {},
            tokens,
            re = /[?&]?([^=]+)=([^&]*)/g;

        while (tokens = re.exec(qs)) {
          params[decodeURIComponent(tokens[1]).trim()] =
            decodeURIComponent(tokens[2]).trim();
        }
        window.globals.parsedParams = params;
        return params;
      }

    };

    (function() {

      var classTypes = [ 'desktop', 'mobile', 'phone', 'tablet' ];

      var addDeviceClasses = function(prefix, testObj) {
        var curr, i;
        for (i = 0; i < classTypes.length; i++) {
          curr = classTypes[i];
          if (testObj[curr]) {
            document.body.classList.add(prefix + curr);
          }
        }
      };

      var params = window.globals.parseParams(),
          isDevicePreview = params.devicepreview === '1',
          isPhoneOverride = params.deviceType === 'phone' || (isDevicePreview && params.phone == '1'),
          isTabletOverride = (params.deviceType === 'tablet' || isDevicePreview) && !isPhoneOverride,
          isMobileOverride = isPhoneOverride || isTabletOverride;

      var deviceView = {
        desktop: !window.isMobile.any && !isMobileOverride,
        mobile: window.isMobile.any || isMobileOverride,
        phone: isPhoneOverride || (window.isMobile.phone && !isTabletOverride),
        tablet: isTabletOverride || window.isMobile.tablet
      };

      window.globals.deviceView = deviceView;
      window.isMobile.desktop = !window.isMobile.any;
      window.isMobile.mobile = window.isMobile.any;

      addDeviceClasses('view-', deviceView);

    })();
  </script>
  
  <script src='story_content/user.js' type=text/javascript></script>
  <div class="slide-loader"></div>

  <script type="text/javascript">
    if (window.globals.deviceView.isMobile) { var doc = document, loader = doc.body.querySelector('.slide-loader'); [ 1, 2, 3 ].forEach(function(n) { var d = doc.createElement('div'); d.style.backgroundColor = window.globals.preloaderColor; d.classList.add('mobile-loader-dot'); d.classList.add('dot' + n); loader.appendChild(d); }); }
  </script>

  <div class="mobile-load-title-overlay" style="display: none">
    <div class="mobile-load-title">&quot;CILLUBA&quot;oke</div>
  </div>

  <div class="mobile-chrome-warning"></div>

  <script>
    
    if (window.autoSpider && window.vInterfaceObject) {
      document.querySelector('.mobile-load-title-overlay').style.display = 'none';
    }
  </script>

  

  <link rel="stylesheet" href="html5/data/css/output.min.css" data-noprefix />
</body>
<script src="html5/lib/scripts/bootstrapper.min.js"></script>
</html>
