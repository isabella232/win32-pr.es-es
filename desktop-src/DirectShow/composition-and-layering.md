---
description: Composición y disposición en capas
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composición y disposición en capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677076"
---
# <a name="composition-and-layering"></a>Composición y disposición en capas

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En una colección de pistas, la primera pista tiene la prioridad más baja (prioridad 0) y cada pista subsiguiente tiene una prioridad un nivel superior. En cada nivel de prioridad, los clips de origen de esa pista ocultan los clips de origen en las pistas situadas debajo, a menos que esa capa también contenga una transición. Por lo tanto, puede imaginar que DES realiza varios pasos cuando se representa.

En primer lugar, representa la pista 0. No hay nada "bajo" pista 0, por lo que las regiones vacías se representan como una imagen en negro sólido. Las transiciones de este nivel se producen entre la imagen negra y la pista 0, o viceversa. DES coloca la pista 1 encima de la pista 0, lo que genera cualquier transición entre las dos pistas. El resultado es el compuesto de las dos pistas. Después, coloca el seguimiento 2 en esta composición. Las transiciones en este nivel se producen entre el compuesto y el seguimiento 2. El proceso continúa hasta que se coloca la última pista (prioridad más alta).

Cuando varias pistas están compuestas juntas, se comportan como una sola pista (denominada pista virtual). El objeto de composición encapsula este comportamiento, lo que permite realizar transiciones complejas. Por ejemplo, un clip de vídeo puede borrarse en un segundo clip, mientras que el compuesto (ambos clips más el barrido) se atenúa hasta un tercer clip.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con servicios de edición de DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



