---
title: Información general sobre desenfoque de DWM
description: Uno de los efectos de Administrador de ventanas de escritorio de firma (DWM) es un área no cliente translúcida y desenfocada. Las API de DWM permiten a las aplicaciones aplicar estos efectos en el área cliente de las ventanas de nivel superior.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Administrador de ventanas de escritorio (DWM), efecto de desenfoque
- DWM (Administrador de ventanas de escritorio), efecto de desenfoque
- efecto de desenfoque
- efecto traslúcido
- efecto de cristal transparente
- Administrador de ventanas de escritorio (DWM), efecto translúcido
- DWM (Administrador de ventanas de escritorio), efecto translúcido
- Administrador de ventanas de escritorio (DWM), efecto de cristal transparente
- DWM (Administrador de ventanas de escritorio), efecto de cristal transparente
- Administrador de ventanas de escritorio (DWM), extender el marco de ventana en el área de cliente
- DWM (Administrador de ventanas de escritorio), extender el marco de ventana en el área de cliente
- extender el marco de ventana en el área de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078267"
---
# <a name="dwm-blur-behind-overview"></a>Información general sobre desenfoque de DWM

Uno de los efectos de Administrador de ventanas de escritorio de firma (DWM) es un área no cliente translúcida y desenfocada. Las API de DWM permiten a las aplicaciones aplicar estos efectos en el área cliente de las ventanas de nivel superior.

> [!Note]  
> Windows Vista Home Basic Edition no admite el efecto de cristal transparente. Las áreas que normalmente se representarían con el efecto de cristal transparente en otras ediciones de Windows se representan como opacas.
> A partir de Windows 8, llamar a esta función no produce el efecto de desenfoque debido a un cambio de estilo en la forma en que se representan las ventanas.


 

En este tema se describen los siguientes escenarios de desenfoque de cliente que el DWM habilita.

-   [Agregar el desenfoque a una región específica del área cliente](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Extender el marco de ventana en el área cliente](#extending-the-window-frame-into-the-client-area)
-   [Temas relacionados](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Agregar el desenfoque a una región específica del área cliente

Una aplicación puede aplicar el efecto de desenfoque detrás de toda la región cliente de la ventana o de una subregión específica. Esto permite a las aplicaciones agregar barras de búsqueda y trazados de estilo que se separan visualmente del resto de la aplicación.

La API usada en este escenario es la función [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) , que hace uso de las [**constantes de desenfoque de DWM**](dwm-bb-constants.md) y de la estructura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) .

En la función de ejemplo siguiente, `EnableBlurBehind` , se muestra cómo aplicar el efecto de desenfoque detrás a toda la ventana.


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



Tenga en cuenta que **null** se especifica en el parámetro *hRgnBlur* . Esto indica al DWM que aplique el desenfoque detrás de la ventana completa.

En la imagen siguiente se muestra el efecto de desenfoque aplicado a toda la ventana.

![efecto de desenfoque aplicado a una ventana](images/dwm-blurbehindwindow.png)

Para aplicar el desenfoque detrás de una subregión, aplique un identificador de región válido (HRGN) al miembro **hRgnBlur** de la estructura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) y agregue la marca **DWM \_ BB \_ BLURREGION** al miembro **dwFlags** .

Cuando se aplica el efecto de desenfoque a una subregión de la ventana, se usa el canal alfa de la ventana para el área no desenfocada. Esto puede producir una transparencia inesperada en la región no desenfocada de una ventana. Por lo tanto, tenga cuidado al aplicar un efecto de desenfoque a una subregión.

## <a name="extending-the-window-frame-into-the-client-area"></a>Extender el marco de ventana en el área cliente

Una aplicación puede extender el desenfoque del marco de la ventana en el área cliente. Esto resulta útil cuando se aplica el efecto de desenfoque detrás de una ventana con una barra de herramientas acoplada o se separan visualmente los controles del resto de una aplicación. Esta funcionalidad se expone mediante la función [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) .

Para habilitar el desenfoque mediante [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use la estructura [**Margins**](/windows/win32/api/uxtheme/ns-uxtheme-margins) para indicar el grado de ampliación en el área cliente. La siguiente función de ejemplo, `ExtendIntoClientBottom` , alterna la extensión de desenfoque en la parte inferior del marco no cliente en el área cliente.


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



En la imagen siguiente se muestra el efecto de desenfoque que se extiende en la parte inferior del área cliente.

![imagen que muestra el efecto de desenfoque subyacente extendido en la parte inferior de un área cliente](images/dwm-extendedbottom.png)

También está disponible a través del método [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) es el efecto "hoja de cristal", donde el efecto de desenfoque se aplica a toda la superficie de la ventana sin un borde de ventana visible. En el ejemplo siguiente se muestra este efecto en el que el área cliente se representa sin un borde de ventana.


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



En la imagen siguiente se ilustra el desenfoque en el estilo de ventana "hoja de cristal".

![imagen que muestra el efecto de desenfoque en el estilo de ventana "hoja de cristal"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desktop Window Manager Overview](dwm-overview.md) (Administrador de ventanas de escritorio)
</dt> <dt>

[Habilitar y controlar la composición de DWM](composition-ovw.md)
</dt> <dt>

[Consideraciones de rendimiento y prácticas recomendadas](bestpractices-ovw.md)
</dt> </dl>

 

 