---
description: La acción MsiPublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Acción MsiPublishAssemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669803"
---
# <a name="msipublishassemblies-action"></a>Acción MsiPublishAssemblies

La acción MsiPublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32. La acción consulta la [tabla MsiAssembly](msiassembly-table.md) para determinar qué ensamblados tienen las características que se están anunciando o instalando en la caché global de ensamblados y qué ensamblados tienen un componente primario que se anuncia o se instala en una ubicación aislada para una aplicación determinada. Para obtener más información, vea [Instalar ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalar ensamblados Win32](installation-of-win32-assemblies.md).

En los sistemas de Microsoft Windows XP y versiones posteriores, Windows Installer puede instalar ensamblados Win32 como [ensamblados en paralelo](side-by-side-assemblies.md). Para obtener más información, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción MsiPublishAssemblies debe aparecer después de la [acción InstallInitialize](installinitialize-action.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md) o en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Contexto de la aplicación.       |
| \[2\] | Nombre del ensamblado.             |



 

## <a name="remarks"></a>Observaciones

Para obtener más información, vea [ensamblados](assemblies.md).

La [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md) administra el anuncio de los ensamblados que se van a quitar.

 

 
