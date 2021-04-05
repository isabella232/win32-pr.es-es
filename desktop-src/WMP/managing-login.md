---
title: Administrar inicio de sesión
description: Administrar inicio de sesión
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player tiendas en línea, administrar inicios de sesión
- tiendas en línea, administrar inicios de sesión
- tipo 1 almacenes en línea, administrar inicios de sesión
- Windows Media Player tiendas en línea, inicios de sesión
- tiendas en línea, inicios de sesión
- tipo 1 tiendas en línea, inicios de sesión
- Windows Media Player tiendas en línea, proceso de inicio de sesión estándar
- tiendas en línea, proceso de inicio de sesión estándar
- tipo 1 almacenes en línea, proceso de inicio de sesión estándar
- Windows Media Player tiendas en línea, proceso de cierre de sesión
- tiendas en línea, proceso de cierre de sesión
- tipo 1 tiendas en línea, proceso de cierre de sesión
- proceso de inicio de sesión estándar
- proceso de cierre de sesión
- inicios de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420279"
---
# <a name="managing-login"></a>Administrar inicio de sesión

Windows Media Player admite una variedad de métodos para que el usuario inicie sesión en una tienda en línea de tipo 1. El reproductor proporciona un cuadro de diálogo de inicio de sesión estándar, pero la tienda en línea puede proporcionar una página web que actúa como alternativa al cuadro de diálogo estándar.

El usuario puede iniciar un intento de inicio de sesión mediante la interacción con la interfaz de usuario de Media Player de Windows o mediante la interacción con una página de detección proporcionada por la tienda en línea. Si el usuario inicia un intento de inicio de sesión mediante la interacción con una página de detección, el script de la página de detección llama al método [external. attemptLogin](external-attemptlogin.md) .

