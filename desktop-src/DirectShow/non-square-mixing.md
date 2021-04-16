---
description: Combinación no cuadrada
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Combinación no cuadrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537690"
---
# <a name="non-square-mixing"></a>Combinación no cuadrada

Este tema se aplica a Windows XP Service Pack 2 o posterior.

Cuando VMR-9 mezcla dos o más secuencias, hay dos puntos en los que puede producirse el escalado: cuando el mezclador compone los flujos de entrada y cuando el asignador de representador representa la imagen compuesta.

![operaciones de combinación de VMR](images/vmr-nonsquare-mixing.png)

Las versiones anteriores de VMR-9 componen siempre los flujos de entrada con una relación de aspecto de píxeles cuadrada (1:1), incluso cuando solo había un flujo de vídeo. Si el flujo de entrada tuviera píxeles no cuadrados, esto provocó una operación de escala innecesaria. El escalado debe evitarse lo máximo posible, por supuesto, porque degrada la calidad final de la imagen.

A partir de Windows XP Service Pack 2, VMR-9 admite dos maneras diferentes de evitar el problema del doble escalado:

-   Implemente un asignador personalizado y admita la interfaz [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .
-   Use el modo de combinación no cuadrado.

En esta sección se describe el modo de combinación no cuadrado. Las aplicaciones pueden combinar ambas técnicas.

**Cómo funciona la combinación no cuadrada**

En el modo de mezcla no cuadrado, VMR-9 selecciona un flujo de entrada para que sea el tamaño y el PAR de destino. El mezclador de VMR no escala el vídeo desde esa secuencia ni desde ningún otro flujo con el mismo tamaño de imagen y PAR. Los flujos con un tamaño o relación de aspecto diferente se escalan para coincidir con el PAR de destino y se muestran en la panorámica para ajustarse al tamaño de la imagen de salida final.

La elección de los flujos depende del modo de mezcla actual:

-   El modo de mezcla YUV está restringido a un flujo de vídeo en el pin 0. (Los otros PIN pueden tener secuencias de subimagen o de subtítulos cerrados). Por lo tanto, VMR-9 selecciona siempre el pin 0 para el tamaño y el PAR de la imagen de destino.
-   En el modo de combinación RGB, VMR selecciona la secuencia con el tamaño de imagen más grande. Si hay más de uno, selecciona el que tiene el orden z más alto; y si sigue habiendo un empate, selecciona la secuencia con el número de PIN más bajo.

**Ejemplos de operación**

**Ejemplo 1.** El flujo 0 es 720 x 480 píxeles con una relación de aspecto de imagen de 16:9. La secuencia 1 es 640 x 480 píxeles con una relación de aspecto de imagen de 4:3.

En este ejemplo, la secuencia 0 tiene el tamaño de la imagen más grande, por lo que la VMR elige este flujo, independientemente del modo de mezcla de RGB o el modo de combinación de YUB. El PAR es 32:27 (16:9/720:480), lo que significa que la imagen se debe ajustar horizontalmente por esta relación para generar la relación de aspecto de la imagen 16:9 correcta.

Para que coincida con el PAR de destino, el mezclador VMR escala el flujo 1 por la relación inversa (27:32), lo que da como resultado una imagen de 540 x 480. Los dos flujos se componen en una superficie. Para mostrar la imagen resultante correctamente, el presentador del asignador debe expandir la imagen horizontalmente para ajustarse a la relación de aspecto de la imagen 16:9.

![ejemplo 1:](images/vmr-nonsquare-mixing2.png)

**Ejemplo 2.** El flujo 0 es 720 x 480 píxeles con una relación de aspecto de imagen de 16:9. La secuencia 1 es 1024 x 768 píxeles con una relación de aspecto de imagen de 4:3.

Si VMR-9 usa el modo de mezcla YUV, siempre selecciona el flujo 0. Por lo tanto, ajusta el flujo 1 a 540 x 480 píxeles para que coincida con el PAR de flujo 0.

Si VMR-9 usa el modo de combinación RGB, selecciona Stream 1 como destino, ya que ese flujo tiene el tamaño de imagen más grande. Ajusta el flujo 0 a un tamaño de imagen de 1024 x 576 píxeles. Tenga en cuenta que, en este caso, la imagen compuesta tiene un PAR de 1:1, por lo que el asignador-Presenter no tiene que corregirse para los píxeles no cuadrados. (Es posible que tenga que ajustar el vídeo para que tenga en cuenta el rectángulo de destino).

**Usar el modo de combinación no cuadrado**

Se recomienda el modo de mezcla no cuadrado si se cumple alguna de las siguientes condiciones:

-   La aplicación nunca envía más de una secuencia de vídeo a VMR-9.
-   La aplicación representa archivos de DVD, televisión o MS-DVR. También debe usar el modo de mezcla YUV en este caso, si el hardware de gráficos lo admite.

Si la aplicación mezcla varias secuencias de vídeo que pueden tener distintos tamaños de imagen o relaciones de aspecto de píxeles, se recomienda usar el modo de combinación de cuadrados predeterminado.

Para configurar el modo de mezcla no cuadrado, el gráfico de filtro debe detenerse y todos los pin de entrada se desconectarán en la VMR-9. Después, llame a [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con la \_ marca MixerPref9 NonSquareMixing:


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> Si combina la marca MixerPref9 \_ NonSquareMixing con la marca MixerPref9 \_ ARADJUSTXORY, VMR-9 omite la \_ marca MixerPref9 ARAdjustXorY.

 

Si la aplicación usa un asignador personalizado con el modo de mezcla sin cuadrado, tenga en cuenta que la imagen compuesta puede tener un PAR no cuadrado. Allocator-Presenter debe escalar la imagen a un PAR cuadrado (1:1).

**Mapas de bits estáticos**

Si usa la interfaz [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) para mezclar un mapa de bits estático en el vídeo, debe considerar que el mapa de bits es una segunda secuencia de vídeo para los fines del modo de mezcla de VMR.

VMR trata el mapa de bits con el mismo PAR que el destino. No escala el mapa de bits para ajustarse a la relación de aspecto de píxeles del destino. En la configuración predeterminada de VMR, el destino tiene un PAR de 1:1, que coincide con la mayoría de los mapas de bits. En el modo de mezcla no cuadrado, el destino puede tener píxeles no cuadrados. Para asegurarse de que el mapa de bits se muestre correctamente, la aplicación debe proporcionar una imagen cuyo PAR coincida con el PAR de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el modo de mezcla de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



