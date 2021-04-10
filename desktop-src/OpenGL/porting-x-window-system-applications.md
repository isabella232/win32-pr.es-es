---
title: Trasladar aplicaciones de sistema de ventana X
description: Trasladar aplicaciones de sistema de ventana X
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL en Windows, portabilidad
- trasladar a OpenGL, sistema de ventanas X
- Portabilidad de OpenGL, sistema X Window
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268872"
---
# <a name="porting-x-window-system-applications"></a>Trasladar aplicaciones de sistema de ventana X

Al igual que Windows, el sistema de ventana X es un sistema basado en mensajes de control de eventos que usa controles de ventana y menús. El código OpenGL de la aplicación X de la ventana del sistema se encuentra probablemente en áreas que se corresponden aproximadamente con el lugar en el que aparece cuando se traslada a Windows. La mayoría del código OpenGL no cambiará, pero debe volver a escribir el código que sea específico del sistema X Window.

**Use el siguiente procedimiento general para trasladar los programas de OpenGL del sistema de ventana X a Windows**

1.  Vuelva a escribir el código específico del sistema de la ventana X mediante código de Windows equivalente. Busque la creación de ventanas y el código de control de eventos. El sistema de ventana X y Windows son sistemas de ventanas basados en mensajes y de control de eventos, lo que facilita determinar dónde realizar los cambios adecuados. (Sin embargo, especialmente en el caso de las aplicaciones de gran tamaño, la reescritura de una aplicación de un sistema operativo a otro puede ser una tarea compleja y difícil).
2.  Busque cualquier código que use funciones GLX. Estas son las funciones que traducirá a sus funciones equivalentes de Windows.
3.  Traduzca funciones de formato de píxel de GLX y funciones visuales/Dibujables al formato de píxeles Windows/OpenGL adecuado y a las funciones de contexto de dispositivo.
4.  Traduzca funciones de contexto de representación de GLX a funciones de contexto de representación de Windows/OpenGL.
5.  Traduzca las funciones de GLX Pixmap a funciones equivalentes de Windows.
6.  Traduzca GLX fotogramas y otras funciones GLX a las funciones de Windows adecuadas.

 

 




