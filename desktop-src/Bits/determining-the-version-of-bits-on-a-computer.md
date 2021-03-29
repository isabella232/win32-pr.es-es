---
title: Determinar la versión de BITS de un equipo
description: Para determinar la versión de BITS en el equipo cliente, Compruebe la versión de QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773398"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a><span data-ttu-id="471a3-103">Determinar la versión de BITS de un equipo</span><span class="sxs-lookup"><span data-stu-id="471a3-103">Determining the Version of BITS on a Computer</span></span>

<span data-ttu-id="471a3-104">Para determinar la versión de BITS en el equipo cliente, Compruebe la versión de QMgr.dll.</span><span class="sxs-lookup"><span data-stu-id="471a3-104">To determine the version of BITS on the client computer, check the version of QMgr.dll.</span></span> <span data-ttu-id="471a3-105">Para buscar el número de versión de la DLL:</span><span class="sxs-lookup"><span data-stu-id="471a3-105">To find the version number of the DLL:</span></span>

-   <span data-ttu-id="471a3-106">Busque QMgr.dll en% WINDIR% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="471a3-106">Locate QMgr.dll in %windir%\\System32.</span></span>
-   <span data-ttu-id="471a3-107">Haga clic con el botón derecho en QMgr.dll y haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="471a3-107">Right-click QMgr.dll and click **Properties**.</span></span>
-   <span data-ttu-id="471a3-108">Haga clic en la pestaña **versión** .</span><span class="sxs-lookup"><span data-stu-id="471a3-108">Click the **Version** tab.</span></span>
-   <span data-ttu-id="471a3-109">Anote el número de versión.</span><span class="sxs-lookup"><span data-stu-id="471a3-109">Note the version number.</span></span>

<span data-ttu-id="471a3-110">También puede usar el siguiente código de PowerShell para determinar la versión del archivo. dll en el sistema:</span><span class="sxs-lookup"><span data-stu-id="471a3-110">You can also use the following PowerShell code to determine the version of the .dll on your system:</span></span>

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

<span data-ttu-id="471a3-111">Si el archivo DLL existe también en% WINDIR% \\ system32 \\ bits, repita los pasos anteriores.</span><span class="sxs-lookup"><span data-stu-id="471a3-111">If the DLL also exists in %windir%\\System32\\Bits, repeat the previous steps.</span></span> <span data-ttu-id="471a3-112">BITS usa el archivo DLL con el número de versión más alto.</span><span class="sxs-lookup"><span data-stu-id="471a3-112">BITS uses the DLL with the higher version number.</span></span>

<span data-ttu-id="471a3-113">En la tabla siguiente se enumeran las versiones de BITS y sus correspondientes números de versión de archivo de QMgr.dll.</span><span class="sxs-lookup"><span data-stu-id="471a3-113">The following table lists the versions of BITS and their corresponding QMgr.dll file version numbers.</span></span>



| <span data-ttu-id="471a3-114">Versión de BITS</span><span class="sxs-lookup"><span data-stu-id="471a3-114">BITS version</span></span> | <span data-ttu-id="471a3-115">QMgr.dll número de versión del archivo</span><span class="sxs-lookup"><span data-stu-id="471a3-115">QMgr.dll file version number</span></span> |
|--------------|------------------------------|
| <span data-ttu-id="471a3-116">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="471a3-116">BITS 10.1</span></span>    | <span data-ttu-id="471a3-117">7.8. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-117">7.8.xxxx.xxxx</span></span>                |
| <span data-ttu-id="471a3-118">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="471a3-118">BITS 5.0</span></span>     | <span data-ttu-id="471a3-119">7.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-119">7.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="471a3-120">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="471a3-120">BITS 4.0</span></span>     | <span data-ttu-id="471a3-121">7.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-121">7.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="471a3-122">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="471a3-122">BITS 3.0</span></span>     | <span data-ttu-id="471a3-123">7.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-123">7.0.xxxx.xxxx</span></span>                |
| <span data-ttu-id="471a3-124">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="471a3-124">BITS 2.5</span></span>     | <span data-ttu-id="471a3-125">6.7. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-125">6.7.xxxx.xxxx</span></span>                |
| <span data-ttu-id="471a3-126">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="471a3-126">BITS 2.0</span></span>     | <span data-ttu-id="471a3-127">6.6. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-127">6.6.xxxx.xxxx</span></span>                |
| <span data-ttu-id="471a3-128">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="471a3-128">BITS 1.5</span></span>     | <span data-ttu-id="471a3-129">6.5. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-129">6.5.xxxx.xxxx</span></span>                |
| <span data-ttu-id="471a3-130">BITS 1,2</span><span class="sxs-lookup"><span data-stu-id="471a3-130">BITS 1.2</span></span>     | <span data-ttu-id="471a3-131">6.2. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-131">6.2.xxxx.xxxx</span></span>                |
| <span data-ttu-id="471a3-132">BITS 1,0</span><span class="sxs-lookup"><span data-stu-id="471a3-132">BITS 1.0</span></span>     | <span data-ttu-id="471a3-133">6.0. xxxx. xxxx</span><span class="sxs-lookup"><span data-stu-id="471a3-133">6.0.xxxx.xxxx</span></span>                |



 

