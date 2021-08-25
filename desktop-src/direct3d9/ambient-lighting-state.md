---
description: La luz ambiente es la luz circundante que se emite desde todas las direcciones. Para obtener información sobre cómo Direct3D usa la luz ambiente, vea Matemáticas de iluminación (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Estado de iluminación ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc32a6ec654bd30627c853bc00c90e94b6008e769fb3aa708e963a9430e0dc85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952695"
---
# <a name="ambient-lighting-state-direct3d-9"></a>Estado de iluminación ambiente (Direct3D 9)

La luz ambiente es la luz circundante que se emite desde todas las direcciones. Para obtener información sobre cómo Direct3D usa la luz ambiente, vea Matemáticas de iluminación [(Direct3D 9).](mathematics-of-lighting.md)

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

 

 
