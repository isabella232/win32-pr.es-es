---
description: El valor lógico de una propiedad que se ha establecido es True.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Usar propiedades en instrucciones condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5dcee5c2d657b8014ac98c0d4d1ce5b56f0f3614a597cd63611ae965e30720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499215"
---
# <a name="using-properties-in-conditional-statements"></a>Usar propiedades en instrucciones condicionales

El valor lógico de una propiedad que se ha establecido es True. Para determinar si una propiedad se establece sin obtener realmente su valor, pruebe la expresión lógica "MyProperty" o "Not MyProperty". Cuando se establece la propiedad MyProperty, la primera se evalúa como True y la segunda como False.

Una o varias propiedades se pueden combinar con operadores para formar expresiones lógicas usadas en instrucciones condicionales. Para obtener más información sobre los operadores que se pueden usar en instrucciones condicionales, vea [Sintaxis de instrucciones condicionales.](conditional-statement-syntax.md)

Se puede especificar una instrucción condicional que use propiedades en la columna Condición de la tabla [Condición](condition-table.md) para modificar el estado de selección de cualquier entrada de la [tabla Característica](feature-table.md).

Las instrucciones condicionales con una o varias propiedades se usan normalmente en la columna Condición de las tablas de base de datos.

Las tablas siguientes tienen una columna para expresiones condicionales:

-   [Tabla de condiciones](condition-table.md)
-   [Tabla ControlEvent](controlevent-table.md)
-   [Tabla LaunchCondition](launchcondition-table.md)
-   [Tabla InstallUISequence](installuisequence-table.md)
-   [Tabla InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabla ControlCondition](controlcondition-table.md)
-   [Tabla AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabla AdvtExecuteSequence](advtexecutesequence-table.md)
-   [Tabla AdminUISequence](adminuisequence-table.md)

Tenga en cuenta que las seis tablas de secuencia de acciones tienen campos para una condición. Si la expresión condicional de este campo se evalúa como False, el instalador omite esa acción.

Si establece una [propiedad](private-properties.md) privada en la secuencia de la interfaz de usuario mediante la creación de una acción personalizada en una de las tablas de secuencia de la interfaz de usuario, esa propiedad no se establece en la secuencia de ejecución. Para establecer la propiedad en la secuencia de ejecución, también debe colocar una acción personalizada en una tabla de secuencia de ejecución. Como alternativa, puede convertir la propiedad en una [propiedad pública](public-properties.md) e incluirla en la [**propiedad SecureCustomProperties.**](securecustomproperties.md)

Para obtener más información, [vea Usar una tabla de secuencia o](using-a-sequence-table.md) Usar [propiedades](using-properties.md).

 

 



