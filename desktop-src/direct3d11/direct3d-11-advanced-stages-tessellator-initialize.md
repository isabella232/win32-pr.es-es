---
title: Cómo inicializar la fase del teselador
description: En este tema se muestra cómo inicializar la fase del teselador.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cfe00a4d59396f0dc1b0157f84e57e9cabc4a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996737"
---
# <a name="how-to-initialize-the-tessellator-stage"></a><span data-ttu-id="74c11-103">Cómo: inicializar la fase del teselador</span><span class="sxs-lookup"><span data-stu-id="74c11-103">How To: Initialize the Tessellator Stage</span></span>

<span data-ttu-id="74c11-104">En general, la teselación expande el modelo compacto, definido por el usuario, de una revisión en geometría que contiene una cantidad de detalle programable.</span><span class="sxs-lookup"><span data-stu-id="74c11-104">In general, tessellation expands the compact, user-defined, model of a patch into geometry that contains a programmable amount of detail.</span></span> <span data-ttu-id="74c11-105">La geometría suele ser un conjunto de triángulos que representa la geometría detallada de la superficie.</span><span class="sxs-lookup"><span data-stu-id="74c11-105">The geometry is typically a set of triangles that represents detailed surface geometry.</span></span> <span data-ttu-id="74c11-106">En este tema se muestra cómo inicializar la fase del teselador.</span><span class="sxs-lookup"><span data-stu-id="74c11-106">This topic shows how to initialize the tessellator stage.</span></span>

<span data-ttu-id="74c11-107">La fase del teselador es la segunda de las tres fases que colaboran en dividirlas o en mosaico con una superficie.</span><span class="sxs-lookup"><span data-stu-id="74c11-107">The tessellator stage is the second of three stages that work together to tessellate or tile a surface.</span></span> <span data-ttu-id="74c11-108">La primera fase es la fase del sombreador de casco; funciona una vez por revisión y configura cómo se comporta la siguiente fase (la función del teselador).</span><span class="sxs-lookup"><span data-stu-id="74c11-108">The first stage is the hull-shader stage; it operates once per patch and configures how the next stage (the fixed function tessellator) behaves.</span></span> <span data-ttu-id="74c11-109">Un sombreador de casco también genera salidas definidas por el usuario como puntos de control de salida y constantes de revisión que se envían después del del teselador directamente a la tercera fase, la fase del sombreador del dominio.</span><span class="sxs-lookup"><span data-stu-id="74c11-109">A hull shader also generates user-defined outputs such as output-control points and patch constants that are sent past the tessellator directly to the third stage, the domain-shader stage.</span></span> <span data-ttu-id="74c11-110">Un sombreador de dominio se invoca una vez por punto de del teselador y evalúa las posiciones de la superficie.</span><span class="sxs-lookup"><span data-stu-id="74c11-110">A domain shader is invoked once per tessellator-stage point and evaluates surface positions.</span></span>

<span data-ttu-id="74c11-111">La fase del teselador es una fase de función fija, no hay ningún sombreador que generar y ningún Estado para establecer.</span><span class="sxs-lookup"><span data-stu-id="74c11-111">The tessellator stage is a fixed function stage, there is no shader to generate, and no state to set.</span></span> <span data-ttu-id="74c11-112">Recibe todo su estado de configuración de la fase del sombreador de casco; una vez inicializada la fase del sombreador de casco, la fase del teselador se inicializa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="74c11-112">It receives all of its setup state from the hull-shader stage; once the hull-shader stage has been initialized, the tessellator stage is automatically initialized.</span></span>

<span data-ttu-id="74c11-113">**Para inicializar la fase del teselador**</span><span class="sxs-lookup"><span data-stu-id="74c11-113">**To initialize the tessellator stage**</span></span>

-   <span data-ttu-id="74c11-114">Inicialice la fase del sombreador de casco mediante [**ID3D11DeviceContext:: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="74c11-114">Initialize the hull-shader stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    <span data-ttu-id="74c11-115">*ppClassInstances* es un puntero a una matriz de interfaces de sombreador, representada por punteros [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) y el número de interfaces, representado por *NumClassInstances*.</span><span class="sxs-lookup"><span data-stu-id="74c11-115">*ppClassInstances* is a pointer to an array of shader interfaces, represented by [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) pointers and the number of interfaces, represented by *NumClassInstances*.</span></span> <span data-ttu-id="74c11-116">Si no se usa, estos parámetros se pueden establecer en **null** y 0 respectivamente.</span><span class="sxs-lookup"><span data-stu-id="74c11-116">If not used, these parameters can be set to **NULL** and 0 respectively.</span></span>

<span data-ttu-id="74c11-117">Una vez inicializada la fase del sombreador de casco, debe inicializar también la fase del sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="74c11-117">After the hull-shader stage is initialized, you should also initialize the domain-shader stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74c11-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74c11-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74c11-119">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="74c11-119">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="74c11-120">Información general sobre teselación</span><span class="sxs-lookup"><span data-stu-id="74c11-120">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




