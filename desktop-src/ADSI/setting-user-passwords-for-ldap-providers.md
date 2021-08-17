---
title: Establecimiento y cambio de contraseñas de usuario con el proveedor LDAP
description: Para establecer una contraseña de usuario, use el método IADsUser.SetPassword.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- PROVEEDOR LDAP ADSI, objeto de usuario, establecimiento de contraseñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbbd0439a011575fbc9278dbe506d46db2210ce03d807ea74097499cb764b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690530"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Establecimiento y cambio de contraseñas de usuario con el proveedor LDAP

Para establecer una contraseña de usuario, use [**el método IADsUser.SetPassword.**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)

El proveedor LDAP para Active Directory utiliza uno de los tres procesos para establecer la contraseña (los directorios LDAP de terceros, como i Kerberos, no usan este proceso de autenticación de contraseña). El método puede variar según la configuración de red. Los métodos de establecer contraseña se producen en el orden siguiente:

-   En primer lugar, el proveedor LDAP intenta usar LDAP a través de una conexión SSL de 128 bits. Para que LDAP SSL funcione correctamente, el servidor LDAP debe tener instalado el certificado de autenticación de servidor adecuado y los clientes que ejecutan el código ADSI deben confiar en la autoridad que emitió esos certificados. Tanto el servidor como el cliente deben admitir el cifrado de 128 bits.
-   En segundo lugar, si la conexión SSL no se realiza correctamente, el proveedor LDAP intenta usar Kerberos. En Windows 2000, es posible que Kerberos no admita la autenticación entre bosques. Las mejoras posteriores a Kerberos admiten la autenticación entre bosques.
-   En tercer lugar, si Kerberos no se realiza correctamente, el proveedor LDAP intenta una llamada API [**NetUserSetInfo.**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) En versiones anteriores, ADSI llamaba a **NetUserSetInfo** en el contexto de seguridad en el que se estaba ejecutando el subproceso y no al contexto de seguridad especificado en la llamada a [**IADsOpenDSObject.OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o [**ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) En versiones posteriores, esto se cambió para que el proveedor DE ADSI LDAP suplanta al usuario especificado en la llamada **a OpenDSObject** cuando llama a **NetUserSetInfo**.

Para cambiar una contraseña de usuario, use [**el método IADsUser.ChangePassword.**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) Al [**igual que SetPassword,**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)este método puede usar varios procesos para cambiar la contraseña. Los métodos de cambio de contraseña se producen en el orden siguiente:

-   En primer lugar, el proveedor LDAP intenta usar LDAP a través de una conexión SSL de 128 bits.
-   En segundo lugar, si la conexión 128-SSL no se realiza correctamente, el proveedor LDAP intenta una llamada API [**NetUserChangePassword.**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) Al igual que [**SetPassword,**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)en versiones anteriores, el proveedor LDAP ADSI suplanta las credenciales de usuario pasadas mediante el método [**IADsOpenDSObject.OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) o la función [**ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)

 

 