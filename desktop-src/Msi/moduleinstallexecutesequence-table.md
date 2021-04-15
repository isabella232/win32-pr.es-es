---
description: Una herramienta de combinación evalúa la tabla ModuleInstallExecuteSequence y, a continuación, inserta las acciones calculadas en la tabla InstallExecuteSequence con un número de secuencia correcto.
ms.assetid: 6cd04d9a-5489-4fde-951e-aa962e9bd755
title: Tabla ModuleInstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d294ddfdf06028bf18d518e1086d37a0719f8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669805"
---
# <a name="moduleinstallexecutesequence-table"></a>Tabla ModuleInstallExecuteSequence

Una herramienta de combinación evalúa la tabla ModuleInstallExecuteSequence y, a continuación, inserta las acciones calculadas en la [tabla InstallExecuteSequence](installexecutesequence-table.md) con un número de secuencia correcto.

La tabla ModuleInstallExecuteSequence contiene las columnas siguientes.



| Columna     | Tipo                         | Clave | Nullable |
|------------|------------------------------|-----|----------|
| Acción     | [Identificador](identifier.md) | Y   | N        |
| Secuencia   | [Entero](integer.md)       |     | Y        |
| BaseAction | [Identificador](identifier.md) |     | Y        |
| Después      | [Entero](integer.md)       |     | Y        |
| Condición  | [Condition](condition.md)   |     | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar
</dt> <dd>

Acción que se va a insertar en la secuencia. Hace referencia a una de las [acciones estándar](standard-actions.md)del instalador o a una entrada en la [tabla CustomAction](customaction-table.md)o la tabla de [cuadro de diálogo](dialog-table.md)del módulo de combinación.

Si se usa una [acción estándar](standard-actions.md) en la columna de acción de una tabla de secuencia de módulo de combinación, las columnas BaseAction y After de ese registro deben ser null.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ
</dt> <dd>

El número de secuencia de una acción estándar. Si se especifica una acción o un cuadro de diálogo personalizado en la columna Acción de esta fila, este campo debe establecerse en NULL.

Al usar [acciones estándar](standard-actions.md) en las tablas de secuencia de módulo de combinación, el valor de la columna de secuencia debe ser el número de secuencia de acción recomendado. Si el número de secuencia del módulo de combinación difiere del de la misma acción en la tabla de secuencia de archivos. msi, la herramienta de combinación utiliza el número de secuencia del archivo. msi. Vea las secuencias sugeridas en [usar una tabla de secuencia](using-a-sequence-table.md) para ver los números de secuencia recomendados de las acciones estándar.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

La columna BaseAction puede contener una acción estándar, una acción personalizada especificada en la tabla de acciones personalizadas del módulo de combinación o un cuadro de diálogo especificado en la tabla de diálogo del módulo. La columna BaseAction es una clave en la columna Action de esta tabla. No puede ser una clave externa en otra tabla o tabla de mezcla del archivo de Windows Installer. Esto significa que todas las acciones, acciones personalizadas o cuadros de diálogo estándar que se enumeran en la columna BaseAction también deben aparecer en la columna Acción de otro registro de esta tabla.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Continuación
</dt> <dd>

Valor booleano que indica si la acción viene antes o después de BaseAction.



| Value | Significado                          |
|-------|----------------------------------|
| 0     | Acción que debe transcurrir antes de BaseAction |
| 1     | Acción que debe aparecer después de BaseAction  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple
</dt> <dd>

Instrucción condicional que indica si la acción se va a ejecutar. Un valor NULL se evalúa como true.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la [tabla ModuleInstallExecuteSequence](installexecutesequence-table.md) está presente, la [tabla InstallExecuteSequence](installexecutesequence-table.md) también debe estar presente en el módulo Merge.

 

 



