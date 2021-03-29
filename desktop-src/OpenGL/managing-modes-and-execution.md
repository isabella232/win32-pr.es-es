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
# <a name="managing-modes-and-execution"></a>Administrar modos y ejecución

El efecto de muchas funciones de OpenGL depende de si un modo determinado está en vigor. Las funciones [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) establecen estos modos; [**glIsEnabled**](glisenabled.md) determina si se ha establecido un modo determinado.

Puede controlar la ejecución de funciones OpenGL emitidas previamente con [**glFinish**](glfinish.md), que obliga a que finalicen todas estas funciones, o [**glFlush**](glflush.md), lo que garantiza que todas estas funciones se completarán en un tiempo finito.

En una implementación concreta de OpenGL, es posible que pueda controlar determinados comportamientos con sugerencias mediante [**glHint**](glhint.md). Estos comportamientos son la calidad de la interpolación de coordenadas de color y textura. la precisión de los cálculos de niebla; y la calidad de muestreo de los puntos, líneas o polígonos con suavizado de contorno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de modos y ejecución](modes-and-execution-reference.md)
</dt> </dl>

 

 




