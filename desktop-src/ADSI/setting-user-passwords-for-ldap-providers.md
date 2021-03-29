---
title: Establecer y cambiar las contraseñas de usuario con el proveedor LDAP
description: Para establecer una contraseña de usuario, use el método IADsUser. SetPassword.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- ADSI Provider de LDAP, objeto de usuario, establecer contraseñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5488146de271ac1108a904cd85163fad9d7dd205
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359410"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Establecer y cambiar las contraseñas de usuario con el proveedor LDAP

Para establecer una contraseña de usuario, use el método [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .

El proveedor LDAP de Active Directory usa uno de tres procesos para establecer la contraseña (los directorios LDAP de terceros como iPlanet no usan este proceso de autenticación de contraseña). El método puede variar según la configuración de red. Los métodos set password se producen en el orden siguiente:

-   En primer lugar, el proveedor LDAP intenta usar LDAP a través de una conexión SSL de 128 bits. Para que SSL de LDAP funcione correctamente, el servidor LDAP debe tener instalado el certificado de autenticación de servidor apropiado y los clientes que ejecutan el código ADSI deben confiar en la autoridad que emitió dichos certificados. Tanto el servidor como el cliente deben admitir el cifrado de 128 bits.
-   En segundo lugar, si la conexión SSL no se realiza correctamente, el proveedor LDAP intenta usar Kerberos. En Windows 2000, es posible que Kerberos no admita la autenticación entre bosques. Las mejoras posteriores a Kerberos admiten la autenticación entre bosques.
-   En tercer lugar, si Kerberos no se realiza correctamente, el proveedor LDAP intenta una llamada a la API de [**NetUserSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) . En versiones anteriores, ADSI llamaba **NetUserSetInfo** en el contexto de seguridad en el que se estaba ejecutando el subproceso, y no el contexto de seguridad especificado en la llamada a [**IADsOpenDSObject. OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject). En versiones posteriores, se cambió para que el proveedor LDAP de ADSI suplante al usuario especificado en la llamada a **OpenDSObject** cuando llama a **NetUserSetInfo**.

Para cambiar una contraseña de usuario, use el método [**IADsUser. ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) . Como [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), este método puede usar varios procesos para cambiar la contraseña. Los métodos de cambio de contraseña se producen en el orden siguiente:

-   En primer lugar, el proveedor LDAP intenta usar LDAP a través de una conexión SSL de 128 bits.
-   En segundo lugar, si la conexión 128-SSL no se realiza correctamente, el proveedor LDAP intenta una llamada a la API [**NetUserChangePassword**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) . Como [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), en versiones anteriores, el proveedor LDAP de ADSI suplanta las credenciales de usuario pasadas mediante el método [**IADsOpenDSObject. OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

 

 