---
title: Habilitación y control de la composición de DWM
description: Las ADMINISTRADOR DE VENTANAS DE ESCRITORIO de composición de Administrador de ventanas de escritorio (DWM) proporcionan varias funciones para establecer y consultar la información básica que usa DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Administrador de ventanas de escritorio (DWM),composition
- DWM (Administrador de ventanas de escritorio),composition
- composición
- composición de escritorio
- Coloración
- representación de regiones que no son de cliente
- Administrador de ventanas de escritorio (DWM),coloración
- DWM (Administrador de ventanas de escritorio),coloración
- Administrador de ventanas de escritorio (DWM), representación de regiones que no son de cliente
- DWM (Administrador de ventanas de escritorio), representación de regiones que no son de cliente
- Administrador de ventanas de escritorio (DWM),messaging
- DWM (Administrador de ventanas de escritorio),messaging
- messaging
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: e8c5df1778436e2cfe23df85483453b01fb80884adc9a6d8ff34955deb3e0c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741585"
---
# <a name="enable-and-control-dwm-composition"></a>Habilitación y control de la composición de DWM

Las ADMINISTRADOR DE VENTANAS DE ESCRITORIO de composición de Administrador de ventanas de escritorio (DWM) proporcionan varias funciones para establecer y consultar la información básica que usa DWM. Estas API permiten consultar y cambiar el estado de composición. Además, puede establecer y consultar la directiva de representación para distintos atributos de ventana de DWM.

## <a name="retrieving-colorization-information"></a>Recuperación de información de coloración

El color de la región que no es de cliente de una ventana viene determinado por el tema de color del sistema actual. El valor de coloración se proporciona a través de las API de DWM para permitir que la aplicación coincida con la interfaz de usuario del cliente con el tema de color del sistema.

Para acceder a este valor de coloración y supervisar el cambio de color, use la [**función DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) y el [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) mensaje.

En este ejemplo se muestra cómo controlar el mensaje de cambio de color y acceder al nuevo color.

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a>Controlar la representación de regiones que no son de cliente

Dos de los efectos visuales que DWM habilita son la transparencia de la región no cliente de una ventana y los efectos de transición. Es posible que la aplicación tenga que deshabilitar o volver a habilitar estos efectos por motivos de compatibilidad o estilo. Las siguientes funciones se usan para administrar la transparencia y el comportamiento del efecto de transición.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Para recuperar el estado de representación que no es de cliente actual para la ventana de una aplicación, llame a [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con *dwAttribute* establecido [**en DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute). Como puede ver en la documentación de [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), al pasar esa marca a **DwmGetWindowAttribute**, el valor del atributo recuperado es de **tipo BOOL**. Las marcas diferentes hacen **que DwmGetWindowAttribute** devuelva valores de tipos diferentes. Aquí tienes un ejemplo de código.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

En este ejemplo siguiente se muestra cómo usar la marca [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) **con DwmGetWindowAttribute para** recuperar el rectángulo de límites de marco extendido de una ventana. La documentación de esa marca nos indica que el valor del atributo recuperado es de tipo **RECT.**

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Siga el mismo patrón de programación mostrado anteriormente al llamar [**a DwmGetWindowAttribute con**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) marcas para distintos atributos. El tema de enumeración [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, en la fila de cada marca, a qué tipo de valor debe pasar un puntero en el parámetro *pvAttribute* **para DwmGetWindowAttribute**. El *parámetro cbAttribute* contiene el tamaño, en bytes, de ese objeto.

[**DwmSetWindowAttribute permite**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) que la aplicación establezca la directiva de representación del área que no es de cliente. Esa función también determina cómo la aplicación debe controlar los efectos de transición de DWM.

En este ejemplo siguiente se deshabilita la representación del área que no es de cliente. Esto hace que las llamadas anteriores a [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) o [a DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) se deshabiliten.

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

Además de controlar la representación del área que no es de cliente, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) también puede controlar los efectos de transición de DWM. Puede establecer el comportamiento de transición mediante **DWMWA \_ TRANSITIONS \_ FORCEDISABLED como** parámetro *dwAttribute.*

## <a name="messages"></a>error de Hadoop

Los mensajes siguientes proporcionan notificación de eventos DWM. Estos mensajes se pueden usar para supervisar cambios como cambios de estado de composición y cambios de tema de color del sistema.

- [**WM \_ DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md)
- [**WM \_ DWMCOMPOSITIONCHANGED**](wm-dwmcompositionchanged.md)
- [**WM \_ DWMNCRENDERINGCHANGED**](wm-dwmncrenderingchanged.md)
- [**WM \_ DWMWINDOWMAXIMIZEDCHANGE**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows-7-and-earlier"></a>Deshabilitar la composición de DWM (Windows 7 y versiones anteriores)

> [!WARNING]
> La información de esta sección solo se aplica a Windows 7 y sistemas anteriores.

Dado que DWM usa la unidad de procesamiento gráfico (GPU) para la composición de escritorio, es posible que la aplicación tenga que deshabilitar DWM por compatibilidad. Las aplicaciones que toman el control total del escritorio, como los juegos que se ejecutan en modo de pantalla completa, deben determinar si el DWM está habilitado y, si es así, deshabilitarlo. Para ello, se necesitan dos funciones.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Una llamada a [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) con *fEnable* establecido en **DWM \_ EC \_ DISABLECOMPOSITION** deshabilita la composición de DWM hasta que se haya cerrado el proceso de llamada o se haya habilitado de nuevo la composición llamando a **DwmEnableComposition** con *fEnable* establecido en **DWM \_ EC \_ ENABLECOMPOSITION**. La composición de DWM se reinicia automáticamente en cuanto todas las aplicaciones que tienen deshabilitada la composición se han apagado o se ha habilitado manualmente mediante una llamada a **DwmEnableComposition**.

> [!NOTE]  
> DwM deshabilita automáticamente la composición cuando una aplicación intenta dibujar directamente en la superficie de presentación principal. La composición se deshabilitará hasta que esa aplicación libera la superficie del dispositivo principal.
