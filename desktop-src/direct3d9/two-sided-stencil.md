---
description: Los volúmenes de sombra se usan para dibujar sombras con el búfer de galería de símbolos.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided galería de símbolos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bca0b960f96d1747b2b7ad51771276df2cfe1da1fa8ac9aa4d7c1ce8ea7c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290515"
---
# <a name="two-sided-stencil-direct3d-9"></a>Two-Sided galería de símbolos (Direct3D 9)

Los volúmenes de sombra se usan para dibujar sombras con el búfer de galería de símbolos. La aplicación calcula los volúmenes de sombra convertidos mediante la oclusión de la geometría, calculando los bordes de contorno y extruyéndolos de la luz en un conjunto de volúmenes 3D. Estos volúmenes se representan dos veces en el búfer de la galería de símbolos.

La primera representación dibuja polígonos orientados hacia delante e incrementa los valores de stencil-buffer. La segunda representación dibuja los polígonos orientados hacia atrás del volumen de sombra y disminuye los valores del búfer de galería de símbolos. Normalmente, todos los valores incrementados y decrementados se cancelan entre sí. Sin embargo, la escena ya se representó con geometría normal, lo que provocaba que algunos píxeles no se realizaran en la prueba del búfer z a medida que se representaba el volumen de sombras. Los valores que quedan en el búfer de la galería de símbolos corresponden a píxeles que están en la sombra. Estos contenidos restantes del búfer de galería de símbolos se usan como máscara para combinar alfamente un cuadrándular negro grande que abarca todo el contenido de la escena. Con el búfer de galería de símbolos que actúa como una máscara, el resultado es ocultar los píxeles que están en las sombras.

Esto significa que la geometría de sombra se dibuja dos veces por fuente de luz, lo que supone presión sobre el rendimiento de vértices de la GPU. La característica de galería de símbolos de dos lados se ha diseñado para mitigar esta situación. En este enfoque, hay dos conjuntos de estado de galería de símbolos (denominados a continuación), uno para los triángulos orientados hacia delante y el otro para los triángulos orientados hacia atrás. De este modo, solo se dibuja un solo paso por volumen de sombra, por luz.

Los cambios en la API están restringidos a un nuevo conjunto de estados de representación. El nuevo estado de representación D3DRS \_ Two \_ Sided \_ StencilMODE se puede establecer en **TRUE** o **FALSE.** Es **FALSE de** forma predeterminada, lo que significa el comportamiento actual (DirectX 8). Cuando se establece en **TRUE** (solo funcionará si D3DSTENCILCAPS TWOSIDED está establecido), los siguientes estados de representación solo se aplicarán a los triángulos frontales (en el sentido de las agujas del \_ reloj).



| Estado de representación        | Descripción                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ STENCINCIIL  | D3DSTENCICOHERENCIA que se debe hacer si se produce un error en la prueba de galería de símbolos.                                                |
| D3DRS \_ STENCILZFAIL | D3DSTENCILOP para hacer si se supera la prueba de galería de símbolos y se produce un error en la prueba z.                              |
| D3DRS \_ STENCILPASS  | D3DSTENCICOHERENCIA que se debe hacer si se supera la galería de símbolos y las pruebas z.                                     |
| D3DRS \_ STENCILFUNC  | D3DCMPFUNC fn. La prueba de galería de símbolos se supera si ((ref & mask) stencilfn (stencil & mask)) es true. |



 

Se aplica un nuevo conjunto de estados de representación a los triángulos orientados hacia atrás (en sentido contrario a las agujas del reloj).



| Estado de representación             | Descripción                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCIRNIL  | D3DSTENCICOHERENCIA que se debe hacer si se produce un error en la prueba de galería de símbolos.                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | D3DSTENCILOP para hacer si se supera la prueba de galería de símbolos y se produce un error en la prueba z.                                    |
| D3DRS \_ CCW \_ STENCILPASS  | D3DSTENCICOHERENCIA que se debe hacer si se supera la galería de símbolos y las pruebas z.                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | Función D3DCMPFUNC. La prueba de galería de símbolos se supera si ((ref & mask) stencilfn (stencil & mask)) es true. |



 

Los estados de representación de galería de símbolos restantes siempre se aplican a triángulos en el sentido de las agujas del reloj y en sentido contrario a las agujas del reloj.

D3DRS Two Sided StencilMODE se omite para las líneas y sprites de punto, lo que significa que el comportamiento no se modifica con \_ \_ respecto a \_ DirectX 8. Se omiten los estados de representación de D3DRS \_ CCW \_ STENCIL. \*

Un nuevo bit de límite indica si el dispositivo admite esta característica. Se espera que los controladores que no admiten esta característica ignoren estos nuevos estados de representación. Todos los demás bits de límite de galería de símbolos se aplican a ambos modos de almacenamiento en búfer de galería de símbolos. Dado que la galería de símbolos de dos lados implica la capacidad de dibujar con \_ \_ D3DCULLMODE NONE establecido, el controlador debe establecer el límite correspondiente si admite este nuevo modo de \_ galería de símbolos. Microsoft Windows Hardware Quality Labs (WHQL) debe aplicar esto.

Nuevos estados de representación:


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



Nuevo límite:


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de galería de símbolos](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
