---
description: Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando una diferencia de z a cada uno de ellos.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Diferencia de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494926"
---
# <a name="depth-bias-direct3d-9"></a>Diferencia de profundidad (Direct3D 9)

Los polígonos que se coplanan en el espacio 3D pueden crearse como si no fueran coplanares agregando una diferencia de z a cada uno de ellos. Se trata de una técnica que se usa normalmente para asegurarse de que las sombras de una escena se muestran correctamente. Por ejemplo, una sombra en un muro probablemente tendrá el mismo valor de profundidad que la pared. Si representa primero la pared y después la sombra, es posible que la sombra no sea visible o que los artefactos de profundidad estén visibles. Puede invertir el orden en que se representan los objetos coplanares con el fin de invertir el efecto, pero es probable que los artefactos de profundidad sigan siendo posibles.

Una aplicación puede ayudar a garantizar que los polígonos coplanoles se representen correctamente agregando una inclinación a los valores z que el sistema utiliza al representar los conjuntos de polígonos coplanares. Para agregar una diferencia de z a un conjunto de polígonos, llame al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) justo antes de su representación, establezca el parámetro de *Estado* en \_ D3DRS DEPTHBIAS y el parámetro de *valor* en un valor Float adecuado (por ejemplo, un valor adecuado podría ser de-1,0 a 1,0); para pasar este valor a **SetRenderState**, también debe convertir el valor en un valor **DWORD**. Un valor de diferencia de z mayor aumenta la probabilidad de que los polígonos que se representan estén visibles cuando se muestren con otros polígonos coplanoles.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



donde m es la pendiente de profundidad máxima del triángulo que se va a representar.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



Las unidades de los \_ Estados de representación D3DRS DEPTHBIAS y D3DRS \_ SLOPESCALEDEPTHBIAS dependen de si está habilitado el almacenamiento en búfer de z o el almacenamiento en búfer de w. La aplicación debe proporcionar los valores adecuados.

La diferencia no se aplica a ningún primitivo de línea y punto. Sin embargo, esta diferencia debe aplicarse a los triángulos dibujados en el modo de trama de alambres.


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 
