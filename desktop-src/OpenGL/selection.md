---
title: Número de selección
description: La selección devuelve el contenido actual de la pila de nombres, que es una matriz de nombres con valores enteros.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- modo de selección OpenGL
- selección llega a OpenGL
- registros de llamadas OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42c057014a4f5a1533e1f5c42683b93f08c31c287dc29f56ea797a5b360d545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776745"
---
# <a name="selection"></a>Número de selección

La selección devuelve el contenido actual de la pila de nombres, que es una matriz de nombres con valores enteros. Asigne los nombres y compile la pila de nombres en el código de modelado que especifica la geometría de los objetos que desea dibujar. A continuación, en el modo de selección, cada vez que una primitiva forma una intersección con el volumen de recorte, se produce una selección. El registro de llamadas, que se escribe en la matriz de selección que ha proporcionado [**con glSelectBuffer,**](glselectbuffer.md)contiene información sobre el contenido de la pila de nombres en el momento del impacto.

> [!Note]  
> Llame [**a glSelectBuffer**](glselectbuffer.md) antes de poner OpenGL en modo de selección [**con glRenderMode**](glrendermode.md). No se garantiza que se devuelva todo el contenido de la pila de nombres hasta que llame a **glRenderMode** para sacar OpenGL del modo de selección.

 

Manipule la pila de nombres [**con glInitNames,**](glinitnames.md) [**glLoadName,**](glloadname.md) [**glPushName**](glpushname.md)y [**glPopName.**](glpopname.md) También puede usar [**gluPickMatrix para**](glupickmatrix.md) la selección.

 

 




