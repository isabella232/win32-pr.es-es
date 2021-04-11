---
title: Enlazar con cifrado
description: Se debe cifrar la información confidencial intercambiada a través de una red.
ms.assetid: 51fe2131-5f7d-41b1-ad88-d965cbb4d630
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, enlazar con cifrado
- Enlazar con cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf19747a8356459f4ab50c0aa409f69b58eb224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993868"
---
# <a name="binding-with-encryption"></a>Enlazar con cifrado

Se debe cifrar la información confidencial intercambiada a través de una red. Para permitirlo, ADSI admite dos tipos de cifrado, Kerberos y Capa de sockets seguros (SSL). Ambos tipos de cifrado requieren el uso de [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) para el enlace.

No se puede usar **GetObject** y [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para el enlace en este caso porque estas funciones hacen que las solicitudes LDAP usadas por ADSI y los datos devueltos del servidor de directorio se transmitan a través de la red como texto sin formato. Con fines de depuración, resulta útil desactivar el cifrado, por lo que el Monitor de red se puede usar para ver las solicitudes LDAP y los datos entre el cliente y el servidor de directorio.

## <a name="kerberos-based-encryption"></a>Cifrado basado en Kerberos

Para usar el cifrado basado en Kerberos, especifique la marca de **\_ \_ sellado usar de ADS** al llamar a [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). La marca de **\_ \_ sellado usar** también puede usarse para comprobar la integridad de los datos, es decir, para asegurarse de que los datos recibidos son los mismos que los datos enviados. Si se especifica la marca de **\_ sellado usar el \_ sellado** , la marca de **\_ \_ firma usar** también se especifica automáticamente. Ambas marcas requieren la autenticación Kerberos, que solo funciona en las siguientes condiciones:

-   El equipo cliente debe haber iniciado sesión en el dominio de Windows o en un dominio de confianza para un dominio de Windows.
-   Se debe llamar a [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) con credenciales null; es decir, no se pueden especificar credenciales alternativas.

## <a name="ssl-based-encryption"></a>Cifrado basado en SSL

Para usar el cifrado basado en SSL, especifique la marca **ADS \_ use \_ SSL** al llamar a [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Si solo se especifica la marca de **\_ uso de \_ SSL de ADS** , ADSI abre el puerto SSL 636 y, a continuación, realiza un enlace simple a través de ese canal SSL. Si se especifican las marcas SSL de **ADS \_ Secure \_ Authentication** y **ADS \_ use \_** , el comportamiento del enlace depende del cliente desde el que se realiza la llamada. En las versiones no admitidas de Windows, ADSI abre primero un canal SSL y realiza un enlace simple con el nombre de usuario y la contraseña especificados o el contexto del usuario actual si el nombre de usuario y la contraseña son NULL. En las versiones compatibles de Windows, ADSI realiza una autenticación segura en lugar de un enlace simple.

Para usar el cifrado basado en SSL mientras se comunica con Active Directory, Active Directory debe tener habilitada la infraestructura de clave pública (PKI). La PKI se puede habilitar mediante la configuración de una entidad de certificación empresarial en uno de los servidores de Active Directory, incluido uno de los servidores de Active Directory. La configuración de una entidad de certificación empresarial hace que un servidor de Active Directory obtenga un certificado de servidor que se puede usar para realizar el cifrado basado en SSL.

 

 




