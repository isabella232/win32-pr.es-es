---
description: A partir de Windows Vista, la tecnología de Tablet PC es compatible con la entrada táctil en Tablet PC con digitalizadores táctiles. Esta compatibilidad incluye una interfaz de usuario mejorada para ayudar a dirigir y a las ventanas de comandos cuando se usa un dedo para la entrada.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Compatibilidad con la entrada táctil en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706569"
---
# <a name="touch-input-support-in-windows-vista"></a>Compatibilidad con la entrada táctil en Windows Vista

A partir de Windows Vista, la tecnología de Tablet PC es compatible con la entrada táctil en Tablet PC con digitalizadores táctiles. Esta compatibilidad incluye una interfaz de usuario mejorada para ayudar a dirigir y a las ventanas de comandos cuando se usa un dedo para la entrada.

## <a name="touch-digitizer-support"></a>Compatibilidad con el digitalizador táctil

### <a name="pen-and-touch-input-not-exclusive"></a>Lápiz y entrada táctil no exclusiva

No asuma que el lápiz y la entrada táctil se excluyen mutuamente en las aplicaciones [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)y [**RealTimeStylus**](realtimestylus-class.md) .

En Windows Vista, cuando el sistema reconoce un lápiz, omite la entrada táctil. Es decir, el trazo táctil finaliza y comienza el trazo del lápiz. Como esto podría cambiar en el futuro, el código no debe asumir que el lápiz y la entrada táctil se excluyen mutuamente.

### <a name="other-mouse-message-sources"></a>Otros orígenes de mensajes del mouse

Hay otros orígenes de mensajes del mouse incluso cuando el usuario solo está interactuando con el dedo o el lápiz. Los orígenes incluyen touchpad, así como el movimiento diseñado para permitir que una aplicación detrás de una ventana superpuesta tenga en cuenta que el mouse se mueve sobre la aplicación.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Habilitación y deshabilitación de la interfaz de usuario de entrada táctil

Puede habilitar o deshabilitar la interfaz de usuario de entrada táctil en función de los requisitos de la aplicación. Para ello, intercepte los mensajes de ventana del sistema operativo en un procedimiento de ventana y modifique el mensaje de Windows. Invalide [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) en la aplicación para interceptar estos mensajes. En el siguiente \# pseudocódigo de C se muestra cómo habilitar y deshabilitar la interfaz de usuario de entrada táctil. El código también muestra cómo usar la misma técnica para deshabilitar el gesto de mantener presionado. Este método también sirve para deshabilitar el lápiz.


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Touch](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
