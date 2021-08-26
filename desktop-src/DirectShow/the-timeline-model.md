---
description: Modelo de escala de tiempo
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Modelo de escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e5eeb60dce31fa466a518476bb3da341a3d2fda4fdeaa47ca58a89a904dded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903824"
---
# <a name="the-timeline-model"></a>Modelo de escala de tiempo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Una *escala* de tiempo es un [objeto DirectShow Editing Services](directshow-editing-services.md) (DES) usa para representar un proyecto de edición de vídeo. Un proyecto de edición se inicia como una colección de clips de origen, tomados de archivos de vídeo, archivos de sonido o archivos de imagen. Una secuencia lineal de clips forma una *pista*. En DirectShow Editing Services (DES), el audio y el vídeo se colocan en pistas independientes.

Las pistas también se pueden capas. Varias pistas de audio se mezclan y pueden incluir efectos de audio, como atenuaciones o reverberación. Se usan varias pistas de vídeo para crear transiciones. Por ejemplo, puede crear un borrado de un clip a otro. Otro ejemplo es una clave de croma, en la que el fondo de un clip se delimita y se reemplaza por una pista diferente. (El previsión meteorológica delante de una imagen de satelite es un ejemplo de la clave de la escoba).

DES usa una estructura de árbol para representar una edición:

-   Los clips de audio y vídeo forman los nodos hoja u *objetos de* origen.
-   Una colección de orígenes con un tipo de medio uniforme (audio o vídeo) es una *pista*.
-   Una colección de pistas es una *composición*. Una composición se representa como la composición de todas las pistas que contiene. Las composiciones pueden contener otras composiciones, lo que permite la organización compleja de pistas.
-   Una colección de nivel superior de composiciones y pistas (todas que representan el mismo tipo de medio) es un *grupo*.
-   Un conjunto de uno o varios grupos forma una escala *de tiempo*. La escala de tiempo es el nodo raíz del árbol.

Una escala de tiempo debe contener al menos un grupo. Cada grupo representa una sola secuencia en la producción final. Un proyecto típico incluye un grupo de vídeo y un grupo de audio. Las composiciones son opcionales; existen para proporcionar más estructura si es necesario.

En la ilustración siguiente se muestran las relaciones de elementos primarios secundarios que son una escala de tiempo:

![estructura de nodo](images/timeline1.png)

A continuación se muestra una escala de tiempo como una secuencia temporal:

![ilustración de escala de tiempo](images/timeline2.png)

La flecha de la parte superior representa la dirección de la escala de tiempo, empezando por la hora cero. Dentro del grupo de vídeos, la pista 1 tiene una prioridad mayor que la pista 0. Los objetos de origen de la pista 1 ocultan los de la pista 0. Donde la pista 1 está vacía, la pista 0 "se muestra a través de". Como se mencionó anteriormente, las pistas de audio simplemente se mezclan entre sí.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con DirectShow Editing Services](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



