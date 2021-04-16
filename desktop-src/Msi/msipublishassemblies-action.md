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
# <a name="msipublishassemblies-action"></a><span data-ttu-id="118ed-103">Acción MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="118ed-103">MsiPublishAssemblies Action</span></span>

<span data-ttu-id="118ed-104">La acción MsiPublishAssemblies administra el anuncio de ensamblados de Common Language Runtime y ensamblados Win32.</span><span class="sxs-lookup"><span data-stu-id="118ed-104">The MsiPublishAssemblies action manages the advertisement of common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="118ed-105">La acción consulta la [tabla MsiAssembly](msiassembly-table.md) para determinar qué ensamblados tienen las características que se están anunciando o instalando en la caché global de ensamblados y qué ensamblados tienen un componente primario que se anuncia o se instala en una ubicación aislada para una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="118ed-105">The action queries the [MsiAssembly table](msiassembly-table.md) to determine which assemblies have features being advertised or installed to the global assembly cache and which assemblies have a parent component being advertised or installed to a location isolated for a particular application.</span></span> <span data-ttu-id="118ed-106">Para obtener más información, vea [Instalar ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md) e [Instalar ensamblados Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="118ed-106">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="118ed-107">En los sistemas de Microsoft Windows XP y versiones posteriores, Windows Installer puede instalar ensamblados Win32 como [ensamblados en paralelo](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="118ed-107">On Microsoft Windows XP and later systems, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="118ed-108">Para obtener más información, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="118ed-108">For more information, see [About Isolated Applications and Side-by-side Assemblies](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="118ed-109">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="118ed-109">Sequence Restrictions</span></span>

<span data-ttu-id="118ed-110">La acción MsiPublishAssemblies debe aparecer después de la [acción InstallInitialize](installinitialize-action.md) en la tabla [InstallExecuteSequence](installexecutesequence-table.md) o en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="118ed-110">The MsiPublishAssemblies action must come after the [InstallInitialize action](installinitialize-action.md) in the [InstallExecuteSequence table](installexecutesequence-table.md) or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="118ed-111">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="118ed-111">ActionData Messages</span></span>



| <span data-ttu-id="118ed-112">Campo</span><span class="sxs-lookup"><span data-stu-id="118ed-112">Field</span></span> | <span data-ttu-id="118ed-113">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="118ed-113">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="118ed-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="118ed-114">\[1\]</span></span> | <span data-ttu-id="118ed-115">Contexto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="118ed-115">Application context.</span></span>       |
| <span data-ttu-id="118ed-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="118ed-116">\[2\]</span></span> | <span data-ttu-id="118ed-117">Nombre del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="118ed-117">Assembly name.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="118ed-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="118ed-118">Remarks</span></span>

<span data-ttu-id="118ed-119">Para obtener más información, vea [ensamblados](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="118ed-119">For more information, see [Assemblies](assemblies.md).</span></span>

<span data-ttu-id="118ed-120">La [acción MsiUnpublishAssemblies](msiunpublishassemblies-action.md) administra el anuncio de los ensamblados que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="118ed-120">The [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md) manages the advertisement of assemblies being removed.</span></span>

 

 
