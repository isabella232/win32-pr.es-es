---
description: ': Valida las tablas de secuencia de un paquete de instalación para las acciones válidas, las restricciones de la secuencia de acción y la organización en las secciones de búsqueda, costo, selección y ejecución.'
ms.assetid: c5292a3c-57bb-4203-96a1-6d747f554178
title: ICE27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb4b90b313f5f78874fb93ce9d32c3650b97064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908713"
---
# <a name="ice27"></a>ICE27

: Valida las [*tablas de secuencia*](s-gly.md) de un paquete de instalación para las acciones válidas, las restricciones de la secuencia de acción y la organización en las secciones de búsqueda, costo, selección y ejecución.

La acción personalizada: valida lo siguiente:

-   Que las acciones enumeradas en la columna Acción de las tablas de secuencia son [acciones estándar](standard-actions.md), una acción personalizada que se muestra en la [tabla CustomAction](customaction-table.md)o un cuadro de diálogo que aparece en la tabla del cuadro de [diálogo](dialog-table.md).
-   Las acciones sujetas a las restricciones de secuenciación se encuentran en el orden relativo correcto entre sí en la secuencia de acción. Las restricciones de secuenciación se producen cuando una acción depende de otra.
-   Que las acciones restringidas a una sección determinada de la secuencia se encuentran donde pertenecen. : Valida la siguiente organización de las tablas de secuencia. Tenga en cuenta que no todas las tablas de secuencia tienen cada sección. Vea las tablas de secuencia sugeridas en [mediante una tabla de secuencia](using-a-sequence-table.md).



| Sección de la tabla Sequence | Intervalo en secuencia de acción                                                                       | Acciones pertenecientes a la sección                                                                                                                                                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Search                 | {Start} a [CostInitialize](costinitialize-action.md)                                         | Acciones que buscan aplicaciones existentes. [AppSearch](appsearch-action.md)<br/> [CCPSearch](ccpsearch-action.md)<br/>                                                                                                         |
| Costos                | Acción de [CostInitialize](costinitialize-action.md) a [CostFinalize](costfinalize-action.md)  | Acciones que realizan el costo de los [archivos](file-costing.md). [CostInitialize](costinitialize-action.md)<br/> [FileCost](filecost-action.md)<br/> [CostFinalize](costfinalize-action.md)<br/>                                           |
| Selección              | [CostFinalize](costfinalize-action.md) a [InstallValidate](installvalidate-action.md)       | Acciones que establecen las carpetas o los Estados de las características. [Acción SetODBCFolders](setodbcfolders-action.md)<br/>                                                                                                                                        |
| Ejecución              | [InstallValidate](installvalidate-action.md) a [InstallFinalize](installfinalize-action.md) | Acciones de script, como registro, publicación, instalación (donde se copian los archivos). Tenga en cuenta que la [acción InstallFinalize](installfinalize-action.md) debe estar en la tabla si y solo si hay acciones en la sección de ejecución.<br/> |
| Postejecución          | [InstallFinalize](installfinalize-action.md) a {end}                                         | [RemoveExistingProducts](removeexistingproducts-action.md)                                                                                                                                                                                      |



 

: Valida las tablas siguientes:

-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

: Envía un mensaje de error si hay tablas de secuencia en el paquete con una secuencia u organización de acción no válida.

## <a name="example"></a>Ejemplo



| Error:                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acción desconocida: ' Action1 ' de la tabla InstallExecuteSequnence. No es una acción estándar y no se encuentra en las tablas de cuadro de diálogo o CustomAction    | Hay una acción en la tabla de secuencia indicada que no es una acción [estándar](standard-actions.md), una acción personalizada que aparece en la [tabla CustomAction](customaction-table.md)o un cuadro de diálogo que aparece en la tabla del cuadro de [diálogo](dialog-table.md).                                                                                                                                                                                                                                                                       |
| ' Action2 ' en la tabla InstallExecute en un lugar incorrecto. Actual: buscar, corregir: costos                                                 | Hay una acción en una tabla de secuencia que se coloca incorrectamente con respecto al número de secuencia de la columna de secuencia. "Actual" indica la posición actual de la acción en las secciones de búsqueda, costo, selección o ejecución de la tabla de secuencia indicada.<br/> "Correcto" indica en qué sección pertenece la acción.<br/> Para corregir este error, cambie el número de secuencia de la acción a dentro de la sección correcta. Tenga en cuenta que algunas acciones pueden encontrarse en más de una sección.<br/> |
| Solo se puede llamar a la acción ' InstallFinalize ' en la tabla InstallExecuteSequence cuando existen operaciones de script que se van a ejecutar             | Hay una [acción InstallFinalize](installfinalize-action.md) en una tabla de secuencia que no contiene ninguna operación de script en la sección de ejecución de la tabla. Agregue acciones a la sección ejecución o quite la acción InstallFinalize de la tabla.<br/>                                                                                                                                                                                                                                                        |
| Se debe llamar a InstallFinalize en la tabla InstallExecuteSequence a medida que existen operaciones de script para ejecutarse                            | Hay una tabla de secuencias que contiene acciones en la sección de ejecución que no incluye la [acción InstallFinalize](installfinalize-action.md). Agregue la acción InstallFinalize a esta tabla de secuencia y asígnele el número de secuencia más alto para colocarlo en último lugar en la secuencia de acción.<br/>                                                                                                                                                                                                                            |
| Acción: ' Action3 ' en la tabla InstallExecuteSequence debe ser anterior a la acción ' Action5 '. SEC actuales \# : 1200. SEQ dependientes \# : 1100 | Hay una acción en la tabla de secuencia indicada que se secuencia después de una acción dependiente. Cambie el número de secuencia en la acción dependiente para que venga antes de la acción.<br/>                                                                                                                                                                                                                                                                                                                                    |
| Acción: ' Action4 ' en la tabla InstallExecuteSequence debe aparecer después de la acción ' Action6 '.                                             | Hay una acción en la tabla de secuencia indicada que se secuencia antes de una acción de la que depende. Cambie el número de secuencia en la acción para que venga después de su acción dependiente.<br/>                                                                                                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




