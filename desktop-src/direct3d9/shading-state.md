---
description: Direct3D admite el sombreado plano y Gouraud. El valor predeterminado es el sombreado Gouraud. Para controlar el modo de sombreado actual, la aplicación de C++ especifica un miembro del tipo enumerado D3DSHADEMODE para el \_ Estado de representación de D3DRS SHADEMODE.
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Estado de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebac826704fee0e1903c1aa2a2348bff4a089c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714719"
---
# <a name="shading-state-direct3d-9"></a><span data-ttu-id="f949c-105">Estado de sombreado (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f949c-105">Shading State (Direct3D 9)</span></span>

<span data-ttu-id="f949c-106">Direct3D admite el sombreado plano y Gouraud.</span><span class="sxs-lookup"><span data-stu-id="f949c-106">Direct3D supports both flat and Gouraud shading.</span></span> <span data-ttu-id="f949c-107">El valor predeterminado es el sombreado Gouraud.</span><span class="sxs-lookup"><span data-stu-id="f949c-107">The default is Gouraud shading.</span></span> <span data-ttu-id="f949c-108">Para controlar el modo de sombreado actual, la aplicación de C++ especifica un miembro del tipo enumerado [**D3DSHADEMODE**](./d3dshademode.md) para el \_ Estado de representación de D3DRS SHADEMODE.</span><span class="sxs-lookup"><span data-stu-id="f949c-108">To control the current shading mode, your C++ application specifies a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type for the D3DRS\_SHADEMODE render state.</span></span>

<span data-ttu-id="f949c-109">En el ejemplo de código de C++ siguiente se muestra el proceso de establecer el estado de sombreado en el modo de sombreado plano.</span><span class="sxs-lookup"><span data-stu-id="f949c-109">The following C++ code example demonstrates the process of setting the shading state to flat shading mode.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a><span data-ttu-id="f949c-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f949c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f949c-111">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="f949c-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
