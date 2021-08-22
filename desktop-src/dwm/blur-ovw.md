---
title: Información general sobre el desenfoque de DWM
description: Uno de los efectos de Administrador de ventanas de escritorio firma (DWM) es un área no cliente translúcida y desenfoque. Las API de DWM permiten a las aplicaciones aplicar estos efectos al área cliente de sus ventanas de nivel superior.
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- Administrador de ventanas de escritorio (DWM), efecto de desenfoque subyacente
- DWM (Administrador de ventanas de escritorio), efecto de desenfoque subyacente
- efecto de desenfoque subyacente
- efecto translúcido
- efecto de cristal transparente
- Administrador de ventanas de escritorio (DWM), efecto translúcido
- DWM (Administrador de ventanas de escritorio), efecto translúcido
- Administrador de ventanas de escritorio (DWM), efecto de cristal transparente
- DWM (Administrador de ventanas de escritorio), efecto de cristal transparente
- Administrador de ventanas de escritorio (DWM), ampliar el marco de ventana en el área de cliente
- DWM (Administrador de ventanas de escritorio), ampliación del marco de ventana en el área de cliente
- ampliación del marco de ventana en el área de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7b357719ea3aa5a4853a933350ee2dda417842777354e2bbf1711e1cbeff1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456090"
---
# <a name="dwm-blur-behind-overview"></a>Información general sobre el desenfoque de DWM

Uno de los efectos de Administrador de ventanas de escritorio firma (DWM) es un área no cliente translúcida y desenfoque. Las API de DWM permiten a las aplicaciones aplicar estos efectos al área cliente de sus ventanas de nivel superior.

> [!Note]  
> Windows La edición Vista Home Basic no admite el efecto de cristal transparente. Las áreas que normalmente se representaría con el efecto de cristal transparente en otras ediciones Windows se representan como opacas.
> A partir Windows 8, llamar a esta función no da como resultado el efecto de desenfoque, debido a un cambio de estilo en la forma en que se representan las ventanas.


 

En este tema se de abordan los siguientes escenarios de desenfoque de cliente que habilita DWM.

-   [Agregar desenfoque a una región específica del área cliente](#adding-blur-to-a-specific-region-of-the-client-area)
-   [Extender el marco de ventana al área cliente](#extending-the-window-frame-into-the-client-area)
-   [Temas relacionados](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a>Agregar desenfoque a una región específica del área cliente

Una aplicación puede aplicar el efecto de desenfoque detrás de toda la región de cliente de la ventana o a una subregión específica. Esto permite a las aplicaciones agregar rutas de acceso con estilo y barras de búsqueda que son visualmente independientes del resto de la aplicación.

La API que se usa en este escenario es la función [**DwmEnableBlurBehindWindow,**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) que usa las constantes de desenfoque de [**DWM subyacentes**](dwm-bb-constants.md) y la estructura [**\_ BLURBEHIND de DWM.**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)

La siguiente función de ejemplo, , muestra cómo aplicar el efecto de desenfoque `EnableBlurBehind` subyacente a toda la ventana.


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



Tenga en **cuenta que se** especifica NULL en el parámetro *hRgnBlur.* Esto indica al DWM que aplique el desenfoque detrás de toda la ventana.

En la imagen siguiente se muestra el efecto de desenfoque subyacente aplicado a toda la ventana.

![efecto de desenfoque subyacente aplicado a una ventana](images/dwm-blurbehindwindow.png)

Para aplicar el desenfoque detrás de una subregión, aplique un identificador de región válido (HRGN) al **miembro hRgnBlur** de la estructura [**\_ DWM BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) y agregue la marca **DWM \_ BB \_ BLURREGION** al **miembro dwFlags.**

Cuando se aplica el efecto de desenfoque subyacente a una subregión de la ventana, el canal alfa de la ventana se usa para el área no ablaurizada. Esto puede provocar una transparencia inesperada en la región no abierta de una ventana. Por lo tanto, tenga cuidado al aplicar un efecto de desenfoque a una subregión.

## <a name="extending-the-window-frame-into-the-client-area"></a>Extender el marco de ventana al área cliente

Una aplicación puede extender el desenfoque del marco de ventana al área de cliente. Esto resulta útil cuando se aplica el efecto de desenfoque detrás de una ventana con una barra de herramientas acoplada o controles separados visualmente del resto de una aplicación. La función [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) expone esta funcionalidad.

Para habilitar el desenfoque mediante [**DwmExtendFrameIntoClientArea,**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)use la estructura [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) para indicar cuánto se extenderá al área cliente. La siguiente función de ejemplo, , alterna la extensión de desenfoque en la parte inferior del marco que no `ExtendIntoClientBottom` es de cliente en el área de cliente.


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



En la imagen siguiente se muestra el efecto de desenfoque subyacente extendido en la parte inferior del área cliente.

![imagen que muestra el efecto de desenfoque subyacente extendido en la parte inferior de un área de cliente](images/dwm-extendedbottom.png)

También está disponible a través del método [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) es el efecto "hoja de cristal", donde el efecto de desenfoque se aplica a toda la superficie de la ventana sin un borde de ventana visible. En el ejemplo siguiente se muestra este efecto en el que el área de cliente se representa sin un borde de ventana.


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



En la imagen siguiente se muestra el desenfoque subyacente en el estilo de ventana "hoja de cristal".

![imagen que muestra el efecto de desenfoque subyacente en el estilo de ventana de "hoja de cristal"](images/dwm-sheetofglass.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desktop Window Manager Overview](dwm-overview.md) (Administrador de ventanas de escritorio)
</dt> <dt>

[Habilitar y controlar la composición de DWM](composition-ovw.md)
</dt> <dt>

[Consideraciones de rendimiento y procedimientos recomendados](bestpractices-ovw.md)
</dt> </dl>

 

 