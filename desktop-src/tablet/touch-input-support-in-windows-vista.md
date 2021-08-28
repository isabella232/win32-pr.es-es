---
description: A partir Windows Vista, la tecnología de tablet PC admite la entrada táctil en tabletas pc con digitalizadores táctiles. Esta compatibilidad incluye una interfaz de usuario mejorada para ayudar a dirigir y dirigir Windows cuando se usa un dedo para la entrada.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Compatibilidad con entrada táctil en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b22130a7c731d49556db263d5c1d5565ef51aa103925969b35c98548a32d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335075"
---
# <a name="touch-input-support-in-windows-vista"></a>Compatibilidad con entrada táctil en Windows Vista

A partir Windows Vista, la tecnología de tablet PC admite la entrada táctil en tabletas pc con digitalizadores táctiles. Esta compatibilidad incluye una interfaz de usuario mejorada para ayudar a dirigir y dirigir Windows cuando se usa un dedo para la entrada.

## <a name="touch-digitizer-support"></a>Compatibilidad con digitalizador táctil

### <a name="pen-and-touch-input-not-exclusive"></a>Entrada táctil y de lápiz no exclusiva

No suponga que la entrada táctil y de lápiz son mutuamente excluyentes en las aplicaciones [**InkCollector,**](inkcollector-class.md) [**InkOverlay**](inkoverlay-class.md)y [**RealTimeStylus.**](realtimestylus-class.md)

En Windows Vista, cuando el sistema reconoce un lápiz, omite la entrada táctil. Es decir, el trazo táctil finaliza y comienza el trazo del lápiz. Dado que esto podría cambiar en el futuro, el código no debe asumir que la entrada táctil y el lápiz son mutuamente excluyentes.

### <a name="other-mouse-message-sources"></a>Otros orígenes de mensajes del mouse

Hay otros orígenes de mensajes del mouse incluso cuando el usuario solo interactúa con el dedo o el lápiz. Los orígenes incluyen los dispositivos táctiles, así como el movimiento destinado a permitir que una aplicación detrás de una ventana en capas tenga en cuenta que el mouse se mueve por encima de la aplicación.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Habilitación y deshabilitación de la entrada táctil Interfaz de usuario

Es posible que desee habilitar o deshabilitar la interfaz de usuario de entrada táctil en función de los requisitos de la aplicación. Para ello, intercepte los mensajes de ventana del sistema operativo en un procedimiento de ventana y modifique Windows mensaje. Invalide [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) en la aplicación para interceptar estos mensajes. El siguiente \# pseudocódigo de C muestra cómo habilitar y deshabilitar la interfaz de usuario de entrada táctil. El código también muestra el uso de la misma técnica para deshabilitar el gesto de mantener presionado. Este método también funciona para deshabilitar el lápiz óptico.


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

[Windows Tocar](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
