---
description: ICE83 valida la tabla MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074527"
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

 

 



