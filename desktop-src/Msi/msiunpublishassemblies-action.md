---
description: La acción MsiUnpublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32 que se van a quitar.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Acción MsiUnpublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074346"
---
# <a name="msiunpublishassemblies-action"></a>Acción MsiUnpublishAssemblies

La acción MsiUnpublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32 que se van a quitar. La acción consulta la tabla [MsiAssembly](msiassembly-table.md) para determinar qué ensamblados han anunciado o instalado características que se quitan de la caché global de ensamblados y qué ensamblados tienen un componente primario anunciado o instalado que se quita de una ubicación aislada para una aplicación determinada. Para obtener información, [vea Instalación de ensamblados en la caché global](installation-of-assemblies-to-the-global-assembly-cache.md) de ensamblados e Instalación de [ensamblados Win32.](installation-of-win32-assemblies.md)

En sistemas que Windows XP y versiones posteriores, Windows Installer puede instalar ensamblados Win32 como [ensamblados en paralelo.](side-by-side-assemblies.md) Para obtener más información, vea [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MsiUnpublishAssemblies debe ir después de [la acción InstallInitialize](installinitialize-action.md) de la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Contexto de la aplicación.       |
| \[2\] | Nombre del ensamblado.             |



 

## <a name="remarks"></a>Observaciones

La [acción MsiPublishAssemblies](msipublishassemblies-action.md) administra el anuncio de los ensamblados que se anuncian o instalan.

 

 
