---
title: Administrar modos y ejecución
description: Administrar modos y ejecución
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665626"
---
# <a name="managing-modes-and-execution"></a><span data-ttu-id="c43b0-104">Administrar modos y ejecución</span><span class="sxs-lookup"><span data-stu-id="c43b0-104">Managing Modes and Execution</span></span>

<span data-ttu-id="c43b0-105">El efecto de muchas funciones de OpenGL depende de si un modo determinado está en vigor.</span><span class="sxs-lookup"><span data-stu-id="c43b0-105">The effect of many OpenGL functions depends on whether a particular mode is in effect.</span></span> <span data-ttu-id="c43b0-106">Las funciones [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) establecen estos modos; [**glIsEnabled**](glisenabled.md) determina si se ha establecido un modo determinado.</span><span class="sxs-lookup"><span data-stu-id="c43b0-106">The [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions set such modes; [**glIsEnabled**](glisenabled.md) determines whether a particular mode is set.</span></span>

<span data-ttu-id="c43b0-107">Puede controlar la ejecución de funciones OpenGL emitidas previamente con [**glFinish**](glfinish.md), que obliga a que finalicen todas estas funciones, o [**glFlush**](glflush.md), lo que garantiza que todas estas funciones se completarán en un tiempo finito.</span><span class="sxs-lookup"><span data-stu-id="c43b0-107">You can control the execution of previously issued OpenGL functions with [**glFinish**](glfinish.md), which forces all such functions to finish, or [**glFlush**](glflush.md), which ensures that all such functions will be completed in a finite time.</span></span>

<span data-ttu-id="c43b0-108">En una implementación concreta de OpenGL, es posible que pueda controlar determinados comportamientos con sugerencias mediante [**glHint**](glhint.md).</span><span class="sxs-lookup"><span data-stu-id="c43b0-108">In a particular implementation of OpenGL, you may be able to control certain behaviors with hints by using [**glHint**](glhint.md).</span></span> <span data-ttu-id="c43b0-109">Estos comportamientos son la calidad de la interpolación de coordenadas de color y textura. la precisión de los cálculos de niebla; y la calidad de muestreo de los puntos, líneas o polígonos con suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="c43b0-109">Such behaviors are the quality of color and texture coordinate interpolation; the accuracy of fog calculations; and the sampling quality of antialiased points, lines, or polygons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c43b0-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c43b0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c43b0-111">Referencia de modos y ejecución</span><span class="sxs-lookup"><span data-stu-id="c43b0-111">Modes and Execution Reference</span></span>](modes-and-execution-reference.md)
</dt> </dl>

 

 




