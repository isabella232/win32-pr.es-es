---
title: Tutorial Tareas iniciales con DirectWrite
description: En este documento se muestra cómo usar DirectWrite y Direct2D para crear texto simple que contiene un único formato y, a continuación, texto que contiene varios formatos.
ms.assetid: cc2758d7-3f47-452a-8d81-3f777fe490ec
keywords:
- DirectWrite,tutorial
- DirectWrite tutorial de introducción
- DirectWrite,Direct2D
- Direct2D
- DirectWrite,IDWriteTextLayout (interfaz)
- Interfaz IDWriteTextLayout
- DirectWrite interfaz IDWriteTypography
- Interfaz IDWriteTypography
- DirectWrite,IDWriteTextFormat (interfaz)
- Interfaz IDWriteTextFormat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ab22f611ea4658870990002bf98ac3c2ab9ffec32405ed8e67c32b819406496
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083485"
---
# <a name="tutorial-getting-started-with-directwrite"></a>Tutorial: Tareas iniciales con DirectWrite

En este documento se muestra cómo usar [DirectWrite](direct-write-portal.md) [y Direct2D](rendering-by-using-direct2d.md) para crear texto simple que contiene un único formato y, a continuación, texto que contiene varios formatos.

Este tutorial contiene las siguientes partes:

