---
title: Cómo crear un sombreador de dominios
description: En este tema se muestra cómo crear un sombreador de dominios.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075247"
---
# <a name="how-to-create-a-domain-shader"></a><span data-ttu-id="38063-103">Cómo: crear un sombreador de dominios</span><span class="sxs-lookup"><span data-stu-id="38063-103">How To: Create a Domain Shader</span></span>

<span data-ttu-id="38063-104">Un sombreador de dominios es el tercero de tres fases que funcionan conjuntamente para implementar la [teselación](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="38063-104">A domain shader is the third of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="38063-105">Las entradas de la fase del sombreador de dominios proceden de un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="38063-105">The inputs for the domain-shader stage come from a hull shader.</span></span> <span data-ttu-id="38063-106">En este tema se muestra cómo crear un sombreador de dominios.</span><span class="sxs-lookup"><span data-stu-id="38063-106">This topic shows how to create a domain shader.</span></span>

<span data-ttu-id="38063-107">Un sombreador de dominio transforma la geometría de la superficie (creada por la fase del teselador de la función fija) mediante los puntos de control de salida del sombreador de casco, la revisión de salida del sombreador de casco-datos constantes y un único conjunto de coordenadas del teselador UV.</span><span class="sxs-lookup"><span data-stu-id="38063-107">A domain shader transforms surface geometry (created by the fixed-function tessellator stage) using hull shader output-control points, hull shader output patch-constant data, and a single set of tessellator uv coordinates.</span></span>

<span data-ttu-id="38063-108">**Para crear un sombreador de dominios**</span><span class="sxs-lookup"><span data-stu-id="38063-108">**To create a domain shader**</span></span>

1.  <span data-ttu-id="38063-109">Diseñar un sombreador de dominios.</span><span class="sxs-lookup"><span data-stu-id="38063-109">Design a domain shader.</span></span> <span data-ttu-id="38063-110">Vea [Cómo: diseñar un sombreador de dominios](direct3d-11-advanced-stages-domain-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="38063-110">See [How To: Design a Domain Shader](direct3d-11-advanced-stages-domain-shader-design.md).</span></span>
2.  <span data-ttu-id="38063-111">Compile el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="38063-111">Compile the shader code.</span></span>
3.  <span data-ttu-id="38063-112">Cree un objeto de sombreador de dominio mediante [**ID3D11Device:: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span><span class="sxs-lookup"><span data-stu-id="38063-112">Create a domain-shader object using [**ID3D11Device::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span></span>
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  <span data-ttu-id="38063-113">Inicialice la fase de canalización con [**ID3D11DeviceContext::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span><span class="sxs-lookup"><span data-stu-id="38063-113">Initialize the pipeline stage using [**ID3D11DeviceContext::DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span></span>
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="38063-114">Un sombreador de dominio debe estar enlazado a la canalización si un sombreador de casco está enlazado.</span><span class="sxs-lookup"><span data-stu-id="38063-114">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="38063-115">En concreto, no es válido transmitir directamente los puntos de control del sombreador de casco con el sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="38063-115">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38063-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38063-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38063-117">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="38063-117">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="38063-118">Información general sobre teselación</span><span class="sxs-lookup"><span data-stu-id="38063-118">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




