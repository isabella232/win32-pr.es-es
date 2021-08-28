---
description: Direct3D admite el sombreado plano y gouraud. El valor predeterminado es sombreado de Gouraud. Para controlar el modo de sombreado actual, la aplicación de C++ especifica un miembro del tipo enumerado D3DSHADEMODE para el estado de representación SHADEMODE de D3DRS. \_
ms.assetid: 0019b1b7-65f2-4009-8d0f-5a99cf32a410
title: Estado de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f28514fefbf39e75bd84a0ae56324fd859f0fd85fa4a25449e349ce592ab3b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727605"
---
# <a name="shading-state-direct3d-9"></a>Estado de sombreado (Direct3D 9)

Direct3D admite el sombreado plano y gouraud. El valor predeterminado es sombreado de Gouraud. Para controlar el modo de sombreado actual, la aplicación de C++ especifica un miembro del tipo enumerado [**D3DSHADEMODE**](./d3dshademode.md) para el estado de representación SHADEMODE de D3DRS. \_

En el siguiente ejemplo de código de C++ se muestra el proceso de establecer el estado de sombreado en modo de sombreado plano.


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 
