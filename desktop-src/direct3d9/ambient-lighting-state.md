---
description: La luz ambiente está rodeando la luz que irradia desde todas las direcciones. Para obtener información sobre cómo Direct3D usa la luz ambiente, vea matemáticas de iluminación (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Estado de iluminación ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bd604941961f5b4abdb301d5c23efba9980791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153305"
---
# <a name="ambient-lighting-state-direct3d-9"></a><span data-ttu-id="3a900-104">Estado de iluminación ambiente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3a900-104">Ambient Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="3a900-105">La luz ambiente está rodeando la luz que irradia desde todas las direcciones.</span><span class="sxs-lookup"><span data-stu-id="3a900-105">Ambient light is surrounding light that radiates from all directions.</span></span> <span data-ttu-id="3a900-106">Para obtener información sobre cómo Direct3D usa la luz ambiente, vea [matemáticas de iluminación (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="3a900-106">For information about how Direct3D uses ambient light, see [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="3a900-107">Una aplicación de C++ establece el color de la iluminación ambiente invocando el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y pasando el valor enumerado D3DRS \_ ambiente como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="3a900-107">A C++ application sets the color of ambient lighting by invoking the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and passing the enumerated value D3DRS\_AMBIENT as the first parameter.</span></span> <span data-ttu-id="3a900-108">El segundo parámetro es un valor de color.</span><span class="sxs-lookup"><span data-stu-id="3a900-108">The second parameter is a color value.</span></span> <span data-ttu-id="3a900-109">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="3a900-109">The default value is zero.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a><span data-ttu-id="3a900-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a900-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a900-111">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="3a900-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
