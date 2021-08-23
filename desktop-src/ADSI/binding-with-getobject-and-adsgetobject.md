---
title: Enlace con GetObject y ADsGetObject
description: Las funciones GetObject y ADsGetObject se usan para enlazar a objetos de servicio de directorio sin autenticación.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , using,binding with GetObject and ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fe3f64368f6bbecf390d07f5258c11b6752badbf701e1f248439ca81428749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082759"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Enlace con GetObject y ADsGetObject

Las **funciones GetObject** [**y ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) se usan para enlazar a objetos de servicio de directorio sin autenticación. No es necesario que la aplicación proporcione credenciales al acceder a los datos del servicio de directorio. ADSI usa el contexto de seguridad del subproceso que realiza la llamada. Sin embargo, si se produce un error en la autenticación segura, ADSI intenta realizar un enlace simple con un nombre de usuario nulo y una contraseña nula. Si el enlace simple se realiza correctamente, el contexto de usuario para el enlace es Invitado. Un enlace simple usa la autenticación de texto no cifrado. Dado que no se transmite ningún nombre de usuario o contraseña a través de la red, no se trata de un problema de seguridad.

La **función GetObject** se usa para enlazar a objetos de servicio de directorio en lenguajes que admiten automatización, como Visual Basic. La **función GetObject** requiere una cadena de moniker. En ADSI, la cadena de enlace es la cadena de moniker.

En lenguajes que no admiten directamente la automatización, como C o C++, ADSI proporciona la función [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para enlazar a objetos de servicio de directorio. Como alternativa, las [**funciones MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) y [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) se pueden usar para lograr el mismo resultado que **GetObject**.

Para un servicio que se ejecuta en la cuenta LocalSystem, el contexto de seguridad utilizado por **GetObject** y [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depende del equipo en el que se ejecuta el servicio. Si el servicio se ejecuta como LocalSystem en un controlador de dominio, el servicio tiene acceso completo de nivel de sistema a Active Directory. Si el servicio no se ejecuta en un controlador de dominio, el servicio tiene los derechos de acceso y privilegios concedidos a la cuenta de equipo para el equipo en el que se ejecuta el servicio. esto es significativamente menos eficaz que el acceso de nivel de sistema.

## <a name="examples"></a>Ejemplos

En el Visual Basic ejemplo de código siguiente se muestra cómo usar la **función GetObject** para enlazar a un objeto .


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



En el siguiente ejemplo de código de C++ se muestra cómo usar la función [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para enlazar a un objeto .


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 