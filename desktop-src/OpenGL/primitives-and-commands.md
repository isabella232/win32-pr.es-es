---
title: Primitivas y comandos
description: Primitivas y comandos
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL,primitives
- OpenGL,commands
- primitives OpenGL
- comandos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362029"
---
# <a name="primitives-and-commands"></a>Primitivas y comandos

OpenGL dibuja puntos *primitivos, segmentos* de línea o polígonossujetivo a varios modos seleccionables. Puede controlar los modos de forma independiente entre sí. Es decir, establecer un modo no afecta a si se establecen otros modos (aunque muchos modos pueden interactuar para determinar qué termina finalmente en el búfer de fotogramas). Para especificar primitivas, establecer modos y realizar otras operaciones de OpenGL, se emiten comandos en forma de llamadas de función.

Los primitivos se definen mediante un grupo de uno o varios *vértices*. Un vértice define un punto, un punto de conexión de una línea o una esquina de un polígono donde se encuentran dos bordes. Los datos (que constan de coordenadas de vértice, colores, normales, coordenadas de textura y marcas de borde) se asocian a un vértice y cada vértice y sus datos asociados se procesan de forma independiente, en orden y de la misma manera. Las únicas excepciones a esta regla son los casos en los que se debe recortar el grupo de vértices para que una primitiva determinada se ajuste dentro de una región especificada. En este caso, se pueden modificar los datos de los vértices y crear nuevos vértices. El tipo de recorte depende del primitivo que representa el grupo de vértices.

Los comandos siempre se procesan en el orden en que se reciben, aunque puede haber un retraso indeterminado antes de que un comando suba efecto. Esto significa que cada primitivo se dibuja completamente antes de que cualquier comando posterior suba efecto. También significa que los comandos de consulta de estado devuelven datos coherentes con la ejecución completa de todos los comandos OpenGL emitidos previamente.

 

 




