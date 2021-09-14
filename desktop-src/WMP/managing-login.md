---
title: Administración del inicio de sesión
description: Administración del inicio de sesión
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Reproductor de Windows Media en línea, administración de inicios de sesión
- tiendas en línea, administración de inicios de sesión
- tiendas en línea de tipo 1, administración de inicios de sesión
- Reproductor de Windows Media en línea, inicios de sesión
- tiendas en línea, inicios de sesión
- tiendas en línea de tipo 1, inicios de sesión
- Reproductor de Windows Media en línea, proceso de inicio de sesión estándar
- tiendas en línea, proceso de inicio de sesión estándar
- tiendas en línea de tipo 1, proceso de inicio de sesión estándar
- Reproductor de Windows Media en línea, proceso de cierre de sesión
- tiendas en línea, proceso de cierre de sesión
- type 1 online stores,log-out process
- proceso de inicio de sesión estándar
- proceso de cierre de sesión
- inicios de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967551"
---
# <a name="managing-login"></a>Administración del inicio de sesión

Reproductor de Windows Media admite una variedad de métodos para que el usuario inicie sesión en una tienda en línea de tipo 1. El reproductor proporciona un cuadro de diálogo de inicio de sesión estándar, pero la tienda en línea puede proporcionar una página web que actúa como alternativa al cuadro de diálogo estándar.

El usuario puede iniciar un intento de inicio de sesión mediante la interacción con la interfaz de usuario Reproductor de Windows Media o mediante la interacción con una página de detección proporcionada por el almacén en línea. Si el usuario inicia un intento de inicio de sesión mediante la interacción con una página de detección, el script de la página de detección llama al [método External.attemptLogin.](external-attemptlogin.md)

