---
description: 'La interfaz IRenderEngine representa un proyecto de servicios de edición de DirectShow (DES) mediante la creación de un gráfico de filtro a partir de una escala de tiempo. DES proporciona dos componentes que implementan esta interfaz: el motor de representación básico crea una salida sin comprimir.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interfaz IRenderEngine (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681027"
---
# <a name="irenderengine-interface"></a><span data-ttu-id="9d77b-103">Interfaz IRenderEngine</span><span class="sxs-lookup"><span data-stu-id="9d77b-103">IRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="9d77b-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9d77b-104">\[Deprecated.</span></span> <span data-ttu-id="9d77b-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9d77b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9d77b-106">La `IRenderEngine` interfaz representa un proyecto de [servicios de edición de DirectShow](directshow-editing-services.md) (des) mediante la creación de un gráfico de filtro a partir de una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="9d77b-106">The `IRenderEngine` interface renders a [DirectShow Editing Services](directshow-editing-services.md) (DES) project by constructing a filter graph from a timeline.</span></span>

<span data-ttu-id="9d77b-107">DES proporciona dos componentes que implementan esta interfaz:</span><span class="sxs-lookup"><span data-stu-id="9d77b-107">DES provides two components that implement this interface:</span></span>

-   <span data-ttu-id="9d77b-108">El *motor de representación básico* crea una salida sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="9d77b-108">The *basic render engine* creates uncompressed output.</span></span> <span data-ttu-id="9d77b-109">Puede usar la salida de la vista previa o enrutarla a través de filtros de compresión y escribirla en un archivo.</span><span class="sxs-lookup"><span data-stu-id="9d77b-109">You can use the output for preview, or route it through compression filters and write it to a file.</span></span>
-   <span data-ttu-id="9d77b-110">El *motor de representación inteligente* crea una salida comprimida mediante la *recompresión inteligente*.</span><span class="sxs-lookup"><span data-stu-id="9d77b-110">The *smart render engine* creates compressed output, using *smart recompression*.</span></span> <span data-ttu-id="9d77b-111">Con la recompresión inteligente, un archivo de código fuente se vuelve a comprimir solo si su formato difiere del formato de salida.</span><span class="sxs-lookup"><span data-stu-id="9d77b-111">With smart recompression, a source file is recompressed only if its format differs from the output format.</span></span> <span data-ttu-id="9d77b-112">Un origen con un formato coincidente se escribe directamente en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="9d77b-112">A source with a matching format is written directly to the output file.</span></span> <span data-ttu-id="9d77b-113">Dependiendo del escenario, la recompresión inteligente puede mejorar considerablemente el tiempo de representación.</span><span class="sxs-lookup"><span data-stu-id="9d77b-113">Depending on the scenario, smart recompression can greatly improve rendering time.</span></span>

