---
description: Composición y capas
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Composición y capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b173ed0727869d3630a2241d7237cf74fb5143a907a95fcc53901a7b85f285c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954234"
---
# <a name="composition-and-layering"></a>Composición y capas

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En una colección de pistas, la primera pista tiene la prioridad más baja (prioridad 0) y cada pista subsiguiente tiene una prioridad un nivel superior. En cada nivel de prioridad, los clips de origen de esa pista ocultan los clips de origen en las pistas que hay debajo, a menos que esa capa también contenga una transición. Por lo tanto, puede imaginar que DES realiza varios pases cuando se representa.

En primer lugar, representa la pista 0. No hay nada "debajo" de la pista 0, por lo que las regiones vacías se representan como una imagen negra sólida. Las transiciones de esta capa se producen entre la imagen negra y el seguimiento 0 o viceversa. DES se encuentra la pista 1 sobre la pista 0, generando cualquier transición entre las dos pistas. El resultado es la composición de las dos pistas. A continuación, coloca el seguimiento 2 en esta composición. Las transiciones en esta capa se producen entre el compuesto y el seguimiento 2. El proceso continúa hasta que se pone en marcha la última pista (de prioridad más alta).

Cuando hay varias pistas compuestas juntas, se comportan como una sola pista (denominada pista virtual). El objeto de composición encapsula este comportamiento, lo que permite realizar transiciones complejas. Por ejemplo, un clip de vídeo puede borrarse a un segundo clip, mientras que el compuesto (ambos clips más el borrado) se atenua a un tercer clip.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con DirectShow Editing Services](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



