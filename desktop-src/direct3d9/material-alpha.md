---
description: Alfa también puede proporcionarse en un material. Para habilitar el contenido alfa, establezca el estado de representación de material difuso de modo que el tiempo de ejecución use los componentes de color difusos de material en lugar de los componentes de color difusos de vértices.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Material alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151942"
---
# <a name="material-alpha-direct3d-9"></a><span data-ttu-id="e15fa-104">Material alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e15fa-104">Material Alpha (Direct3D 9)</span></span>

<span data-ttu-id="e15fa-105">Alfa también puede proporcionarse en un material.</span><span class="sxs-lookup"><span data-stu-id="e15fa-105">Alpha can also be supplied in a material.</span></span> <span data-ttu-id="e15fa-106">Para habilitar el contenido alfa, establezca el estado de representación de material difuso de modo que el tiempo de ejecución use los componentes de color difusos de material en lugar de los componentes de color difusos de vértices.</span><span class="sxs-lookup"><span data-stu-id="e15fa-106">To enable material alpha, set the diffuse material render state so that the runtime will use the material diffuse color components rather than the vertex diffuse color components.</span></span>


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



<span data-ttu-id="e15fa-107">Inicialice el material con un valor alfa y establezca el material antes del dibujo.</span><span class="sxs-lookup"><span data-stu-id="e15fa-107">Initialize the material with an alpha value, and set the material before drawing.</span></span>


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a><span data-ttu-id="e15fa-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e15fa-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e15fa-109">Combinación alfa</span><span class="sxs-lookup"><span data-stu-id="e15fa-109">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



