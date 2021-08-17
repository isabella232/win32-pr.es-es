---
description: Alfa también se puede proporcionar en un material. Para habilitar el material alfa, establezca el estado de representación del material difuso para que el tiempo de ejecución use los componentes de color difuso de material en lugar de los componentes de color difuso de vértice.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Material Alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a70ed4a3f5bcaf38f4ace079af5b2e1804af0e24340e5004898c9ed26707d40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798982"
---
# <a name="material-alpha-direct3d-9"></a>Material Alfa (Direct3D 9)

Alfa también se puede proporcionar en un material. Para habilitar el material alfa, establezca el estado de representación del material difuso para que el tiempo de ejecución use los componentes de color difuso de material en lugar de los componentes de color difuso de vértice.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



Inicialice el material con un valor alfa y establezca el material antes de dibujarlo.


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 



