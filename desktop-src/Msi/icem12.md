---
description: ICEM12 comprueba que, en una tabla ModuleSequence, las acciones estándar tienen números de secuencia y las acciones personalizadas tienen valores BaseAction y After.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074470"
---
# <a name="icem12"></a>ICEM12

ICEM12 comprueba que, en una tabla ModuleSequence, las acciones estándar tienen números de secuencia y las acciones personalizadas tienen valores BaseAction y After.

Este ICEM está disponible en el archivo Mergemod.uu proporcionado en el SDK de Windows Installer 2.0 y versiones posteriores. Para obtener más información, [consulte Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Resultado

ICEM12 publica un error en los casos siguientes:

-   Encuentra que el módulo contiene una acción [estándar sin](standard-actions.md) un número de secuencia.
-   Encuentra que una acción estándar tiene valores especificados en los campos BaseAction o After de la tabla [ModuleAdminUISequence](moduleadminuisequence-table.md), la tabla [ModuleAdminExecuteSequence,](moduleadminexecutesequence-table.md)la tabla [ModuleAdvtExecuteSequence,](moduleadvtexecutesequence-table.md)la tabla [ModuleInstallUISequence](moduleinstalluisequence-table.md)o la tabla [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).
-   Busca que el módulo [](custom-actions.md) contiene una acción personalizada sin ningún valor especificado en los campos Sequence, BaseAction o After de la tabla [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)table , [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md)o [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)table .

ICEM12 envía una advertencia si encuentra una acción personalizada que tiene un número de secuencia especificado, pero ningún valor en los campos BaseAction o After.

Tenga en cuenta que todas las acciones que se encuentran en [la tabla CustomAction se](customaction-table.md) consideran acciones personalizadas. Todas las demás acciones se consideran acciones estándar.

## <a name="example"></a>Ejemplo

ICEM12 publica los siguientes mensajes de error y advertencia para un módulo que contiene las entradas de base de datos que se muestran a continuación:

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
| Action1 | 30   | source1 | target1 |
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

-   Quite el número de secuencia de la acción personalizada Action1 y use los campos BaseAction y After en su lugar.
-   Escriba valores en los campos Sequence, BaseAction o After para la acción personalizada Action3. Deje los campos BaseAction y After vacíos para la acción estándar Action2.
-   No deje el campo Secuencia vacío para la acción estándar Action2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



