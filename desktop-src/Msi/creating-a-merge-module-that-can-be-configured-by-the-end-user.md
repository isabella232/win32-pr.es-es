---
description: Para crear módulos de combinación, utilice las directrices generales que se describen en el tema creación de módulos de combinación.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Crear un módulo de combinación que puede ser configurado por el End-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db6ff7bd85fb1b6704fc2452c488b8a3bbc06b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277565"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Crear un módulo de combinación que puede ser configurado por el End-User

Para crear módulos de combinación, utilice las directrices generales que se describen en el tema [creación de módulos de combinación](authoring-merge-modules.md) . Además, debe hacer lo siguiente para crear un módulo de combinación que puede ser configurado por el usuario final del módulo:

-   Los usuarios finales deben tener Mergemod.dll versión 2,0 para configurar el módulo. Los usuarios que tienen versiones anteriores de Mergemod.dll pueden aplicar el módulo, pero siempre obtienen los valores predeterminados.
-   Agregue una [tabla ModuleConfiguration](moduleconfiguration-table.md) al módulo de fusión mediante combinación para identificar los elementos que puede configurar un usuario final. Agregue un registro en esta tabla para cada elemento configurable. Estos elementos se sustituyen en las plantillas que se especifican en la [tabla ModuleSubstitution](modulesubstitution-table.md). Escriba un nombre para cada elemento configurable en el campo nombre. Escriba el formato, el tipo y el contexto semántico de cada elemento en las columnas Format, Type y ContextData. Para obtener más información, vea [tipos semánticos](semantic-types.md). Escriba un valor predeterminado para el elemento en el campo DefaultValue con el [formato especial de CMsM](cmsm-special-format.md).
-   Agregue una [tabla ModuleSubstitution](modulesubstitution-table.md) al módulo de combinación. Cada registro de esta tabla corresponde a una sustitución de uno o más elementos configurables en un campo de la base de datos del módulo de combinación. Escriba la tabla, la fila y la columna del campo que recibe la sustitución. Escriba una plantilla de formato para la sustitución en la columna valor mediante el [formato especial de CMsM](cmsm-special-format.md).
-   Agregue registros a la [tabla de validación](-validation-table.md) para las tablas ModuleSubstitution y ModuleConfiguration.
-   Agregue registros a la [tabla ModuleIgnoreTable](moduleignoretable-table.md) para la [tabla ModuleSubstitution](modulesubstitution-table.md) y la [tabla ModuleConfiguration](moduleconfiguration-table.md). Esto garantiza que el módulo sea compatible con los usuarios que tengan versiones de Mergemod.dll anteriores a la versión 2,0.

 

 



