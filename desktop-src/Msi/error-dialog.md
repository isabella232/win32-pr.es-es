---
description: Un cuadro de diálogo Error es un cuadro de diálogo modal que muestra un mensaje de error. Puede haber más de un cuadro de diálogo Error en cada instalación.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Cuadro de diálogo de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8582996ad4380d8adc62f684f638092857b45d464e7e8ef150c1fed141027f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692505"
---
# <a name="error-dialog"></a>Cuadro de diálogo de error

Un cuadro de diálogo Error es un cuadro de diálogo modal que muestra un mensaje de error. Puede haber más de un cuadro de diálogo Error en cada instalación.

Se debe establecer una propiedad ErrorDialog que especifique qué cuadro de diálogo se va a usar. Si esta propiedad no está establecida o no apunta a un cuadro de diálogo Error válido, no se mostrarán los mensajes de error. En este caso, el error solo se registra con una advertencia sobre el cuadro de diálogo que falta.

Un cuadro de diálogo Error debe tener el conjunto [de bits Estilo de diálogo de error.](error-dialog-style-bit.md) El cuadro de diálogo debe tener un [control Text](text-control.md) denominado ErrorText. El registro del cuadro de diálogo Error de la [tabla Dialog](dialog-table.md) debe tener el control ErrorText especificado en el campo Control \_ First.

El cuadro de diálogo debe contener siete [PushButtons](pushbutton-control.md). Todos estos botones especifican [EndDialog](enddialog-controlevent.md) ControlEvent en la [tabla ControlEvent](controlevent-table.md). Cada botón especifica uno de los atributos siguientes: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.

> [!Note]  
> El foco de estos controles no debe vincularse mediante el uso de la columna Control \_ Siguiente de la tabla [Control](control-table.md).

 

Estos botones deben colocarse aproximadamente en la misma posición en el cuadro de diálogo porque, cuando se crea, solo se crea un subconjunto de estos siete botones, en función del mensaje. La coordenada X de los botones se modifica para que los botones que se muestran estén espaciados uniformemente. La coordenada Y, el alto y el ancho de los botones no se modifican. Dado que los botones se organizan horizontalmente, no se puede colocar ningún otro control en la misma región horizontal del cuadro de diálogo.

En el caso de un cuadro de diálogo Error, se omiten los campos Control Predeterminado y \_ Cancelar de control de la tabla \_ [Diálogo.](dialog-table.md) El campo \_ Control First de un cuadro de diálogo Error debe especificar el control ErrorText.

Si en [este cuadro de](icon-control.md) diálogo se incluye un control Icon denominado ErrorIcon, se muestran los siguientes iconos Windows estándar:

-   ERROR de IDI \_ en respuesta a mensajes imtFatalExit.
-   IDI \_ WARNING en respuesta a mensajes imtError e imtWarning.
-   IDI \_ INFORMATION en respuesta a mensajes imtOutOfDiskSpace.

El control ErrorIcon debe crearse con el atributo de [control FixedSize](fixedsize-control-attribute.md) establecido para evitar un ajuste de tamaño incorrecto de los iconos Windows estándar.

 

 



