---
description: Compilar aplicaciones de DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Compilar aplicaciones de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677027"
---
# <a name="building-directshow-applications"></a><span data-ttu-id="e8e3a-103">Compilar aplicaciones de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e8e3a-103">Building DirectShow Applications</span></span>

<span data-ttu-id="e8e3a-104">En este tema se describen los encabezados y las bibliotecas necesarios para compilar aplicaciones de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-104">This topic describes the headers and libraries needed to build DirectShow applications.</span></span>

<span data-ttu-id="e8e3a-105">Los encabezados y las bibliotecas de DirectShow más recientes están disponibles en el [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8e3a-105">The latest DirectShow headers and libraries are available in the [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span></span>

## <a name="header-files"></a><span data-ttu-id="e8e3a-106">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e8e3a-106">Header Files</span></span>

<span data-ttu-id="e8e3a-107">Todas las aplicaciones de DirectShow usan el archivo de encabezado que se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-107">All DirectShow applications use the header file shown in the following table.</span></span>



| <span data-ttu-id="e8e3a-108">Archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="e8e3a-108">Header File</span></span> | <span data-ttu-id="e8e3a-109">Necesario para</span><span class="sxs-lookup"><span data-stu-id="e8e3a-109">Required For</span></span>                 |
|-------------|------------------------------|
| <span data-ttu-id="e8e3a-110">DShow. h</span><span class="sxs-lookup"><span data-stu-id="e8e3a-110">Dshow.h</span></span>     | <span data-ttu-id="e8e3a-111">Todas las aplicaciones de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-111">All DirectShow applications.</span></span> |



 

<span data-ttu-id="e8e3a-112">Algunas interfaces de DirectShow requieren archivos de encabezado adicionales.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-112">Some DirectShow interfaces require additional header files.</span></span> <span data-ttu-id="e8e3a-113">Estos requisitos se indican en la referencia de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-113">These requirements are noted in the interface reference.</span></span>

## <a name="library-files"></a><span data-ttu-id="e8e3a-114">Archivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8e3a-114">Library Files</span></span>

<span data-ttu-id="e8e3a-115">DirectShow usa los archivos de biblioteca estáticos que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-115">DirectShow uses the static library files shown in the following table.</span></span>



| <span data-ttu-id="e8e3a-116">Archivo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8e3a-116">Library File</span></span> | <span data-ttu-id="e8e3a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8e3a-117">Description</span></span>                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e3a-118">Strmiids. lib</span><span class="sxs-lookup"><span data-stu-id="e8e3a-118">Strmiids.lib</span></span> | <span data-ttu-id="e8e3a-119">Exporta identificadores de clase (CLSID) e identificadores de interfaz (IID).</span><span class="sxs-lookup"><span data-stu-id="e8e3a-119">Exports class identifiers (CLSIDs) and interface identifiers (IIDs).</span></span>                                                           |
| <span data-ttu-id="e8e3a-120">Quartz. lib</span><span class="sxs-lookup"><span data-stu-id="e8e3a-120">Quartz.lib</span></span>   | <span data-ttu-id="e8e3a-121">Exporta la función [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) .</span><span class="sxs-lookup"><span data-stu-id="e8e3a-121">Exports the [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) function.</span></span> <span data-ttu-id="e8e3a-122">Si no llama a esta función, esta biblioteca no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-122">If you do not call this function, this library is not required.</span></span> |



 

<span data-ttu-id="e8e3a-123">Utilice los mismos archivos. lib para las compilaciones de depuración y lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-123">Use the same .lib files for debug and release builds.</span></span>

## <a name="filter-base-classes"></a><span data-ttu-id="e8e3a-124">Filtrar clases base</span><span class="sxs-lookup"><span data-stu-id="e8e3a-124">Filter Base Classes</span></span>

<span data-ttu-id="e8e3a-125">El Windows SDK proporciona un conjunto de clases de C++ que se recomiendan si se escribe un filtro DirectShow personalizado.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-125">The Windows SDK provides a set of C++ classes that are recommended if you are writing a custom DirectShow filter.</span></span> <span data-ttu-id="e8e3a-126">Estas clases se proporcionan como código de ejemplo, que se puede compilar en una biblioteca estática.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-126">These classes are provided as sample code, which you can compile to a static library.</span></span> <span data-ttu-id="e8e3a-127">Para obtener más información, vea [clases base de DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="e8e3a-127">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="redistributable-dlls"></a><span data-ttu-id="e8e3a-128">Archivos dll redistribuibles</span><span class="sxs-lookup"><span data-stu-id="e8e3a-128">Redistributable DLLs</span></span>

<span data-ttu-id="e8e3a-129">Las aplicaciones de DirectShow escritas para Windows XP con Service Pack 2 (SP2) y versiones posteriores no necesitan redistribuir los archivos dll de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-129">DirectShow applications written for Windows XP with Service Pack 2 (SP2) and later do not need to redistribute any DirectShow DLLs.</span></span>

<span data-ttu-id="e8e3a-130">En el caso de Windows XP con Service Pack 1 (SP1) y versiones anteriores, los archivos dll de DirectShow redistribuibles están disponibles en el SDK de Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-130">For Windows XP with Service Pack 1 (SP1) and earlier, redistributable DirectShow DLLs are available from the Microsoft DirectX SDK.</span></span> <span data-ttu-id="e8e3a-131">La versión más reciente de estos archivos dll es la versión 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-131">The latest version of these DLLs is version 9.0c.</span></span> <span data-ttu-id="e8e3a-132">No se prevé ningún otro desarrollo de estos archivos dll redistribuibles.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-132">No further development of these redistributable DLLs is planned.</span></span> <span data-ttu-id="e8e3a-133">Windows XP con Service Pack 2 (SP2) contiene los archivos dll de c de la versión 9.0.</span><span class="sxs-lookup"><span data-stu-id="e8e3a-133">Windows XP with Service Pack 2 (SP2) contains the version 9.0c DLLs.</span></span>

<span data-ttu-id="e8e3a-134">Los paquetes de redstributable contienen los siguientes archivos dll:</span><span class="sxs-lookup"><span data-stu-id="e8e3a-134">The redstributable packages contain the following DLLs:</span></span>

-   <span data-ttu-id="e8e3a-135">dxnt.cab</span><span class="sxs-lookup"><span data-stu-id="e8e3a-135">dxnt.cab</span></span>
    -   <span data-ttu-id="e8e3a-136">amstream.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-136">amstream.dll</span></span>
    -   <span data-ttu-id="e8e3a-137">devenum.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-137">devenum.dll</span></span>
    -   <span data-ttu-id="e8e3a-138">encapi.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-138">encapi.dll</span></span>
    -   <span data-ttu-id="e8e3a-139">ks.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-139">ks.sys</span></span>
    -   <span data-ttu-id="e8e3a-140">ksolay.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-140">ksolay.ax</span></span>
    -   <span data-ttu-id="e8e3a-141">ksproxy.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-141">ksproxy.ax</span></span>
    -   <span data-ttu-id="e8e3a-142">ksuser.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-142">ksuser.dll</span></span>
    -   <span data-ttu-id="e8e3a-143">l3codecx.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-143">l3codecx.ax</span></span>
    -   <span data-ttu-id="e8e3a-144">mciqtz32.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-144">mciqtz32.dll</span></span>
    -   <span data-ttu-id="e8e3a-145">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-145">mpg2splt.ax</span></span>
    -   <span data-ttu-id="e8e3a-146">msdmo.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-146">msdmo.dll</span></span>
    -   <span data-ttu-id="e8e3a-147">mskssrv.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-147">mskssrv.sys</span></span>
    -   <span data-ttu-id="e8e3a-148">mspclock.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-148">mspclock.sys</span></span>
    -   <span data-ttu-id="e8e3a-149">mspqm.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-149">mspqm.sys</span></span>
    -   <span data-ttu-id="e8e3a-150">mstee.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-150">mstee.sys</span></span>
    -   <span data-ttu-id="e8e3a-151">mswebdvd.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-151">mswebdvd.dll</span></span>
    -   <span data-ttu-id="e8e3a-152">qasf.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-152">qasf.dll</span></span>
    -   <span data-ttu-id="e8e3a-153">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-153">qcap.dll</span></span>
    -   <span data-ttu-id="e8e3a-154">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-154">qdv.dll</span></span>
    -   <span data-ttu-id="e8e3a-155">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-155">qdvd.dll</span></span>
    -   <span data-ttu-id="e8e3a-156">qedit.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-156">qedit.dll</span></span>
    -   <span data-ttu-id="e8e3a-157">qedwipes.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-157">qedwipes.dll</span></span>
    -   <span data-ttu-id="e8e3a-158">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-158">quartz.dll</span></span>
    -   <span data-ttu-id="e8e3a-159">stream.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-159">stream.sys</span></span>
    -   <span data-ttu-id="e8e3a-160">swenum.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-160">swenum.sys</span></span>
-   <span data-ttu-id="e8e3a-161">bda.cab</span><span class="sxs-lookup"><span data-stu-id="e8e3a-161">bda.cab</span></span>
    -   <span data-ttu-id="e8e3a-162">bdaplgin.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-162">bdaplgin.ax</span></span>
    -   <span data-ttu-id="e8e3a-163">bdasup.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-163">bdasup.sys</span></span>
    -   <span data-ttu-id="e8e3a-164">ccdecode.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-164">ccdecode.sys</span></span>
    -   <span data-ttu-id="e8e3a-165">ipsink.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-165">ipsink.ax</span></span>
    -   <span data-ttu-id="e8e3a-166">kstvtune.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-166">kstvtune.ax</span></span>
    -   <span data-ttu-id="e8e3a-167">kswdmcap.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-167">kswdmcap.ax</span></span>
    -   <span data-ttu-id="e8e3a-168">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-168">ksxbar.ax</span></span>
    -   <span data-ttu-id="e8e3a-169">mpe.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-169">mpe.sys</span></span>
    -   <span data-ttu-id="e8e3a-170">mpeg2data.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-170">mpeg2data.ax</span></span>
    -   <span data-ttu-id="e8e3a-171">msdv.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-171">msdv.sys</span></span>
    -   <span data-ttu-id="e8e3a-172">msdvbnp.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-172">msdvbnp.ax</span></span>
    -   <span data-ttu-id="e8e3a-173">msvidctl.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-173">msvidctl.dll</span></span>
    -   <span data-ttu-id="e8e3a-174">msyuv.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-174">msyuv.dll</span></span>
    -   <span data-ttu-id="e8e3a-175">nabtsfec.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-175">nabtsfec.sys</span></span>
    -   <span data-ttu-id="e8e3a-176">ndisip.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-176">ndisip.sys</span></span>
    -   <span data-ttu-id="e8e3a-177">psisdecd.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-177">psisdecd.dll</span></span>
    -   <span data-ttu-id="e8e3a-178">psisrndr.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-178">psisrndr.ax</span></span>
    -   <span data-ttu-id="e8e3a-179">slip.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-179">slip.sys</span></span>
    -   <span data-ttu-id="e8e3a-180">streamip.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-180">streamip.sys</span></span>
    -   <span data-ttu-id="e8e3a-181">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="e8e3a-181">vbisurf.ax</span></span>
    -   <span data-ttu-id="e8e3a-182">wstcodec.sys</span><span class="sxs-lookup"><span data-stu-id="e8e3a-182">wstcodec.sys</span></span>
    -   <span data-ttu-id="e8e3a-183">wstdecod.dll</span><span class="sxs-lookup"><span data-stu-id="e8e3a-183">wstdecod.dll</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8e3a-184">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8e3a-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8e3a-185">Compilar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="e8e3a-185">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> </dl>

 

 
