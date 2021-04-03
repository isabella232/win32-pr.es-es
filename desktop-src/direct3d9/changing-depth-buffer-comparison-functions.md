---
description: De forma predeterminada, cuando se realiza la prueba de profundidad en una superficie de representación, el sistema Direct3D actualiza la superficie de representación y destino si el valor de profundidad correspondiente (z o w) de cada punto es menor que el valor del búfer de profundidad.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Cambiar las funciones de comparación de búfer de profundidad (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807946"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a><span data-ttu-id="ce57b-103">Cambiar las funciones de comparación de búfer de profundidad (D3D9)</span><span class="sxs-lookup"><span data-stu-id="ce57b-103">Changing Depth Buffer Comparison Functions (D3D9)</span></span>

<span data-ttu-id="ce57b-104">De forma predeterminada, cuando se realiza la prueba de profundidad en una superficie de representación, el sistema Direct3D actualiza la superficie de representación y destino si el valor de profundidad correspondiente (z o w) de cada punto es menor que el valor del búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="ce57b-104">By default, when depth-testing is performed on a rendering surface, the Direct3D system updates the render-target surface if the corresponding depth value (z or w) for each point is less than the value in the depth buffer.</span></span> <span data-ttu-id="ce57b-105">En una aplicación de C++, se cambia el modo en que el sistema realiza comparaciones en valores de profundidad llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) con el parámetro de *Estado* establecido en D3DRS \_ ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="ce57b-105">In a C++ application, you change how the system performs comparisons on depth values by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method with the *State* parameter set to D3DRS\_ZFUNC.</span></span> <span data-ttu-id="ce57b-106">El parámetro *Value* debe establecerse en un valor en el tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="ce57b-106">The *Value* parameter should be set to a value in the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce57b-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce57b-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce57b-108">Búferes de profundidad</span><span class="sxs-lookup"><span data-stu-id="ce57b-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
