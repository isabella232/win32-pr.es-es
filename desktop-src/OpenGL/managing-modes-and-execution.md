---
title: Administración de modos y ejecución
description: Administración de modos y ejecución
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec448fa94c8ed0983be68f8aa1dbbef0974d2e040c4f68b002b026b300406981
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553985"
---
# <a name="managing-modes-and-execution"></a>Administración de modos y ejecución

El efecto de muchas funciones OpenGL depende de si un modo determinado está en vigor. Las [**funciones glEnable**](glenable.md) [**y glDisable**](gldisable.md) establecen estos modos; [**glIsEnabled**](glisenabled.md) determina si se establece un modo determinado.

Puede controlar la ejecución de funciones OpenGL emitidas previamente con [**glFinish**](glfinish.md), que obliga a que finalicen todas estas funciones, o [**glFlush**](glflush.md), que garantiza que todas estas funciones se completarán en un momento finito.

En una implementación determinada de OpenGL, puede controlar determinados comportamientos con sugerencias mediante [**glHint**](glhint.md). Estos comportamientos son la calidad de la interpolación de coordenadas de color y textura; la precisión de los cálculos de cálculo de cálculos de cálculo; y la calidad de muestreo de puntos, líneas o polígonos suavizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos y referencia de ejecución](modes-and-execution-reference.md)
</dt> </dl>

 

 




