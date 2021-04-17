---
description: Representa información sobre el historial de píxeles.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixelHistoryOperation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705219"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span data-ttu-id="2cd0a-103"><span id="vspixengine.pixelhistoryoperation"></span>Estructura PixelHistoryOperation</span><span class="sxs-lookup"><span data-stu-id="2cd0a-103"><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation structure</span></span>

<span data-ttu-id="2cd0a-104">Representa información sobre el historial de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-104">Represents information about pixel history.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd0a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cd0a-105">Syntax</span></span>


```C++
} PixelHistoryOperation;
```

## <a name="members"></a><span data-ttu-id="2cd0a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2cd0a-106">Members</span></span>

<span data-ttu-id="2cd0a-107">**Eid**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-107">**eid**</span></span>  
<span data-ttu-id="2cd0a-108">IDENTIFICADOR del evento de gráficos asociado a esta operación.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-108">The ID of the graphics event associated with this operation.</span></span>

<span data-ttu-id="2cd0a-109">**MEDICO**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-109">**PCP**</span></span>  
<span data-ttu-id="2cd0a-110">Llamadas empaquetadas asociadas a esta operación.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-110">Packed calls associated with this operation.</span></span>

<span data-ttu-id="2cd0a-111">**renderTargetPtr**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-111">**renderTargetPtr**</span></span>  
<span data-ttu-id="2cd0a-112">Destino de representación asociado originalmente (dentro de la aplicación capturada) con esta operación.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-112">The render target originally associated (inside the captured application) with this operation.</span></span>

<span data-ttu-id="2cd0a-113">**iPrim**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-113">**iPrim**</span></span>  
<span data-ttu-id="2cd0a-114">Índice del primitivo real asociado a su operación.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-114">The index of the actual primitive associated witht his operation.</span></span>

<span data-ttu-id="2cd0a-115">**numPrims**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-115">**numPrims**</span></span>  
<span data-ttu-id="2cd0a-116">Número total de primitivas asociadas a esta operación.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-116">The total number of primitives associated with this operation.</span></span>

<span data-ttu-id="2cd0a-117">**numVertsPerPrim**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-117">**numVertsPerPrim**</span></span>  
<span data-ttu-id="2cd0a-118">El número de vértices por primitivo.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-118">The number of vertices per primitive.</span></span>

<span data-ttu-id="2cd0a-119">**iInstance**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-119">**iInstance**</span></span>  
<span data-ttu-id="2cd0a-120">Al representar instancias, el número de instancia de la instancia real asociada a esta operación.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-120">When rendering instances, the instance number of the actual instance associated with this operation.</span></span>

<span data-ttu-id="2cd0a-121">**iInstanceCount**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-121">**iInstanceCount**</span></span>  
<span data-ttu-id="2cd0a-122">Al representar las instancias, el número total de instancias asociadas a esta operación.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-122">When rendering instances, the total number of instances associated with this operation.</span></span>

<span data-ttu-id="2cd0a-123">**bAssemblerStageGeneratesInstanceID**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-123">**bAssemblerStageGeneratesInstanceID**</span></span>  
<span data-ttu-id="2cd0a-124">True si el ensamblador de entrada genera identificadores de instancia; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-124">true if the input assembler generates instance IDs; otherwise false.</span></span>

<span data-ttu-id="2cd0a-125">**flags**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-125">**flags**</span></span>  
<span data-ttu-id="2cd0a-126">Combinación de valores de PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-126">A combination of PIXELHISTORYFLAGS values.</span></span> <span data-ttu-id="2cd0a-127">Para obtener más información, consulte la enumeración PIXELHISTORYFLAGS.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-127">For more information, see the PIXELHISTORYFLAGS enumeration.</span></span>

<span data-ttu-id="2cd0a-128">**pVSFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-128">**pVSFile**</span></span>  
<span data-ttu-id="2cd0a-129">Un FILEPTR para la secuencia de bytes del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-129">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="2cd0a-130">Esto se devuelve para depurar.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-130">This is passed back in order to debug.</span></span>

<span data-ttu-id="2cd0a-131">**pGSFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-131">**pGSFile**</span></span>  
<span data-ttu-id="2cd0a-132">FILEPTR para el flujo de bytes del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-132">A FILEPTR for the geometry shader byte stream.</span></span> <span data-ttu-id="2cd0a-133">Esto se devuelve para depurar.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-133">This is passed back in order to debug.</span></span>

<span data-ttu-id="2cd0a-134">**pPSFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-134">**pPSFile**</span></span>  
<span data-ttu-id="2cd0a-135">Un FILEPTR para la secuencia de bytes del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-135">A FILEPTR for the pixel shader byte stream.</span></span> <span data-ttu-id="2cd0a-136">Esto se devuelve para depurar.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-136">This is passed back in order to debug.</span></span>

