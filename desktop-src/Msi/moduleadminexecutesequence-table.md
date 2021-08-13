---
description: Una herramienta de combinación evalúa la tabla ModuleAdminExecuteSequence y, a continuación, inserta las acciones calculadas en la tabla AdminExecuteSequence con un número de secuencia correcto.
ms.assetid: 26cc5e15-8dfd-4bf5-8830-225164302278
title: Tabla ModuleAdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e820c721fbbaa7d8925b07ee584cbb0b97fee66eac05fd7b8dafbe38f3f319d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628721"
---
# <a name="moduleadminexecutesequence-table"></a>Tabla ModuleAdminExecuteSequence

Una herramienta de combinación evalúa la tabla ModuleAdminExecuteSequence y, a continuación, inserta las acciones calculadas en la tabla [AdminExecuteSequence](adminexecutesequence-table.md) con un número de secuencia correcto.

La tabla ModuleAdminExecuteSequence tiene las columnas siguientes.



| Columna     | Tipo                         | Key | Nullable |
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

Acción que se inserta en secuencia. Hace referencia a una de las acciones [estándar del](standard-actions.md)instalador o a una entrada en la tabla [CustomAction](customaction-table.md) del módulo de mezcla o en la [tabla Dialog](dialog-table.md).

Si se [usa una acción](standard-actions.md) estándar en la columna Acción de una tabla de secuencia de módulos de mezcla, las columnas BaseAction y After de ese registro deben ser NULL.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

Número de secuencia de una acción estándar. Si se especifica una acción personalizada o un cuadro de diálogo en la columna Acción de esta fila, este campo debe establecerse en Null.

Cuando se [usan acciones estándar en](standard-actions.md) tablas de secuencia de módulos de combinación, el valor de la columna Secuencia debe ser el número de secuencia de acción recomendado. Si el número de secuencia del módulo de combinación difiere del de la misma acción en la tabla de secuencia de archivos de .msi, la herramienta de combinación usa el número de secuencia del archivo .msi combinación. Consulte las secuencias sugeridas en [Uso de una tabla de secuencias](using-a-sequence-table.md) para obtener los números de secuencia recomendados de acciones estándar.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

La columna BaseAction puede contener una acción estándar, una acción personalizada especificada en la tabla de acciones personalizada del módulo de mezcla o un cuadro de diálogo especificado en la tabla de diálogos del módulo. La columna BaseAction es una clave en la columna Acción de esta tabla. No puede ser una clave externa en otra tabla o tabla de combinación en el .msi de mezcla. Esto significa que todas las acciones estándar, acciones personalizadas o diálogos enumerados en la columna BaseAction también deben aparecer en la columna Acción de otro registro de esta tabla.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Después
</dt> <dd>

Booleano para si Action viene antes o después de BaseAction.



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

Si esta tabla está presente, [la tabla AdminExecuteSequence](adminexecutesequence-table.md) también debe estar presente en el módulo merge.

 

 



