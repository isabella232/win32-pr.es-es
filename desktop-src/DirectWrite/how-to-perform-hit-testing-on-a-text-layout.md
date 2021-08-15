---
title: Cómo realizar pruebas de acceso en un diseño de texto
description: Proporciona un breve tutorial sobre cómo agregar pruebas de acceso a una aplicación DirectWrite que muestra texto mediante la interfaz IDWriteTextLayout.
ms.assetid: ef30c931-10f6-4317-b2ea-b446990778b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d42967b069a7a5008de75c1cecb453a6158857eb2b05d2dd0298584a67cef69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816579"
---
# <a name="how-to-perform-hit-testing-on-a-text-layout"></a>Cómo realizar pruebas de acceso en un diseño de texto

Proporciona un breve tutorial sobre cómo agregar pruebas de acceso a una aplicación [DirectWrite](direct-write-portal.md) que muestra texto mediante la [**interfaz IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

El resultado de este tutorial es una aplicación que subraya el carácter en el que se hace clic con el botón izquierdo del mouse, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de "haga clic en este texto"](images/hittest.png)

Este procedimiento contiene las siguientes partes:

- [Paso 1: Crear un diseño de texto.](#step-1-create-a-text-layout)
- [Paso 2: Agregar un método OnClick.](#step-2-add-an-onclick-method)
- [Paso 3: Realizar pruebas de impacto.](#step-3-perform-hit-testing)
- [Paso 4: Subraya el texto en el que se ha hecho clic.](#step-4-underline-the-clicked-text)
- [Paso 5: Controlar el mensaje \_ WM LBUTTONDOWN.](/windows)

## <a name="step-1-create-a-text-layout"></a>Paso 1: Crear un diseño de texto.

Para empezar, necesitará una aplicación que use un [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Si ya tiene una aplicación que muestra texto con un diseño de texto, vaya al paso 2.

Para agregar un diseño de texto, debe hacer lo siguiente:

1. Declare un puntero a una [**interfaz IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase .

    ```cpp
    IDWriteTextLayout* pTextLayout_;
    ```

2. Al final del método **CreateDeviceIndependentResources,** cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al [**método CreateTextLayout.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout)

    ```cpp
    // Create a text layout using the text format.
    if (SUCCEEDED(hr))
    {
        RECT rect;
        GetClientRect(hwnd_, &rect); 
        float width  = rect.right  / dpiScaleX_;
        float height = rect.bottom / dpiScaleY_;

        hr = pDWriteFactory_->CreateTextLayout(
            wszText_,      // The string to be laid out and formatted.
            cTextLength_,  // The length of the string.
            pTextFormat_,  // The text format to apply to the string (contains font information, etc).
            width,         // The width of the layout box.
            height,        // The height of the layout box.
            &pTextLayout_  // The IDWriteTextLayout interface pointer.
            );
    }
    ```

3. A continuación, debe cambiar la llamada al método [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) a [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) como se muestra en el código siguiente.

    ```cpp
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    ```

## <a name="step-2-add-an-onclick-method"></a>Paso 2: Agregar un método OnClick.

Ahora agregue un método a la clase que usará la funcionalidad de prueba de acceso del diseño de texto.

1. Declare un **método OnClick** en el archivo de encabezado de clase.

    ```cpp
    void OnClick(
        UINT x,
        UINT y
        );
    ```

2. Defina un **método OnClick** en el archivo de implementación de clase.

   ```cpp
    void DemoApp::OnClick(UINT x, UINT y)
    {    
    }
    ```

## <a name="step-3-perform-hit-testing"></a>Paso 3: Realizar pruebas de impacto.

Para determinar dónde el usuario ha hecho clic en el diseño de texto, usaremos el [**método IDWriteTextLayout::HitTestPoint.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)

Agregue lo siguiente al **método OnClick** que definió en el paso 2.

1. Declare las variables que se pasarán como parámetros al método .

    ```cpp
    DWRITE_HIT_TEST_METRICS hitTestMetrics;
    BOOL isTrailingHit;
    BOOL isInside; 
    ```

    El [**método HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) genera los parámetros siguientes.

    | Variable         | Descripción                                                                                                                             |
    |------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
    | *hitTestMetrics* | Geometría que incluye completamente la ubicación de la prueba de impacto.                                                                                     |
    | *isInside*       | Indica si la ubicación de la prueba de éxito está dentro de la cadena de texto o no. Cuando es FALSE, se devuelve la posición más cercana al borde del texto. |
    | *isTrailingHit*  | Indica si la ubicación de la prueba de posición está en el lado inicial o final del carácter.                                        |

2. Llame al [**método HitTestPoint**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint) del [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

    ```cpp
    pTextLayout_->HitTestPoint(
                    (FLOAT)x, 
                    (FLOAT)y,
                    &isTrailingHit,
                    &isInside,
                    &hitTestMetrics
                    );
    ```

    El código de este ejemplo pasa las variables *x* e *y* para la posición sin ninguna modificación. Esto se puede hacer en este ejemplo porque el diseño de texto tiene el mismo tamaño que la ventana y se origina en la esquina superior izquierda de la ventana. Si este no fuera el caso, tendría que determinar las coordenadas en relación con el origen del diseño de texto.

## <a name="step-4-underline-the-clicked-text"></a>Paso 4: Subraya el texto en el que se ha hecho clic.

Agregue lo siguiente a **OnClick** que definió en el paso 2, después de la llamada al [**método HitTestPoint.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint)

```cpp
if (isInside == TRUE)
{
    BOOL underline;

    pTextLayout_->GetUnderline(hitTestMetrics.textPosition, &underline);

    DWRITE_TEXT_RANGE textRange = {hitTestMetrics.textPosition, 1};

    pTextLayout_->SetUnderline(!underline, textRange);
}
```

Este código hace lo siguiente.

1. Comprueba si el punto de prueba de acceso estaba dentro del texto mediante la variable *isInside.*
2. El **miembro textPosition** de la *estructura hitTestMetrics* contiene el índice de base cero del carácter en el que se ha hecho clic.

    Obtiene el subrayado de este carácter pasando este valor al [**método IDWriteTextLayout::GetUnderline.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline)

3. Declara una variable [**DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) con la posición inicial establecida en **hitTestMetrics.textPosition** y una longitud de 1.
4. Alterna el subrayado mediante el [**método IDWriteTextLayout::SetUnderline.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline)

Después de establecer el subrayado, vuelva a dibujar el texto llamando al **método DrawD2DContent** de la clase .

```cpp
DrawD2DContent();
```

## <a name="step-5-handle-the-wm_lbuttondown-message"></a>Paso 5: Controlar el mensaje \_ WM LBUTTONDOWN.

Por último, agregue **el mensaje \_ WM LBUTTONDOWN** al controlador de mensajes de la aplicación y llame al **método OnClick** de la clase .

```cpp
case WM_LBUTTONDOWN:
    {
        int x = GET_X_LPARAM(lParam); 
        int y = GET_Y_LPARAM(lParam);

        pDemoApp->OnClick(x, y);
    }
    break;
```

**GET \_ Las macros \_ X LPARAM** **y GET X \_ \_ LPARAM** se declaran en el archivo de encabezado windowsx.h. Recuperan fácilmente la posición x e y del clic del mouse.
