---
description: Direct3D permite seleccionar un modo de sombreado a la vez.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Establecer el modo de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495316"
---
# <a name="setting-the-shading-mode-direct3d-9"></a>Establecer el modo de sombreado (Direct3D 9)

Direct3D permite seleccionar un modo de sombreado a la vez. De forma predeterminada, se selecciona sombreado Gouraud. En C++, puede cambiar el modo de sombreado llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) . Establezca el parámetro de *Estado* en D3DRS \_ SHADEMODE. El parámetro *State* debe establecerse en un miembro de la enumeración [**D3DSHADEMODE**](./d3dshademode.md) . En los siguientes ejemplos de código de ejemplo se muestra cómo se puede establecer el modo de sombreado actual de una aplicación Direct3D en modo de sombreado plano o Gouraud.


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

 

 
