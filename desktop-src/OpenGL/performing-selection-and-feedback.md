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
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161072"
---
# <a name="performing-selection-and-feedback"></a>Realización de la selección y los comentarios

La selección, los comentarios y la representación son modos de funcionamiento mutuamente excluyentes. La representación es el modo normal y predeterminado durante el cual los fragmentos se generan mediante la rasterización.

En los modos de selección y comentarios, no se genera ningún fragmento; por lo tanto, no se produce ninguna modificación del búfer de fotogramas. En el modo de selección, puede determinar qué primitivas se dibujarán en alguna región de una ventana; en el modo de comentarios, la información sobre las primitivas que se van a rasterizar se introduce de nuevo en la aplicación.

Seleccione entre estos tres modos con [**glRenderMode**](glrendermode.md).

-   [Selección](selection.md)
-   [Comentarios](feedback.md)
-   [Referencia de selección y comentarios](selection-and-feedback-reference.md)

 

 




