---
description: El \_ derecho de acceso de seguridad del sistema de acceso \_ controla la capacidad de obtener o establecer la SACL en un descriptor de seguridad de objetos. El sistema concede este derecho de acceso si el \_ \_ privilegio de nombre de seguridad se habilita en el token de acceso del subproceso que lo solicita.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Derecho de acceso SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666661"
---
# <a name="sacl-access-right"></a>Derecho de acceso SACL

El \_ derecho de acceso de seguridad del sistema de acceso \_ controla la capacidad de obtener o establecer la SACL en el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto. El sistema concede este derecho de acceso solo si el \_ \_ privilegio de nombre de seguridad se habilita en el [*token de acceso*](/windows/desktop/SecGloss/a-gly) del subproceso que lo solicita.

**Para tener acceso a la SACL de un objeto**

1.  Llame a la función [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar el \_ privilegio de nombre de seguridad de se \_ .
2.  Solicite el \_ derecho de acceso de seguridad del sistema de acceso \_ cuando abra un identificador para el objeto.
3.  Obtiene o establece la SACL del objeto mediante una función como [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  Llame a [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para deshabilitar el privilegio de nombre de seguridad de se \_ \_ .

Para acceder a una SACL mediante las funciones [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , habilite el \_ privilegio de nombre de seguridad de se \_ . La función solicita internamente el derecho de acceso.

El \_ \_ derecho de acceso de seguridad del sistema de acceso no es válido en una DACL porque las DACL no controlan el acceso a una SACL. Sin embargo, puede usar el \_ \_ derecho de acceso de seguridad del sistema de acceso en una SACL para auditar los intentos de usar el derecho de acceso.

 

 
