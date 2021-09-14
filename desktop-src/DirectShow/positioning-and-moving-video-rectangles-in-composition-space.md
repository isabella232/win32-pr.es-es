---
title: Posición y movimiento de rectángulos de vídeo en el espacio de composición
description: Colocar y mover rectángulos de vídeo en el espacio de composición
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254223"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Posición y movimiento de rectángulos de vídeo en el espacio de composición

Cuando vmr mezcla varios flujos de entrada, coloca cada secuencia dentro de un rectángulo normalizado, denominado "espacio de composición". Dentro del espacio de composición, las coordenadas (0.0, 0.0) a (1.0, 1.0) forman el rectángulo de vídeo visible. Las coordenadas que se encuentran fuera de este rectángulo se recortan.

Una aplicación puede realizar efectos especiales al mover, extender y reducir el vídeo de un flujo de entrada, cambiando el rectángulo de destino en el espacio de composición de esa secuencia. Si el rectángulo especificado tiene un tamaño diferente al del rectángulo de vídeo nativo, el vídeo nativo se verá reducido o se ajustará para ajustarse. El rectángulo de destino se especifica mediante una llamada al [**método IVMRMixerControl::SetOutputRect.**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs)

Por ejemplo, suponga que la secuencia 0 (que corresponde a la patilla 0) contiene la secuencia de vídeo principal y la secuencia 1 (que corresponde al pin 1) contiene un vídeo secundario. La secuencia 1 se puede colocar completamente fuera de pantalla especificando un rectángulo normalizado de { -1.0f, 0.0f, 0.0f, 1.0f }. A continuación, el flujo 1 se puede mover al área visible modificando los lados izquierdo y derecho del rectángulo en llamadas sucesivas a **SetOutputRect**:



| Etiqueta | Value |
|--------|-----------------------------|
| Hora   | Rectángulo                   |
| t + 0  | { -1.0f, 0.0f, 0.0f, 1.0f } |
| t + 1  | { -0.9f, 0.0f, 0.1f, 1.0f } |
| t + 2  | { -0.8f, 0.0f, 0.2f, 1.0f } |
| ...    | ...                         |
| t + 10 | { 0.0f, 0.0f, 1.0f, 1.0f }  |



 

![mover una secuencia de vídeo en el espacio de composición](images/composition-space.png)

En el momento t+10, el vídeo de la secuencia 1 es completamente visible. En este ejemplo, el tamaño nativo de la secuencia 1 se mantiene mientras se movía. También puede extender o reducir el rectángulo para producir efectos interesantes. También puede voltear el vídeo verticalmente, especificando un valor mayor para la parte superior que la parte inferior, o reflejar el vídeo horizontalmente, especificando un valor mayor para la izquierda que para la derecha.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