<span data-ttu-id="2cd0a-137">**pHSFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-137">**pHSFile**</span></span>  
<span data-ttu-id="2cd0a-138">Un FILEPTR para la secuencia de bytes del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-138">A FILEPTR for the hull shader byte stream.</span></span> <span data-ttu-id="2cd0a-139">Esto se devuelve para depurar.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-139">This is passed back in order to debug.</span></span>

<span data-ttu-id="2cd0a-140">**pDSFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-140">**pDSFile**</span></span>  
<span data-ttu-id="2cd0a-141">FILEPTR para el flujo de bytes del sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-141">A FILEPTR for the domain shader byte stream.</span></span> <span data-ttu-id="2cd0a-142">Esto se devuelve para depurar.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-142">This is passed back in order to debug.</span></span>

<span data-ttu-id="2cd0a-143">**pCSFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-143">**pCSFile**</span></span>  
<span data-ttu-id="2cd0a-144">Un FILEPTR para la secuencia de bytes del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-144">A FILEPTR for the compute shader byte stream.</span></span> <span data-ttu-id="2cd0a-145">Esto se devuelve para depurar.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-145">This is passed back in order to debug.</span></span>

<span data-ttu-id="2cd0a-146">**VertexShaderFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-146">**VertexShaderFile**</span></span>  
<span data-ttu-id="2cd0a-147">Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-147">A COM string containing the filepath of the vertex shader source file.</span></span>

<span data-ttu-id="2cd0a-148">**PixelShaderFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-148">**PixelShaderFile**</span></span>  
<span data-ttu-id="2cd0a-149">Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-149">A COM string containing the filepath of the pixel shader source file.</span></span>

<span data-ttu-id="2cd0a-150">**GeometryShaderFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-150">**GeometryShaderFile**</span></span>  
<span data-ttu-id="2cd0a-151">Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-151">A COM string containing the filepath of the geometry shader source file.</span></span>

<span data-ttu-id="2cd0a-152">**HullShaderFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-152">**HullShaderFile**</span></span>  
<span data-ttu-id="2cd0a-153">Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-153">A COM string containing the filepath of the hull shader source file.</span></span>

<span data-ttu-id="2cd0a-154">**DomainShaderFile**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-154">**DomainShaderFile**</span></span>  
<span data-ttu-id="2cd0a-155">Cadena COM que contiene la ruta de acceso del archivo de origen del sombreador de dominios.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-155">A COM string containing the filepath of the domain shader source file.</span></span>

<span data-ttu-id="2cd0a-156">**psRed**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-156">**psRed**</span></span>  
<span data-ttu-id="2cd0a-157">Salida del sombreador de píxeles: valor del componente de color rojo.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-157">Pixel shader output: value of red color component.</span></span>

<span data-ttu-id="2cd0a-158">**psGreen**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-158">**psGreen**</span></span>  
<span data-ttu-id="2cd0a-159">Salida del sombreador de píxeles: valor del componente de color verde.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-159">Pixel shader output: value of green color component.</span></span>

<span data-ttu-id="2cd0a-160">**psBlue**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-160">**psBlue**</span></span>  
<span data-ttu-id="2cd0a-161">Salida del sombreador de píxeles: valor de componente de color azul</span><span class="sxs-lookup"><span data-stu-id="2cd0a-161">Pixel shader output: value of blue color component</span></span>

<span data-ttu-id="2cd0a-162">**psAlpha**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-162">**psAlpha**</span></span>  
<span data-ttu-id="2cd0a-163">Salida del sombreador de píxeles: valor del componente de color alfa</span><span class="sxs-lookup"><span data-stu-id="2cd0a-163">Pixel shader output: value of alpha color component</span></span>

<span data-ttu-id="2cd0a-164">**LabelPSRed**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-164">**LabelPSRed**</span></span>  
<span data-ttu-id="2cd0a-165">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo de la salida del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-165">A COM string containing the name of the label associated with the red color component of the pixel shader output.</span></span>

<span data-ttu-id="2cd0a-166">**LabelPSGreen**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-166">**LabelPSGreen**</span></span>  
<span data-ttu-id="2cd0a-167">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde de la salida del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-167">A COM string containing the name of the label associated with the green color component of the pixel shader output.</span></span>

<span data-ttu-id="2cd0a-168">**LabelPSBlue**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-168">**LabelPSBlue**</span></span>  
<span data-ttu-id="2cd0a-169">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul de la salida del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-169">A COM string containing the name of the label associated with the blue color component of the pixel shader output.</span></span>

<span data-ttu-id="2cd0a-170">**LabelPSAlpha**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-170">**LabelPSAlpha**</span></span>  
<span data-ttu-id="2cd0a-171">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa de la salida del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-171">A COM string containing the name of the label associated with the alpha color component of the pixel shader output.</span></span>

