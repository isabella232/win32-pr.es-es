---
description: ICE27 valida las tablas de secuencia de un paquete de instalación para acciones válidas, restricciones de secuencia de acciones y organización en las secciones Búsqueda, Costo, Selección y Ejecución.
ms.assetid: c5292a3c-57bb-4203-96a1-6d747f554178
title: ICE27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedada0b2bd7ae936e12ad4c980f4ab0394c55e711db286fa6312ba446b9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528795"
---
# <a name="ice27"></a>ICE27

ICE27 valida [](s-gly.md) las tablas de secuencia de un paquete de instalación para acciones válidas, restricciones de secuencia de acciones y organización en las secciones Búsqueda, Costo, Selección y Ejecución.

La acción personalizada ICE27 valida lo siguiente:

-   Que las acciones enumeradas en la columna Acción de las tablas de secuencia son acciones [estándar,](standard-actions.md)una acción personalizada enumerada en la [tabla CustomAction](customaction-table.md)o un cuadro de diálogo que aparece en la tabla [Dialog](dialog-table.md).
-   Las acciones sujetas a restricciones de secuenciación están en el orden relativo correcto entre sí en la secuencia de acciones. Las restricciones de secuenciación se aplican cuando una acción depende de otra.
-   Las acciones restringidas a una sección determinada de la secuencia se encuentran donde pertenecen. ICE27 valida la organización siguiente de las tablas de secuencia. Tenga en cuenta que no todas las tablas de secuencias tienen todas las secciones. Vea las tablas de secuencia sugeridas en [Uso de una tabla de secuencia.](using-a-sequence-table.md)



| Sección tabla de secuencias | Intervalo en secuencia de acciones                                                                       | Acciones que pertenecen a la sección                                                                                                                                                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Búsqueda                 | {start} a [CostInitialize](costinitialize-action.md)                                         | Acciones que buscan aplicaciones existentes. [AppSearch](appsearch-action.md)<br/> [CCPSearch](ccpsearch-action.md)<br/>                                                                                                         |
| Costando                | [Acción CostInitialize](costinitialize-action.md) to [CostFinalize](costfinalize-action.md)  | Acciones que hacen el [costo de archivos](file-costing.md). [CostInitialize](costinitialize-action.md)<br/> [FileCost](filecost-action.md)<br/> [CostFinalize](costfinalize-action.md)<br/>                                           |
| Número de selección              | [CostFinalize](costfinalize-action.md) to [InstallValidate](installvalidate-action.md)       | Acciones que establecen carpetas o estados de características. [Acción SetODBCFolders](setodbcfolders-action.md)<br/>                                                                                                                                        |
| Ejecución              | [InstallValidate](installvalidate-action.md) to [InstallFinalize](installfinalize-action.md) | Acciones de script, como Registro, Publicación, Instalación (donde se copian los archivos). Tenga en [cuenta que la acción InstallFinalize](installfinalize-action.md) debe estar en la tabla si y solo si hay acciones en la sección Ejecución.<br/> |
| PostExecution          | [InstallFinalize](installfinalize-action.md) en {end}                                         | [RemoveExistingProducts](removeexistingproducts-action.md)                                                                                                                                                                                      |



 

ICE27 valida las tablas siguientes:

-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Resultado

ICE27 publica un mensaje de error si hay tablas de secuencia en el paquete con secuenciación de acciones no válidas u organización.

## <a name="example"></a>Ejemplo



| Error ice27                                                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Acción desconocida: "Action1" de la tabla InstallExecuteSequnence. No es una acción estándar y no se encuentra en las tablas CustomAction o Dialog    | Hay una acción enumerada en la tabla de secuencia que indica que no es una acción [estándar,](standard-actions.md)una acción personalizada enumerada en la [tabla CustomAction](customaction-table.md)o un cuadro de diálogo que aparece en la tabla [Dialog](dialog-table.md).                                                                                                                                                                                                                                                                       |
| "Action2" en la tabla InstallExecute en un lugar incorrecto. Actual: Búsqueda, Correcto: Costo                                                 | Hay una acción en una tabla de secuencia que se coloca incorrectamente con respecto al número de secuencia en la columna Secuencia. "Actual" indica la posición actual de la acción en las secciones Búsqueda, Cálculo de costos, Selección o Ejecución de la tabla de secuencia indicada.<br/> "Correcto" indica a qué sección pertenece la acción.<br/> Para corregir este error, cambie el número de secuencia de la acción a dentro de la sección correcta. Tenga en cuenta que alguna acción se puede encontrar en más de una sección.<br/> |
| La acción 'InstallFinalize' de la tabla InstallExecuteSequence solo se puede llamar cuando hay operaciones de script que se deben ejecutar.             | Hay una acción [InstallFinalize en](installfinalize-action.md) una tabla de secuencia que no contiene ninguna operación de script en la sección Ejecución de la tabla. Agregue acciones a la sección Ejecución o quite la acción InstallFinalize de la tabla.<br/>                                                                                                                                                                                                                                                        |
| Se debe llamar a InstallFinalize en la tabla InstallExecuteSequence, ya que existen operaciones de script que se deben ejecutar.                            | Hay una tabla de secuencia que contiene acciones en la sección Ejecución que no incluye la [acción InstallFinalize](installfinalize-action.md). Agregue la acción InstallFinalize a esta tabla de secuencia y asícele el mayor número de secuencia para colocarla en último lugar en la secuencia de acciones.<br/>                                                                                                                                                                                                                            |
| Acción: "Action3" en la tabla InstallExecuteSequence debe ir antes que la acción "Action5". Seq \# actual: 1200. Seq \# dependiente: 1100 | Hay una acción en la tabla de secuencias indicada que se secuencia después de una acción dependiente. Cambie el número de secuencia de la acción dependiente para que llegue antes que la acción.<br/>                                                                                                                                                                                                                                                                                                                                    |
| Acción: "Action4" en la tabla InstallExecuteSequence debe ir después de la acción "Action6".                                             | Hay una acción en la tabla de secuencias indicada que se secuencia antes de una acción de la que depende. Cambie el número de secuencia de la acción para que llegue después de su acción dependiente.<br/>                                                                                                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




