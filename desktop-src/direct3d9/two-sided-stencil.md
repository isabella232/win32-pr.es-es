---
description: Los volúmenes de sombra se usan para dibujar sombras con el búfer de estarcido.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided Galería de símbolos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714772"
---
# <a name="two-sided-stencil-direct3d-9"></a>Two-Sided Galería de símbolos (Direct3D 9)

Los volúmenes de sombra se usan para dibujar sombras con el búfer de estarcido. La aplicación calcula los volúmenes de sombra convertidos por geometría occluding, mediante el cálculo de los bordes de la silueta y la extrusión de la luz en un conjunto de volúmenes 3D. A continuación, estos volúmenes se representan dos veces en el búfer de estarcido.

La primera representación dibuja polígonos hacia delante e incrementa los valores del búfer de estarcido. La segunda representación dibuja los polígonos hacia delante del volumen de instantáneas y disminuye los valores de búfer de la galería de símbolos. Normalmente, todos los valores incrementados y disminuidos se cancelan entre sí. Sin embargo, la escena ya se representó con geometría normal, lo que provoca que algunos píxeles no superen la prueba de búfer z mientras se representa el volumen de la instantánea. Los valores que quedan en el búfer de estarcido se corresponden con los píxeles que están en la sombra. El resto del contenido del búfer de la galería de símbolos se usa como máscara, para que la combinación de alfa sea una gran cantidad de color negro que abarque a la escena. Con el búfer de estarcido que actúa como máscara, el resultado es oscurecer los píxeles que se encuentran en las sombras.

Esto significa que la geometría de la sombra se dibuja dos veces por origen de la luz, por lo que se pone presión sobre el rendimiento de los vértices de la GPU. La característica de galería de símbolos de dos caras se ha diseñado para mitigar esta situación. En este enfoque, hay dos conjuntos de estado de la galería de símbolos (denominados a continuación), uno para cada uno de los triángulos orientados delante y otro para los triángulos de cara a la inversa. De este modo, solo se dibuja un único paso por volumen de instantánea, por luz.

Los cambios de la API se restringen a un nuevo conjunto de Estados de representación. El nuevo estado de representación D3DRS \_ dos \_ \_ StencilMODE se puede establecer en **true** o **false**. Es **false** de forma predeterminada, lo que significa que es el comportamiento actual (DirectX 8). Cuando se establece en **true** (solo funcionará si \_ se establece D3DSTENCILCAPS TWOSIDED), los siguientes Estados de representación solo se aplicarán a los triángulos orientados hacia delante (en el sentido de las agujas del reloj).



| Estado de representación        | Descripción                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ STENCILFAIL  | D3DSTENCILOP si se produce un error en la prueba de estarcido.                                                |
| D3DRS \_ STENCILZFAIL | D3DSTENCILOP si se supera la prueba de estarcido y se produce un error en la prueba z.                              |
| D3DRS \_ STENCILPASS  | D3DSTENCILOP si se superan las pruebas de estarcido y z.                                     |
| D3DRS \_ STENCILFUNC  | D3DCMPFUNC FN. La prueba de estarcido se supera si (((Ref & Mask) stencilfn (Galería de símbolos & máscara)) es true. |



 

Un nuevo conjunto de Estados de representación se aplica a los triángulos hacia delante (en sentido contrario a las agujas del reloj).



| Estado de representación             | Descripción                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCILFAIL  | D3DSTENCILOP si se produce un error en la prueba de estarcido.                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | D3DSTENCILOP si se supera la prueba de estarcido y se produce un error en la prueba z.                                    |
| D3DRS \_ CCW \_ STENCILPASS  | D3DSTENCILOP si se superan las pruebas de estarcido y z.                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | Función D3DCMPFUNC. La prueba de estarcido se supera si (((Ref & Mask) stencilfn (Galería de símbolos & máscara)) es true. |



 

Los Estados de representación de estarcido restantes siempre se aplican a los triángulos en el sentido de las agujas del reloj y en el sentido contrario

D3DRS \_ dos \_ \_ StencilMODE se omiten para las líneas y los sprites de punto, lo que significa que el comportamiento no se ha modificado desde DirectX 8. \_ \_ Se omiten los Estados de representación de la galería de símbolos CCW de D3DRS \* .

Un nuevo bit Cap indica si el dispositivo admite esta característica. Se espera que los controladores que no admiten esta característica omitan estos nuevos Estados de representación. Todos los demás bits de los extremos de la galería de símbolos se aplican a ambos modos de almacenamiento en búfer. Dado que dos \_ \_ galerías de símbolos están a la vez la capacidad de dibujar con D3DCULLMODE \_ None establecido, el controlador debe establecer el límite correspondiente si es compatible con este nuevo modo de estarcido. Los laboratorios de calidad de hardware (WHQL) de Microsoft Windows deberían aplicar esto.

Nuevos Estados de representación:


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



Nuevo Cap:


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Técnicas de búfer de estarcido](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
