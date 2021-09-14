---
description: Una herramienta de combinación evalúa la tabla ModuleAdminUISequence y, a continuación, inserta las acciones calculadas en la tabla AdminUISequence con un número de secuencia correcto.
ms.assetid: c71477e7-22bc-420a-9902-39bbf98b4ee5
title: ModuleAdminUISequence (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e128aebd6481c077827f4d1ba2b487eafe6132d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261212"
---
# <a name="moduleadminuisequence-table"></a>ModuleAdminUISequence (tabla)

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

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Acción
</dt> <dd>

Acción que se insertará en secuencia. Hace referencia a una de las acciones [estándar del](standard-actions.md)instalador o a una entrada de la tabla [CustomAction](customaction-table.md) o de la tabla [Dialog del módulo de mezcla.](dialog-table.md)

Si se [usa una acción](standard-actions.md) estándar en la columna Acción de una tabla de secuencias de módulo de mezcla, las columnas BaseAction y After de ese registro deben ser NULL.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

Número de secuencia de una acción estándar. Si se especifica una acción personalizada o un cuadro de diálogo en la columna Acción de esta fila, este campo debe establecerse en Null.

Cuando se [usan acciones estándar](standard-actions.md) en tablas de secuencias de módulos de combinación, el valor de la columna Secuencia debe ser el número de secuencia de acción recomendado. Si el número de secuencia del módulo de combinación difiere del de la misma acción en la tabla de secuencia de archivos de .msi, la herramienta de combinación usa el número de secuencia del archivo .msi. Consulte las secuencias sugeridas en [Uso de una tabla de secuencias](using-a-sequence-table.md) para obtener los números de secuencia recomendados de las acciones estándar.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

La columna BaseAction puede contener una acción estándar, una acción personalizada especificada en la tabla de acciones personalizadas del módulo de mezcla o un cuadro de diálogo especificado en la tabla de diálogos del módulo. La columna BaseAction es una clave en la columna Acción de esta tabla. No puede ser una clave externa en otra tabla o tabla de combinación del archivo .msi combinación. Esto significa que todas las acciones estándar, acciones personalizadas o cuadros de diálogo que aparecen en la columna BaseAction también deben aparecer en la columna Acción de otro registro de esta tabla.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Después
</dt> <dd>

Booleano para saber si Action viene antes o después de BaseAction.



| Value | Significado                          |
|-------|----------------------------------|
| 0     | Acción que debe ir antes de BaseAction |
| 1     | Acción que se debe realizar después de BaseAction  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Instrucción condicional que indica si se ejecuta la acción. Null se evalúa como true.

</dd> </dl>

## <a name="remarks"></a>Observaciones

<dl> <dt>

<span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>Si esta tabla está presente, [la tabla AdminUISequence](adminuisequence-table.md) también debe estar presente en el módulo merge.
</dt> <dd></dd> </dl>

 

 