<span data-ttu-id="2cd0a-172">**pixelKillReason**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-172">**pixelKillReason**</span></span>  
<span data-ttu-id="2cd0a-173">Salida del sombreador de píxeles: motivo por el que se eliminó la salida del píxel.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-173">Pixel shader output: reason the pixel output was killed.</span></span>

<span data-ttu-id="2cd0a-174">**pixelOccluded**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-174">**pixelOccluded**</span></span>  
<span data-ttu-id="2cd0a-175">True si el píxel es ocluidos; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-175">true if the pixel is occluded; otherwise, false.</span></span>

<span data-ttu-id="2cd0a-176">**fbRed**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-176">**fbRed**</span></span>  
<span data-ttu-id="2cd0a-177">Fotogramas: valor del componente de color rojo de fotogramas antes de que se combine el resultado del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-177">Framebuffer: value of red color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="2cd0a-178">**fbGreen**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-178">**fbGreen**</span></span>  
<span data-ttu-id="2cd0a-179">Fotogramas: valor del componente de color verde de fotogramas antes de que se combine el resultado del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-179">Framebuffer: value of green color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="2cd0a-180">**fbBlue**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-180">**fbBlue**</span></span>  
<span data-ttu-id="2cd0a-181">Fotogramas: valor del componente de color azul de fotogramas antes de que se combine el resultado del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-181">Framebuffer: value of blue color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="2cd0a-182">**fbAlpha**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-182">**fbAlpha**</span></span>  
<span data-ttu-id="2cd0a-183">Fotogramas: valor del componente de color alfa de fotogramas antes de que se combine el resultado del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-183">Framebuffer: value of alpha color component of framebuffer before pixel shader output is merged.</span></span>

<span data-ttu-id="2cd0a-184">**LabelFBRed**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-184">**LabelFBRed**</span></span>  
<span data-ttu-id="2cd0a-185">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-185">A COM string containing the name of the label associated with the red color component of the framebuffer.</span></span>

<span data-ttu-id="2cd0a-186">**LabelFBGreen**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-186">**LabelFBGreen**</span></span>  
<span data-ttu-id="2cd0a-187">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-187">A COM string containing the name of the label associated with the green color component of the framebuffer.</span></span>

<span data-ttu-id="2cd0a-188">**LabelFBBlue**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-188">**LabelFBBlue**</span></span>  
<span data-ttu-id="2cd0a-189">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-189">A COM string containing the name of the label associated with the blue color component of the framebuffer.</span></span>

<span data-ttu-id="2cd0a-190">**LabelFBAlpha**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-190">**LabelFBAlpha**</span></span>  
<span data-ttu-id="2cd0a-191">Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-191">A COM string containing the name of the label associated with the alpha color component of the framebuffer.</span></span>

<span data-ttu-id="2cd0a-192">**topología**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-192">**topology**</span></span>  
<span data-ttu-id="2cd0a-193">La topología de vértices de las llamadas a Draw (lista de triángulos, franja de triángulo, etc.).</span><span class="sxs-lookup"><span data-stu-id="2cd0a-193">The vertex topology of the draw calls (triangle list, triangle strip, etc).</span></span>

<span data-ttu-id="2cd0a-194">**vértices**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-194">**vertices**</span></span>  
<span data-ttu-id="2cd0a-195">Cadena COM que contiene el búfer de vértices a partir de este primitivo.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-195">A COM string containing the vertex buffer starting at this primitive.</span></span> <span data-ttu-id="2cd0a-196">El búfer de vértices sigue el formato de diseño de entrada especificado en la fase de canalización.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-196">The vertex buffer follows the input layout format specified in the pipeline stage.</span></span>

<span data-ttu-id="2cd0a-197">**vertexSize**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-197">**vertexSize**</span></span>  
<span data-ttu-id="2cd0a-198">Tamaño de un único vértice en bytes.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-198">The size of a single vertex in bytes.</span></span>

<span data-ttu-id="2cd0a-199">**InputLayout**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-199">**InputLayout**</span></span>  
<span data-ttu-id="2cd0a-200">Cadena COM que contiene una secuencia de estructuras InputLayoutStruct asociadas a la llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-200">A COM string containing a sequence of InputLayoutStruct structures associated with the draw call.</span></span>

<span data-ttu-id="2cd0a-201">**HResult**</span><span class="sxs-lookup"><span data-stu-id="2cd0a-201">**HResult**</span></span>  
<span data-ttu-id="2cd0a-202">HRESULT de DirectX.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-202">The DirectX Hresult.</span></span> <span data-ttu-id="2cd0a-203">En caso de que se produce un problema, se puede usar para mostrar el error.</span><span class="sxs-lookup"><span data-stu-id="2cd0a-203">In the event of a problem this can be used to display the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd0a-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cd0a-204">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2cd0a-205">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cd0a-205">Header</span></span></p></td><td><span data-ttu-id="2cd0a-206">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2cd0a-206">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



