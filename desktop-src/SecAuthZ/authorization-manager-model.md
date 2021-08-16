---
description: El Administrador de autorización ofrece un marco de trabajo flexible para integrar el control del acceso basado en roles en las aplicaciones. Permite a los administradores que utilizan estas aplicaciones proporcionar acceso a través de roles de usuario asignados en relación con las funciones de trabajo.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modelo del administrador de autorización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20973b8b3e1b35780cc771c04302430b44352a112745842dcbdb66e92b948aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784204"
---
# <a name="authorization-manager-model"></a>Modelo del administrador de autorización

El Administrador de autorización ofrece un marco de trabajo flexible para integrar el control del acceso basado en roles en las aplicaciones. Permite a los administradores que utilizan estas aplicaciones proporcionar acceso a través de roles de usuario asignados en relación con las funciones de trabajo.

Las aplicaciones del administrador de autorización almacenan la directiva de autorización en forma de almacenes de autorización que se guardan en Active Directory o archivos XML y aplican la directiva de autorización en tiempo de ejecución.

A continuación, las aplicaciones llaman a un método de comprobación de acceso en tiempo de ejecución que comprueba el acceso con la información de directiva en el almacén de autorización.

La directiva de autorización incluye las siguientes partes:

-   [Almacenes de directivas, aplicaciones y ámbitos](policy-stores--applications--and-scopes.md)
-   [Usuarios y grupos](users-and-groups.md)
-   [Operaciones y tareas](operations-and-tasks.md)
-   [Roles](roles.md)
-   [Reglas de negocio](business-rules.md)
-   [Colecciones](collections.md)

 

 



