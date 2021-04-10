---
description: Alfa también puede proporcionarse en un material. Para habilitar el contenido alfa, establezca el estado de representación de material difuso de modo que el tiempo de ejecución use los componentes de color difusos de material en lugar de los componentes de color difusos de vértices.
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: Material alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151942"
---
# <a name="material-alpha-direct3d-9"></a>Material alfa (Direct3D 9)

Alfa también puede proporcionarse en un material. Para habilitar el contenido alfa, establezca el estado de representación de material difuso de modo que el tiempo de ejecución use los componentes de color difusos de material en lugar de los componentes de color difusos de vértices.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



Inicialice el material con un valor alfa y establezca el material antes del dibujo.


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación alfa](alpha-blending.md)
</dt> </dl>

 

 



