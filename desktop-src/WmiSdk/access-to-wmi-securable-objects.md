---
description: WMI se basa en los descriptores de seguridad de Windows estándar para controlar y proteger el acceso a objetos protegibles como espacios de nombres WMI, impresoras, servicios y aplicaciones DCOM.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Acceso a objetos protegibles de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278778"
---
# <a name="access-to-wmi-securable-objects"></a>Acceso a objetos protegibles de WMI

WMI se basa en los [*descriptores de seguridad*](/windows/desktop/SecGloss/s-gly) de Windows estándar para controlar y proteger el acceso a objetos protegibles como espacios de nombres WMI, impresoras, servicios y aplicaciones DCOM. Para obtener más información, vea [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md).

En esta sección se explican los temas siguientes:

-   [Descriptores de seguridad y SID](#security-descriptors-and-sids)
-   [Control de acceso](#access-control)
-   [Cambiar la seguridad de acceso](#changing-access-security)
-   [Temas relacionados](#related-topics)

## <a name="security-descriptors-and-sids"></a>Descriptores de seguridad y SID

WMI mantiene la seguridad de acceso al comparar el [*token de acceso*](/windows/desktop/SecGloss/a-gly) del usuario que intenta tener acceso a un objeto protegible con el descriptor de seguridad del objeto.

Cuando se crea un usuario o grupo en un sistema, a la cuenta se le asigna un [*identificador de seguridad (SID)*](/windows/desktop/SecGloss/s-gly) . el SID garantiza que una cuenta creada con el mismo nombre que una cuenta previamente eliminada no hereda la configuración de seguridad anterior. Un token de acceso se crea mediante la combinación del SID, la lista de grupos a los que pertenece el usuario y la lista de privilegios habilitados o deshabilitados. Estos tokens se asignan a todos los procesos y subprocesos que pertenecen al usuario.

## <a name="access-control"></a>Control de acceso

Cuando el usuario desea usar un objeto protegido, el token de acceso se compara con la [*lista de control de acceso discrecional (DACL)*](/windows/desktop/SecGloss/d-gly) del descriptor de seguridad del objeto. DACL contiene permisos denominados [*entradas de control de acceso (ACE)*](/windows/desktop/SecGloss/a-gly). Las [*listas de control de acceso del sistema (SACL)*](/windows/desktop/SecGloss/s-gly) hacen lo mismo que las DACL, pero pueden generar eventos de auditoría de seguridad. A partir de Windows Vista, WMI puede realizar entradas de auditoría en el registro de seguridad de Windows. Para obtener más información acerca de la auditoría en WMI, consulte [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md).

La DACL y la SACL constan de una lista de ACE que describen qué usuarios tienen derechos de acceso específicos, incluida la escritura en el repositorio WMI, el acceso remoto y la ejecución, y los permisos de inicio de sesión. WMI almacena estas ACL en el repositorio WMI.

Las ACE contienen tres tipos de niveles de acceso o derechos de concesión o denegación: permitir, denegar para DACL y auditoría del sistema (para SACL). Las ACE de denegación preceden a las ACE de permiso en la DACL o SACL. Al comprobar los derechos de acceso de usuario, WMI se ejecuta consecutivamente a través de la lista de control de acceso hasta que encuentra una ACE de permiso que se aplica al token de acceso que realiza la solicitud. Las ACE restantes no se comprueban después de este punto. Si no se encuentra ningún ACE de permiso adecuado, se denegará el acceso. Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) y [crear una DACL](/windows/desktop/SecBP/creating-a-dacl).

## <a name="changing-access-security"></a>Cambiar la seguridad de acceso

Con los permisos adecuados, puede cambiar la seguridad de un objeto protegible con un script o una aplicación. También puede cambiar la configuración de seguridad en los espacios de nombres WMI mediante el [*control WMI*](gloss-w.md) o agregando una cadena de [lenguaje de definición de descriptores de seguridad (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) en el archivo [*Managed Object Format (MOF)*](gloss-m.md) que define las clases para el espacio de nombres. Para obtener más información, vea [acceso a espacios de nombres WMI](access-to-wmi-namespaces.md), [protección de espacios de nombres WMI](securing-wmi-namespaces.md)y [cambio de la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[Control de cuentas de usuario y WMI](user-account-control-and-wmi.md)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
