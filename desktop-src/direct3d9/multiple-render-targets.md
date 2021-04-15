---
description: Varios destinos de representación (MRT) hacen referencia a la capacidad de representar en varias superficies (vea IDirect3D9Surface) con una única llamada a Draw.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Varios destinos de representación (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495287"
---
# <a name="multiple-render-targets-direct3d-9"></a>Varios destinos de representación (Direct3D 9)

Varios destinos de representación (MRT) hacen referencia a la capacidad de representar en varias superficies (vea [**IDirect3D9Surface**](/windows/desktop/api)) con una única llamada a Draw. Estas superficies pueden crearse de forma independiente entre sí. Los destinos de representación se pueden establecer mediante [**IDirect3DDevice9:: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).

Varios destinos de representación tienen las siguientes restricciones:

-   Todas las superficies de destino de representación que se usan juntas deben tener la misma profundidad de bits, pero pueden tener distintos formatos, a menos que \_ se establezca el límite de MRTINDEPENDENTBITDEPTHS de D3DPMISCCAPS.
-   Todas las superficies de un destino de representación múltiple deben tener el mismo ancho y alto.
-   Algunas implementaciones no pueden realizar operaciones de sombreador de postpíxel en varios destinos de representación, entre los que se incluyen: sin interpolación, prueba alfa, sin vaho, sin fusión o enmascaramiento, excepto la prueba de la z y el estarcido. Los dispositivos que admiten operaciones de sombreador de postpíxel establecen el bit Cap en D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING.

    Cuando \_ se establece el límite de MRTPOSTPIXELSHADERBLENDING de D3DPMISCCAPS, primero debe consultar a [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con el \_ \_ \_ resultado de combinación de POSTPIXELSHADER de consulta de uso para el formato de superficie específico. Si es false, no habrá ninguna operación de fusión de sombreador de postpíxel disponible para ese formato de superficie específico. Si es true, se espera que el dispositivo aplique el mismo estado a todos los destinos de representación simultáneos de la siguiente manera:

    -   Alpha Blend: el valor de color de oCi se combina con el destino de representación iésimo.
    -   Prueba alfa: la comparación se realizará con oC0. Si se produce un error en la comparación, se finaliza la prueba de píxeles para todos los destinos de representación.
    -   Niebla: el destino de representación 0 se mostrará en la luneta trasera. Otros destinos de representación no están definidos. Las implementaciones pueden optar por la niebla de todos con el mismo estado.
    -   Interpolación: sin definir.

-   No se admite el suavizado de contorno.
-   Algunas de las implementaciones no aplican la máscara de escritura de salida (D3DRS \_ COLORWRITEENABLE). Las que pueden tener máscaras de escritura de color independientes. Esto se expresa mediante un nuevo bit de capacidad. El número de máscaras de escritura de color independientes disponibles será igual al número máximo de elementos que admite el dispositivo.

Nuevas Cap de hardware:


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de píxeles](pixel-pipeline.md)
</dt> </dl>

 

 
