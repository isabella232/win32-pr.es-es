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
# <a name="selection"></a><span data-ttu-id="4fed5-106">Selección</span><span class="sxs-lookup"><span data-stu-id="4fed5-106">Selection</span></span>

<span data-ttu-id="4fed5-107">Selection devuelve el contenido actual de la pila de nombres, que es una matriz de nombres con valores enteros.</span><span class="sxs-lookup"><span data-stu-id="4fed5-107">Selection returns the current contents of the name stack, which is an array of names with integer values.</span></span> <span data-ttu-id="4fed5-108">Asigne los nombres y compile la pila de nombres en el código de modelado que especifica la geometría de los objetos que desea dibujar.</span><span class="sxs-lookup"><span data-stu-id="4fed5-108">You assign the names and build the name stack within the modeling code that specifies the geometry of objects you want to draw.</span></span> <span data-ttu-id="4fed5-109">A continuación, en el modo de selección, cada vez que una primitiva intersecta con el volumen de clip, se produce una visita de selección.</span><span class="sxs-lookup"><span data-stu-id="4fed5-109">Then, in selection mode, whenever a primitive intersects the clip volume, a selection hit occurs.</span></span> <span data-ttu-id="4fed5-110">El registro de aciertos, que se escribe en la matriz de selección que ha proporcionado con [**glSelectBuffer**](glselectbuffer.md), contiene información sobre el contenido de la pila de nombres en el momento de la visita.</span><span class="sxs-lookup"><span data-stu-id="4fed5-110">The hit record, which is written into the selection array you've supplied with [**glSelectBuffer**](glselectbuffer.md), contains information about the contents of the name stack at the time of the hit.</span></span>

> [!Note]  
> <span data-ttu-id="4fed5-111">Llame a [**glSelectBuffer**](glselectbuffer.md) antes de colocar OpenGL en el modo de selección con [**glRenderMode**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="4fed5-111">Call [**glSelectBuffer**](glselectbuffer.md) before you put OpenGL into selection mode with [**glRenderMode**](glrendermode.md).</span></span> <span data-ttu-id="4fed5-112">No se garantiza que el contenido completo de la pila de nombres se devuelva hasta que llame a **glRenderMode** para sacar el modo de selección de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4fed5-112">The entire contents of the name stack aren't guaranteed to be returned until you call **glRenderMode** to take OpenGL out of selection mode.</span></span>

 

<span data-ttu-id="4fed5-113">Manipular la pila de nombres con [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)y [**glPopName**](glpopname.md).</span><span class="sxs-lookup"><span data-stu-id="4fed5-113">Manipulate the name stack with [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md), and [**glPopName**](glpopname.md).</span></span> <span data-ttu-id="4fed5-114">También puede usar [**gluPickMatrix**](glupickmatrix.md) para la selección.</span><span class="sxs-lookup"><span data-stu-id="4fed5-114">You can also use [**gluPickMatrix**](glupickmatrix.md) for selection.</span></span>

 

 