La tienda en línea mantiene el estado de inicio de sesión del usuario. Cuando cambia el estado de inicio de sesión del usuario, o si se produce un error en un intento de inicio de sesión, el complemento de la tienda en línea notifica a Windows Media Player llamando a [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnLoginStateChange en el parámetro de *tipo* . El reproductor pasa la notificación a la página de detección generando el evento [. OnLoginChange externo](external-onloginchange-event.md) .

Una llamada a **OnLoginChange** no significa necesariamente que haya cambiado el estado de inicio de sesión del usuario. podría significar que se produjo un error al intentar iniciar sesión. Para determinar el estado de inicio de sesión del usuario, el controlador de eventos **OnLoginChange** puede inspeccionar la propiedad [external. userLoggedIn](external-userloggedin.md) .

En las secciones siguientes se describe el proceso de inicio de sesión estándar, el proceso de inicio de sesión alternativo y el proceso de cierre de sesión.

## <a name="standard-log-in"></a>Inicio de sesión estándar

El proceso de inicio de sesión estándar consta de los siguientes pasos:

1.  El usuario inicia un intento de inicio de sesión mediante la interacción con la interfaz de usuario de Media Player de Windows o mediante la interacción con una página de detección.
2.  Windows Media Player muestra un cuadro de diálogo que solicita al usuario un nombre de usuario y una contraseña.
3.  Cuando el usuario hace clic en el botón **iniciar sesión** del cuadro de diálogo, Windows Media Player llama a [IWMPContentPartner:: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), que se implementa mediante el complemento de la tienda en línea.
4.  El complemento se comunica con la tienda en línea y se realiza correctamente o no puede iniciar sesión en el usuario.
5.  Si el intento de inicio de sesión se realiza correctamente, el complemento notifica a Windows Media Player llamando a **IWMPContentPartnerCallback:: Notify**, pasando Variant \_ true en el miembro **boolVal** del parámetro *pContext* . Si se produce un error en el intento de inicio de sesión, el complemento notifica a Windows Media Player llamando a **IWMPContentPartnerCallback:: Notify**, pasando un valor de 32 bits en el miembro **UlVal** del parámetro *pContext* . A continuación, el reproductor pasa el valor de 32 bits a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para obtener la dirección URL de una página web que puede controlar el error.

## <a name="alternative-login"></a>Inicio de sesión alternativo

Si la \_ marca ALTLOGIN de límite de suscripción \_ se establece en la entrada del registro **Capabilities** para el complemento de la tienda en línea, Windows Media Player no utiliza el cuadro de diálogo Inicio de sesión estándar. En su lugar, Windows Media Player llama a **IWMPContentPartner:: GetItemInfo** para recuperar la dirección URL de una página web que realiza el proceso de inicio de sesión. Para obtener más información acerca de la entrada del registro **Capabilities** , consulte [claves del registro y entradas para una tienda en línea de tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).

El reproductor llama a **GetItemInfo** dos veces: una vez pasado g \_ szItemInfo \_ ALTLoginURL para recuperar la dirección URL de la Página Web de inicio de sesión y después pasar g \_ szItemInfo \_ ALTLoginCaption para recuperar el título de la ventana que hospeda la Página Web. Cuando **GetItemInfo** devuelve la dirección URL de la Página Web de inicio de sesión, puede especificar el tamaño de la ventana de inicio de sesión anexando la siguiente cadena de parámetro a la dirección URL:

? DlgX =*ancho*&DlgY =*alto*

En la cadena de parámetro, *ancho* y *alto* son el ancho y el alto de la ventana en píxeles. Por ejemplo, **GetItemInfo** podría devolver la siguiente cadena para especificar que AltLogin.htm debe mostrarse en una ventana con un ancho de 800 píxeles y un alto de 400 píxeles.


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



El proceso de inicio de sesión alternativo implica los siguientes pasos:

1.  El usuario inicia un intento de inicio de sesión mediante la interacción con la interfaz de usuario de Media Player de Windows o mediante la interacción con una página de detección.
2.  Windows Media Player abre una ventana modal que muestra la Página Web de inicio de sesión proporcionada por la tienda en línea.
3.  La página web se comunica con la tienda en línea y se realiza correctamente o no puede iniciar sesión en el usuario.
4.  Si el intento de inicio de sesión se realiza correctamente, la página web notifica al complemento de la tienda en línea llamando a [external. SendMessage](external-sendmessage.md), lo que da como resultado una llamada a [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage). El complemento de la tienda en línea determina que el intento de inicio de sesión se realizó correctamente mediante la inspección de los parámetros pasados a **IWMPContentPartner:: SendMessage**. Los parámetros no son interpretados por Media Player de Windows; solo tienen significado en la tienda en línea. El complemento llama a **IWMPContentPartnerCallback:: Notify**, pasando Variant \_ true en el miembro **boolVal** del parámetro *pContext* . Si se produce un error en el inicio de sesión, la tienda en línea debe determinar cómo ayudar al usuario. Una posibilidad es mostrar una nueva página web en la ventana modal que hospeda la Página Web de inicio de sesión alternativa.

## <a name="log-out"></a>Cierre sesión.

El proceso de cierre de sesión implica los pasos siguientes.

1.  El usuario inicia un intento de cierre de sesión interactuando con la interfaz de usuario de Media Player de Windows o interactuando con una página de detección.
2.  Windows Media Player llama a [IWMPContentPartner:: Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), que se implementa mediante el complemento de la tienda en línea.
3.  El complemento se comunica con la tienda en línea y se realiza correctamente o no puede cerrar la sesión del usuario.
4.  Si el intento de cierre de sesión se realiza correctamente, el complemento notifica a Windows Media Player llamando a **IWMPContentPartnerCallback:: Notify**, pasando Variant \_ false en el miembro **boolVal** del parámetro *pContext* .

Cuando un intento de iniciar o cerrar sesión se realiza correctamente, el complemento de la tienda en línea llama a **IWMPContentPartnerCallback:: Notify**, pasando wmpcnLoginStateChange en el parámetro de *tipo* . El complemento usa el parámetro *pContext* para especificar el estado de inicio de sesión actual del usuario. Si el complemento establece *pContext* -> **boolVal** en Variant \_ true, el usuario ha iniciado sesión. Si el complemento establece *pContext* -> **boolVal** en Variant \_ false, se cerrará la sesión del usuario. Tenga en cuenta que *pContext* no indica si el intento se realizó correctamente o no. en su lugar, indica el estado de inicio de sesión actual del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**Evento external. OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner:: login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**IWMPContentPartner:: logout**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**Guía de programación para las tiendas en línea de tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




