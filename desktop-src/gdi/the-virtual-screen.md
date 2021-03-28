---
description: El rectángulo delimitador de todos los monitores es la pantalla virtual. El escritorio cubre la pantalla virtual en lugar de un monitor único. En la ilustración siguiente se muestra una posible organización de tres monitores.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: La pantalla virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997929"
---
# <a name="the-virtual-screen"></a>La pantalla virtual

El rectángulo delimitador de todos los monitores es la *pantalla virtual*. El escritorio cubre la pantalla virtual en lugar de un monitor único. En la ilustración siguiente se muestra una posible organización de tres monitores.

![Ilustración en la que se muestran tres cuadros que representan monitores organizados dentro de un cuadro que representa la pantalla virtual](images/multimon-1.png)

El *monitor principal* contiene el origen (0,0). Esto es para la compatibilidad con las aplicaciones existentes que esperan un monitor con un origen. Sin embargo, el monitor principal no tiene que estar en la parte superior izquierda de la pantalla virtual. En la figura 1, está cerca del centro. Cuando el monitor principal no está en la parte superior izquierda de la pantalla virtual, las partes de la pantalla virtual tienen coordenadas negativas. Dado que el usuario establece la disposición de los monitores, todas las aplicaciones deben diseñarse para que funcionen con coordenadas negativas. Para obtener más información, consulte [consideraciones de varios monitores para programas anteriores](multiple-monitor-considerations-for-older-programs.md).

Las coordenadas de la pantalla virtual se representan mediante un valor de 16 bits con signo debido a los valores de 16 bits contenidos en muchos mensajes existentes. Por lo tanto, los límites de la pantalla virtual son:

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



