---
title: Funciones de contexto de representación
description: Cinco funciones WGL administran contextos de representación, como se describe en la tabla siguiente.
ms.assetid: e03ec03d-2a85-49de-a2be-fe81a5ec5f7f
keywords:
- Funciones WGL, contextos de representación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efb419caa2771b8dbee0eb25c8b5bdaf2a673df565f82ab25df10cbcc11cc39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776845"
---
# <a name="rendering-context-functions"></a>Funciones de contexto de representación

Cinco funciones WGL administran contextos de representación, como se describe en la tabla siguiente.



| WGL (Función)                                         | Descripción                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)         | Crea un nuevo contexto de representación.                                                             |
| [**WglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)             | Establece el contexto de representación actual de un subproceso.                                                   |
| [**WglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) | Obtiene un identificador para el contexto de representación actual de un subproceso.                                    |
| [**WglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)           | Obtiene un identificador para el contexto de dispositivo asociado al contexto de representación actual de un subproceso. |
| [**WglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)         | Elimina un contexto de representación.                                                                 |



 

La [**función wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) toma un identificador de contexto de dispositivo como parámetro y devuelve un identificador de contexto de representación. El contexto de representación creado es adecuado para dibujar en el dispositivo al que hace referencia el identificador de contexto del dispositivo. En concreto, su formato de píxel es el mismo que el formato de píxel del contexto del dispositivo. Después de crear un contexto de representación, puede liberar o eliminar el contexto del dispositivo. Consulte [Contextos de dispositivo para](/windows/desktop/gdi/device-contexts) obtener más detalles sobre cómo crear, obtener, liberar y eliminar un contexto de dispositivo.

> [!Note]  
> El contexto de dispositivo enviado a [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) debe ser un contexto de dispositivo para mostrar, un contexto de dispositivo de memoria o un contexto de dispositivo de impresora de color que use cuatro o más bits por píxel. El contexto del dispositivo no puede ser un contexto de dispositivo de impresora monocromática.

 

La [**función wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) toma un identificador de contexto de representación y un identificador de contexto de dispositivo como parámetros. Todas las llamadas OpenGL posteriores realizadas por el subproceso se realizan a través de ese contexto de representación y se dibujan en el dispositivo al que hace referencia ese contexto de dispositivo. El contexto del dispositivo no tiene que ser el mismo pasado a **wglCreateContext** cuando se creó el contexto de representación, pero debe estar en el mismo dispositivo y tener el mismo formato de píxel. La llamada a **wglMakeCurrent crea** una asociación entre el contexto de representación proporcionado y el contexto del dispositivo. No se puede liberar ni eliminar el contexto de dispositivo asociado a un contexto de representación actual hasta después de que el contexto de representación no sea actual.

Una vez que un subproceso tiene un contexto de representación actual, puede realizar llamadas a gráficos OpenGL. Todas las llamadas deben pasar a través de un contexto de representación. No ocurre nada si realiza llamadas de gráficos OpenGL desde un subproceso que carece de un contexto de representación actual.

La [**función wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) no toma ningún parámetro y devuelve un identificador al contexto de representación actual del subproceso que realiza la llamada. Si el subproceso no tiene ningún contexto de representación actual, el valor devuelto es **NULL.**

Cuando se obtiene un identificador para el contexto de dispositivo asociado al contexto de representación actual de un subproceso mediante una llamada a [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc), la asociación se crea cuando se hace actual un contexto de representación.

Puede interrumpir la asociación entre un contexto de representación actual y un subproceso llamando a [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con cualquiera de los dos identificadores:

-   Un **identificador de contexto** de representación null
-   Un identificador distinto del que se llamó originalmente

Después de llamar [**a wglMakeCurrent con**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) el parámetro de identificador de contexto de representación establecido en **NULL**, el subproceso que realiza la llamada no tiene ningún contexto de representación actual. El contexto de representación se libera de su conexión al subproceso y finaliza la asociación del contexto de representación a un contexto de dispositivo. OpenGL vacía todos los comandos de dibujo y puede liberar algunos recursos. No se realizará ningún dibujo OpenGL hasta la siguiente llamada a **wglMakeCurrent**, porque el subproceso no puede realizar llamadas a gráficos OpenGL hasta que recupera un contexto de representación actual.

La segunda manera de interrumpir la asociación entre un contexto de representación y un subproceso es llamar a **wglMakeCurrent** con un contexto de representación diferente. Después de una llamada de este tipo, el subproceso que realiza la llamada tiene un nuevo contexto de representación actual, el contexto de representación actual anterior se libera de su conexión con el subproceso y finaliza la asociación del contexto de representación actual anterior a un contexto de dispositivo.

La [**función wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext) toma un único parámetro, el identificador del contexto de representación que se va a eliminar. Antes de llamar **a wglDeleteContext**, haga que el contexto de representación no sea actual mediante una llamada a [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)y elimine o libere el contexto de dispositivo asociado mediante una llamada [a DeleteDC](/windows/desktop/api/wingdi/nf-wingdi-deletedc) o [ReleaseDC](/windows/desktop/api/winuser/nf-winuser-releasedc) según corresponda.

Es un error que un subproceso elimine un contexto de representación que es el contexto de representación actual de otro subproceso. Sin embargo, si un contexto de representación es el contexto de representación actual del subproceso que realiza la llamada, **wglDeleteContext** vacía todos los comandos de dibujo de OpenGL y hace que el contexto de representación no sea actual antes de eliminarlo. En este caso, confiar en **wglDeleteContext para** que un contexto de representación no sea actual requiere que el programador elimine o libere el contexto de dispositivo asociado.

 

 