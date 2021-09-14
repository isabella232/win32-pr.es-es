---
description: Para crear módulos de mezcla, use las directrices generales que se describen en el tema Creación de módulos de mezcla.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Crear un módulo de mezcla que pueda configurar el End-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db6ff7bd85fb1b6704fc2452c488b8a3bbc06b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158737"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Crear un módulo de mezcla que pueda configurar el End-User

Para crear módulos de mezcla, use las directrices generales que se describen en el tema [Creación de módulos de mezcla.](authoring-merge-modules.md) Además, debe hacer lo siguiente para crear un módulo de combinación que pueda configurar el usuario final del módulo:

-   Los usuarios finales deben tener Mergemod.dll versión 2.0 para configurar el módulo. Los usuarios que tienen versiones anteriores de Mergemod.dll pueden aplicar el módulo, pero siempre obtienen la configuración predeterminada.
-   Agregue una [tabla ModuleConfiguration](moduleconfiguration-table.md) al módulo de combinación para identificar los elementos que un usuario final puede configurar. Agregue un registro en esta tabla para cada elemento configurable. Estos elementos se sustituyen en las plantillas especificadas en [la tabla ModuleSubstitution](modulesubstitution-table.md). Escriba un nombre para cada elemento configurable en el campo Nombre. Escriba el formato, el tipo y el contexto semántico de cada elemento de las columnas Format, Type y ContextData. Para obtener más información, vea [Tipos semánticos](semantic-types.md). Escriba un valor predeterminado para el elemento en el campo DefaultValue con el [formato especial de CMSM](cmsm-special-format.md).
-   Agregue una [tabla ModuleSubstitution al](modulesubstitution-table.md) módulo merge. Cada registro de esta tabla corresponde a una sustitución de uno o varios elementos configurables en un campo de la base de datos del módulo de mezcla. Escriba la tabla, fila y columna del campo que recibe la sustitución. Escriba una plantilla de formato para la sustitución en la columna Valor mediante el [formato especial de CMSM](cmsm-special-format.md).
-   Agregue registros a la [tabla de validación para](-validation-table.md) las tablas ModuleSubstitution y ModuleConfiguration.
-   Agregue registros a la [tabla ModuleIgnoreTable para](moduleignoretable-table.md) [la tabla ModuleSubstitution y](modulesubstitution-table.md) la tabla [ModuleConfiguration](moduleconfiguration-table.md). Esto garantiza que el módulo sea compatible con los usuarios que tienen versiones de Mergemod.dll anteriores a la versión 2.0.

 

 



