---
description: Se proporcionan varias funciones que recuperan información de control de acceso de una lista de control de acceso (ACL).
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Obtención de información de una ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f87aebc2bc9b05191b5026b990714c2519091be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278564"
---
# <a name="getting-information-from-an-acl"></a>Obtención de información de una ACL

Se proporcionan varias funciones que recuperan información de control de acceso de una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL). Incluyen funciones para determinar los derechos de acceso que una ACL concede o audita para un administrador de [confianza](trustees.md)especificado. Otras funciones permiten extraer información sobre las entradas de [*control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) en una ACL.

La función [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) recupera una matriz de estructuras [**de \_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) que describen las ACE en una ACL. Esto puede ser útil cuando se copia información ACE de una ACL a otra. Por ejemplo, una llamada a **GetExplicitEntriesFromAcl** para obtener información sobre las ACE en una ACL se puede seguir pasando las estructuras de **\_ acceso explícita** devueltas en una llamada a la función [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para crear ACE equivalentes en una nueva ACL.

La función [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) le permite determinar los derechos de acceso efectivos que una DACL concede a un administrador de confianza especificado. Los derechos de acceso efectivo del administrador de confianza son los derechos de acceso que una DACL concede al administrador de confianza o a los grupos de los que el administrador de confianza es miembro. **GetEffectiveRightsFromAcl** comprueba todas las ACE de acceso concedidos y de acceso denegado en la DACL especificada.

**Siga estos pasos para determinar los derechos de acceso de un administrador de confianza a un objeto.**

1.  Llame a la función [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obtener un puntero a la DACL de un objeto.
2.  Llame a la función [**GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) para recuperar los derechos de acceso que la DACL concede a un administrador de confianza especificado.

La función [**GetAuditedPermissionsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) permite comprobar una SACL para determinar los derechos de acceso auditados para un administrador de confianza especificado o para cualquier grupo del que sea miembro el administrador de confianza. Los derechos auditados indican los tipos de intentos de acceso que hacen que el sistema genere un registro de auditoría en el registro de eventos de seguridad. La función devuelve dos [*máscaras de acceso*](/windows/desktop/SecGloss/a-gly): una que contiene los derechos de acceso supervisados para los intentos de acceso incorrectos y otra que contiene los derechos de acceso supervisados para obtener acceso correctamente. **GetAuditedPermissionsFromAcl** comprueba todas las ACE de auditoría del sistema en una SACL.

 

 
