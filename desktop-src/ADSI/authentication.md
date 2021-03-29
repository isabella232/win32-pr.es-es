---
title: Autenticación (ADSI)
description: En ADSI, las credenciales que constan de un nombre de usuario y contraseña se usan para proporcionar o restringir el acceso a los objetos del servicio de directorio.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- ADSI de autenticación
- ADSI, usar, autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad32b2f32f115b20c99e47578ad76b73ad72a123
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104487299"
---
# <a name="authentication-adsi"></a>Autenticación (ADSI)

En ADSI, las credenciales que constan de un nombre de usuario y contraseña se usan para proporcionar o restringir el acceso a los objetos del servicio de directorio. La función [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) usa las credenciales del subproceso de llamada para la autenticación. La función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) se pueden usar para especificar credenciales distintas de las del subproceso que realiza la llamada. Cuando un objeto se enlaza a con un usuario autenticado, el usuario puede acceder al objeto según los requisitos de seguridad del servicio de directorio subyacente.

> [!Note]  
> La función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) no se deben utilizar para validar las credenciales de usuario. Para obtener más información acerca de la validación de las credenciales de usuario, vea el artículo de Microsoft Knowledge Base 180548 [HOWTO: validar las credenciales de usuario en los sistemas operativos de Microsoft](https://support.microsoft.com/kb/180548).

 

En el ejemplo de código siguiente se muestra cómo usar el método [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) para autenticar a un usuario.


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




