---
description: ICEM12 comprueba que en una tabla ModuleSequence, las acciones estándar tienen números de secuencia y acciones personalizadas tienen valores de BaseAction y after.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082260"
---
# <a name="icem12"></a>ICEM12

ICEM12 comprueba que en una tabla ModuleSequence, las acciones estándar tienen números de secuencia y acciones personalizadas tienen valores de BaseAction y after.

Este ICEM está disponible en el archivo Mergemod. Cub proporcionado en el SDK de Windows Installer 2,0 y versiones posteriores. Para obtener más información, consulte [componentes de Windows SDK para desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM12 publica un error en los siguientes casos:

-   Busca el módulo que contiene una [acción estándar](standard-actions.md) sin un número de secuencia.
-   Detecta que una acción estándar tiene valores especificados en los campos BaseAction o After de la [tabla ModuleAdminUISequence](moduleadminuisequence-table.md), tabla [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), tabla [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), tabla [ModuleInstallUISequence](moduleinstalluisequence-table.md)o [tabla ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).
-   Busca el módulo contiene una [acción personalizada](custom-actions.md) sin ningún valor especificado en los campos Sequence, BaseAction o After de la [tabla ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)Table, [ModuleInstallUISequence Table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence Table](moduleinstallexecutesequence-table.md).

ICEM12 publica una advertencia si encuentra una acción personalizada que tiene un número de secuencia especificado, pero ningún valor en los campos BaseAction o After.

Tenga en cuenta que todas las acciones que se encuentran en la [tabla CustomAction](customaction-table.md) se consideran acciones personalizadas. Todas las demás acciones se consideran acciones estándar.

## <a name="example"></a>Ejemplo

ICEM12 expone los siguientes mensajes de error y advertencia para un módulo que contiene las entradas de base de datos que se muestran a continuación:

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[CustomAction](customaction-table.md)



| Acción  | Tipo | Source  | Destino  |
|---------|------|---------|---------|
| Action1 | 30   | Source1 | target1 |
| Action3 | 30   | source3 | target3 |



 

[ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)



| Acción  | Secuencia | BaseAction | Después | Condición |
|---------|----------|------------|-------|-----------|
| Action2 |          | Action1    | 1     | true      |
| Action3 |          |            |       | true      |



 

[ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Acción  | Secuencia | BaseAction | Después | Condición |
|---------|----------|------------|-------|-----------|
| Action1 | 1        |            |       | true      |



 

Para corregir estos errores, pruebe lo siguiente:

-   Quite el número de secuencia de la acción personalizada Action1 y use en su lugar los campos BaseAction y after.
-   Escriba valores en los campos Sequence, BaseAction o After para la acción personalizada Action3. Deje los campos BaseAction y After vacíos para la acción estándar Action2.
-   No deje el campo de secuencia vacío para la acción estándar Action2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



