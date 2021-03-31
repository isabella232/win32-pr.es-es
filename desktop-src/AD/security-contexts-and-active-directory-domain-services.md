---
title: Contextos de seguridad y Active Directory Domain Services
description: Cuando una aplicación se enlaza a un controlador de Dominio de Active Directory (DC), lo hace en el contexto de seguridad de una entidad de seguridad, que puede ser un usuario o una entidad como, por ejemplo, un equipo o un servicio de sistema.
ms.assetid: 7ad0acbe-f81b-46d6-be87-3526b0bfbd1b
ms.tgt_platform: multiple
keywords:
- Active Directory de Active Directory, contextos de seguridad
- contextos de seguridad Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337cb05f8158dbb90f231652c42fb10a486aef4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077494"
---
# <a name="security-contexts-and-active-directory-domain-services"></a>Contextos de seguridad y Active Directory Domain Services

Cuando una aplicación se enlaza a un controlador de Dominio de Active Directory (DC), lo hace en el contexto de seguridad de una entidad de seguridad, que puede ser un usuario o una entidad como, por ejemplo, un equipo o un servicio de sistema. El contexto de seguridad es la cuenta de usuario que el sistema utiliza para exigir la seguridad cuando un subproceso intenta tener acceso a un objeto protegible. Estos datos incluyen el identificador de seguridad (SID) del usuario, las pertenencias a grupos y los privilegios.

Un usuario establece un contexto de seguridad mediante la presentación de credenciales para la autenticación. Si se autentican las credenciales, el sistema genera un token de acceso que identifica las pertenencias a grupos y los privilegios asociados a la cuenta de usuario. El sistema comprueba el token de acceso al intentar tener acceso a un objeto de directorio. Compara los datos del token de acceso con las cuentas y grupos a los que el descriptor de seguridad de objeto ha concedido o denegado.

Use los métodos siguientes para controlar el contexto de seguridad con el que se enlaza a un Active Directory DC:

-   Enlace mediante la opción de **\_ \_ autenticación segura de ADS** con la función [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) o el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) y especifique explícitamente un nombre de usuario y una contraseña. El sistema autentica estas credenciales y genera un token de acceso que utiliza para la comprobación de acceso mientras dure dicho enlace. Para más información, consulte [Autenticación](authentication.md).
-   Enlazar mediante la opción de **\_ \_ autenticación segura de ADS** , pero sin especificar credenciales. Si no va a suplantar a un usuario, el sistema utiliza el contexto de seguridad principal de la aplicación, es decir, el contexto de seguridad del usuario que inició la aplicación. En el caso de un servicio del sistema, este es el contexto de seguridad de la cuenta de servicio o la cuenta LocalSystem.
-   Suplantar a un usuario y, a continuación, enlazar con la **\_ \_ autenticación segura de ADS**, pero sin especificar credenciales. En este caso, el sistema utiliza el contexto de seguridad del cliente que se suplanta. Para obtener más información, vea [suplantación de cliente](/windows/desktop/SecAuthZ/client-impersonation).
-   Enlace con [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) con la opción **ADS \_ no \_ Authentication** . Este método enlaza sin autenticación y da como resultado "todos" como el contexto de seguridad. Solo el proveedor LDAP es compatible con esta opción.

Si es posible, enlace sin especificar credenciales. Es decir, use el contexto de seguridad del usuario que ha iniciado sesión o del cliente suplantado. Esto le permite evitar el almacenamiento en caché de las credenciales. Si debe usar credenciales de usuario alternativas, pida las credenciales y enlácelo, pero no las almacene en caché. Para usar el mismo contexto de seguridad en varias operaciones de enlace, puede especificar el nombre de usuario y la contraseña para la primera operación de enlace y, a continuación, especificar solo el nombre de usuario para realizar los siguientes enlaces. Para obtener más información sobre el uso de esta técnica, vea [autenticación](authentication.md).

Algunos contextos de seguridad son más eficaces que otros. Por ejemplo, la cuenta LocalSystem en un controlador de dominio tiene acceso completo a Active Directory Domain Services, mientras que un usuario típico solo tiene acceso limitado a algunos de los objetos del directorio. En general, la aplicación no debe ejecutarse en un contexto de seguridad eficaz, como LocalSystem, cuando un contexto de seguridad menos eficaz es suficiente para realizar las operaciones. Esto significa que es posible que desee dividir la aplicación en componentes independientes, cada uno de los cuales se ejecuta en un contexto de seguridad adecuado para las operaciones que se deben realizar. Por ejemplo, la configuración de la aplicación puede dividirse de la siguiente manera:

-   Realizar cambios de esquema y extensiones en el contexto de un usuario que sea miembro del grupo administradores de esquema.
-   Realizar cambios en el contenedor de configuración en el contexto de un usuario que sea miembro del grupo administradores de empresas.
-   Realizar cambios en el contenedor de dominio en el contexto de un usuario que sea miembro del grupo administradores de dominio.

 

 