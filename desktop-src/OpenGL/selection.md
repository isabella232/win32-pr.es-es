---
title: Selección
description: Selection devuelve el contenido actual de la pila de nombres, que es una matriz de nombres con valores enteros.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- modo de selección OpenGL
- resultados de selección de OpenGL
- registros de aciertos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357271"
---
# <a name="selection"></a>Selección

Selection devuelve el contenido actual de la pila de nombres, que es una matriz de nombres con valores enteros. Asigne los nombres y compile la pila de nombres en el código de modelado que especifica la geometría de los objetos que desea dibujar. A continuación, en el modo de selección, cada vez que una primitiva intersecta con el volumen de clip, se produce una visita de selección. El registro de aciertos, que se escribe en la matriz de selección que ha proporcionado con [**glSelectBuffer**](glselectbuffer.md), contiene información sobre el contenido de la pila de nombres en el momento de la visita.

> [!Note]  
> Llame a [**glSelectBuffer**](glselectbuffer.md) antes de colocar OpenGL en el modo de selección con [**glRenderMode**](glrendermode.md). No se garantiza que el contenido completo de la pila de nombres se devuelva hasta que llame a **glRenderMode** para sacar el modo de selección de OpenGL.

 

Manipular la pila de nombres con [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)y [**glPopName**](glpopname.md). También puede usar [**gluPickMatrix**](glupickmatrix.md) para la selección.

 

 




