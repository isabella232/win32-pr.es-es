---
title: Primitivas y comandos
description: Primitivas y comandos
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitivos
- OpenGL, comandos
- primitivas OpenGL
- comandos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774995"
---
# <a name="primitives-and-commands"></a>Primitivas y comandos

OpenGL dibuja puntos *primitivos* , segmentos de línea o polygonssubject en varios modos seleccionables. Puede controlar los modos de forma independiente entre sí. Es decir, el establecimiento de un modo no afecta a si se establecen otros modos (aunque muchos modos pueden interactuar para determinar lo que acaba finalmente en el fotogramas). Para especificar primitivos, modos set y realizar otras operaciones de OpenGL, se emiten comandos en forma de llamadas a funciones.

Los primitivos se definen mediante un grupo de uno o más *vértices*. Un vértice define un punto, un punto de conexión de una línea o una esquina de un polígono con dos bordes. Los datos (que se componen de coordenadas de vértices, colores, normales, coordenadas de textura y marcas de borde) se asocian con un vértice, y cada vértice y sus datos asociados se procesan de forma independiente, en orden y de la misma manera. Las únicas excepciones a esta regla son los casos en los que el grupo de vértices se debe recortar para que una primitiva determinada quepa en una región especificada. En este caso, se pueden modificar los datos de vértice y crear nuevos vértices. El tipo de recorte depende de la primitiva que representa el grupo de vértices.

Los comandos siempre se procesan en el orden en que se reciben, aunque puede haber un retraso indeterminado antes de que un comando surta efecto. Esto significa que cada primitivo se dibuja completamente antes de que cualquier comando subsiguiente surta efecto. También significa que los comandos de consulta de estado devuelven datos coherentes con la ejecución completa de todos los comandos OpenGL emitidos anteriormente.

 

 




