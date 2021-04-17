---
description: Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando una diferencia de z a cada uno de ellos.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Diferencia de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494926"
---
# <a name="depth-bias-direct3d-9"></a><span data-ttu-id="07935-103">Diferencia de profundidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="07935-103">Depth Bias (Direct3D 9)</span></span>

<span data-ttu-id="07935-104">Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando una diferencia de z a cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="07935-104">Polygons that are coplanar in your 3D space can be made to appear as if they are not coplanar by adding a z-bias to each one.</span></span> <span data-ttu-id="07935-105">Se trata de una técnica que se usa normalmente para asegurarse de que las sombras de una escena se muestran correctamente.</span><span class="sxs-lookup"><span data-stu-id="07935-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="07935-106">Por ejemplo, una sombra en un muro probablemente tendrá el mismo valor de profundidad que la pared.</span><span class="sxs-lookup"><span data-stu-id="07935-106">For instance, a shadow on a wall will likely have the same depth value as the wall does.</span></span> <span data-ttu-id="07935-107">Si representa primero la pared y después la sombra, es posible que la sombra no sea visible o que los artefactos de profundidad estén visibles.</span><span class="sxs-lookup"><span data-stu-id="07935-107">If you render the wall first and then the shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span> <span data-ttu-id="07935-108">Puede invertir el orden en que se representan los objetos coplanares con el fin de invertir el efecto, pero es probable que los artefactos de profundidad sigan siendo posibles.</span><span class="sxs-lookup"><span data-stu-id="07935-108">You can reverse the order in which you render the coplanar objects in hopes of reversing the effect, but depth artifacts are still likely.</span></span>

<span data-ttu-id="07935-109">Una aplicación puede ayudar a garantizar que los polígonos coplanoles se representen correctamente agregando una inclinación a los valores z que el sistema utiliza al representar los conjuntos de polígonos coplanares.</span><span class="sxs-lookup"><span data-stu-id="07935-109">An application can help ensure that coplanar polygons are rendered properly by adding a bias to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="07935-110">Para agregar una diferencia de z a un conjunto de polígonos, llame al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) justo antes de su representación, establezca el parámetro de *Estado* en \_ D3DRS DEPTHBIAS y el parámetro de *valor* en un valor Float adecuado (por ejemplo, un valor adecuado podría ser de-1,0 a 1,0); para pasar este valor a **SetRenderState**, también debe convertir el valor en un valor **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="07935-110">To add a z-bias to a set of polygons, call the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method just before rendering them, setting the *State* parameter to D3DRS\_DEPTHBIAS, and the *Value* parameter to a suitable float value (for example, a suitable value might be from -1.0 to 1.0); to pass this value to **SetRenderState**, you must also cast the value to a **DWORD**.</span></span> <span data-ttu-id="07935-111">Un valor de diferencia de z mayor aumenta la probabilidad de que los polígonos que se representan estén visibles cuando se muestren con otros polígonos coplanoles.</span><span class="sxs-lookup"><span data-stu-id="07935-111">A higher z-bias value increases the likelihood that the polygons you render will be visible when displayed with other coplanar polygons.</span></span>


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



<span data-ttu-id="07935-112">donde m es la pendiente de profundidad máxima del triángulo que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="07935-112">where m is the maximum depth slope of the triangle being rendered.</span></span>


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



<span data-ttu-id="07935-113">Las unidades de los \_ Estados de representación D3DRS DEPTHBIAS y D3DRS \_ SLOPESCALEDEPTHBIAS dependen de si está habilitado el almacenamiento en búfer de z o el almacenamiento en búfer de w.</span><span class="sxs-lookup"><span data-stu-id="07935-113">The units for the D3DRS\_DEPTHBIAS and D3DRS\_SLOPESCALEDEPTHBIAS render states depend on whether z-buffering or w-buffering is enabled.</span></span> <span data-ttu-id="07935-114">La aplicación debe proporcionar los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="07935-114">The application must provide suitable values.</span></span>

<span data-ttu-id="07935-115">La diferencia no se aplica a ningún primitivo de línea y punto.</span><span class="sxs-lookup"><span data-stu-id="07935-115">The bias is not applied to any line and point primitive.</span></span> <span data-ttu-id="07935-116">Sin embargo, esta diferencia debe aplicarse a los triángulos dibujados en el modo de trama de alambres.</span><span class="sxs-lookup"><span data-stu-id="07935-116">However, this bias needs to be applied to triangles drawn in wireframe mode.</span></span>


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a><span data-ttu-id="07935-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07935-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07935-118">Canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="07935-118">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
