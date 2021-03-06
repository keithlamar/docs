# Auth0 APIs
Auth0 exposes two APIs for developers to consume in their applications. The first API is the Authentication API and handles all the primary identity related functions. The second API is the Management API which enables you to automate various tasks in Auth0 such as creating users. Below you will find more information about each of these APIs.

## Authentication API
The Authentication API exposes all of the identity functionality of Auth0 as well as all of the supported identity protocols such as OpenID Connect, OAuth, and SAML. Generally speaking you will consume this API through one of our SDKs like [Auth0.js](/libraries/auth0js) or libraries such as the [Lock](/libraries/lock) widget. However, if you are building all of your authentication UI manually you will likely interact with this API directly.

<div class="api-info-wrapper">
  <div class="block-links">
    <div class="api-info">
      <div class="row">
        <div class="col-md-6">
          <div class="wrapper-left">
            <a href="/auth-api" class="illustration i-apiexplorer"></a>
            <h4>API Explorer</h4>
            <p>Learn about and use the Auth0 Authentication API in the browser.</p>
            <p><a href="/auth-api">Open API Explorer</a></p>
          </div>
        </div>
        <div class="col-md-6">
          <div class="wrapper-right">
            <span href="#" class="illustration i-postman"></span>
            <h4>Postman</h4>
            <p>Try the Auth0 Authentication API in Postman.</p>
            <p><div class="postman-run-button" data-postman-action="collection/import" data-postman-var-1="608670c820cda215594c"></div></p>
            <p><a href="/api/postman">How to use our Postman Collections</a></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

## Management API v2
The Auth0 Management API can be used to manage all aspects of your Auth0 account. You can use the API to automate the configuration of your environments and use this API for runtime tasks such as creating users.

<div class="api-info-wrapper">
  <div class="block-links">
    <div class="api-info">
      <div class="row">
        <div class="col-md-6">
          <div class="wrapper-left">
            <a href="/api/v2" class="illustration i-apiexplorer"></a>
            <h4>API Explorer</h4>
            <p>Learn about and use the Auth0 Management API in the browser.</p>
            <p><a href="/api/v2">Open API Explorer</a></p>
          </div>
        </div>
        <div class="col-md-6">
          <div class="wrapper-right">
            <span href="#" class="illustration i-postman"></span>
            <h4>Postman</h4>
            <p>Try the Auth0 Management API in Postman.</p>
            <p><div class="postman-run-button" data-postman-action="collection/import" data-postman-var-1="b822a82a1f0e18a85617"></div></p>
            <p><a href="/api/postman">How to use our Postman Collections</a></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

## Management API v1 (deprecated)
The Auth0 Management API v1 contains various management functions for your Auth0 account. This API is **deprecated** and should not be used for new projects. If you have an existing app that uses the v1 Management API you can browse the [API explorer](/api/v1).

<script type="text/javascript">
  (function (p,o,s,t,m,a,n) {
    !p[s] && (p[s] = function () { (p[t] || (p[t] = [])).push(arguments); });
    !o.getElementById(s+t) && o.getElementsByTagName("head")[0].appendChild((
      (n = o.createElement("script")),
      (n.id = s+t), (n.async = 1), (n.src = m), n
    ));
  }(window, document, "_pm", "PostmanRunObject", "https://run.pstmn.io/button.js"));

  _pm('env.create', '${account.tenant}', { auth0_domain: '${account.namespace}' }); 
</script>
