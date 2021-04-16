---
description: El valor lógico de una propiedad que se ha establecido es true.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Usar propiedades en instrucciones condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677395"
---
# <a name="using-properties-in-conditional-statements"></a>Usar propiedades en instrucciones condicionales

El valor lógico de una propiedad que se ha establecido es true. Para determinar si una propiedad se establece sin obtener realmente su valor, pruebe la expresión lógica "propiedad" o "no propiedad". Cuando se establece la propiedad Property, el primero se evalúa como true y el último como false.

Una o más propiedades se pueden combinar con operadores para formar expresiones lógicas utilizadas en instrucciones condicionales. Para obtener más información sobre los operadores que se pueden utilizar en instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).

Se puede especificar una instrucción condicional con propiedades en la columna condición de la [tabla condición](condition-table.md) para modificar el estado de selección de cualquier entrada en la [tabla de características](feature-table.md).

Las instrucciones condicionales con una o más propiedades se usan normalmente en la columna condición de las tablas de base de datos.

Cada una de las tablas siguientes tiene una columna para las expresiones condicionales:

-   [Tabla de condiciones](condition-table.md)
-   [Tabla ControlEvent,](controlevent-table.md)
-   [Tabla LaunchCondition](launchcondition-table.md)
-   [Tabla InstallUISequence](installuisequence-table.md)
-   [Tabla InstallExecuteSequence](installexecutesequence-table.md)
-   [Tabla ControlCondition](controlcondition-table.md)
-   [Tabla AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabla AdvtExecuteSequence](advtexecutesequence-table.md)
-   [Tabla AdminUISequence](adminuisequence-table.md)

Tenga en cuenta que las seis tablas de secuencia de acciones tienen campos para una condición. Si la expresión condicional de este campo se evalúa como false, el instalador omite esa acción.

Si establece una [propiedad privada](private-properties.md) en la secuencia de la interfaz de usuario mediante la creación de una acción personalizada en una de las tablas de secuencia de la interfaz de usuario, esa propiedad no se establece en la secuencia de ejecución. Para establecer la propiedad en la secuencia de ejecución, también debe colocar una acción personalizada en una tabla de secuencia de ejecución. Como alternativa, puede convertir la propiedad en una [propiedad pública](public-properties.md) e incluirla en la propiedad [**SecureCustomProperties**](securecustomproperties.md) .

Para obtener más información, vea [usar una tabla de secuencia](using-a-sequence-table.md) o [usar propiedades](using-properties.md).

 

 



