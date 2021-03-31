---
description: Transiciones
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912881"
---
# <a name="transitions"></a>Transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Una transición es una forma de segue de una pista de vídeo a otra, con un efecto visual como un fundido o un barrido. En la ilustración siguiente se muestra una escala de tiempo con una transición:

![escala de tiempo con transición](images/timeline3.png)

El objeto de transición está en el seguimiento 1 y representa una transición de la pista 0 a la del seguimiento 1. Al inicio de la transición, el vídeo representado está completo de la pista 0 (origen A). Al final, el vídeo está por completo de la pista 1 (origen C). En, la salida pasa del origen a al origen C. Por ejemplo, en una transición de atenuación, un origen se atenúa progresivamente hasta el otro. El resultado final es esquematizados a lo largo de la parte inferior de la ilustración.

Las transiciones no se pueden superponer en el tiempo dentro de la misma pista, pero puede crear transiciones que se superpongan mediante el objeto de composición, como se describe en [composición y disposición en capas](composition-and-layering.md).

Una transición tiene una dirección. De forma predeterminada, se inicia a partir de la pista de menor prioridad (origen A, en el ejemplo anterior) y termina en la pista de prioridad más alta (origen C). Entre, el vídeo es una combinación de los dos orígenes. Sin embargo, puede especificar el comportamiento opuesto, tal como se muestra en la siguiente ilustración:

![ntrack con dos transiciones](images/fade.png)

En este caso, la primera transición de la pista 0 atenúa el seguimiento 1, que es el comportamiento predeterminado. La segunda transición vuelve de la pista 1 a la pista 0. Tenga en cuenta que ambas transiciones se encuentran en el seguimiento 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con servicios de edición de DirectShow](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Transiciones y efectos](transitions-and-effects.md)
</dt> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



