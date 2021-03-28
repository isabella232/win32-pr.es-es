---
title: Creación de un sombreador de casco
description: En este tema se muestra cómo crear un sombreador de casco.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773717"
---
# <a name="how-to-create-a-hull-shader"></a><span data-ttu-id="d0c0d-103">Cómo: crear un sombreador de casco</span><span class="sxs-lookup"><span data-stu-id="d0c0d-103">How To: Create a Hull Shader</span></span>

<span data-ttu-id="d0c0d-104">Un sombreador de casco es la primera de las tres fases que funcionan conjuntamente para implementar la [teselación](direct3d-11-advanced-stages-tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="d0c0d-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="d0c0d-105">La salida del sombreador de casco controla la fase de del teselador, así como la fase del sombreador del dominio.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-105">The hull-shader outputs drive the tessellator stage, as well as the domain-shader stage.</span></span> <span data-ttu-id="d0c0d-106">En este tema se muestra cómo crear un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-106">This topic shows how to create a hull shader.</span></span>

<span data-ttu-id="d0c0d-107">Un sombreador de casco transforma un conjunto de puntos de control de entrada (de un sombreador de vértices) en un conjunto de puntos de control de salida.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-107">A hull shader transforms a set of input control points (from a vertex shader) into a set of output control points.</span></span> <span data-ttu-id="d0c0d-108">El número de puntos de entrada y salida puede variar en el contenido y el número dependiendo de la transformación (una transformación típica sería una transformación de base).</span><span class="sxs-lookup"><span data-stu-id="d0c0d-108">The number of input and output points can vary in contents and number depending on the transform (a typical transformation would be a basis transformation).</span></span>

<span data-ttu-id="d0c0d-109">Un sombreador de casco también genera información de constantes de revisión, como factores de teselación, para un sombreador de dominio y del teselador.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-109">A hull shader also outputs patch constant information, such as tessellation factors, for a domain shader and the tessellator.</span></span> <span data-ttu-id="d0c0d-110">La fase del teselador de función fija usa los factores de teselación, así como otro estado declarado en un sombreador de casco para determinar cuánto dividirlas.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-110">The fixed-function tessellator stage uses the tessellation factors as well as other state declared in a hull shader to determine how much to tessellate.</span></span>

<span data-ttu-id="d0c0d-111">**Para crear un sombreador de casco**</span><span class="sxs-lookup"><span data-stu-id="d0c0d-111">**To create a hull shader**</span></span>

1.  <span data-ttu-id="d0c0d-112">Diseñar un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-112">Design a hull shader.</span></span> <span data-ttu-id="d0c0d-113">Vea [Cómo: diseñar un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="d0c0d-113">See [How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md).</span></span>
2.  <span data-ttu-id="d0c0d-114">Compilar el código del sombreador</span><span class="sxs-lookup"><span data-stu-id="d0c0d-114">Compile the shader code</span></span>
3.  <span data-ttu-id="d0c0d-115">Cree un objeto de sombreador de casco mediante [**ID3D11Device:: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span><span class="sxs-lookup"><span data-stu-id="d0c0d-115">Create a hull-shader object using [**ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span></span>
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  <span data-ttu-id="d0c0d-116">Inicialice la fase de canalización mediante [**ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="d0c0d-116">Initialize the pipeline stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="d0c0d-117">Un sombreador de dominio debe estar enlazado a la canalización si un sombreador de casco está enlazado.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-117">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="d0c0d-118">En concreto, no es válido transmitir directamente los puntos de control del sombreador de casco con el sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="d0c0d-118">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0c0d-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0c0d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0c0d-120">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d0c0d-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="d0c0d-121">Información general sobre teselación</span><span class="sxs-lookup"><span data-stu-id="d0c0d-121">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




