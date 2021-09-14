---
title: Porte de contextos de dispositivo y formatos de píxel
description: Porte de contextos de dispositivo y formatos de píxel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- porting to OpenGL,pixels
- Porte de OpenGL, píxeles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169181"
---
# <a name="porting-device-contexts-and-pixel-formats"></a>Porte de contextos de dispositivo y formatos de píxel

Cada ventana de la implementación de Microsoft de OpenGL para Windows tiene su propio formato de píxel actual. Un formato de píxel se define mediante una estructura de datos [**PIXELFORMATDESCRIPTOR.**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) Dado que cada ventana tiene su propio formato de píxel, se obtiene un contexto de dispositivo, se establece el formato de píxel del contexto del dispositivo y, a continuación, se crea un contexto de representación openGL para el contexto del dispositivo. El contexto de representación usa automáticamente el formato de píxel de su contexto de dispositivo.

El sistema de ventanas X también usa una estructura de datos, **XVisualInfo**, para especificar las propiedades de píxeles en una ventana. **Las estructuras XVisualInfo** contienen una **estructura de** datos visual que describe cómo se usan los recursos de color en una pantalla específica.

En el sistema de ventanas **X, XVisualInfo** se usa para crear una ventana estableciendo la ventana en el formato de píxel que desee. La estructura devuelta se usa para crear la ventana y un contexto de representación. En Windows, primero debe crear una ventana y obtener un identificador para un contexto de dispositivo (HDC) de la ventana. A continuación, se usa HDC para establecer el formato de píxel de la ventana. El contexto de representación usa el formato de píxel de la ventana.

En la tabla siguiente se comparan las funciones visuales Del sistema de ventanas X y GLX con sus funciones de formato Windows píxeles equivalentes.



| Ventana X/Función visual GLX                                                                                     | Windows de formato de píxel                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| XVisualInfo \* **glXChooseVisual**( Display *\* dpy*,int *screen*,int *\* attribList*)                               | int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\* ppfd*)                                      |
| int **glXGetConfig**( Display *\* dpy*,XVisualInfo *\* vis*,int *\* attribList*,int *\* value*)                      | int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*, int *iPixelFormat*, UINT *nBytes*,LPIXXELFORMATDESCRIPTOR *ppfd*) |
| XVisualInfo \* **XGetVisualInfo**( Mostrar *\* dpy*,long *vinfo \_ mask*,XVisualInfo *\* vinfo \_ templ*,int *\* nitems*) | int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)                                                                           |
| El *objeto visual* devuelto por **glxChooseVisual** se usa cuando se crea una ventana.                                   | BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*, int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\* ppfd*)                        |



 

En las secciones siguientes se proporcionan ejemplos de fragmentos de código con formato de píxel para un programa del sistema de ventanas X y el mismo código después de que se haya portado a Windows.

-   [Ejemplo de código de formato de píxeles GLX](glx-pixel-format-code-sample.md)
-   [Windows Ejemplo de código de formato de píxel](win32-pixel-format-code-sample.md)

Para obtener más información sobre los formatos de píxel, vea [Formatos de píxel.](pixel-formats.md)

 

 