<span data-ttu-id="9d77b-114">El motor de representación inteligente también admite la interfaz [**ISmartRenderEngine**](ismartrenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="9d77b-114">The smart render engine also supports the [**ISmartRenderEngine**](ismartrenderengine.md) interface.</span></span>

<span data-ttu-id="9d77b-115">Aunque una aplicación puede crear un gráfico de filtro y pasarlo a un motor de representación, el escenario típico es que el motor de representación cree el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="9d77b-115">Although an application can create a filter graph and pass it to a render engine, the typical scenario is for the render engine to create the filter graph.</span></span> <span data-ttu-id="9d77b-116">La compilación del gráfico es un proceso de dos fases.</span><span class="sxs-lookup"><span data-stu-id="9d77b-116">Building the graph is a two-stage process.</span></span> <span data-ttu-id="9d77b-117">En primer lugar, compile el front-end llamando al método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="9d77b-117">First, build the front end by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="9d77b-118">A continuación, conecte los terminales de salida en el front-end a los filtros de representación deseados:</span><span class="sxs-lookup"><span data-stu-id="9d77b-118">Then connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="9d77b-119">Representadores de vídeo y audio para la versión preliminar, o</span><span class="sxs-lookup"><span data-stu-id="9d77b-119">Video and audio renderers for preview, or</span></span>
-   <span data-ttu-id="9d77b-120">Compresores, Multiplexores y escritores de archivos para generar la salida final.</span><span class="sxs-lookup"><span data-stu-id="9d77b-120">Compressors, multiplexers, and file writers to generate the final output.</span></span>

## <a name="members"></a><span data-ttu-id="9d77b-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d77b-121">Members</span></span>

<span data-ttu-id="9d77b-122">La interfaz **IRenderEngine** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9d77b-122">The **IRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9d77b-123">**IRenderEngine** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9d77b-123">**IRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="9d77b-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d77b-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9d77b-125">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d77b-125">Methods</span></span>

<span data-ttu-id="9d77b-126">La interfaz **IRenderEngine** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9d77b-126">The **IRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="9d77b-127">Método</span><span class="sxs-lookup"><span data-stu-id="9d77b-127">Method</span></span>                                                                             | <span data-ttu-id="9d77b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d77b-128">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d77b-129">**Promete**</span><span class="sxs-lookup"><span data-stu-id="9d77b-129">**Commit**</span></span>](irenderengine-commit.md)                                             | <span data-ttu-id="9d77b-130">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9d77b-130">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="9d77b-131">**ConnectFrontEnd**</span><span class="sxs-lookup"><span data-stu-id="9d77b-131">**ConnectFrontEnd**</span></span>](irenderengine-connectfrontend.md)                           | <span data-ttu-id="9d77b-132">Crea el front-end del gráfico de filtro a partir de la escala de tiempo actual.</span><span class="sxs-lookup"><span data-stu-id="9d77b-132">Builds the front end of the filter graph from the current timeline.</span></span><br/>        |
| [<span data-ttu-id="9d77b-133">**Anular**</span><span class="sxs-lookup"><span data-stu-id="9d77b-133">**Decommit**</span></span>](irenderengine-decommit.md)                                         | <span data-ttu-id="9d77b-134">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9d77b-134">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="9d77b-135">**DoSmartRecompression**</span><span class="sxs-lookup"><span data-stu-id="9d77b-135">**DoSmartRecompression**</span></span>](irenderengine-dosmartrecompression.md)                 | <span data-ttu-id="9d77b-136">No se admite.</span><span class="sxs-lookup"><span data-stu-id="9d77b-136">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="9d77b-137">**GetCaps**</span><span class="sxs-lookup"><span data-stu-id="9d77b-137">**GetCaps**</span></span>](irenderengine-getcaps.md)                                           | <span data-ttu-id="9d77b-138">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="9d77b-138">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="9d77b-139">**GetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="9d77b-139">**GetFilterGraph**</span></span>](irenderengine-getfiltergraph.md)                             | <span data-ttu-id="9d77b-140">Recupera el gráfico de filtro que el motor de representación ha construido, si existe.</span><span class="sxs-lookup"><span data-stu-id="9d77b-140">Retrieves the filter graph that the render engine has constructed, if any.</span></span><br/> |
| [<span data-ttu-id="9d77b-141">**GetGroupOutputPin**</span><span class="sxs-lookup"><span data-stu-id="9d77b-141">**GetGroupOutputPin**</span></span>](irenderengine-getgroupoutputpin.md)                       | <span data-ttu-id="9d77b-142">Recupera el PIN de salida para el grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="9d77b-142">Retrieves the output pin for the specified group.</span></span><br/>                          |
| [<span data-ttu-id="9d77b-143">**GetTimelineObject**</span><span class="sxs-lookup"><span data-stu-id="9d77b-143">**GetTimelineObject**</span></span>](irenderengine-gettimelineobject.md)                       | <span data-ttu-id="9d77b-144">Recupera la escala de tiempo que el motor de representación está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="9d77b-144">Retrieves the timeline that the render engine is currently using.</span></span><br/>          |
| [<span data-ttu-id="9d77b-145">**GetVendorString**</span><span class="sxs-lookup"><span data-stu-id="9d77b-145">**GetVendorString**</span></span>](irenderengine-getvendorstring.md)                           | <span data-ttu-id="9d77b-146">Recupera la cadena de proveedor.</span><span class="sxs-lookup"><span data-stu-id="9d77b-146">Retrieves the vendor string.</span></span><br/>                                               |
| [<span data-ttu-id="9d77b-147">**RenderOutputPins**</span><span class="sxs-lookup"><span data-stu-id="9d77b-147">**RenderOutputPins**</span></span>](irenderengine-renderoutputpins.md)                         | <span data-ttu-id="9d77b-148">Crea la parte de vista previa del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="9d77b-148">Creates the previewing portion of the filter graph.</span></span><br/>                        |
| [<span data-ttu-id="9d77b-149">**ScrapIt**</span><span class="sxs-lookup"><span data-stu-id="9d77b-149">**ScrapIt**</span></span>](irenderengine-scrapit.md)                                           | <span data-ttu-id="9d77b-150">Descarta el gráfico de filtro del motor de representación y todos los objetos asociados.</span><span class="sxs-lookup"><span data-stu-id="9d77b-150">Discards the render engine's filter graph and all associated objects.</span></span><br/>      |
| [<span data-ttu-id="9d77b-151">**SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="9d77b-151">**SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)         | <span data-ttu-id="9d77b-152">Establece el nivel de reconexión dinámica durante la representación.</span><span class="sxs-lookup"><span data-stu-id="9d77b-152">Sets the level of dynamic reconnection during rendering.</span></span><br/>                   |
| [<span data-ttu-id="9d77b-153">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="9d77b-153">**SetFilterGraph**</span></span>](irenderengine-setfiltergraph.md)                             | <span data-ttu-id="9d77b-154">Especifica un gráfico de filtro para que lo use el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="9d77b-154">Specifies a filter graph for the render engine to use.</span></span><br/>                     |
| [<span data-ttu-id="9d77b-155">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="9d77b-155">**SetInterestRange**</span></span>](irenderengine-setinterestrange.md)                         | <span data-ttu-id="9d77b-156">No se admite.</span><span class="sxs-lookup"><span data-stu-id="9d77b-156">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="9d77b-157">**SetInterestRange2**</span><span class="sxs-lookup"><span data-stu-id="9d77b-157">**SetInterestRange2**</span></span>](irenderengine-setinterestrange2.md)                       | <span data-ttu-id="9d77b-158">No se admite.</span><span class="sxs-lookup"><span data-stu-id="9d77b-158">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="9d77b-159">**SetRenderRange**</span><span class="sxs-lookup"><span data-stu-id="9d77b-159">**SetRenderRange**</span></span>](irenderengine-setrenderrange.md)                             | <span data-ttu-id="9d77b-160">Establece el intervalo de tiempo que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="9d77b-160">Sets the range of time to be rendered.</span></span><br/>                                     |
| [<span data-ttu-id="9d77b-161">**SetRenderRange2**</span><span class="sxs-lookup"><span data-stu-id="9d77b-161">**SetRenderRange2**</span></span>](irenderengine-setrenderrange2.md)                           | <span data-ttu-id="9d77b-162">Establece el intervalo de tiempo que se va a representar, como un **valor de tipo Double**.</span><span class="sxs-lookup"><span data-stu-id="9d77b-162">Sets the range of time to be rendered, as a **double**.</span></span><br/>                    |
| [<span data-ttu-id="9d77b-163">**SetSourceConnectCallback**</span><span class="sxs-lookup"><span data-stu-id="9d77b-163">**SetSourceConnectCallback**</span></span>](irenderengine-setsourceconnectcallback.md)         | <span data-ttu-id="9d77b-164">No se admite.</span><span class="sxs-lookup"><span data-stu-id="9d77b-164">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="9d77b-165">**SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="9d77b-165">**SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)           | <span data-ttu-id="9d77b-166">Especifica cómo valida el motor de representación los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="9d77b-166">Specifies how the render engine validates file names.</span></span><br/>                      |
| [<span data-ttu-id="9d77b-167">**SetTimelineObject**</span><span class="sxs-lookup"><span data-stu-id="9d77b-167">**SetTimelineObject**</span></span>](irenderengine-settimelineobject.md)                       | <span data-ttu-id="9d77b-168">Establece la escala de tiempo que va a usar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="9d77b-168">Sets the timeline for the render engine to use.</span></span><br/>                            |
| [<span data-ttu-id="9d77b-169">**UseInSmartRecompressionGraph**</span><span class="sxs-lookup"><span data-stu-id="9d77b-169">**UseInSmartRecompressionGraph**</span></span>](irenderengine-useinsmartrecompressiongraph.md) | <span data-ttu-id="9d77b-170">No se admite.</span><span class="sxs-lookup"><span data-stu-id="9d77b-170">Not supported.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="9d77b-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d77b-171">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9d77b-172">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9d77b-172">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9d77b-173">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9d77b-173">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9d77b-174">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9d77b-174">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9d77b-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d77b-175">Requirements</span></span>



| <span data-ttu-id="9d77b-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d77b-176">Requirement</span></span> | <span data-ttu-id="9d77b-177">Value</span><span class="sxs-lookup"><span data-stu-id="9d77b-177">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d77b-178">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d77b-178">Header</span></span><br/>  | <dl> <span data-ttu-id="9d77b-179"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d77b-179"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9d77b-180">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d77b-180">Library</span></span><br/> | <dl> <span data-ttu-id="9d77b-181"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d77b-181"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d77b-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d77b-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d77b-183">Representar un proyecto</span><span class="sxs-lookup"><span data-stu-id="9d77b-183">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
