---
title: Delegación
description: La delegación es una de las características de seguridad más importantes de Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- AD de delegación
- seguridad AD, Delegación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993913"
---
# <a name="delegation"></a>Delegación

La *delegación* es una de las características de seguridad más importantes de Active Directory Domain Services. La delegación permite a una autoridad administrativa superior conceder derechos administrativos específicos para contenedores y subárboles a usuarios y grupos. Ya no se necesitan administradores de dominio, con una amplia autoridad sobre grandes segmentos de usuarios.

Una ACE puede conceder derechos administrativos específicos para los objetos de un contenedor a un usuario o grupo. Los derechos se conceden para operaciones específicas en clases de objeto específicas mediante ACE en la ACL del contenedor. Por ejemplo, para permitir que un usuario llamado "usuario 1" sea un administrador de la unidad organizativa "contabilidad corporativa", agregue ACE a la ACL en "contabilidad corporativa" como se indica a continuación:

"" usuario 1 "; Garantizar Crear, modificar, eliminar; usuario de clase de objeto "usuario 1"; Garantizar Crear, modificar, eliminar; grupo de clase de objeto "usuario 1"; Garantizar Escritura; usuario de clase de objeto; Contraseña de atributo "

Ahora, el usuario 1 puede crear nuevos usuarios y grupos en las cuentas corporativas y establecer las contraseñas de los usuarios existentes, pero el usuario 1 no puede crear ninguna otra clase de objeto y no puede afectar a los usuarios de ningún otro contenedor, a menos que, por supuesto, se conceda al usuario 1 acceso mediante ACE en los otros contenedores.

 

 




