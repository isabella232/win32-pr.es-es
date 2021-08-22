---
title: Nombres de función OpenGL
description: Muchas funciones OpenGL son variaciones entre sí, que difieren principalmente en los tipos de datos de sus argumentos.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nombres de función
- nombres de función OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7729ca1f8a092c261a2ae87a835b51ea253ff2d09de710a830458c0825642bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936885"
---
# <a name="opengl-function-names"></a>Nombres de función OpenGL

Muchas funciones OpenGL son variaciones entre sí, que difieren principalmente en los tipos de datos de sus argumentos. Algunas funciones difieren en el número de argumentos relacionados y si esos argumentos se pueden especificar como vector o deben especificarse por separado en una lista. Por ejemplo, si usa la función **glVertex2f,** debe proporcionar coordenadas x e y como números de punto flotante de 32 bits. con **glVertex3sv**, debe proporcionar una matriz de tres valores enteros cortos (de 16 bits) para x, y y z. En los temas siguientes solo se usa el nombre base de la función. Un asterisco indica que puede haber más en el nombre real de la función que se muestra. Por ejemplo, [glVertex \*](glvertex-functions.md) representa todas las variaciones de la función que se usa para especificar vértices: **glVertex2d,** **glVertex2f,** **glVertex2i,** y así sucesivamente.

El efecto de una función OpenGL puede variar en función de si determinados modos están habilitados. Por ejemplo, debe habilitar la iluminación si las funciones relacionadas con la iluminación van a generar un objeto encendido correctamente. Para habilitar un modo determinado, use la función [**glEnable**](glenable.md) y proporcione la constante adecuada para identificar el modo (por ejemplo, GL \_ LIGHTING). Para deshabilitar un modo, use [**glDisable**](gldisable.md). Consulte **glEnable para** obtener una lista completa de los modos que se pueden habilitar.

 

 




