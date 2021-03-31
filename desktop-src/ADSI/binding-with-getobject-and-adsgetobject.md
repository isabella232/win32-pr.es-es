---
title: Enlazar con GetObject y ADsGetObject
description: Las funciones GetObject y ADsGetObject se usan para enlazar con objetos de servicio de directorio sin autenticación.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, enlazar con GetObject y ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995616"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Enlazar con GetObject y ADsGetObject

Las funciones **GetObject** y [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) se usan para enlazar con objetos de servicio de directorio sin autenticación. No es necesario que la aplicación proporcione credenciales al acceder a los datos del servicio de directorio. ADSI utiliza el contexto de seguridad del subproceso que realiza la llamada. Sin embargo, si se produce un error en la autenticación segura, ADSI intenta realizar un enlace simple con un nombre de usuario NULL y una contraseña nula. Si el enlace simple se realiza correctamente, el contexto de usuario para el enlace es Guest. Un enlace simple utiliza la autenticación de texto simple. Dado que no se transmite ningún nombre de usuario o contraseña a través de la red, no se trata de un problema de seguridad.

La función **GetObject** se utiliza para enlazar con objetos de servicio de directorio en lenguajes que admiten la automatización, como Visual Basic. La función **GetObject** requiere una cadena de moniker. En ADSI, la cadena de enlace es la cadena de moniker.

En los lenguajes que no admiten directamente automatización, como C o C++, ADSI proporciona la función [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para enlazar con objetos de servicio de directorio. Como alternativa, las funciones [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) y [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) se pueden usar para lograr el mismo resultado que **GetObject**.

Para un servicio que se ejecuta con la cuenta LocalSystem, el contexto de seguridad utilizado por **GetObject** y [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depende del equipo en el que se ejecuta el servicio. Si el servicio se ejecuta como LocalSystem en un controlador de dominio, el servicio tiene acceso de nivel de sistema completo a Active Directory. Si el servicio no se está ejecutando en un controlador de dominio, el servicio tiene los derechos de acceso y los privilegios concedidos a la cuenta de equipo para el equipo en el que se está ejecutando el servicio; Esto es significativamente menos eficaz que el acceso de nivel de sistema.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de Visual Basic se muestra cómo utilizar la función **GetObject** para enlazar a un objeto.


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



En el ejemplo de código de C++ siguiente se muestra cómo usar la función [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para enlazar a un objeto.


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



 

 