---
description: Un cuadro de diálogo de error es un cuadro de diálogo modal que muestra un mensaje de error. Puede haber más de un cuadro de diálogo de error en cada instalación.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Cuadro de diálogo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543027"
---
# <a name="error-dialog"></a>Cuadro de diálogo de error

Un cuadro de diálogo de error es un cuadro de diálogo modal que muestra un mensaje de error. Puede haber más de un cuadro de diálogo de error en cada instalación.

Es necesario establecer una propiedad ErrorDialog que especifique qué cuadro de diálogo se va a usar. Si esta propiedad no está establecida o no señala a un cuadro de diálogo de error válido, no se mostrarán los mensajes de error. En este caso, el error solo se registra con una advertencia sobre el cuadro de diálogo que falta.

Un cuadro de diálogo de error debe tener establecido el [bit de estilo del cuadro de diálogo de error](error-dialog-style-bit.md) . El cuadro de diálogo debe tener un [control de texto](text-control.md) denominado ErrorText. El registro para el cuadro de diálogo de error de la [tabla de diálogo](dialog-table.md) debe tener el control ErrorText escrito en el \_ primer campo de control.

El cuadro de diálogo debe contener siete [pulsadores](pushbutton-control.md). Todos estos botones especifican [EndDialog](enddialog-controlevent.md) ControlEvent, en la [tabla ControlEvent,](controlevent-table.md). Cada botón especifica uno de los siguientes atributos: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.

> [!Note]  
> El foco de estos controles no debe vincularse mediante el uso de la \_ siguiente columna control de la [tabla de control](control-table.md).

 

Estos botones deben colocarse aproximadamente en la misma posición en el cuadro de diálogo porque, cuando se crea, solo se crea un subconjunto de estos siete botones, dependiendo del mensaje. La coordenada X de los botones se modifica para que los botones que se muestran se espacian uniformemente. La coordenada Y, el alto y el ancho de los botones no cambian. Dado que los botones están dispuestos horizontalmente, no se puede colocar ningún otro control en la misma región horizontal del cuadro de diálogo.

En el caso de un cuadro de diálogo de error, \_ se omiten los campos predeterminados del control y cancelar el control \_ de la [tabla del cuadro de diálogo](dialog-table.md) . El \_ primer campo de control de un cuadro de diálogo de error debe especificar el control ErrorText.

Si en este cuadro de diálogo se incluye un [control de icono](icon-control.md) denominado ErrorIcon, se muestran los siguientes iconos estándar de Windows:

-   \_Error de IDI en respuesta a los mensajes de imtFatalExit.
-   \_ADVERTENCIA IDI en respuesta a los mensajes imtError y imtWarning.
-   IDI \_ información en respuesta a los mensajes de imtOutOfDiskSpace.

El control ErrorIcon debe crearse con el [atributo de control FixedSize](fixedsize-control-attribute.md) establecido para evitar el tamaño incorrecto de los iconos estándar de Windows.

 

 



