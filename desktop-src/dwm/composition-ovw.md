---
title: Habilitar y controlar la composición de DWM
description: Las API de composición de Administrador de ventanas de escritorio (DWM) proporcionan varias funciones para establecer y consultar información básica que utiliza DWM.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- Administrador de ventanas de escritorio (DWM), composición
- DWM (Administrador de ventanas de escritorio), composición
- composición
- composición de escritorio
- coloración
- representación de regiones no cliente
- Administrador de ventanas de escritorio (DWM), coloración
- DWM (Administrador de ventanas de escritorio), coloración
- Administrador de ventanas de escritorio (DWM), representación de regiones no cliente
- DWM (Administrador de ventanas de escritorio), representación de regiones no cliente
- Administrador de ventanas de escritorio (DWM), mensajería
- DWM (Administrador de ventanas de escritorio), mensajería
- messaging
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903782"
---
# <a name="enable-and-control-dwm-composition"></a>Habilitar y controlar la composición de DWM

Las API de composición de Administrador de ventanas de escritorio (DWM) proporcionan varias funciones para establecer y consultar información básica que utiliza DWM. Estas API permiten consultar y cambiar el estado de composición. Además, puede establecer y consultar la Directiva de representación para los distintos atributos de la ventana de DWM.

## <a name="retrieving-colorization-information"></a>Recuperar información de color

El color de la región no cliente de una ventana viene determinado por el tema de color del sistema actual. El valor de coloración se proporciona a través de las API de DWM para permitir que la aplicación coincida con la interfaz de usuario del cliente con el tema de color del sistema.

Para tener acceso a este valor de coloración y supervisar el cambio de color, utilice la función [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) y el mensaje [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) .

En este ejemplo se muestra cómo controlar el mensaje de cambio de color y cómo obtener acceso al nuevo color.

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

## <a name="controlling-non-client-region-rendering"></a>Controlar la representación de regiones no cliente

Dos de los efectos visuales que DWM permite son la transparencia de la región no cliente de una ventana y los efectos de la transición. Es posible que la aplicación tenga que deshabilitar o volver a habilitar estos efectos por motivos de compatibilidad o estilo. Las funciones siguientes se usan para administrar el comportamiento de la transparencia y del efecto de transición.

- [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

Para recuperar el estado actual de representación no cliente de la ventana de una aplicación, llame a [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con *dwAttribute* establecido en [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute). Como puede ver en la documentación de [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), al pasar esa marca a **DwmGetWindowAttribute**, el valor del atributo recuperado es de tipo **bool**. Las distintas marcas hacen que **DwmGetWindowAttribute** devuelva valores de tipos diferentes. Aquí tienes un ejemplo de código.

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

En el ejemplo siguiente se muestra cómo usar la marca [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) con **DwmGetWindowAttribute** para recuperar el rectángulo de límites de marco extendido de una ventana. La documentación de esa marca nos indica que el valor del atributo recuperado es de tipo **Rect**.

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> Siga el mismo patrón de programación que se mostró anteriormente al llamar a [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) con marcas para los distintos atributos. El tema de enumeración [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) indica, en la fila de cada marcador, el tipo de valor al que debe pasar un puntero en el parámetro *pvAttribute* para **DwmGetWindowAttribute**. El parámetro *cbAttribute* contiene el tamaño, en bytes, de ese objeto.

[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) permite que la aplicación establezca la Directiva de representación de área no cliente. Esa función también determina el modo en que la aplicación debe controlar los efectos de transición de DWM.

En el siguiente ejemplo se deshabilita la representación del área no cliente. Esto hace que se deshabiliten las llamadas anteriores a [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) o [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .

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

Además de controlar la representación del área no cliente, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) también puede controlar los efectos de transición de DWM. Puede establecer el comportamiento de transición mediante **DWMWA \_ Transitions \_ FORCEDISABLED** como el parámetro *dwAttribute* .

## <a name="messages"></a>error de Hadoop

Los mensajes siguientes proporcionan la notificación de eventos de DWM. Estos mensajes se pueden usar para supervisar cambios, como cambios de estado de composición y cambios de tema de color del sistema.

- [**DWMCOLORIZATIONCOLORCHANGED de WM \_**](wm-dwmcolorizationcolorchanged.md)
- [**DWMCOMPOSITIONCHANGED de WM \_**](wm-dwmcompositionchanged.md)
- [**DWMNCRENDERINGCHANGED de WM \_**](wm-dwmncrenderingchanged.md)
- [**DWMWINDOWMAXIMIZEDCHANGE de WM \_**](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a>Deshabilitar la composición de DWM (Windows 7 y versiones anteriores)

> [!WARNING]
> La información de esta sección solo se aplica a Windows 7 y sistemas anteriores.

Dado que DWM usa la unidad de procesamiento de gráficos (GPU) para la composición del escritorio, es posible que la aplicación tenga que deshabilitar DWM por compatibilidad. Las aplicaciones que tienen control total sobre el escritorio, como los juegos que se ejecutan en modo de pantalla completa, deben determinar si DWM está habilitado y, si es así, deshabilitarlo. Para ello, se necesitan dos funciones.

- [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

Una llamada a [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) con *FEnable* establecido en **DWM \_ EC \_ DISABLECOMPOSITION** deshabilita la composición de DWM hasta que el proceso de llamada se ha cerrado o se ha vuelto a habilitar la composición mediante una llamada a **DwmEnableComposition** con *fEnable* establecido en **DWM \_ EC \_ ENABLECOMPOSITION**. La composición DWM se reinicia automáticamente en cuanto todas las aplicaciones que tienen la composición deshabilitada se apagan o se vuelven a habilitar manualmente mediante una llamada a **DwmEnableComposition**.

> [!NOTE]  
> El DWM deshabilita automáticamente la composición cuando una aplicación intenta dibujar directamente en la superficie de visualización principal. La composición se deshabilitará hasta que la superficie del dispositivo principal sea publicada por esa aplicación.
