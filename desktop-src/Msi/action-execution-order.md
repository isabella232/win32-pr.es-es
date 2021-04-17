---
description: El orden de ejecución de la acción viene determinado por la secuencia de acciones que se han creado en las tablas de secuencia y por el orden en que el instalador ejecuta las tablas de secuencia.
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: Orden de ejecución de la acción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954c44f6e2525deb3375cb9ea72d0320df3a5f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667063"
---
# <a name="action-execution-order"></a>Orden de ejecución de la acción

El orden de ejecución de la acción viene determinado por la secuencia de acciones que se han creado en las [*tablas de secuencia*](s-gly.md) y por el orden en que el instalador ejecuta las tablas de secuencia. Para obtener más información, consulte las secuencias de acción sugeridas en [usar una tabla de secuencia](using-a-sequence-table.md).

El instalador ejecuta las tablas de secuencia en respuesta a una solicitud de instalación, [anuncio](advertisement.md)o [instalación administrativa](administrative-installation.md). Por ejemplo, en respuesta al uso de las opciones de la línea de [comandos](command-line-options.md)/I,/J o/a, no se llama a las acciones de [instalación](install-action.md), [anuncio](advertise-action.md)y [Administración](admin-action.md) desde la secuencia de acción. En su lugar, estas acciones de alto nivel se pasan al instalador cuando se inicializa el instalador.

Si se pasa al instalador la acción de instalación y el paquete de instalación se ha creado con una interfaz de usuario, el instalador ejecuta primero las acciones en la [tabla InstallUISequence](installuisequence-table.md) y, a continuación, ejecuta las acciones en la [tabla InstallExecuteSequence](installexecutesequence-table.md) en orden. Si el paquete no tiene ninguna interfaz de usuario, el instalador ejecuta las acciones en la tabla InstallExecuteSequence en orden.

Si se pasa el instalador a la acción de administración y el paquete de instalación se ha creado con una interfaz de usuario, el instalador ejecuta primero la [tabla AdminUISequence](adminuisequence-table.md) y, a continuación, ejecuta la [tabla AdminExecuteSequence](adminexecutesequence-table.md). Si el paquete no tiene ninguna interfaz de usuario, el instalador ejecuta la tabla AdminExecute.

Si al instalador se le pasa la acción de anuncio, el instalador ejecuta la tabla [AdvtExecuteSequence](advtexecutesequence-table.md) .

> [!Note]  
> El instalador no utiliza la tabla [AdvtUISequence](advtuisequence-table.md) . La tabla AdvtUISequence no debe existir en la base de datos de instalación o debe dejarse vacía.

 

Cuando el instalador ejecuta una tabla de secuencia, ejecuta las acciones en el orden de los números de secuencia enumerados en la columna de secuencia. El orden de la acción siempre es lineal, sin bifurcación ni bucle. Los desarrolladores de paquetes pueden impedir condicionalmente la ejecución de una acción determinada mediante la creación de una expresión lógica en la columna condición. El instalador omite la acción cada vez que la condición se evalúa como false. Vea [usar una tabla de secuencia y una sintaxis de](using-a-sequence-table.md) [instrucción condicional](conditional-statement-syntax.md).

Todas las tablas de secuencia tienen las columnas siguientes.



| Columna    | Descripción                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acción    | La clave principal de la tabla; el nombre de la acción debe ser único.                                                                                                                                                                                |
| Condición | Expresión booleana que se usa para determinar si se va a realizar la acción. La acción se ejecuta si este campo está en blanco o contiene una expresión que se evalúa como true. La acción no se ejecuta si la expresión se evalúa como false. |
| Secuencia  | Un número de secuencia relativo que se usa para determinar el orden en el que se ejecutan las acciones.                                                                                                                                                         |



 

 

 



