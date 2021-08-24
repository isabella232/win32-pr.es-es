---
title: ELEMENTO VIEW
description: ELEMENTO VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Reproductor de Windows Media máscaras, elemento VIEW
- skins,VIEW, elemento
- ELEMENTO VIEW
- referencia de máscaras, elemento VIEW
- elements,VIEW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d2b14f75d3cf5405c1663e23ad343e3c22bb2a80f60919de4505808cdf0a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571663"
---
# <a name="view-element"></a>ELEMENTO VIEW

El **elemento VIEW** contiene los detalles de la interfaz de usuario de una máscara y usa los atributos, métodos y controladores de eventos que se muestran en las tablas siguientes.

Se pueden definir varios elementos **VIEW** como elementos secundarios del elemento **THEME** de una máscara para proporcionar interfaces diferentes para diferentes situaciones. **Los** elementos VIEW no se pueden especificar como elementos secundarios de ningún otro elemento y contienen todos los demás elementos de máscara. Tenga en cuenta que cada vista tiene su propio ámbito de variable, lo que significa que no puede compartir valores de atributo con otras vistas.

El **atributo** global de vista se puede usar para hacer referencia a un elemento **VIEW** específico desde cualquier lugar dentro de él. Se trata de una alternativa al uso de su atributo **id,** que se debe usar desde otros elementos **VIEW** o desde dentro del **elemento THEME.**

El **elemento VIEW** admite los atributos siguientes. Los atributos marcados con un asterisco ( \* ) también son compatibles con el elemento **SUBVIEW.**



| Atributo                                                       | Descripción                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)\*                  | Especifica o recupera el color de fondo de **VIEW** o **SUBVIEW.**                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Especifica o recupera la imagen de fondo de **VIEW** o **SUBVIEW.**                                             |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Especifica o recupera la cantidad por la que se desplaza el matiz de la imagen de fondo.                                  |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Especifica o recupera el valor de saturación de la imagen de fondo.                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | Especifica o recupera un valor que indica si la imagen de fondo de **VIEW** o **SUBVIEW** está en mosaico.         |
| [category](view-category.md)                                   | Especifica o recupera la categoría para la que aparecerá la interfaz de usuario.                                           |
| [focusObjectID](view-focusobjectid.md)                         | Especifica o recupera un valor que indica qué elemento tiene el foco del teclado.                                             |
| [maxHeight](view-maxheight.md)                                 | Especifica o recupera el alto máximo de **VIEW** al redimensionar.                                                |
| [maxWidth](view-maxwidth.md)                                   | Especifica o recupera el ancho máximo de **VIEW** al volver a ajustar el tamaño.                                                 |
| [minHeight](view-minheight.md)                                 | Especifica o recupera el alto mínimo de **VIEW** al redimensionar.                                                |
| [minWidth](view-minwidth.md)                                   | Especifica o recupera el ancho mínimo de **VIEW** al volver a ajustar el tamaño.                                                 |
| [Redimensionable](view-resizable.md)                                 | Especifica o recupera un valor que indica si se puede cambiar el tamaño de **VIEW.**                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.                                  |
| [scriptFile](view-scriptfile.md)                               | Especifica los nombres de archivo de los archivos JScript adjuntos.                                                                 |
| [timerInterval](view-timerinterval.md)                         | Especifica o recupera el intervalo, en milisegundos, en el que el temporizador dispara eventos al **controlador de eventos ontimer.** |
| [title](view-title.md)                                         | Especifica o recupera el título de **VIEW.** Solo se puede establecer en tiempo de diseño.                                       |
| [titleBar](view-titlebar.md)                                   | Especifica o recupera un valor que indica si se muestra la barra de título de la ventana.                                        |
| [transparencyColor](view-transparencycolor.md)\*              | Especifica o recupera el color de transparencia de la imagen de fondo.                                                  |



 

El **elemento VIEW** admite los métodos siguientes.



| Método                                              | Descripción                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Cierra la **vista**.                                       |
| [Maximizar](view-maximize.md)                       | Maximiza la **vista**.                                    |
| [Minimizar](view-minimize.md)                       | Minimiza la **vista**.                                    |
| [restore](view-restore.md)                         | Restaura la **vista**.                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | Devuelve el usuario al modo completo de Reproductor de Windows Media. |
| [size](view-size.md)                               | Cambia el tamaño **de VIEW** en un borde especificado.                  |



 

El **elemento VIEW** puede implementar los siguientes controladores de eventos.



| Controlador de eventos               | Descripción                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [onclose](view-onclose.md) | Controla un evento que tiene lugar cuando **la vista** está a punto de cerrarse.      |
| [Onerror](view-onerror.md) | Controla un evento de error **si Configuración.enableErrorDialogs** está establecido en false. |
| [Onload](view-onload.md)   | Controla un evento que tiene lugar cuando se **muestra la vista** por primera vez.         |
| [ontimer](view-ontimer.md) | Controla los eventos de temporizador.                                                      |



 

El **elemento VIEW** admite los atributos ambientales y puede implementar los controladores de eventos ambientales, excepto donde se indica. Para obtener más información, vea [Atributos ambientales](ambient-attributes.md) y [controladores de eventos de ambiente](ambient-event-handlers.md),

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscaras**](skin-programming-reference.md)
</dt> </dl>

 

 




