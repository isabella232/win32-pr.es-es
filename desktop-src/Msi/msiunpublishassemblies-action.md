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
# <a name="msiunpublishassemblies-action"></a><span data-ttu-id="49b7a-103">Acción MsiUnpublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="49b7a-103">MsiUnpublishAssemblies Action</span></span>

<span data-ttu-id="49b7a-104">La acción MsiUnpublishAssemblies administra el anuncio de Common Language Runtime ensamblados y ensamblados Win32 que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="49b7a-104">The MsiUnpublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies that are being removed.</span></span> <span data-ttu-id="49b7a-105">La acción consulta la [tabla MsiAssembly](msiassembly-table.md) para determinar qué ensamblados han quitado las características anunciadas o instaladas de la caché global de ensamblados y qué ensamblados tienen un componente primario anunciado o instalado que se va a quitar de una ubicación aislada para una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="49b7a-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have advertised or installed features being removed from the global assembly cache and which assemblies have an advertised or installed parent component being removed from a location isolated for a particular application.</span></span> <span data-ttu-id="49b7a-106">Para obtener más información, vea [Instalar ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalar ensamblados Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="49b7a-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="49b7a-107">En los sistemas que ejecutan Windows XP y versiones posteriores, Windows Installer pueden instalar ensamblados Win32 como [ensamblados en paralelo](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="49b7a-107">On systems running Windows XP and later, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="49b7a-108">Para obtener más información, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="49b7a-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="49b7a-109">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="49b7a-109">Sequence Restrictions</span></span>

<span data-ttu-id="49b7a-110">La acción MsiUnpublishAssemblies debe aparecer después de la [acción InstallInitialize](installinitialize-action.md) en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="49b7a-110">The MsiUnpublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="49b7a-111">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="49b7a-111">ActionData Messages</span></span>



| <span data-ttu-id="49b7a-112">Campo</span><span class="sxs-lookup"><span data-stu-id="49b7a-112">Field</span></span> | <span data-ttu-id="49b7a-113">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="49b7a-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="49b7a-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="49b7a-114">\[1\]</span></span> | <span data-ttu-id="49b7a-115">Contexto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49b7a-115">Application context.</span></span>       |
| <span data-ttu-id="49b7a-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="49b7a-116">\[2\]</span></span> | <span data-ttu-id="49b7a-117">Nombre del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="49b7a-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="49b7a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49b7a-118">Remarks</span></span>

<span data-ttu-id="49b7a-119">La [acción MsiPublishAssemblies](msipublishassemblies-action.md) administra el anuncio de los ensamblados que se están anunciando o instalando.</span><span class="sxs-lookup"><span data-stu-id="49b7a-119">The [MsiPublishAssemblies Action](msipublishassemblies-action.md) manages the advertisement of assemblies being advertised or installed.</span></span>

 

 
