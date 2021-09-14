---
description: El Administrador de autorización ofrece un marco de trabajo flexible para integrar el control del acceso basado en roles en las aplicaciones. Permite a los administradores que utilizan estas aplicaciones proporcionar acceso a través de roles de usuario asignados en relación con las funciones de trabajo.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Modelo del administrador de autorización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250460"
---
# <a name="authorization-manager-model"></a>Modelo del administrador de autorización

El Administrador de autorización ofrece un marco de trabajo flexible para integrar el control del acceso basado en roles en las aplicaciones. Permite a los administradores que utilizan estas aplicaciones proporcionar acceso a través de roles de usuario asignados en relación con las funciones de trabajo.

Las aplicaciones del administrador de autorización almacenan la directiva de autorización en forma de almacenes de autorización que se guardan en Active Directory o archivos XML y aplican la directiva de autorización en tiempo de ejecución.

A continuación, las aplicaciones llaman a un método de comprobación de acceso en tiempo de ejecución que comprueba el acceso con la información de la directiva en el almacén de autorización.

La directiva de autorización incluye las siguientes partes:

-   [Almacenes de directivas, aplicaciones y ámbitos](policy-stores--applications--and-scopes.md)
-   [Usuarios y grupos](users-and-groups.md)
-   [Operaciones y tareas](operations-and-tasks.md)
-   [Roles](roles.md)
-   [Reglas de negocio](business-rules.md)
-   [Colecciones](collections.md)

 

 