<span data-ttu-id="471a3-134">También puede usar los identificadores de clase simbólicos para determinar la versión de BITS registrada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="471a3-134">You can also use the symbolic class identifiers to determine the version of BITS that is registered on the computer.</span></span> <span data-ttu-id="471a3-135">En la tabla siguiente se enumeran las versiones de BITS y sus identificadores de clase simbólico correspondientes.</span><span class="sxs-lookup"><span data-stu-id="471a3-135">The following table lists the versions of BITS and their corresponding symbolic class identifiers.</span></span> <span data-ttu-id="471a3-136">La función **CoCreateInstance** devuelve **REGDB \_ E \_ CLASSNOTREG** si la clase no está registrada.</span><span class="sxs-lookup"><span data-stu-id="471a3-136">The **CoCreateInstance** function returns **REGDB\_E\_CLASSNOTREG** if the class is not registered.</span></span>



| <span data-ttu-id="471a3-137">Versión de BITS</span><span class="sxs-lookup"><span data-stu-id="471a3-137">BITS version</span></span>  | <span data-ttu-id="471a3-138">Identificador de clase simbólica</span><span class="sxs-lookup"><span data-stu-id="471a3-138">Symbolic class identifier</span></span>         |
|---------------|-----------------------------------|
| <span data-ttu-id="471a3-139">BITS 10,1</span><span class="sxs-lookup"><span data-stu-id="471a3-139">BITS 10.1</span></span>     | <span data-ttu-id="471a3-140">CLSID \_ BackgroundCopyManager10 \_ 1</span><span class="sxs-lookup"><span data-stu-id="471a3-140">CLSID\_BackgroundCopyManager10\_1</span></span> |
| <span data-ttu-id="471a3-141">BITS 5,0</span><span class="sxs-lookup"><span data-stu-id="471a3-141">BITS 5.0</span></span>      | <span data-ttu-id="471a3-142">CLSID \_ BackgroundCopyManager5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="471a3-142">CLSID\_BackgroundCopyManager5\_0</span></span>  |
| <span data-ttu-id="471a3-143">BITS 4,0</span><span class="sxs-lookup"><span data-stu-id="471a3-143">BITS 4.0</span></span>      | <span data-ttu-id="471a3-144">CLSID \_ BackgroundCopyManager4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="471a3-144">CLSID\_BackgroundCopyManager4\_0</span></span>  |
| <span data-ttu-id="471a3-145">BITS 3,0</span><span class="sxs-lookup"><span data-stu-id="471a3-145">BITS 3.0</span></span>      | <span data-ttu-id="471a3-146">CLSID \_ BackgroundCopyManager3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="471a3-146">CLSID\_BackgroundCopyManager3\_0</span></span>  |
| <span data-ttu-id="471a3-147">BITS 2.5</span><span class="sxs-lookup"><span data-stu-id="471a3-147">BITS 2.5</span></span>      | <span data-ttu-id="471a3-148">CLSID \_ BackgroundCopyManager2 \_ 5</span><span class="sxs-lookup"><span data-stu-id="471a3-148">CLSID\_BackgroundCopyManager2\_5</span></span>  |
| <span data-ttu-id="471a3-149">BITS 2,0</span><span class="sxs-lookup"><span data-stu-id="471a3-149">BITS 2.0</span></span>      | <span data-ttu-id="471a3-150">CLSID \_ BackgroundCopyManager2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="471a3-150">CLSID\_BackgroundCopyManager2\_0</span></span>  |
| <span data-ttu-id="471a3-151">BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="471a3-151">BITS 1.5</span></span>      | <span data-ttu-id="471a3-152">CLSID \_ BackgroundCopyManager1 \_ 5</span><span class="sxs-lookup"><span data-stu-id="471a3-152">CLSID\_BackgroundCopyManager1\_5</span></span>  |
| <span data-ttu-id="471a3-153">BITS 1,2, 1,0</span><span class="sxs-lookup"><span data-stu-id="471a3-153">BITS 1.2, 1.0</span></span> | <span data-ttu-id="471a3-154">CLSID \_ BackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="471a3-154">CLSID\_BackgroundCopyManager</span></span>      |



 

 

 




