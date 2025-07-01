# Creating IG User Media

```md
POST /<YOUR_APP_USERS_INSTAGRAM_USER_ID>/media
```

* Create an image, carousel, story or reel [IG Container](https://developers.facebook.com/docs/instagram-api/reference/ig-container) for use in the post publishing process. See the [Content Publishing](https://developers.facebook.com/docs/instagram-api/guides/content-publishing) guide for complete publishing steps

Steps to publish a media object include the following:

1. Create a container
2. Upload the media to the container
3. Publish the container

## Limitations

### General Limitations

* Containers expire after 24 hours

* An Instagram account can only create 400 containers within a rolling 24 hour period

* If the Page connected to the targeted Instagram professional account requires [Page Publishing Authorization](https://www.facebook.com/help/www/1939753742723975) (PPA), PPA must be completed or the request will fail

* If the Page connected to the targeted Instagram professional account requires two-factor authentication, the Facebook User must also have performed two-factor authentication or the request will fail

* We strongly recommended the HTTP IETF standard character set for URLs, URLs that contain only US ASCII characters, or the request will fail

## Requirements

| Type | Description |
| --- | --- |
| [Access Tokens](https://developers.facebook.com/docs/facebook-login/access-tokens#usertokens) | [User](https://developers.facebook.com/docs/facebook-login/access-tokens#usertokens) |
| [Business Roles](https://www.facebook.com/business/help/442345745885606) | If creating containers for [product tagging](https://developers.facebook.com/docs/instagram-api/guides/product-tagging), the app user must have an admin role on the [Business Manager](https://business.facebook.com/) that owns the IG User's [Instagram Shop](https://help.instagram.com/1187859655048322?fbclid=IwZXh0bgNhZW0CMTEAAR4QWMauZaKuQxCqCwZu39AikrWChcXht7CLOBG9KMiUjemZL8SXK42h6IEN2Q_aem_1woeTRGmJRTulctMOMozvg). |
| [Permissions](https://developers.facebook.com/docs/apps/review/login-permissions) | ```instagram_basic```<br/>```instagram_content_publish```<br/>```pages_read_engagement``` If the app user was granted a role on the Page via the Business Manager, you will also need one of:<br/><br/>```ads_management```<br/>```ads_read```<br/><br/>If creating containers for [product tagging](https://developers.facebook.com/docs/instagram-api/guides/product-tagging), you will also need:<br/><br/>```catalog_management```<br/>```instagram_shopping_tag_products``` |
| [Tasks](https://developers.facebook.com/docs/instagram-api/overview#tasks) | Your app user must be able to perform the ```MANAGE``` or ```CREATE_CONTENT``` tasks on the Page linked to their Instagram professional account. |

## Image Specifications

* Format: JPEG

* File size: 8 MB maximum.

* Aspect ratio: Must be within a 4:5 to 1.91:1 range

* Minimum width: 320 (will be scaled up to the minimum if necessary)

* Maximum width: 1440 (will be scaled down to the maximum if necessary)

* Height: Varies, depending on width and aspect ratio

* Color Space: sRGB. Images using other color spaces will have their color spaces converted to sRGB.
