h1. Dependencies

h2. Zendesk API
This library requires a Zendesk API available at GitHub.
Since this isn't controlled by Composer call the following from your application's root directory:
 
    git clone git://github.com/ludwigzzz/Zendesk-API.git vendor/zendesk-api

In app/autoload.php, add the following lines before AnnotationRegistry::registerLoader(array($loader, 'loadClass')):

    $loader->addClassMap( array( 'zendesk' =>  __DIR__.'/../vendor/zendesk-api/zendesk.php' ) );

Add the following fields to your application's parameters.yml:

    parameters:
        zendesk_api_key:   yourkey
        zendesk_api_user:  youruser
        zendesk_api_subdomain: yoursubdomain