El estado de inicio de sesión del usuario se mantiene en la tienda en línea. Cuando cambia el estado de inicio de sesión del usuario, o si se produce un error en un intento de inicio de sesión, el complemento del almacén en línea notifica a Reproductor de Windows Media mediante una llamada a [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnLoginStateChange en el parámetro *type.* El reproductor pasa la notificación a la página de detección generando el [evento External.OnLoginChange.](external-onloginchange-event.md)

Una llamada a **OnLoginChange** no significa necesariamente que el estado de inicio de sesión del usuario haya cambiado; podría significar un error al intentar iniciar sesión. Para determinar el estado de inicio de sesión del usuario, el controlador de eventos **OnLoginChange** puede inspeccionar la [propiedad External.userLoggedIn.](external-userloggedin.md)

En las secciones siguientes se describe el proceso de inicio de sesión estándar, el proceso de inicio de sesión alternativo y el proceso de cierre de sesión.

## <a name="standard-log-in"></a>Inicio de sesión estándar

El proceso de inicio de sesión estándar implica los pasos siguientes:

1.  El usuario inicia un intento de inicio de sesión mediante la interacción con la interfaz Reproductor de Windows Media usuario o mediante la interacción con una página de detección.
2.  Reproductor de Windows Media muestra un cuadro de diálogo que solicita al usuario un nombre de usuario y una contraseña.
3.  Cuando el usuario  hace clic en el botón Iniciar sesión en el cuadro de diálogo, Reproductor de Windows Media llama a [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), que se implementa mediante el complemento de la tienda en línea.
4.  El complemento se comunica con la tienda en línea y se realiza correctamente o no se puede iniciar sesión en el usuario.
5.  Si el intento de inicio de sesión se realiza correctamente, el complemento notifica a Reproductor de Windows Media mediante una llamada a **IWMPContentPartnerCallback::Notify**, pasando VARIANT TRUE en el miembro \_ **boolVal** del *parámetro pContext.* Si se produce un error en el intento de inicio de sesión, el complemento notifica a Reproductor de Windows Media mediante una llamada a **IWMPContentPartnerCallback::Notify**, pasando un valor de 32 bits en el **miembro ulVal** del *parámetro pContext.* A continuación, el reproductor pasa ese valor de 32 bits a [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para obtener la dirección URL de una página web que puede controlar el error.

## <a name="alternative-login"></a>Inicio de sesión alternativo

Si la marca \_ SUBSCRIPTION CAP ALTLOGIN se establece en la entrada del Registro capabilities del complemento de la tienda en línea, Reproductor de Windows Media no usa el cuadro de diálogo de inicio de sesión \_ estándar.  En su lugar, Reproductor de Windows Media llama a **IWMPContentPartner::GetItemInfo** para recuperar la dirección URL de una página web que realiza el proceso de inicio de sesión. Para obtener más información sobre la entrada del Registro **Capabilities,** vea Claves y entradas del Registro [para un almacén en línea de tipo 1.](registry-keys-and-entries-for-a-type-1-online-store.md)

El reproductor llama a **GetItemInfo** dos veces: una vez que se pasa g szItemInfo ALTLoginURL para recuperar la dirección URL de la página web de inicio de sesión y después se pasa \_ \_ g \_ szItemInfo ALTLoginCaption para recuperar el título de la ventana que hospeda la página \_ web. Cuando **GetItemInfo** devuelve la dirección URL de la página web de inicio de sesión, puede especificar el tamaño de la ventana de inicio de sesión anexando la siguiente cadena de parámetro a la dirección URL:

? DlgX=*width&* DlgY=*height*

En la cadena del parámetro, *width* y *height* son el ancho y alto de la ventana en píxeles. Por **ejemplo, GetItemInfo** podría devolver la cadena siguiente para especificar que AltLogin.htm debe mostrarse en una ventana con un ancho de 800 píxeles y un alto de 400 píxeles.


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



El proceso de inicio de sesión alternativo implica los pasos siguientes:

1.  El usuario inicia un intento de inicio de sesión mediante la interacción con la interfaz Reproductor de Windows Media usuario o mediante la interacción con una página de detección.
2.  Reproductor de Windows Media abre una ventana modal que muestra la página web de inicio de sesión proporcionada por la tienda en línea.
3.  La página web se comunica con la tienda en línea y se realiza correctamente o no se puede iniciar sesión en el usuario.
4.  Si el intento de inicio de sesión se realiza correctamente, la página web notifica al complemento de la tienda en línea llamando a [External.sendMessage](external-sendmessage.md), lo que da como resultado una llamada a [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage). El complemento de la tienda en línea determina que el intento de inicio de sesión se ha hecho correctamente inspeccionando los parámetros pasados a **IWMPContentPartner::SendMessage**. Estos parámetros no se interpretan mediante Reproductor de Windows Media; solo tienen significado para la tienda en línea. El complemento llama a **IWMPContentPartnerCallback::Notify**, pasando VARIANT TRUE en el \_ **miembro boolVal** del *parámetro pContext.* Si se produce un error en el inicio de sesión, la tienda en línea debe determinar cómo ayudar al usuario. Una posibilidad es mostrar una nueva página web en la ventana modal que hospeda la página web de inicio de sesión alternativa.

## <a name="log-out"></a>Cierre sesión.

El proceso de cierre de sesión implica los pasos siguientes.

1.  El usuario inicia un intento de cierre de sesión mediante la interacción con la interfaz Reproductor de Windows Media usuario o mediante la interacción con una página de detección.
2.  Reproductor de Windows Media llama [a IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), que se implementa mediante el complemento de la tienda en línea.
3.  El complemento se comunica con la tienda en línea y se realiza correctamente o no se puede cerrar la sesión del usuario.
4.  Si el intento de cierre de sesión se realiza correctamente, el complemento notifica a Reproductor de Windows Media mediante una llamada a **IWMPContentPartnerCallback::Notify**, pasando VARIANT FALSE en el miembro \_ **boolVal** del *parámetro pContext.*

Cuando un intento de iniciar o cerrar sesión es correcto, el complemento de la tienda en línea llama a **IWMPContentPartnerCallback::Notify**, pasando wmpcnLoginStateChange en el parámetro de tipo.  El complemento usa el *parámetro pContext* para especificar el estado de inicio de sesión actual del usuario. Si el complemento establece *pContext* -> **boolVal** en VARIANT \_ TRUE, el usuario inicia sesión. Si el complemento establece *pContext* -> **boolVal** en VARIANT \_ FALSE, el usuario se registra. Tenga en *cuenta que pContext* no indica el éxito o error del intento; en su lugar, indica el estado de inicio de sesión actual del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External.attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**Evento External.OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External.userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner::Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**IWMPContentPartner::Logout**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**Guía de programación para almacenes en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




