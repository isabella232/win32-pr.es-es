---
description: Los polígonos que son coplanares en el espacio 3D pueden aparecer como si no fuera coplanar agregando un sesgo z a cada uno.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Sesgo de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc99d606a561fd6f4eec412774ce53d9b5dd5e62c7f50b118a4e90a88664a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523820"
---
# <a name="depth-bias-direct3d-9"></a>Sesgo de profundidad (Direct3D 9)

Los polígonos que son coplanares en el espacio 3D pueden aparecer como si no fuera coplanar agregando un sesgo z a cada uno. Se trata de una técnica que se usa normalmente para asegurarse de que las sombras de una escena se muestran correctamente. Por ejemplo, una sombra en un muro probablemente tendrá el mismo valor de profundidad que la pared. Si primero representa la pared y, a continuación, la sombra, es posible que la sombra no esté visible o que los artefactos de profundidad sean visibles. Puede invertir el orden en el que se representan los objetos coplanares con la esperanza de revertir el efecto, pero los artefactos de profundidad siguen siendo probables.

Una aplicación puede ayudar a garantizar que los polígonos coplanares se representan correctamente agregando un sesgo a los valores z que usa el sistema al representar los conjuntos de polígonos coplanares. Para agregar un sesgo z a un conjunto de polígonos, llame al método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) justo antes de representarlos, estableciendo el parámetro *State* en D3DRS DEPTHBIAS y el parámetro Value en un valor float adecuado (por ejemplo, un valor adecuado podría ser de \_ -1.0 a 1.0); para pasar este valor a **SetRenderState**, también debe convertir el valor en **DWORD.**  Un valor z-bias mayor aumenta la probabilidad de que los polígonos que represente sean visibles cuando se muestren con otros polígonos coplanares.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



donde m es la pendiente de profundidad máxima del triángulo que se representa.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



Las unidades de los estados de representación D3DRS \_ DEPTHBIAS y D3DRS LADEDEPTHBIAS dependen de si el almacenamiento en búfer z o \_ w-buffering está habilitado. La aplicación debe proporcionar valores adecuados.

El sesgo no se aplica a ninguna línea y primitiva de punto. Sin embargo, este sesgo debe aplicarse a los triángulos dibujados en modo wireframe.


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

 

 
