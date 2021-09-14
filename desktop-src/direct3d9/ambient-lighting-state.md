---
description: La luz ambiental es la luz circundante que se emite desde todas las direcciones. Para obtener información sobre cómo Direct3D usa la luz ambiental, vea Matemáticas de iluminación (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Estado de iluminación ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bd604941961f5b4abdb301d5c23efba9980791
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060786"
---
# <a name="ambient-lighting-state-direct3d-9"></a>Estado de iluminación ambiente (Direct3D 9)

La luz ambiental es la luz circundante que se emite desde todas las direcciones. Para obtener información sobre cómo Direct3D usa la luz ambiental, vea Matemáticas de iluminación [(Direct3D 9).](mathematics-of-lighting.md)

Una aplicación de C++ establece el color de la iluminación ambiente invocando el método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) y pasando el valor enumerado D3DRS AMBIENT como primer \_ parámetro. El segundo parámetro es un valor de color. El valor predeterminado es cero.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 
