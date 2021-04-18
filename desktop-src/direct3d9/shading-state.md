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
# <a name="shading-state-direct3d-9"></a>Estado de sombreado (Direct3D 9)

Direct3D admite el sombreado plano y Gouraud. El valor predeterminado es el sombreado Gouraud. Para controlar el modo de sombreado actual, la aplicación de C++ especifica un miembro del tipo enumerado [**D3DSHADEMODE**](./d3dshademode.md) para el \_ Estado de representación de D3DRS SHADEMODE.

En el ejemplo de código de C++ siguiente se muestra el proceso de establecer el estado de sombreado en el modo de sombreado plano.


```
// This code example assumes that d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface.
// Set the shading state.
d3dDevice->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 
