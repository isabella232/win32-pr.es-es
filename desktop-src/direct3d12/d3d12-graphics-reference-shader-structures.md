---
title: Estructuras de sombreador (gráficos de Direct3D 12)
description: d3d12shader. h declara las siguientes estructuras, que se usan para crear y usar sombreadores.
ms.assetid: b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0
keywords:
- estructuras, sombreadores de Direct3D 12
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400d50c48b8b94fc9a59d8e48179aae43e14a4f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695828"
---
# <a name="shader-structures-direct3d-12-graphics"></a><span data-ttu-id="e1f81-104">Estructuras de sombreador (gráficos de Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="e1f81-104">Shader Structures (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="e1f81-105">d3d12shader. h declara las siguientes estructuras, que se usan para crear y usar sombreadores.</span><span class="sxs-lookup"><span data-stu-id="e1f81-105">d3d12shader.h declares the following structures, which are used to create and use shaders.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e1f81-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e1f81-106">In this section</span></span>



| <span data-ttu-id="e1f81-107">Tema</span><span class="sxs-lookup"><span data-stu-id="e1f81-107">Topic</span></span>                                                                                  | <span data-ttu-id="e1f81-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1f81-108">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="e1f81-109">**D3D12 \_ función \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e1f81-109">**D3D12\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_function_desc)<br/>                        | <span data-ttu-id="e1f81-110">Describe una función.</span><span class="sxs-lookup"><span data-stu-id="e1f81-110">Describes a function.</span></span> <br/>                                       |
| [<span data-ttu-id="e1f81-111">**Descripción de la \_ biblioteca D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e1f81-111">**D3D12\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc)<br/>                          | <span data-ttu-id="e1f81-112">Describe una biblioteca de.</span><span class="sxs-lookup"><span data-stu-id="e1f81-112">Describes a library.</span></span> <br/>                                        |
| [<span data-ttu-id="e1f81-113">**\_Parámetro D3D12 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e1f81-113">**D3D12\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc)<br/>                      | <span data-ttu-id="e1f81-114">Describe un parámetro de función.</span><span class="sxs-lookup"><span data-stu-id="e1f81-114">Describes a function parameter.</span></span> <br/>                             |
| [<span data-ttu-id="e1f81-115">**\_Desc. búfer del sombreador de D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e1f81-115">**D3D12\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_buffer_desc)<br/>             | <span data-ttu-id="e1f81-116">Describe un búfer de constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1f81-116">Describes a shader constant-buffer.</span></span> <br/>                         |
| [<span data-ttu-id="e1f81-117">**\_Descripción del sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e1f81-117">**D3D12\_SHADER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_desc)<br/>                            | <span data-ttu-id="e1f81-118">Describe un sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1f81-118">Describes a shader.</span></span> <br/>                                         |
| [<span data-ttu-id="e1f81-119">**\_DESC de enlace de entrada del sombreador D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e1f81-119">**D3D12\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc)<br/>    | <span data-ttu-id="e1f81-120">Describe cómo un recurso de sombreador se enlaza a una entrada de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1f81-120">Describes how a shader resource is bound to a shader input.</span></span> <br/> |
| [<span data-ttu-id="e1f81-121">**\_Tipo de sombreador D3D12 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e1f81-121">**D3D12\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_type_desc)<br/>                 | <span data-ttu-id="e1f81-122">Describe un tipo de variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1f81-122">Describes a shader-variable type.</span></span> <br/>                           |
| [<span data-ttu-id="e1f81-123">**D3D12 \_ variable de sombreador \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e1f81-123">**D3D12\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc)<br/>         | <span data-ttu-id="e1f81-124">Describe una variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1f81-124">Describes a shader variable.</span></span> <br/>                                |
| [<span data-ttu-id="e1f81-125">**\_Parámetro de firma D3D12 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="e1f81-125">**D3D12\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc)<br/> | <span data-ttu-id="e1f81-126">Describe una firma de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e1f81-126">Describes a shader signature.</span></span> <br/>                               |



 

## <a name="related-topics"></a><span data-ttu-id="e1f81-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1f81-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1f81-128">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e1f81-128">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="e1f81-129">Referencia de los sombreadores</span><span class="sxs-lookup"><span data-stu-id="e1f81-129">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





