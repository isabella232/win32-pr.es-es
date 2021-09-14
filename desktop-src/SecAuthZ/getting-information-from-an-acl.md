---
description: Se proporcionan varias funciones que recuperan información de control de acceso de una lista de control de acceso (ACL).
ms.assetid: a0839c49-09e9-4407-8702-051b88ef2231
title: Obtener información de una ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f87aebc2bc9b05191b5026b990714c2519091be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073698"
---
# <a name="getting-information-from-an-acl"></a>Obtener información de una ACL

Se proporcionan varias funciones que recuperan información de control de acceso de una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL). Estas incluyen funciones para determinar los derechos de acceso que una ACL concede o audita para un administrador de [confianza especificado.](trustees.md) Otras funciones permiten extraer información sobre las entradas [*de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACE) en una ACL.

La [**función GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) recupera una matriz de estructuras [**DE ACCESO \_ EXPLÍCITO**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) que describen las ACE en una ACL. Esto puede ser útil al copiar información ace de una ACL a otra. Por ejemplo, una llamada a **GetExplicitEntriesFromAcl** para obtener información sobre las ACE en una ACL se puede seguir pasando las estructuras DE ACCESO **EXPLÍCITO \_** devueltas en una llamada a la función [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) para crear ace equivalentes en una nueva ACL.

La [**función GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) permite determinar los derechos de acceso efectivos que una DACL concede a un administrador de confianza especificado. Los derechos de acceso efectivos del administrador de confianza son los derechos de acceso que una DACL concede al administrador de confianza o a cualquier grupo del que sea miembro el administrador de confianza. **GetEffectiveRightsFromAcl** comprueba todas las ACE con acceso permitido y denegado en la DACL especificada.

**Siga estos pasos para determinar los derechos de acceso de un administrador de confianza a un objeto.**

1.  Llame a [**la función GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**o GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obtener un puntero a la DACL de un objeto.
2.  Llame a [**la función GetEffectiveRightsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-geteffectiverightsfromacla) para recuperar los derechos de acceso que la DACL concede a un administrador de confianza especificado.

La función [**GetAuditedPermissionsFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getauditedpermissionsfromacla) permite comprobar una SACL para determinar los derechos de acceso auditados para un administrador de confianza especificado o para los grupos de los que el administrador de confianza es miembro. Los derechos auditados indican los tipos de intentos de acceso que hacen que el sistema genere un registro de auditoría en el registro de eventos de seguridad. La función devuelve dos máscaras de acceso: una que contiene los derechos de acceso supervisados para los intentos de acceso con errores y otra que contiene los derechos de acceso [*supervisados*](/windows/desktop/SecGloss/a-gly)para el acceso correcto. **GetAuditedPermissionsFromAcl** comprueba todas las ACE de auditoría del sistema en una SACL.

 

 
