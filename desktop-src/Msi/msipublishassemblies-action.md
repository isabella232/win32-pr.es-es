---
description: La acción MsiPublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Acción MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524175a957249a48f7c72409ad7b4c55b31f642753db11875a9567ef35a2acf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804195"
---
# <a name="msipublishassemblies-action"></a>Acción MsiPublishAssemblies

La acción MsiPublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32. La acción consulta la tabla [MsiAssembly](msiassembly-table.md) para determinar qué ensamblados tienen características que se anuncian o instalan en la caché global de ensamblados y qué ensamblados tienen un componente primario que se anuncia o se instala en una ubicación aislada para una aplicación determinada. Para obtener información, [vea Instalación de ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalación de ensamblados Win32](installation-of-win32-assemblies.md).

En Microsoft Windows XP y sistemas [posteriores,](side-by-side-assemblies.md)Windows Installer puede instalar ensamblados Win32 como ensamblados en paralelo. Para obtener más información, vea [Acerca de las aplicaciones aisladas y ensamblados en paralelo.](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MsiPublishAssemblies debe ir después de la acción [InstallInitialize](installinitialize-action.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md) o en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Contexto de la aplicación.       |
| \[2\] | Nombre del ensamblado.             |



 

## <a name="remarks"></a>Comentarios

Para obtener más información, vea [Ensamblados](assemblies.md).

La [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md) administra el anuncio de los ensamblados que se quitan.

 

 
