---
description: Explica las partes del modelo de control de acceso.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Partes del modelo de Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3aa6d3547d486c33f4b31cdb5d5de24c7d27cec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908994"
---
# <a name="parts-of-the-access-control-model"></a>Partes del modelo de Access Control

Hay dos partes básicas del modelo de control de acceso:

-   [Tokens de acceso](access-tokens.md), que contienen información sobre un usuario que ha iniciado sesión
-   [Descriptores de seguridad](security-descriptors.md), que contienen la información de seguridad que protege un [objeto protegible](securable-objects.md)

Cuando un usuario inicia sesión, el sistema [*autentica*](/windows/desktop/SecGloss/a-gly) el nombre de cuenta y la contraseña del usuario. Si el inicio de sesión se realiza correctamente, el sistema crea un token de acceso. Cada [*proceso*](/windows/desktop/SecGloss/p-gly) ejecutado en nombre de este usuario tendrá una copia de este token de acceso. El token de acceso contiene los [identificadores de seguridad](security-identifiers.md) que identifican la cuenta del usuario y las cuentas de grupo a las que pertenece el usuario. El token también contiene una lista de los [privilegios](privileges.md) que mantiene el usuario o los grupos del usuario. El sistema utiliza este token para identificar al usuario asociado cuando un proceso intenta tener acceso a un objeto protegible o realizar una tarea de administración del sistema que requiere privilegios.

Cuando se crea un objeto protegible, el sistema le asigna un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) que contiene la información de seguridad especificada por su creador o la información de seguridad predeterminada si no se especifica ninguno. Las aplicaciones pueden usar funciones para recuperar y establecer la información de seguridad de un objeto existente.

Un descriptor de seguridad identifica el propietario del objeto y también puede contener las siguientes [listas de control de acceso](access-control-lists.md):

-   Una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) que identifica a los usuarios y grupos a los que se permite o deniega el acceso al objeto.
-   Una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL) que controla el modo en que las [auditorías](audit-generation.md) del sistema intentan obtener acceso al objeto.

Una ACL contiene una lista de [entradas de control de acceso](access-control-entries.md) (ACE). Cada ACE especifica un conjunto de [derechos de acceso](access-rights-and-access-masks.md) y contiene un SID que identifica un [Administrador de confianza](trustees.md) para el que se permiten, deniegan o auditan los derechos. Un administrador de confianza puede ser una cuenta de usuario, una cuenta de grupo o una [*sesión de inicio*](/windows/desktop/SecGloss/l-gly)de sesión.

Use funciones para manipular el contenido de los descriptores de seguridad, los SID y las ACL en lugar de tener acceso a ellos directamente. Esto ayuda a garantizar que estas estructuras sigan siendo sintácticamente precisas e impedirá que las futuras mejoras en el sistema de seguridad interrumpan el código existente.

En los temas siguientes se proporciona información sobre las partes del modelo de control de acceso:

-   [Tokens de acceso](access-tokens.md)
-   [Descriptor de seguridad](security-descriptors.md)
-   [Access Control listas](access-control-lists.md)
-   [Access Control entradas](access-control-entries.md)
-   [Derechos de acceso y máscaras de acceso](access-rights-and-access-masks.md)
-   [Cómo funciona AccessCheck](how-dacls-control-access-to-an-object.md)
-   [Directiva de autorización centralizada](centralized-authorization-policy.md)
-   [Identificadores de seguridad](security-identifiers.md)

 

 
