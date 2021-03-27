---
title: Estructuras de sombreador (gráficos de Direct3D 11)
description: Las estructuras se usan para crear y usar sombreadores.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- estructuras, sombreadores de Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800842"
---
# <a name="shader-structures-direct3d-11-graphics"></a><span data-ttu-id="91d9c-104">Estructuras de sombreador (gráficos de Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="91d9c-104">Shader Structures (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="91d9c-105">Las estructuras se usan para crear y usar sombreadores.</span><span class="sxs-lookup"><span data-stu-id="91d9c-105">Structures are used to create and use shaders.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="91d9c-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="91d9c-106">In this section</span></span>



| <span data-ttu-id="91d9c-107">Tema</span><span class="sxs-lookup"><span data-stu-id="91d9c-107">Topic</span></span>                                                                                       | <span data-ttu-id="91d9c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="91d9c-108">Description</span></span>                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="91d9c-109">**Descripción de la \_ instancia de clase D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-109">**D3D11\_CLASS\_INSTANCE\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | <span data-ttu-id="91d9c-110">Describe una instancia de la clase HLSL.</span><span class="sxs-lookup"><span data-stu-id="91d9c-110">Describes an HLSL class instance.</span></span><br/>                           |
| [<span data-ttu-id="91d9c-111">**\_Descripción de \_ seguimiento del sombreador de cálculo de \_ D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-111">**D3D11\_COMPUTE\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | <span data-ttu-id="91d9c-112">Describe una instancia de un sombreador de cálculo que se va a trazar.</span><span class="sxs-lookup"><span data-stu-id="91d9c-112">Describes an instance of a compute shader to trace.</span></span><br/>         |
| [<span data-ttu-id="91d9c-113">**\_Descripción de \_ seguimiento del sombreador de dominio de \_ D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-113">**D3D11\_DOMAIN\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | <span data-ttu-id="91d9c-114">Describe una instancia de un sombreador de dominio para realizar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="91d9c-114">Describes an instance of a domain shader to trace.</span></span><br/>          |
| [<span data-ttu-id="91d9c-115">**D3D11 \_ función \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="91d9c-115">**D3D11\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | <span data-ttu-id="91d9c-116">Describe una función.</span><span class="sxs-lookup"><span data-stu-id="91d9c-116">Describes a function.</span></span><br/>                                       |
| [<span data-ttu-id="91d9c-117">**D3D11 \_ \_ DESC del sombreador de geometría \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-117">**D3D11\_GEOMETRY\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | <span data-ttu-id="91d9c-118">Describe una instancia de un sombreador de geometría del que se realiza el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="91d9c-118">Describes an instance of a geometry shader to trace.</span></span><br/>        |
| [<span data-ttu-id="91d9c-119">**DESC. de \_ \_ seguimiento del sombreador de casco D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-119">**D3D11\_HULL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | <span data-ttu-id="91d9c-120">Describe una instancia de un sombreador de casco para realizar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="91d9c-120">Describes an instance of a hull shader to trace.</span></span><br/>            |
| [<span data-ttu-id="91d9c-121">**Descripción de la \_ biblioteca D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-121">**D3D11\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | <span data-ttu-id="91d9c-122">Describe una biblioteca de.</span><span class="sxs-lookup"><span data-stu-id="91d9c-122">Describes a library.</span></span><br/>                                        |
| [<span data-ttu-id="91d9c-123">**\_Parámetro D3D11 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="91d9c-123">**D3D11\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | <span data-ttu-id="91d9c-124">Describe un parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="91d9c-124">Describes a function parameter.</span></span> <br/>                            |
| [<span data-ttu-id="91d9c-125">**DESC. de \_ \_ seguimiento del sombreador de píxeles D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-125">**D3D11\_PIXEL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | <span data-ttu-id="91d9c-126">Describe una instancia de un sombreador de píxeles para el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="91d9c-126">Describes an instance of a pixel shader to trace.</span></span><br/>           |
| [<span data-ttu-id="91d9c-127">**\_Desc. búfer del sombreador de D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-127">**D3D11\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | <span data-ttu-id="91d9c-128">Describe un búfer de constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="91d9c-128">Describes a shader constant-buffer.</span></span><br/>                         |
| [<span data-ttu-id="91d9c-129">**\_Descripción del sombreador D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-129">**D3D11\_SHADER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | <span data-ttu-id="91d9c-130">Describe un sombreador.</span><span class="sxs-lookup"><span data-stu-id="91d9c-130">Describes a shader.</span></span><br/>                                         |
| [<span data-ttu-id="91d9c-131">**\_DESC de enlace de entrada del sombreador D3D11 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-131">**D3D11\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | <span data-ttu-id="91d9c-132">Describe cómo un recurso de sombreador se enlaza a una entrada de sombreador.</span><span class="sxs-lookup"><span data-stu-id="91d9c-132">Describes how a shader resource is bound to a shader input.</span></span><br/> |
| [<span data-ttu-id="91d9c-133">**\_Descripción del sombreador de D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-133">**D3D11\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | <span data-ttu-id="91d9c-134">Describe un objeto de seguimiento de sombreador.</span><span class="sxs-lookup"><span data-stu-id="91d9c-134">Describes a shader-trace object.</span></span><br/>                            |
| [<span data-ttu-id="91d9c-135">**\_Tipo de sombreador D3D11 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="91d9c-135">**D3D11\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | <span data-ttu-id="91d9c-136">Describe un tipo de variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="91d9c-136">Describes a shader-variable type.</span></span><br/>                           |
| [<span data-ttu-id="91d9c-137">**D3D11 \_ variable de sombreador \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-137">**D3D11\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | <span data-ttu-id="91d9c-138">Describe una variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="91d9c-138">Describes a shader variable.</span></span><br/>                                |
| [<span data-ttu-id="91d9c-139">**\_Parámetro de firma D3D11 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="91d9c-139">**D3D11\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | <span data-ttu-id="91d9c-140">Describe una firma de sombreador.</span><span class="sxs-lookup"><span data-stu-id="91d9c-140">Describes a shader signature.</span></span><br/>                               |
| [<span data-ttu-id="91d9c-141">**\_Registro de seguimiento de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-141">**D3D11\_TRACE\_REGISTER**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | <span data-ttu-id="91d9c-142">Describe un registro de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="91d9c-142">Describes a trace register.</span></span><br/>                                 |
| [<span data-ttu-id="91d9c-143">**\_Estadísticas de seguimiento de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-143">**D3D11\_TRACE\_STATS**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | <span data-ttu-id="91d9c-144">Especifica las estadísticas de un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="91d9c-144">Specifies statistics about a trace.</span></span><br/>                         |
| [<span data-ttu-id="91d9c-145">**\_Paso de seguimiento de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-145">**D3D11\_TRACE\_STEP**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | <span data-ttu-id="91d9c-146">Describe un paso de seguimiento, que es una instrucción.</span><span class="sxs-lookup"><span data-stu-id="91d9c-146">Describes a trace step, which is an instruction.</span></span><br/>            |
| [<span data-ttu-id="91d9c-147">**\_Valor de seguimiento D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-147">**D3D11\_TRACE\_VALUE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | <span data-ttu-id="91d9c-148">Describe un valor de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="91d9c-148">Describes a trace value.</span></span><br/>                                    |
| [<span data-ttu-id="91d9c-149">**\_Descripción de \_ seguimiento del sombreador de VÉRTICEs D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="91d9c-149">**D3D11\_VERTEX\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | <span data-ttu-id="91d9c-150">Describe una instancia de un sombreador de vértices para realizar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="91d9c-150">Describes an instance of a vertex shader to trace.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="91d9c-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91d9c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91d9c-152">Referencia de los sombreadores</span><span class="sxs-lookup"><span data-stu-id="91d9c-152">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





