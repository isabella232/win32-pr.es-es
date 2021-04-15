---
title: Elemento de vista
description: Elemento de vista
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Aspectos de Windows Media Player, elemento VIEW
- aspectos, elemento de vista
- Elemento de vista
- referencia de las máscaras, elemento de vista
- elementos, vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418828"
---
# <a name="view-element"></a>Elemento de vista

El elemento de **vista** contiene los detalles de la interfaz de usuario de una máscara y usa los atributos, métodos y controladores de eventos que se muestran en las tablas siguientes.

Se pueden definir varios elementos de **vista** como elementos secundarios del elemento de **tema** de una máscara para proporcionar diferentes interfaces para diferentes situaciones. Los elementos de **vista** no se pueden especificar como elementos secundarios de ningún otro elemento y contienen todos los demás elementos de máscara. Tenga en cuenta que cada vista tiene su propio ámbito de variable, lo que significa que no puede compartir valores de atributo con otras vistas.

El atributo de **vista** global se puede usar para hacer referencia a un elemento de **vista** específico desde cualquier lugar dentro de él. Se trata de una alternativa al uso del atributo **ID** , que debe usarse desde otros elementos de **vista** o desde dentro del elemento **Theme** .

El elemento **View** admite los siguientes atributos. Los atributos marcados con un asterisco ( \* ) también se admiten en el elemento de la **subvista** .



| Atributo                                                       | Descripción                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [BackgroundColor](view-backgroundcolor.md)\*                  | Especifica o recupera el color de fondo de la **vista** o la **subvista**.                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | Especifica o recupera la imagen de fondo de la **vista** o la **subvista**.                                             |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Especifica o recupera la cantidad por la que se desplaza el matiz de la imagen de fondo.                                  |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Especifica o recupera el valor de saturación de la imagen de fondo.                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | Especifica o recupera un valor que indica si la imagen de fondo de la **vista** o la **subvista** está en mosaico.         |
| [category](view-category.md)                                   | Especifica o recupera la categoría para la que aparecerá la interfaz de usuario.                                           |
| [focusObjectID](view-focusobjectid.md)                         | Especifica o recupera un valor que indica qué elemento tiene el foco de teclado.                                             |
| [maxHeight](view-maxheight.md)                                 | Especifica o recupera el alto máximo de la **vista** al cambiar el tamaño.                                                |
| [maxWidth](view-maxwidth.md)                                   | Especifica o recupera el ancho máximo de la **vista** al cambiar el tamaño.                                                 |
| [minHeight](view-minheight.md)                                 | Especifica o recupera el alto mínimo de la **vista** al cambiar el tamaño.                                                |
| [minWidth](view-minwidth.md)                                   | Especifica o recupera el ancho mínimo de la **vista** al cambiar el tamaño.                                                 |
| [tamaño](view-resizable.md)                                 | Especifica o recupera un valor que indica si se puede cambiar el tamaño de la **vista** .                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.                                  |
| [scriptFile](view-scriptfile.md)                               | Especifica los nombres de archivo de los archivos JScript que lo acompañan.                                                                 |
| [timerInterval](view-timerinterval.md)                         | Especifica o recupera el intervalo, en milisegundos, en el que el temporizador activa eventos al controlador de eventos de **tiempo de actividad** . |
| [title](view-title.md)                                         | Especifica o recupera el título de la **vista**. Solo se puede establecer en tiempo de diseño.                                       |
| [titleBar](view-titlebar.md)                                   | Especifica o recupera un valor que indica si se muestra la barra de título de la ventana.                                        |
| [transparencyColor](view-transparencycolor.md)\*              | Especifica o recupera el color de transparencia de la imagen de fondo.                                                  |



 

El elemento **View** admite los métodos siguientes.



| Método                                              | Descripción                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | Cierra la **vista**.                                       |
| [maximizar](view-maximize.md)                       | Maximiza la **vista**.                                    |
| [miniMIZE](view-minimize.md)                       | Minimiza la **vista**.                                    |
| [restore](view-restore.md)                         | Restaura la **vista**.                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | Devuelve el usuario al modo completo de Windows Media Player. |
| [size](view-size.md)                               | Cambia el tamaño de la **vista** en un borde especificado.                  |



 

El elemento de **vista** puede implementar los controladores de eventos siguientes.



| Controlador de eventos               | Descripción                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [OnClose](view-onclose.md) | Controla un evento que se produce cuando la **vista** está a punto de cerrarse.      |
| [OnError](view-onerror.md) | Controla un evento de error si **Settings. enableErrorDialogs** está establecido en false. |
| [carga](view-onload.md)   | Controla un evento que se produce cuando se muestra la **vista** por primera vez.         |
| [tiempo de espera](view-ontimer.md) | Controla los eventos del temporizador.                                                      |



 

El elemento **View** admite los atributos de ambiente y puede implementar los controladores de eventos ambiente, excepto donde se indique. Para obtener más información, vea [atributos de ambiente](ambient-attributes.md) y controladores de eventos de [ambiente](ambient-event-handlers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> </dl>

 

 




