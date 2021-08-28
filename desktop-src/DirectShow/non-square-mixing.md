---
description: Combinación sin cuadrados
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Combinación sin cuadrados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4674891b7b9d44cb35522b6040723bc71436d677b10a4326d9f00a269ce3aff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102425"
---
# <a name="non-square-mixing"></a>Combinación sin cuadrados

Este tema se aplica a Windows XP Service Pack 2 o posterior.

Cuando VMR-9 combina dos o más flujos, hay dos puntos en los que puede producirse el escalado: cuando el mezclador compone los flujos de entrada y cuando el asignador-presentador representa la imagen compuesta.

![Operaciones de combinación de vmr](images/vmr-nonsquare-mixing.png)

Las versiones anteriores de VMR-9 com compuestos siempre las secuencias de entrada mediante una relación de aspecto de píxeles (PAR) cuadrada (1:1), incluso cuando solo había una sola secuencia de vídeo. Si el flujo de entrada tenía píxeles no cuadrados, esto produjo una operación de escalado innecesaria. El escalado debe evitarse tanto como sea posible, por supuesto, porque degrada la calidad final de la imagen.

A partir Windows XP Service Pack 2, VMR-9 admite dos maneras diferentes de evitar el problema del escalado doble:

-   Implemente un asignador-presentador personalizado y admita la [**interfaz IVMRSurfaceAllocatorEx9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9)
-   Use el modo de combinación sin cuadrados.

En esta sección se describe el modo de combinación sin cuadrados. Las aplicaciones pueden combinar ambas técnicas.

**Funcionamiento de la mezcla no cuadrada**

En el modo de combinación sin cuadrados, VMR-9 selecciona un flujo de entrada para que sea el tamaño de destino y par. El mezclador de VMR no escala el vídeo desde esa secuencia ni desde ninguna otra secuencia con el mismo tamaño de imagen y PAR. Secuencias con un tamaño o una relación de aspecto diferentes se escalan para que coincidan con el PAR de destino y se les ha escrito una letra para que se ajuste al tamaño final de la imagen de salida.

La elección de secuencias depende del modo de combinación actual:

-   El modo de combinación YUV está restringido a una secuencia de vídeo en el pin 0. (Los demás pines pueden tener secuencias de subtítulos o subpicture). Por lo tanto, VMR-9 siempre selecciona el pin 0 para el tamaño de la imagen de destino y par.
-   En el modo de combinación RGB, vmr selecciona la secuencia con el tamaño de imagen más grande. Si hay más de uno, selecciona el que tiene el orden Z más alto; y si todavía hay un empate, selecciona la secuencia con el número de pin más bajo.

**Ejemplos de operación**

**Ejemplo 1.** El flujo 0 es de 720 x 480 píxeles con una relación de aspecto de imagen de 16:9. El flujo 1 es de 640 x 480 píxeles con una relación de aspecto de imagen de 4:3.

En este ejemplo, la secuencia 0 tiene el tamaño de imagen más grande, por lo que vmr elige esta secuencia, independientemente del modo de combinación RGB o del modo de combinación YUB. El PAR es 32:27 (16:9 / 720:480), lo que significa que la imagen debe extenderse horizontalmente por esta proporción para generar la relación de aspecto de imagen 16:9 correcta.

Para que coincida con el PAR de destino, el mezclador de VMR escala el flujo 1 por la relación inversa (27:32), lo que da como resultado una imagen de 540 x 480. A continuación, las dos secuencias se composiciónn en una superficie. Para mostrar la imagen resultante correctamente, el presentador del asignador debe ajustar la imagen horizontalmente para ajustarse a la relación de aspecto de la imagen 16:9.

![ejemplo 1.](images/vmr-nonsquare-mixing2.png)

**Ejemplo 2.** El flujo 0 es de 720 x 480 píxeles con una relación de aspecto de imagen de 16:9. El flujo 1 es de 1024 x 768 píxeles con una relación de aspecto de imagen de 4:3.

Si VMR-9 usa el modo de combinación YUV, siempre selecciona el flujo 0. Por lo tanto, se extiende el flujo de 1 a 540 x 480 píxeles, para que coincida con el PAR de la secuencia 0.

Si VMR-9 usa el modo de combinación RGB, selecciona el flujo 1 como destino, ya que esa secuencia tiene el tamaño de imagen más grande. Extiende el flujo 0 a un tamaño de imagen de 1024 x 576 píxeles. Tenga en cuenta que, en este caso, la imagen compuesta tiene un PAR de 1:1, por lo que el asignador-presentador no tiene que corregir los píxeles que no son cuadrados. (Es posible que tenga que extender el vídeo para tener en cuenta el rectángulo de destino).

**Uso del modo de combinación sin cuadrados**

Se recomienda el modo de combinación sin cuadrados si se cumple alguna de las condiciones siguientes:

-   La aplicación nunca envía más de una secuencia de vídeo a VMR-9.
-   La aplicación representa archivos DVD, tv o ms-dvr. También debe usar el modo de combinación YUV en este caso, si el hardware gráfico lo admite.

Si la aplicación combina varias secuencias de vídeo que pueden tener diferentes tamaños de imagen o relaciones de aspecto de píxeles, se recomienda el modo de combinación cuadrada predeterminado.

Para configurar el modo de combinación sin cuadrados, se debe detener el gráfico de filtros y desconectar todos los pines de entrada en VMR-9. A continuación, [**llame a IVMR MixerControl9::Set MixingPrefs con**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) la marca MixerPref9 \_ NonSquare Mixing:


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> Si combina la marca MixerPref9 NonSquare Mixing con la marca \_ MIXERPref9 \_ ARAdjustXorY, VMR-9 omite la marca MIXERPref9 \_ ARAdjustXorY.

 

Si la aplicación usa un asignador-presentador personalizado con el modo de combinación sin cuadrados, tenga en cuenta que la imagen compuesta puede tener un PAR no cuadrado. El asignador-presentador debe escalar la imagen a un PAR cuadrado (1:1).

**Mapas de bits estáticos**

Si usa la interfaz [**IVMR MixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) para combinar un mapa de bits estático en el vídeo, debe considerar que el mapa de bits es una segunda secuencia de vídeo para fines del modo de combinación de VMR.

VmR trata el mapa de bits como que tiene el mismo PAR que el destino. No escala el mapa de bits para ajustarlo a la relación de aspecto de píxeles del destino. En la configuración predeterminada de VMR, el destino tiene un PAR 1:1, que coincide con la mayoría de los mapas de bits. En el modo de combinación no cuadrada, el destino podría tener píxeles no cuadrados. Para asegurarse de que el mapa de bits se muestra correctamente, la aplicación debe proporcionar una imagen cuyo PAR coincida con el PAR de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



