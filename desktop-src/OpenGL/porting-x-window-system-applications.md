---
title: Porting X Window System Applications
description: Porting X Window System Applications
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL on Windows,porting
- porting to OpenGL,X Window System
- Porte de OpenGL, sistema de ventanas X
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07a20de68df3806da40629252246f176beece0a4c3951180d484d9fadc6b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034765"
---
# <a name="porting-x-window-system-applications"></a>Porting X Window System Applications

Al Windows, el sistema de ventanas X es un sistema basado en mensajes y control de eventos que usa controles y menús de ventana. El código OpenGL de la aplicación X Window System probablemente se encuentra en áreas que se corresponden aproximadamente con el lugar donde aparecerá al portabilidad a Windows. La mayor parte del código OpenGL no cambiará, pero debe volver a escribir cualquier código que sea específico del sistema de ventanas X.

**Use el siguiente procedimiento general para portabilidad de los programas OpenGL del sistema X Window Windows**

1.  Vuelva a escribir el código específico del sistema de ventana X mediante código Windows equivalente. Busque código de creación de ventanas y control de eventos. El sistema de ventanas X Windows sistemas de ventana basados en mensajes y control de eventos, lo que facilita determinar dónde realizar los cambios adecuados. (Sin embargo, especialmente para aplicaciones de gran tamaño, volver a escribir una aplicación de un sistema operativo a otro puede ser una tarea compleja y difícil).
2.  Busque cualquier código que use funciones GLX. Estas son las funciones que traducirá a sus funciones de Windows equivalentes.
3.  Traduzca las funciones de formato de píxel GLX y las funciones de Visual/Drawable a las funciones de contexto de dispositivo y Windows de píxeles o OpenGL adecuadas.
4.  Traducir funciones de contexto de representación GLX Windows funciones de contexto de representación de OpenGL o de lectura.
5.  Traducir funciones GLXMap en funciones Windows equivalentes.
6.  Traduzca el búfer de fotogramas GLX y otras funciones GLX a las Windows adecuadas.

 

 




