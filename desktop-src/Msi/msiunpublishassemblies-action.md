---
description: La acción MsiUnpublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32 que se van a quitar.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Acción MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f640338e13f53b115ca3b93aa2a63987efb5aa7cf053d4c8a59d8d20d0f7e3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943902"
---
# <a name="msiunpublishassemblies-action"></a>Acción MsiUnpublishAssemblies

La acción MsiUnpublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32 que se van a quitar. La acción consulta la tabla [MsiAssembly](msiassembly-table.md) para determinar qué ensamblados han anunciado o instalado características que se quitan de la caché global de ensamblados y qué ensamblados tienen un componente primario anunciado o instalado que se quita de una ubicación aislada para una aplicación determinada. Para obtener información, [vea Instalación de ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalación de ensamblados Win32](installation-of-win32-assemblies.md).

En sistemas que Windows XP y versiones posteriores, Windows Installer puede instalar ensamblados Win32 como ensamblados [en paralelo.](side-by-side-assemblies.md) Para obtener más información, vea [Acerca de las aplicaciones aisladas y ensamblados en paralelo.](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MsiUnpublishAssemblies debe ir después de la acción [InstallInitialize](installinitialize-action.md) de la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Contexto de la aplicación.       |
| \[2\] | Nombre del ensamblado.             |



 

## <a name="remarks"></a>Comentarios

La [acción MsiPublishAssemblies](msipublishassemblies-action.md) administra el anuncio de los ensamblados que se anuncian o instalan.

 

 
