---
description: Una lista de control de acceso (ACL) es una lista de entradas de control de acceso (ACE).
ms.assetid: c9aff246-fe11-4d82-b944-b10c3d9ae170
title: Listas de control de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a788f02f8a04711be7db8268833375b2519d0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073759"
---
# <a name="access-control-lists"></a>Listas de control de acceso

Una [*lista de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACL) es una lista de entradas de control de [acceso](access-control-entries.md) (ACE). Cada ACE de una ACL identifica a un [usuario de confianza](trustees.md) y especifica los [derechos de acceso](access-rights-and-access-masks.md) concedidos, denegados o auditados para dicho usuario. El [descriptor de seguridad](security-descriptors.md) de un objeto [protegible](securable-objects.md) puede contener dos tipos de ACL: una DACL y una SACL.

Una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) identifica a los administradores de confianza a los que se les permite o se deniega el acceso a un objeto protegible. Cuando un [*proceso*](/windows/desktop/SecGloss/p-gly) intenta acceder a un objeto protegible, el sistema comprueba las ACE de la DACL del objeto para determinar si se debe conceder acceso a él. Si el objeto no tiene una DACL, el sistema concede acceso total a todos los usuarios. Si la DACL del objeto no tiene ACE, el sistema deniega todos los intentos de acceso al objeto porque dacl no permite ningún derecho de acceso. El sistema comprueba las ACE en secuencia hasta que encuentra uno o varios AEE que permitan todos los derechos de acceso solicitados, o hasta que se deniegue cualquiera de los derechos de acceso solicitados. Para obtener más información, vea [Cómo controlan las DACL el acceso a un objeto](how-dacls-control-access-to-an-object.md). Para obtener información sobre cómo crear correctamente una DACL, vea [Creación de una DACL.](/windows/desktop/SecBP/creating-a-dacl)

Una [*lista de control de acceso del*](/windows/desktop/SecGloss/s-gly) sistema (SACL) permite a los administradores registrar intentos de acceso a un objeto protegido. Cada ACE especifica los tipos de intentos de acceso por parte de un administrador de confianza especificado que hacen que el sistema genere un registro en el registro de eventos de seguridad. Una ACE en una SACL puede generar registros de auditoría cuando se produce un error en un intento de acceso, cuando se realiza correctamente o en ambos casos. Para obtener más información sobre las SACL, vea [Generación de auditorías](audit-generation.md) y Derecho [de acceso SACL.](sacl-access-right.md)

No intente trabajar directamente con el contenido de una ACL. Para asegurarse de que las ACL son semánticamente correctas, use las funciones adecuadas para crear y manipular acl. Para obtener más información, vea [Obtener información de una ACL y](getting-information-from-an-acl.md) Crear o modificar una [ACL.](creating-or-modifying-an-acl.md)

Las ACL también proporcionan control de acceso a los objetos Active Directory servicio de directorio de Microsoft. Active Directory interfaces de servicio (ADSI) incluyen rutinas para crear y modificar el contenido de estas ACL. Para obtener más información, vea [Controlar el acceso a Active Directory objetos](/windows/desktop/AD/controlling-access-to-objects-in-active-directory-domain-services).

 

 
