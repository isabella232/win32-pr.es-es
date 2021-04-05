---
description: Incluya las tablas de MergeModuleSequence en el archivo. MSM si el módulo de fusión mediante combinación debe modificar las tablas de secuencia de acciones del archivo. msi de destino. La combinación no agrega estas tablas al archivo. msi. Estas tablas solo se producen en los módulos de combinación.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Crear tablas de secuencia de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b21780601e626c006967cefa0dcff5700bdec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001728"
---
# <a name="authoring-merge-module-sequence-tables"></a>Crear tablas de secuencia de módulo de combinación

Incluya las tablas de MergeModuleSequence en el archivo. MSM si el módulo de fusión mediante combinación debe modificar las [*tablas de secuencia*](s-gly.md) de acciones del archivo. msi de destino. La combinación no agrega estas tablas al archivo. msi. Estas tablas solo se producen en los módulos de combinación.

Si alguna de las tablas ModuleSequence se encuentra en un archivo. MSM, también debe crearse una copia vacía de la tabla de secuencia de instalador correspondiente en el módulo de combinación. Por ejemplo, si un módulo de combinación contiene una tabla ModuleAdminExecuteSequence, el módulo de combinación también debe incluir una tabla AdminExecuteSequence vacía. Durante una combinación, estas tablas vacías proporcionan la herramienta de combinación con las directrices de esquema necesarias.

Al usar [acciones estándar](standard-actions.md) en las tablas de secuencia de módulo de combinación, el valor de la columna de secuencia debe ser el número de secuencia de acción recomendado para la acción estándar. Vea las secuencias de acción sugeridas que se indican a continuación para ver los números de secuencia recomendados en cada tabla de secuencia. Si el número de secuencia de la tabla de secuencia del módulo de combinación difiere del número de secuencia de la misma acción en el archivo. msi, la herramienta de combinación utiliza el número de secuencia del archivo. msi durante la combinación.



| Tabla MergeModuleSequence                                                    | Secuencias de acciones recomendadas                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [AdminUISequence sugerido](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [AdminExecuteSequence sugerido](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [AdvtUISequence sugerido](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [AdvtExecuteSequence sugerido](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [InstallUISequence sugerido](suggested-installuisequence.md)           |
| [Tabla ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | [InstallExecuteSequence sugerido](suggested-installexecutesequence.md) |



 

Si se usa una [acción estándar](standard-actions.md) en la columna de acción de una tabla de secuencia de módulo de combinación, las columnas BaseAction y After de ese registro deben ser null.

Si se especifica una acción o un cuadro de diálogo personalizado en la columna de acción, la columna de secuencia debe ser null.

Si se especifica una acción que devuelve una marca de finalización en la columna de acción, la columna de secuencia debe contener el valor negativo para esa marca y las columnas BaseAction y After de ese registro deben ser null. Los siguientes valores negativos indican que se llama a la acción si el instalador devuelve la marca de finalización.



| Marca de terminación          | Value | Descripción              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | -1    | Finalización correcta.   |
| msiDoActionStatusUserExit | -2    | El usuario finaliza la instalación. |
| msiDoActionStatusFailure  | -3    | Se termina la salida grave.   |
| msiDoActionStatusSuspend  | -4    | La instalación está suspendida.    |



 

La columna BaseAction puede contener una acción estándar, una acción personalizada especificada en la tabla de acciones personalizadas del módulo de combinación o un cuadro de diálogo especificado en la tabla de diálogo del módulo. La columna BaseAction es una clave en la columna Action de esta tabla. No puede ser una clave externa en otra tabla o tabla de mezcla del archivo. msi. Esto significa que todas las acciones, acciones personalizadas o cuadros de diálogo estándar que se enumeran en la columna BaseAction también deben aparecer en la columna Acción de otro registro de esta tabla.

 

 



