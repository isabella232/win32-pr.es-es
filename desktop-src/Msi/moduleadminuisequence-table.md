---
description: Una herramienta de combinación evalúa la tabla ModuleAdminUISequence y, a continuación, inserta las acciones calculadas en la tabla AdminUISequence con un número de secuencia correcto.
ms.assetid: c71477e7-22bc-420a-9902-39bbf98b4ee5
title: Tabla ModuleAdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e128aebd6481c077827f4d1ba2b487eafe6132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652995"
---
# <a name="moduleadminuisequence-table"></a>Tabla ModuleAdminUISequence

Una herramienta de combinación evalúa la tabla ModuleAdminUISequence y, a continuación, inserta las acciones calculadas en la [tabla AdminUISequence](adminuisequence-table.md) con un número de secuencia correcto.

La tabla ModuleAdminUISequence tiene las columnas siguientes.



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

Acción que se va a insertar en la secuencia. Hace referencia a una de las [acciones estándar](standard-actions.md)del instalador o a una entrada en la tabla o el [cuadro de diálogo](dialog-table.md)de [CustomAction](customaction-table.md) del módulo de combinación.

Si se usa una [acción estándar](standard-actions.md) en la columna de acción de una tabla de secuencia de módulo de combinación, las columnas BaseAction y After de ese registro deben ser null.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ
</dt> <dd>

El número de secuencia de una acción estándar. Si se especifica una acción o un cuadro de diálogo personalizado en la columna Acción de esta fila, este campo debe establecerse en NULL.

Al usar [acciones estándar](standard-actions.md) en las tablas de secuencia de módulo de combinación, el valor de la columna de secuencia debe ser el número de secuencia de acción recomendado. Si el número de secuencia del módulo de combinación difiere del de la misma acción en la tabla de secuencia de archivos. msi, la herramienta de combinación utiliza el número de secuencia del archivo. msi. Vea las secuencias sugeridas en [usar una tabla de secuencia](using-a-sequence-table.md) para ver los números de secuencia recomendados de las acciones estándar.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

La columna BaseAction puede contener una acción estándar, una acción personalizada especificada en la tabla de acciones personalizadas del módulo de combinación o un cuadro de diálogo especificado en la tabla de diálogo del módulo. La columna BaseAction es una clave en la columna Action de esta tabla. No puede ser una clave externa en otra tabla o tabla de mezcla del archivo. msi. Esto significa que todas las acciones, acciones personalizadas o cuadros de diálogo estándar que se enumeran en la columna BaseAction también deben aparecer en la columna Acción de otro registro de esta tabla.

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

Instrucción condicional que indica si se ejecuta la acción. NULL se evalúa como true.

</dd> </dl>

## <a name="remarks"></a>Observaciones

<dl> <dt>

<span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>Si esta tabla está presente, la [tabla AdminUISequence](adminuisequence-table.md) también debe estar presente en el módulo de combinación.
</dt> <dd></dd> </dl>

 

 



