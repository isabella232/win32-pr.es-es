---
title: Nombres de funciones OpenGL
description: Muchas funciones de OpenGL son variaciones entre sí, que se diferencian principalmente en los tipos de datos de sus argumentos.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nombres de función
- nombres de función OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776141"
---
# <a name="opengl-function-names"></a>Nombres de funciones OpenGL

Muchas funciones de OpenGL son variaciones entre sí, que se diferencian principalmente en los tipos de datos de sus argumentos. Algunas funciones difieren en el número de argumentos relacionados y si esos argumentos se pueden especificar como vector o se deben especificar por separado en una lista. Por ejemplo, si usa la función **glVertex2f** , debe proporcionar coordenadas x e y como números de punto flotante de 32 bits; con **glVertex3sv**, debe proporcionar una matriz de tres valores enteros cortos (de 16 bits) para x, y y z. En los temas siguientes solo se usa el nombre base de la función. Un asterisco indica que puede haber más en el nombre de función real que el que se muestra. Por ejemplo, [glVertex \*](glvertex-functions.md) representa todas las variaciones de la función que se usan para especificar vértices: **glVertex2d**, **glVertex2f**, **glVertex2i**, etc.

El efecto de una función de OpenGL puede variar en función de si están habilitados determinados modos. Por ejemplo, debe habilitar la iluminación si las funciones relacionadas con la iluminación producen un objeto iluminado correctamente. Para habilitar un modo determinado, use la función [**glEnable**](glenable.md) y proporcione la constante adecuada para identificar el modo (por ejemplo, iluminación de GL \_ ). Para deshabilitar un modo, use [**glDisable**](gldisable.md). Consulte **glEnable** para obtener una lista completa de los modos que se pueden habilitar.

 

 