-   [Código fuente](#source-code)
-   [Dibujar texto simple](#drawing-simple-text)
    -   [Parte 1: Declarar recursos DirectWrite y Direct2D.](#part-1-declare-directwrite-and-direct2d-resources)
    -   [Parte 2: Crear recursos independientes del dispositivo.](#part-2-create-device-independent-resources)
    -   [Parte 3: Crear Device-Dependent recursos.](#part-3-create-device-dependent-resources)
    -   [Parte 4: Dibujar texto mediante el método DrawText de Direct2D.](#part-4-draw-text-by-using-the-direct2d-drawtext-method)
    -   [Parte 5: Representación del contenido de la ventana mediante Direct2D](#part-5-render-the-window-contents-using-direct2d)
-   [Dibujar texto con varios formatos.](#drawing-text-with-multiple-formats)
    -   [Parte 1: Crear una interfaz IDWriteTextLayout.](#part-1-create-an-idwritetextlayout-interface)
    -   [Parte 2: Aplicar formato con IDWriteTextLayout.](#part-2-applying-formatting-with-idwritetextlayout)
    -   [Parte 3: Agregar características tipográficas con IDWriteTypography.](#part-3-adding-typographic-features-with-idwritetypography)
    -   [Parte 4: Dibujar texto mediante el método DrawTextLayout de Direct2D.](#part-4-draw-text-using-the-direct2d-drawtextlayout-method)

## <a name="source-code"></a>Código fuente

El código fuente que se muestra en esta información general se toma del DirectWrite Hola mundo [ejemplo](/samples/browse/?redirectedfrom=MSDN-samples). Cada parte se implementa en una clase independiente (SimpleText y MultiformattedText) y se muestra en una ventana secundaria independiente. Cada clase representa una ventana de Microsoft Win32. Además del método *WndProc,* cada clase contiene los métodos siguientes:



| Función                              | Descripción                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| **CreateDeviceIndependentResources**  | Crea recursos que son independientes del dispositivo, por lo que se pueden reutilizar en cualquier lugar.                      |
| **DiscardDeviceIndependentResources** | Libera los recursos independientes del dispositivo una vez que ya no son necesarios.                          |
| **CreateDeviceResources**             | Crea recursos, como pinceles y destinos de representación, que están asociados a un dispositivo determinado.        |
| **DiscardDeviceResources**            | Libera los recursos dependientes del dispositivo una vez que ya no son necesarios.                            |
| **DrawD2DContent**                    | Usa [Direct2D para](../direct2d/direct2d-portal.md) representar en la pantalla.                              |
| **Drawtext**                          | Dibuja la cadena de texto mediante [Direct2D.](../direct2d/direct2d-portal.md)                            |
| **Onresize**                          | Cambia el tamaño [del destino de representación de Direct2D](../direct2d/direct2d-portal.md) cuando se cambia el tamaño de la ventana. |



 

Puede usar el ejemplo proporcionado o usar las instrucciones siguientes para agregar [DirectWrite](direct-write-portal.md) [y Direct2D](rendering-by-using-direct2d.md) a su propia aplicación Win32. Para obtener más información sobre el ejemplo y los archivos de proyecto asociados, vea el [ejemplo DirectWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples).

## <a name="drawing-simple-text"></a>Dibujar texto simple

En esta sección se muestra cómo [usar DirectWrite](direct-write-portal.md) [y Direct2D](../direct2d/direct2d-portal.md) para representar texto simple con un único formato, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de "Hello world using directwrite!" en un solo formato](images/simplecropped.png)

Dibujar texto simple en la pantalla requiere cuatro componentes:

-   Cadena de caracteres que se representará.
-   Instancia de [**IDWriteTextFormat.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
-   Dimensiones del área que contiene el texto.
-   Objeto que puede representar el texto. En este tutorial. usa un destino [de representación de Direct2D.](../direct2d/direct2d-portal.md)

La [**interfaz IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) describe el nombre, el tamaño, el peso, el estilo y el stretch de la familia de fuentes que se usan para dar formato al texto y se describe la información de configuración regional. **IDWriteTextFormat también** define métodos para establecer y obtener las siguientes propiedades:

-   Espaciado de línea.
-   Alineación del texto con respecto a los bordes izquierdo y derecho del cuadro de diseño.
-   Alineación del párrafo con respecto a la parte superior e inferior del cuadro de diseño.
-   Dirección de lectura.
-   Granularidad de recorte de texto para el texto que desborda el cuadro de diseño.
-   La tabulación incremental se detiene.
-   Dirección del flujo de párrafo.

La [**interfaz IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) es necesaria para dibujar texto que usa ambos procesos descritos en este documento.

Para poder crear un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o cualquier otro objeto [DirectWrite,](direct-write-portal.md) necesita una [**instancia de IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) Se usa una **instancia de IDWriteFactory para** crear instancias **IDWriteTextFormat** y otros DirectWrite objetos. Para obtener una instancia de generador, use la [**función DWriteCreateFactory.**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory)

### <a name="part-1-declare-directwrite-and-direct2d-resources"></a>Parte 1: Declarar recursos DirectWrite y Direct2D.

En esta parte, declarará los objetos que usará más adelante para crear y mostrar texto como miembros de datos privados de la clase. Todas las interfaces, funciones y tipos de datos de [DirectWrite](direct-write-portal.md) se declaran en el archivo de encabezado *dwrite.h* y las de [Direct2D](../direct2d/direct2d-portal.md) se declaran en *d2d1.h*; Si aún no lo ha hecho, incluya estos encabezados en el proyecto.

1.  En el archivo de encabezado de clase (SimpleText.h), declare punteros a las interfaces [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) e [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) como miembros privados.
    ```C++
    IDWriteFactory* pDWriteFactory_;
    IDWriteTextFormat* pTextFormat_;
    
    ```

    

2.  Declare miembros para contener la cadena de texto que se representará y la longitud de la cadena.
    ```C++
    const wchar_t* wszText_;
    UINT32 cTextLength_;
    
    ```

    

3.  Declare punteros a las interfaces [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para representar el texto con [Direct2D.](../direct2d/direct2d-portal.md)
    ```C++
    ID2D1Factory* pD2DFactory_;
    ID2D1HwndRenderTarget* pRT_;
    ID2D1SolidColorBrush* pBlackBrush_;
    
    ```

    

### <a name="part-2-create-device-independent-resources"></a>Parte 2: Crear recursos independientes del dispositivo.

[Direct2D proporciona](rendering-by-using-direct2d.md) dos tipos de recursos: recursos dependientes del dispositivo y recursos independientes del dispositivo. Los recursos dependientes del dispositivo están asociados a un dispositivo de representación y ya no funcionan si se quita ese dispositivo. Por otro lado, los recursos independientes del dispositivo pueden durar para el ámbito de la aplicación.

[DirectWrite](direct-write-portal.md) recursos son independientes del dispositivo.

En esta sección, creará los recursos independientes del dispositivo que usa la aplicación. Estos recursos deben liberarse con una llamada al **método Release** de la interfaz .

Algunos de los recursos que se usan tienen que crearse solo una vez y no están vinculados a un dispositivo. La inicialización de estos recursos se coloca en el método *SimpleText::CreateDeviceIndependentResources,* al que se llama al inicializar la clase.

1.  Dentro del método *SimpleText::CreateDeviceIndependentResources* del archivo de implementación de clase (SimpleText.cpp), llame a la función [**D2D1CreateFactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) para crear una interfaz [**ID2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que es la interfaz de generador raíz para todos los objetos [direct2D.](../direct2d/direct2d-portal.md) Use el mismo generador para crear instancias de otros recursos de Direct2D.
    ```C++
    hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &pD2DFactory_
        );
    
    ```

    

2.  Llame a [**la función DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) para crear una interfaz [**IDWriteFactory,**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) que es la interfaz de generador raíz para todos [los DirectWrite](direct-write-portal.md) datos. Use el mismo generador para crear instancias de otros DirectWrite recursos.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory_)
            );
    }
    
    ```

    

3.  Inicialice la cadena de texto y almacene su longitud.

    ```C++
    wszText_ = L"Hello World using  DirectWrite!";
    cTextLength_ = (UINT32) wcslen(wszText_);
    
    ```

    

4.  Cree un [**objeto de interfaz IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) mediante el [**método IDWriteFactory::CreateTextFormat.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) **IDWriteTextFormat** especifica la fuente, el peso, el stretch, el estilo y la configuración regional que se usarán para representar la cadena de texto.
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTextFormat(
            L"Gabriola",                // Font family name.
            NULL,                       // Font collection (NULL sets it to use the system font collection).
            DWRITE_FONT_WEIGHT_REGULAR,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            72.0f,
            L"en-us",
            &pTextFormat_
            );
    }
    
    ```

    

5.  Centre el texto horizontal y verticalmente mediante una llamada a los métodos [**IDWriteTextFormat::SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) e [**IDWriteTextFormat::SetParagraphAlignment.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment)
    ```C++
    // Center align (horizontally) the text.
    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTextFormat_->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    }
    
    ```

    

En esta parte, inicializó los recursos independientes del dispositivo que usa la aplicación. En la siguiente parte, inicializará los recursos dependientes del dispositivo.

### <a name="part-3-create-device-dependent-resources"></a>Parte 3: Crear Device-Dependent recursos.

En esta parte, creará un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) y un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) para representar el texto.

Un destino de representación es un objeto direct2D que crea recursos de dibujo y representa comandos de dibujo en un dispositivo de representación. [**Id2D1HwndRenderTarget es**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) un destino de representación que se representa en **un HWND.**

Uno de los recursos de dibujo que un destino de representación puede crear es un pincel para dibujar contornos, rellenos y texto. [**Id2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta con un color sólido.

Las interfaces [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) se enlazan a un dispositivo de representación cuando se crean y se deben liberar y volver a crear si el dispositivo deja de ser válido.

1.  Dentro del método SimpleText::CreateDeviceResources, compruebe si el puntero de destino de representación es **NULL.** Si es así, recupere el tamaño del área de representación y cree un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) de ese tamaño. Use **id2D1HwndRenderTarget para** crear un [**objeto ID2D1SolidColorBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
    ```C++
    RECT rc;
    GetClientRect(hwnd_, &rc);

    D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

    if (!pRT_)
    {
        // Create a Direct2D render target.
        hr = pD2DFactory_->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(
                    hwnd_,
                    size
                    ),
                &pRT_
                );

        // Create a black brush.
        if (SUCCEEDED(hr))
        {
            hr = pRT_->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black),
                &pBlackBrush_
                );
        }
    }
    
    ```

    

2.  En el método SimpleText::D iscardDeviceResources, libere el pincel y el destino de representación.
    ```C++
    SafeRelease(&pRT_);
    SafeRelease(&pBlackBrush_);
    
    ```

    

Ahora que ha creado un destino de representación y un pincel, puede usarlos para representar el texto.

### <a name="part-4-draw-text-by-using-the-direct2d-drawtext-method"></a>Parte 4: Dibujar texto mediante el método DrawText de Direct2D.

1.  En el método SimpleText::D rawText de la clase , defina el área para el diseño de texto recuperando las dimensiones del área de representación y cree un rectángulo [direct2D](../direct2d/direct2d-portal.md) que tenga las mismas dimensiones.
    ```C++
    D2D1_RECT_F layoutRect = D2D1::RectF(
        static_cast<FLOAT>(rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.top) / dpiScaleY_,
        static_cast<FLOAT>(rc.right - rc.left) / dpiScaleX_,
        static_cast<FLOAT>(rc.bottom - rc.top) / dpiScaleY_
        );
    
    ```

    

2.  Use el [**método ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) y el objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para representar texto en la pantalla. El **método ID2D1RenderTarget::D rawText** toma los parámetros siguientes:
    -   Cadena que se representará.
    -   Puntero a una [**interfaz IDWriteTextFormat.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
    -   Rectángulo [de diseño de Direct2D.](../direct2d/direct2d-portal.md)
    -   Puntero a una interfaz que expone [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush).

    ```C++
    pRT_->DrawText(
        wszText_,        // The string to render.
        cTextLength_,    // The string's length.
        pTextFormat_,    // The text format.
        layoutRect,       // The region of the window where the text will be rendered.
        pBlackBrush_     // The brush used to draw the text.
        );
    
    ```

    

### <a name="part-5-render-the-window-contents-using-direct2d"></a>Parte 5: Representación del contenido de la ventana mediante Direct2D

Para representar el contenido de la ventana mediante [Direct2D cuando](../direct2d/direct2d-portal.md) se recibe un mensaje de pintura, haga lo siguiente:

1.  Cree los recursos dependientes del dispositivo mediante una llamada al método SimpleText::CreateDeviceResources implementado en la parte 3.
2.  Llame al [**método ID2D1HwndRenderTarget::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) del destino de representación.
3.  Borre el destino de representación mediante una llamada al [**método ID2D1HwndRenderTarget::Clear.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))
4.  Llame al método SimpleText::D rawText, implementado en la parte 4.
5.  Llame al [**método ID2D1HwndRenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) del destino de representación.
6.  Si es necesario, descarte los recursos dependientes del dispositivo para que se puedan volver a crear cuando se vuelva a dibujar la ventana.


```C++
hr = CreateDeviceResources();

if (SUCCEEDED(hr))
{
    pRT_->BeginDraw();

    pRT_->SetTransform(D2D1::IdentityMatrix());

    pRT_->Clear(D2D1::ColorF(D2D1::ColorF::White));

    // Call the DrawText method of this class.
    hr = DrawText();

    if (SUCCEEDED(hr))
    {
        hr = pRT_->EndDraw(
            );
    }
}

if (FAILED(hr))
{
    DiscardDeviceResources();
}

```



La clase SimpleText se implementa en SimpleText.h y SimpleText.cpp.

## <a name="drawing-text-with-multiple-formats"></a>Dibujar texto con varios formatos.

En esta sección se muestra cómo [usar DirectWrite](direct-write-portal.md) [y Direct2D](../direct2d/direct2d-portal.md) para representar texto con varios formatos, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de "Hello world using directwrite!", con algunas partes en diferentes estilos, tamaños y formatos](images/multiformattedcropped.png)

El código de esta sección se implementa como la clase MultiformattedText en el [ejemplo DWriteHelloWorld](/samples/browse/?redirectedfrom=MSDN-samples). Se basa en los pasos de la sección anterior.

Para crear texto con formato múltiple, use la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) además de la interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) introducida en la sección anterior. La **interfaz IDWriteTextLayout** describe el formato y el diseño de un bloque de texto. Además del formato predeterminado especificado por un objeto **IDWriteTextFormat,** el formato de intervalos de texto específicos se puede cambiar mediante **IDWriteTextLayout**. Esto incluye el nombre de familia de fuentes, el tamaño, el peso, el estilo, el stretch, el tachado y la línea de base.

[**IDWriteTextLayout también**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) proporciona métodos de prueba de llamadas. Las métricas de prueba de llamadas devueltas por estos métodos son relativas al cuadro de diseño especificado cuando se crea el objeto de interfaz **IDWriteTextLayout** mediante el método [**CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) de la interfaz [**IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)

La [**interfaz IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) se usa para agregar características tipográficas [openType](../intl/opentype-font-format.md) opcionales a un diseño de texto, como bañadores y conjuntos de texto estilísticos alternativos. Las características tipográficas se pueden agregar a un intervalo específico de texto dentro de un diseño de texto mediante una llamada al método [**AddFontFeature**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature) de la **interfaz IDWriteTypography.** Este método recibe una estructura [**\_ DWRITE FONT \_ FEATURE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) como un parámetro que contiene una constante de enumeración **DWRITE \_ FONT FEATURE \_ \_ TAG** y un parámetro de ejecución **UINT32.** Puede encontrar una lista de características registradas de OpenType en el Registro [de etiquetas de](https://www.microsoft.com/typography/otspec/features_ae.htm) diseño de OpenType en microsoft.com. Para obtener el equivalente DirectWrite de enumeración, vea **DWRITE \_ FONT FEATURE \_ \_ TAG**.

### <a name="part-1-create-an-idwritetextlayout-interface"></a>Parte 1: Crear una interfaz IDWriteTextLayout.

1.  Declare un puntero a una [**interfaz IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) como miembro de la clase MultiformattedText.
    ```C++
    IDWriteTextLayout* pTextLayout_;
    
    ```

    

2.  Al final del método MultiformattedText::CreateDeviceIndependentResources, cree un objeto de interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) llamando al [**método CreateTextLayout.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) La **interfaz IDWriteTextLayout** proporciona características de formato adicionales, como la capacidad de aplicar formatos diferentes a partes seleccionadas de texto.
    ```C++
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

    

### <a name="part-2-applying-formatting-with-idwritetextlayout"></a>Parte 2: Aplicar formato con IDWriteTextLayout.

El formato, como el tamaño de fuente, el peso y la subrayado, se puede aplicar a las subcadenas del texto que se va a mostrar mediante la interfaz [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

1.  Establezca el tamaño de fuente de la subcadena "Di" de "DirectWrite" en 100 declarando [**DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) y llamando al método [**IDWriteTextLayout::SetFontSize.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize)
    ```C++
    // Format the "DirectWrite" substring to be of font size 100.
    if (SUCCEEDED(hr))
    {
        DWRITE_TEXT_RANGE textRange = {20,        // Start index where "DirectWrite" appears.
                                        6 };      // Length of the substring "Direct" in "DirectWrite".
        hr = pTextLayout_->SetFontSize(100.0f, textRange);
    }
    ```

    

2.  Subraya la subcadena "DirectWrite" llamando al [**método IDWriteTextLayout::SetUnderline.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline)
    ```C++
    // Format the word "DWrite" to be underlined.
    if (SUCCEEDED(hr))
    {
        
        DWRITE_TEXT_RANGE textRange = {20,      // Start index where "DirectWrite" appears.
                                       11 };    // Length of the substring "DirectWrite".
        hr = pTextLayout_->SetUnderline(TRUE, textRange);
    }
    ```

    

3.  Establezca el grosor de la fuente en negrita para la subcadena "DirectWrite" mediante una llamada al [**método IDWriteTextLayout::SetFontWeight.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight)
    ```C++
    if (SUCCEEDED(hr))
    {
        // Format the word "DWrite" to be bold.
        DWRITE_TEXT_RANGE textRange = {20,
                                       11 };
        hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
    }
    ```

    

### <a name="part-3-adding-typographic-features-with-idwritetypography"></a>Parte 3: Agregar características tipográficas con IDWriteTypography.

1.  Declare y cree un [**objeto de interfaz IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) llamando al [**método IDWriteFactory::CreateTypography.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtypography)
    ```C++
    // Declare a typography pointer.
    IDWriteTypography* pTypography = NULL;

    // Create a typography interface object.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory_->CreateTypography(&pTypography);
    }
    
    ```

    

2.  Agregue una característica de fuente declarando un objeto [**DWRITE \_ FONT \_ FEATURE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) que tenga especificado el conjunto estilístico 7 y llamando al [**método IDWriteTypography::AddFontFeature.**](/windows/win32/api/dwrite/nf-dwrite-idwritetypography-addfontfeature)
    ```C++
    // Set the stylistic set.
    DWRITE_FONT_FEATURE fontFeature = {DWRITE_FONT_FEATURE_TAG_STYLISTIC_SET_7,
                                       1};
    if (SUCCEEDED(hr))
    {
        hr = pTypography->AddFontFeature(fontFeature);
    }
    
    ```

    

3.  Establezca el diseño de texto para usar la tipografía en toda la cadena declarando una variable [**DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) y llamando al método [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) y pasando el intervalo de texto.
    ```C++
    if (SUCCEEDED(hr))
    {
        // Set the typography for the entire string.
        DWRITE_TEXT_RANGE textRange = {0,
                                       cTextLength_};
        hr = pTextLayout_->SetTypography(pTypography, textRange);
    }
    
    ```

    

4.  Establezca el nuevo ancho y alto para el objeto de diseño de texto en el método MultiformattedText::OnResize.
    ```C++
    if (pTextLayout_)
    {
        pTextLayout_->SetMaxWidth(static_cast<FLOAT>(width / dpiScaleX_));
        pTextLayout_->SetMaxHeight(static_cast<FLOAT>(height / dpiScaleY_));
    }
    ```

    

### <a name="part-4-draw-text-using-the-direct2d-drawtextlayout-method"></a>Parte 4: Dibujar texto mediante el método DrawTextLayout de Direct2D.

Para dibujar el texto con la configuración de diseño de texto especificada por el objeto [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) cambie el código del método MultiformattedText::D rawText para usar [**IDWriteTextLayout::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout).

1.  Delcare a [**D2D1 \_ POINT \_ 2F**](../direct2d/d2d1-point-2f.md) variable and set it to the upper-left point of the window.
    ```C++
    D2D1_POINT_2F origin = D2D1::Point2F(
        static_cast<FLOAT>(rc.left / dpiScaleX_),
        static_cast<FLOAT>(rc.top / dpiScaleY_)
        );
    
    ```

    

2.  Dibuje el texto en la pantalla llamando al método [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) del destino de representación de [Direct2D](../direct2d/direct2d-portal.md) y pasando el puntero [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
    ```C++
    pRT_->DrawTextLayout(
        origin,
        pTextLayout_,
        pBlackBrush_
        );
    
    ```

    

La clase MultiformattedText se implementa en MultiformattedText.h y MultiformattedText.cpp.

 

 