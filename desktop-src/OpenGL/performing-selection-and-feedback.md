---
title: Realización de una selección y comentarios
description: Realización de una selección y comentarios
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, selección
- OpenGL, comentarios
- OpenGL, representación
- modo de selección OpenGL
- modo de comentarios OpenGL
- modo de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357102"
---
# <a name="performing-selection-and-feedback"></a>Realización de una selección y comentarios

Selección, comentarios y representación son modos de operación mutuamente excluyentes. La representación es el modo predeterminado y normal durante el cual se generan fragmentos mediante la rasterización.

En los modos de selección y de comentarios, no se generan fragmentos; por lo tanto, no se produce ninguna modificación de fotogramas. En el modo de selección, puede determinar qué primitivos se van a dibujar en alguna región de una ventana. en el modo de comentarios, la información acerca de los primitivos que se van a rasterizar se revierte a la aplicación.

Puede seleccionar uno de estos tres modos con [**glRenderMode**](glrendermode.md).

-   [Selección](selection.md)
-   [Comentarios](feedback.md)
-   [Selección y referencia de comentarios](selection-and-feedback-reference.md)

 

 




