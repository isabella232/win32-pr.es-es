---
description: Direct3D permite seleccionar un modo de sombreado a la vez.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Establecer el modo de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769908513d4388fafae73f5a6788aef37c3ac9456a00f2e3280c57e04c18b462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068965"
---
# <a name="setting-the-shading-mode-direct3d-9"></a>Establecer el modo de sombreado (Direct3D 9)

Direct3D permite seleccionar un modo de sombreado a la vez. De forma predeterminada, el sombreado de Gouraud está seleccionado. En C++, puede cambiar el modo de sombreado llamando al método [**IDirect3DDevice9::SetRenderState.**](/windows/desktop/api) Establezca el *parámetro State* en D3DRS \_ SHADEMODE. El *parámetro State* debe establecerse en un miembro de la [**enumeración D3DSHADEMODE.**](./d3dshademode.md) En los ejemplos de código de ejemplo siguientes se muestra cómo se puede establecer el modo de sombreado actual de una aplicación Direct3D en modo plano o en modo de sombreado de Gouraud.


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreado](shading.md)
</dt> </dl>

 

 
