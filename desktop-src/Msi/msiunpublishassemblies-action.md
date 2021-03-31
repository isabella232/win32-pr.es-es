---
description: La acción MsiUnpublishAssemblies administra el anuncio de Common Language Runtime ensamblados y ensamblados Win32 que se van a quitar.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Acción MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912086"
---
# <a name="msiunpublishassemblies-action"></a>Acción MsiUnpublishAssemblies

La acción MsiUnpublishAssemblies administra el anuncio de Common Language Runtime ensamblados y ensamblados Win32 que se van a quitar. La acción consulta la [tabla MsiAssembly](msiassembly-table.md) para determinar qué ensamblados han quitado las características anunciadas o instaladas de la caché global de ensamblados y qué ensamblados tienen un componente primario anunciado o instalado que se va a quitar de una ubicación aislada para una aplicación determinada. Para obtener más información, vea [Instalar ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalar ensamblados Win32](installation-of-win32-assemblies.md).

En los sistemas que ejecutan Windows XP y versiones posteriores, Windows Installer pueden instalar ensamblados Win32 como [ensamblados en paralelo](side-by-side-assemblies.md). Para obtener más información, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MsiUnpublishAssemblies debe aparecer después de la [acción InstallInitialize](installinitialize-action.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Contexto de la aplicación.       |
| \[2\] | Nombre del ensamblado.             |



 

## <a name="remarks"></a>Observaciones

La [acción MsiPublishAssemblies](msipublishassemblies-action.md) administra el anuncio de los ensamblados que se están anunciando o instalando.

 

 
