---
title: Realización de la selección y los comentarios
description: Realización de la selección y los comentarios
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL,selection
- OpenGL, comentarios
- OpenGL, rendering
- modo de selección OpenGL
- modo de comentarios OpenGL
- modo de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95efe3f07e86056cd0364daaed1e6a9c0ef402afc18b14d74cca313c9835479f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936291"
---
# <a name="performing-selection-and-feedback"></a>Realización de la selección y los comentarios

La selección, los comentarios y la representación son modos de funcionamiento mutuamente excluyentes. La representación es el modo normal y predeterminado durante el cual los fragmentos se generan mediante la rasterización.

En los modos de selección y comentarios, no se genera ningún fragmento; por lo tanto, no se produce ninguna modificación del búfer de fotogramas. En el modo de selección, puede determinar qué primitivas se dibujarán en alguna región de una ventana; en el modo de comentarios, la información sobre las primitivas que se van a rasterizar se introduce de nuevo en la aplicación.

Seleccione entre estos tres modos con [**glRenderMode**](glrendermode.md).

-   [Selección](selection.md)
-   [Comentarios](feedback.md)
-   [Referencia de selección y comentarios](selection-and-feedback-reference.md)

 

 




