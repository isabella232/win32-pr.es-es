---
description: El rectángulo delimitador de todos los monitores es la pantalla virtual. El escritorio cubre la pantalla virtual en lugar de un solo monitor. En la ilustración siguiente se muestra una posible disposición de tres monitores.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: La pantalla virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5516ef0cb5d99124200ab7810e484ea79027cf832a0e8da74833bf709ce5cc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037523"
---
# <a name="the-virtual-screen"></a>La pantalla virtual

El rectángulo delimitador de todos los monitores es la *pantalla virtual*. El escritorio cubre la pantalla virtual en lugar de un solo monitor. En la ilustración siguiente se muestra una posible disposición de tres monitores.

![ilustración que muestra tres cuadros que representan monitores organizados dentro de un cuadro que representa la pantalla virtual](images/multimon-1.png)

El *monitor principal* contiene el origen (0,0). Esto es por compatibilidad con aplicaciones existentes que esperan un monitor con un origen. Sin embargo, el monitor principal no tiene que estar en la parte superior izquierda de la pantalla virtual. En la figura 1, está cerca del centro. Cuando el monitor principal no está en la parte superior izquierda de la pantalla virtual, las partes de la pantalla virtual tienen coordenadas negativas. Dado que el usuario establece la disposición de los monitores, todas las aplicaciones deben diseñarse para trabajar con coordenadas negativas. Para obtener más información, [vea Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).

Las coordenadas de la pantalla virtual se representan mediante un valor de 16 bits con firma debido a los valores de 16 bits contenidos en muchos mensajes existentes. Por lo tanto, los límites de la pantalla virtual son:

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



