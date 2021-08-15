---
title: Autenticación (ADSI)
description: En ADSI, las credenciales que constan de un nombre de usuario y una contraseña se usan para proporcionar o restringir el acceso a objetos en el servicio de directorio.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- ADSI de autenticación
- ADSI, Usar, Autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19177153d8d66f3c27db5c0c2027faa2e02b213305d760d070f5af90b6ba1058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840562"
---
# <a name="authentication-adsi"></a>Autenticación (ADSI)

En ADSI, las credenciales que constan de un nombre de usuario y una contraseña se usan para proporcionar o restringir el acceso a objetos en el servicio de directorio. La [**función ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) usa las credenciales del subproceso que realiza la llamada para la autenticación. La [**función ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y el método [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) se pueden usar para especificar credenciales que no sean las del subproceso que realiza la llamada. Cuando un objeto está enlazado a con un usuario autenticado, se permite al usuario el acceso al objeto según lo admitido por los requisitos de seguridad del servicio de directorio subyacente.

> [!Note]  
> La [**función ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y el [**método IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) no deben usarse para validar las credenciales de usuario. Para obtener más información sobre cómo validar las credenciales de usuario, vea Microsoft Knowledge Base artículo 180548 [HOWTO: Validate User Credentials on Microsoft Operating Systems](https://support.microsoft.com/kb/180548).

 

En el ejemplo de código siguiente se muestra cómo usar el [**método OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) para autenticar a un usuario.


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



 

 




