---
title: Colocar y mover rectángulos de vídeo en el espacio de composición
description: Colocar y mover rectángulos de vídeo en el espacio de composición
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677111"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Colocar y mover rectángulos de vídeo en el espacio de composición

Cuando el VMR mezcla varios flujos de entrada, coloca cada flujo dentro de un rectángulo normalizado, denominado "espacio de composición". Dentro del espacio de composición, las coordenadas (0,0, 0,0) a (1,0, 1,0) forman el rectángulo de vídeo visible. Se recortan las coordenadas que se encuentran fuera de este rectángulo.

Una aplicación puede realizar efectos especiales con mover, ajustar y reducir el vídeo de un flujo de entrada, cambiando el rectángulo de destino en el espacio de composición de esa secuencia. Si el rectángulo especificado tiene un tamaño diferente que el del rectángulo de vídeo nativo, el vídeo nativo se reducirá o se ajustará para ajustarse. El rectángulo de destino se especifica mediante una llamada al método [**IVMRMixerControl:: SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) .

Por ejemplo, supongamos que el flujo 0 (que corresponde a la patilla 0) contiene la secuencia de vídeo principal y que el flujo 1 (que corresponde a la patilla 1) contiene un vídeo secundario. El flujo 1 se puede colocar completamente fuera de la cadena especificando un rectángulo normalizado de {-1,0 f, 0.0 f, 0.0 f, 1.0 f}. A continuación, el flujo 1 se puede pasar al área visible modificando los lados izquierdo y derecho del rectángulo en las sucesivas llamadas a **SetOutputRect**:



|        |                             |
|--------|-----------------------------|
| Hora   | Rectángulo                   |
| t + 0  | {-1,0 f, 0.0 f, 0.0 f, 1,0 f} |
| t + 1  | {-0.9 f, 0.0 f, 0.1 f, 1,0 f} |
| t + 2  | {-0,8 f, 0.0 f, 0,2 f, 1,0 f} |
| ...    | ...                         |
| t + 10 | {0.0 f, 0.0 f, 1.0 f, 1.0 f}  |



 

![mover una secuencia de vídeo en el espacio de composición](images/composition-space.png)

En el momento t + 10, el vídeo de la secuencia 1 está completamente visible. En este ejemplo, el tamaño nativo de la secuencia 1 se mantuvo mientras se estaba moviendo. También puede ampliar o reducir el rectángulo para producir efectos interesantes. También puede voltear el vídeo verticalmente; para ello, especifique un valor mayor en la parte superior a la parte inferior, o bien refleje el vídeo horizontalmente; para ello, especifique un valor mayor para el lado izquierdo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el modo de mezcla de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



