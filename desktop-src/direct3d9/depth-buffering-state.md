---
description: El almacenamiento en búfer de profundidad es un método para quitar líneas y superficies ocultas. De forma predeterminada, Direct3D no usa el almacenamiento en búfer de profundidad.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: Estado de almacenamiento en búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d6d0494511c7fc0434d97988152426eb888d6c3044de4e2359ac2cb41110ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988324"
---
# <a name="depth-buffering-state-direct3d-9"></a>Estado de almacenamiento en búfer de profundidad (Direct3D 9)

El almacenamiento en búfer de profundidad es un método para quitar líneas y superficies ocultas. De forma predeterminada, Direct3D no usa el almacenamiento en búfer de profundidad.

Para obtener información general conceptual de los búferes de profundidad, vea [Búferes de profundidad (Direct3D 9).](depth-buffers.md)

Las aplicaciones de C++ actualizan el estado de almacenamiento en búfer de profundidad con el estado de representación D3DRS ZENABLE, mediante un miembro de la enumeración \_ [**D3BUFFERTYPE**](./d3dzbuffertype.md) para especificar el nuevo valor de estado.

Si la aplicación necesita evitar que Direct3D escriba en el búfer de profundidad, puede usar el valor enumerado D3DRS ZWRITEENABLE, especificando D3DDEVICE FALSE como segundo parámetro para la llamada a \_ \_ [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

En el ejemplo de código siguiente se muestra cómo se establece el estado del búfer de profundidad para habilitar el almacenamiento en búfer z.


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



La aplicación también puede usar el estado de representación D3DRS AHORAUNC para controlar la función de comparación que usa Direct3D al realizar el almacenamiento \_ en búfer de profundidad.

El sesgo Z es un método para mostrar una superficie delante de otra, incluso si sus valores de profundidad son los mismos. Puede usar esta técnica para diversos efectos. Un ejemplo común es la representación de sombras en las paredes. Tanto la sombra como la pared tienen el mismo valor de profundidad. Sin embargo, quiere que la aplicación muestre la sombra en la pared. Si se da un sesgo z a la sombra, Direct3D las muestra correctamente (consulte D3DRS \_ DEPTHBIAS).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 
