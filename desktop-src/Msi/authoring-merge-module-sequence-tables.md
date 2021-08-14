---
description: Incluya las tablas MergeModuleSequence en el archivo .msm si el módulo de mezcla debe modificar las tablas de secuencia de acciones del archivo de .msi destino. La combinación no agrega estas tablas al .msi archivo. Estas tablas solo se producen en módulos de combinación.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Creación de tablas de secuencias de módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45e4cf86c846030854054d7ab700e34210d4e27367cd31d606c78c24f2a9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381190"
---
# <a name="authoring-merge-module-sequence-tables"></a>Creación de tablas de secuencias de módulos de mezcla

Incluya las tablas MergeModuleSequence en el archivo .msm [](s-gly.md) si el módulo de mezcla debe modificar las tablas de secuencia de acciones del archivo de .msi destino. La combinación no agrega estas tablas al .msi archivo. Estas tablas solo se producen en módulos de combinación.

Si alguna de las tablas ModuleSequence está presente en un archivo .msm, también se debe crear una copia vacía de la tabla de secuencia del instalador correspondiente en el módulo merge. Por ejemplo, si un módulo de mezcla contiene una tabla ModuleAdminExecuteSequence, el módulo de mezcla también debe incluir una tabla AdminExecuteSequence vacía. Durante una combinación, estas tablas vacías proporcionan a la herramienta de combinación las directrices de esquema necesarias.

Cuando se [usan acciones estándar](standard-actions.md) en tablas de secuencia de módulos de combinación, el valor de la columna Secuencia debe ser el número de secuencia de acción recomendado para la acción estándar. Consulte las secuencias de acción sugeridas que se indican a continuación para ver los números de secuencia recomendados en cada tabla de secuencias. Si el número de secuencia de la tabla de secuencias del módulo de mezcla difiere del número de secuencia de la misma acción en el archivo .msi, la herramienta de combinación usa el número de secuencia en el archivo .msi durante la combinación.



| Tabla MergeModuleSequence                                                    | Secuencias de acciones recomendadas                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [Administración sugeridaUISequence](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [Administración sugeridaExecuteSequence](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [AdvtUISequence sugerido](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [AdvtExecuteSequence sugerido](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [Instalación sugeridaUISequence](suggested-installuisequence.md)           |
| [Tabla ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) | [Instalación sugeridaExecuteSequence](suggested-installexecutesequence.md) |



 

Si se [usa una acción](standard-actions.md) estándar en la columna Acción de una tabla de secuencia de módulos de mezcla, las columnas BaseAction y After de ese registro deben ser NULL.

Si se especifica una acción personalizada o un cuadro de diálogo en la columna Acción, la columna Secuencia debe ser Null.

Si se especifica una acción que devuelve una marca de terminación en la columna Acción, la columna Secuencia debe contener el valor negativo de esa marca y las columnas BaseAction y After de ese registro deben ser NULL. Los siguientes valores negativos indican que se llama a la acción si el instalador devuelve la marca de terminación.



| Marca de terminación          | Valor | Descripción              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | -1    | Finalización correcta.   |
| msiDoActionStatusUserExit | -2    | El usuario finaliza la instalación. |
| msiDoActionStatusFailure  | -3    | Finaliza la salida irrescindiendo.   |
| msiDoActionStatusSuspend  | -4    | La instalación se suspende.    |



 

La columna BaseAction puede contener una acción estándar, una acción personalizada especificada en la tabla de acciones personalizada del módulo de mezcla o un cuadro de diálogo especificado en la tabla de diálogos del módulo. La columna BaseAction es una clave en la columna Acción de esta tabla. No puede ser una clave externa en otra tabla o tabla de combinación en el .msi de mezcla. Esto significa que todas las acciones estándar, acciones personalizadas o diálogos enumerados en la columna BaseAction también deben aparecer en la columna Acción de otro registro de esta tabla.

 

 



