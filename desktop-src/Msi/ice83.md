---
description: ICE83 valida la tabla MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082537"
---
# <a name="ice83"></a>ICE83

ICE83 valida la [tabla MsiAssembly](msiassembly-table.md). Esta acción personalizada de ICE publica un error si la ruta de acceso de la clave de un componente que contiene un ensamblado Win32 se establece en el archivo de manifiesto. Explícitamente, el error se expone si el valor especificado en el campo de ruta de acceso de la [tabla de componentes](component-table.md) es igual al valor especificado en el \_ campo manifiesto de archivo de la tabla MsiAssembly. Esta acción personalizada de ICE publica un error si hay al menos un registro en la tabla MsiAssembly y la [tabla InstallExecuteSequence](installexecutesequence-table.md) no contiene la [acción MsiPublishAssemblies](msipublishassemblies-action.md) y la [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

## <a name="result"></a>Resultado

ICE83 expone los siguientes errores.



| Error ICE83                                                                                                   | Descripción                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La ruta de acceso de la clave para el ensamblado SxS Win32 (componente \_ = \[ 1 \] ) no debe ser su archivo de manifiesto                       | ICE83 envía este error cuando el campo de ruta de acceso de un ensamblado de Win32 se establece en su archivo de manifiesto (Component. ruta de acceso = = MsiAssembly. file \_ manifest). \[1 \] es la ruta de rutas en la tabla de componentes                          |
| Las acciones MsiPublishAssemblies y MsiUnpublishAssemblies deben estar presentes en la tabla InstallExecuteSequence. | ICE83 envía este error cuando hay al menos una entrada en la tabla MsiAssembly, pero la tabla InstallExecuteSequence no contiene la acción MsiAssemblyPublish y la acción MsiAssemblyUnpublish. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



