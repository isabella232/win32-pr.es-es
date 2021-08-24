---
description: ICE83 valida la tabla MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e8014f8feee76e4d1910fb601e186bec928a0fd6d6d34469ce2c2b201b724d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580755"
---
# <a name="ice83"></a>ICE83

ICE83 valida la [tabla MsiAssembly](msiassembly-table.md). Esta acción personalizada de ICE genera un error si la ruta de acceso de clave de un componente que contiene un ensamblado Win32 está establecida en el archivo de manifiesto. Explícitamente, el error se publica si el valor especificado en el campo KeyPath de la tabla [Component](component-table.md) es igual al valor especificado en el campo Manifiesto de archivo de la \_ tabla MsiAssembly. Esta acción personalizada de ICE genera un error si hay al menos un registro en la tabla MsiAssembly y la tabla [InstallExecuteSequence](installexecutesequence-table.md) no contiene las acciones [MsiPublishAssemblies y](msipublishassemblies-action.md) [MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

## <a name="result"></a>Resultado

ICE83 publica los siguientes errores.



| Error ICE83                                                                                                   | Descripción                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La ruta de acceso de clave para el ensamblado SXS de Win32 (componente \_ = \[ \] 1) NO DEBE ser su archivo de manifiesto.                       | ICE83 publica este error cuando el campo KeyPath de un ensamblado Win32 está establecido en su archivo de manifiesto (Component.KeyPath == MsiAssembly.File \_ Manifest). \[1 \] es KeyPath en la tabla Component                          |
| Las acciones MsiPublishAssemblies y MsiUnpublishAssemblies DEBEN estar presentes en la tabla InstallExecuteSequence. | ICE83 publica este error cuando hay al menos una entrada en la tabla MsiAssembly, pero la tabla InstallExecuteSequence no contiene la acción MsiAssemblyPublish y la acción MsiAssemblyUnpublish. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



