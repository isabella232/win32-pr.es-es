---
description: Explica las partes del modelo de control de acceso.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Partes del modelo de Access Control datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bffdbf6542a9e29360437c50f47495d83467334e09c7aa55e8a136a8fc7556d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785675"
---
# <a name="parts-of-the-access-control-model"></a>Partes del modelo de Access Control datos

Hay dos partes básicas del modelo de control de acceso:

-   [Tokens de](access-tokens.md)acceso, que contienen información sobre un usuario que ha iniciado sesión
-   [Descriptores de seguridad](security-descriptors.md), que contienen la información de seguridad que protege un [objeto protegible](securable-objects.md)

Cuando un usuario inicia sesión, el sistema [*autentica*](/windows/desktop/SecGloss/a-gly) el nombre de cuenta y la contraseña del usuario. Si el inicio de sesión se realiza correctamente, el sistema crea un token de acceso. Cada [*proceso*](/windows/desktop/SecGloss/p-gly) ejecutado en nombre de este usuario tendrá una copia de este token de acceso. El token de acceso contiene [identificadores de seguridad](security-identifiers.md) que identifican la cuenta del usuario y las cuentas de grupo a las que pertenece el usuario. El token también contiene una lista de los [privilegios que](privileges.md) tiene el usuario o los grupos del usuario. El sistema usa este token para identificar al usuario asociado cuando un proceso intenta acceder a un objeto protegible o realizar una tarea de administración del sistema que requiere privilegios.

Cuando se crea un objeto protegible, el sistema le asigna un [*descriptor*](/windows/desktop/SecGloss/s-gly) de seguridad que contiene información de seguridad especificada por su creador, o información de seguridad predeterminada si no se especifica ninguno. Las aplicaciones pueden usar funciones para recuperar y establecer la información de seguridad de un objeto existente.

Un descriptor de seguridad identifica el propietario del objeto y también puede contener las siguientes listas [de control de acceso:](access-control-lists.md)

-   Lista [*de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) que identifica los usuarios y grupos a los que se les ha permitido o denegado el acceso al objeto.
-   Lista [*de control de acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL) que controla cómo las [auditorías del](audit-generation.md) sistema intentan acceder al objeto

Una ACL contiene una lista de entradas [de control de acceso](access-control-entries.md) (ACE). Cada ACE especifica un [](access-rights-and-access-masks.md) conjunto de derechos de acceso y contiene un SID que identifica [a](trustees.md) un administrador de confianza para el que se permiten, deniegan o auditan los derechos. Un administrador de confianza puede ser una cuenta de usuario, una cuenta de grupo o una [*sesión de inicio de sesión*](/windows/desktop/SecGloss/l-gly).

Use funciones para manipular el contenido de descriptores de seguridad, SID y ACL en lugar de acceder a ellos directamente. Esto ayuda a garantizar que estas estructuras siguen siendo sintácticamente precisas y evita que futuras mejoras en el sistema de seguridad rompa el código existente.

En los temas siguientes se proporciona información sobre las partes del modelo de control de acceso:

-   [Tokens de acceso](access-tokens.md)
-   [Descriptor de seguridad](security-descriptors.md)
-   [Access Control listas](access-control-lists.md)
-   [Access Control entradas](access-control-entries.md)
-   [Derechos de acceso y máscaras de acceso](access-rights-and-access-masks.md)
-   [Funcionamiento de AccessCheck](how-dacls-control-access-to-an-object.md)
-   [Directiva de autorización centralizada](centralized-authorization-policy.md)
-   [Identificadores de seguridad](security-identifiers.md)

 

 
