---
description: Modelo de escala de tiempo
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Modelo de escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569892"
---
# <a name="the-timeline-model"></a>Modelo de escala de tiempo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Una *escala de tiempo* es un objeto que los [servicios de edición de DirectShow](directshow-editing-services.md) (des) usan para representar un proyecto de edición de vídeo. Un proyecto de edición se inicia como una colección de clips de origen, tomada de archivos de vídeo, archivos de sonido o archivos de imagen fija. Una secuencia lineal de clips forma una *pista*. En los servicios de edición de DirectShow (DES), el audio y el vídeo se colocan en pistas independientes.

Las pistas también se pueden colocar en capas. Varias pistas de audio se mezclan juntas y pueden incluir efectos de audio, como fundidos o reverberación. Se usan varias pistas de vídeo para crear transiciones. Por ejemplo, puede crear un borrado de un clip a otro. Otro ejemplo es una clave cromada, en la que el fondo de un clip se codifica y se reemplaza por una pista diferente. (El Pronóstico meteorológico delante de una imagen satelite es un ejemplo de generación de claves de croma).

DES usa una estructura de árbol para representar una edición:

-   Los clips de audio y vídeo forman los nodos hoja, u objetos de *origen* .
-   Una colección de orígenes con un tipo de medio uniforme (audio o vídeo) es una *pista*.
-   Una colección de pistas es una *composición*. Una composición se representa como el compuesto de todas las pistas que contiene. Las composiciones pueden contener otras composiciones, lo que permite disposiciones complejas de pistas.
-   Una colección de nivel superior de composiciones y pistas (que representan el mismo tipo de medio) es un *Grupo*.
-   Un conjunto de uno o varios grupos forma una *escala de tiempo*. La escala de tiempo es el nodo raíz del árbol.

Una escala de tiempo debe contener al menos un grupo. Cada grupo representa un único flujo en la producción final. Un proyecto típico incluye un grupo de vídeos y un grupo de audio. Las composiciones son opcionales; existen para proporcionar más estructura si es necesario.

En la ilustración siguiente se muestran las relaciones de elementos primarios y secundarios que constituyen una escala de tiempo:

![estructura del nodo](images/timeline1.png)

A continuación se muestra una escala de tiempo como una secuencia temporal:

![Ilustración de la escala de tiempo](images/timeline2.png)

La flecha de la parte superior representa la dirección de la escala de tiempo, empezando por cero de la hora. Dentro del grupo de vídeos, el seguimiento 1 tiene una prioridad más alta que la pista 0. Los objetos de origen de Track 1 ocultan los de la pista 0. Donde Track 1 está vacío, Track 0 "se muestra a través de". Como se mencionó anteriormente, las pistas de audio se combinan simplemente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con servicios de edición de DirectShow](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



