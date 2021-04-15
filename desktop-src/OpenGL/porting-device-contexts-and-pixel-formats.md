---
title: Portabilidad de los contextos de dispositivo y formatos de píxel
description: Portabilidad de los contextos de dispositivo y formatos de píxel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- trasladar a OpenGL, píxeles
- Portabilidad de OpenGL, píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665605"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>Portabilidad de los contextos de dispositivo y formatos de píxel

Cada ventana de la implementación de Microsoft de OpenGL para Windows tiene su propio formato de píxel actual. Un formato de píxel se define mediante una estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) . Dado que cada ventana tiene su propio formato de píxel, se obtiene un contexto de dispositivo, se establece el formato de píxel del contexto del dispositivo y, a continuación, se crea un contexto de representación de OpenGL para el contexto del dispositivo. El contexto de representación utiliza automáticamente el formato de píxel de su contexto de dispositivo.

El sistema de ventana X también utiliza una estructura de datos, **XVisualInfo**, para especificar las propiedades de los píxeles en una ventana. Las estructuras **XVisualInfo** contienen una estructura de datos **Visual** que describe cómo se usan los recursos de color en una pantalla concreta.

En el sistema de ventana X, **XVisualInfo** se usa para crear una ventana estableciendo la ventana en el formato de píxel que desee. La estructura devuelta se usa para crear la ventana y un contexto de representación. En Windows, primero se crea una ventana y se obtiene un identificador de un contexto de dispositivo (HDC) de la ventana. A continuación, se usa HDC para establecer el formato de píxel para la ventana. El contexto de representación usa el formato de píxel de la ventana.

En la tabla siguiente se comparan las funciones visuales del sistema de ventanas X y GLX con sus funciones de formato de Windows píxeles equivalentes.



| X Window/GLX función visual)                                                                                     | Función de formato de Windows píxeles                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| XVisualInfo \* **glXChooseVisual**(Mostrar *\* dpy*, int *Screen*, int *\* attribList*)                               | int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, PIXELFORMATDESCRIPTOR *\* ppfd*)                                      |
| int **glXGetConfig**(display *\* dpy*, XVisualInfo *\* Vis*, int *\* attribList*, int *\* Value*)                      | int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *iPixelFormat*, uint *nBytes*, LPPIXELFORMATDESCRIPTOR *ppfd*) |
| XVisualInfo \* **XGetVisualInfo**(display *\* dpy*, Long *vinfo \_ Mask*, XVisualInfo *\* vinfo \_ templ*, int *\* nitems*) | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)                                                                           |
| El *Visual* devuelto por **glxChooseVisual** se usa cuando se crea una ventana.                                   | BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *iPixelFormat*, PIXELFORMATDESCRIPTOR *\* ppfd*)                        |



 

En las secciones siguientes se proporcionan ejemplos de fragmentos de código de formato de píxel para un programa de sistema de ventana X y el mismo código después de que se haya trasladado a Windows.

-   [GLX ejemplo de código de formato de píxeles](glx-pixel-format-code-sample.md)
-   [Ejemplo de código de formato de Windows píxeles](win32-pixel-format-code-sample.md)

Para obtener más información sobre los formatos de píxeles, consulte [formatos de píxeles](pixel-formats.md).

 

 




