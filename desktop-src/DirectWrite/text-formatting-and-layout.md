---
title: Formato y diseño de texto
description: DirectWrite proporciona dos interfaces para dar formato al texto IDWriteTextFormat y IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, formato de texto
- DirectWrite, diseño
- DirectWrite, interfaz IDWriteTextFormat
- DirectWrite, interfaz IDWriteTextLayout
- Interfaz IDWriteTextFormat
- Interfaz IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fcf884c15015af2645c32e217d3b4a6b433554
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271347"
---
# <a name="text-formatting-and-layout"></a>Formato y diseño de texto

[DirectWrite](direct-write-portal.md) proporciona dos interfaces para dar formato al texto: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextFormat** describe solo el formato del texto y se utiliza en casos en los que una cadena completa debe ser del mismo tamaño de fuente, estilo, peso, etc. Por otro lado, **IDWriteTextLayout** encapsula una cadena de texto y el formato de los intervalos especificados de la cadena. En este documento se describe cada interfaz y sus usos. Para obtener más información sobre la creación y los métodos de estas interfaces, vea las páginas de referencia de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Este documento contiene las siguientes partes:

-   [IDWriteTextFormat](#modifying-an-idwritetextformat)
    -   [Modificar un IDWriteTextFormat](#modifying-an-idwritetextformat)
-   [IDWriteTextLayout](#idwritetextlayout)
    -   [Aplicar formato a un intervalo de texto](#formatting-a-range-of-text)
    -   [Opciones de representación](#rendering-options)

## <a name="idwritetextformat"></a>IDWriteTextFormat

Un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se usa para:

-   Describe el formato de una cadena completa cuando se representa. Para representar una cadena con varios formatos, use un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .
-   Especifique el formato de texto predeterminado al crear un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Para crear un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , se usa el método [**IDWriteFactory:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) y se especifica la familia de fuentes, la colección de fuentes, el espesor de fuente, el tamaño de fuente (en DIP) y el nombre de la configuración regional.

### <a name="modifying-an-idwritetextformat"></a>Modificar un IDWriteTextFormat

Una vez creada una interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , algunos valores no se pueden cambiar: la familia de fuentes, la colección, el peso y el tamaño, así como el nombre de la configuración regional. Para cambiar estos valores, se debe crear un nuevo objeto **IDWriteTextFormat** .

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) permite cambiar las propiedades anteriores sin volver a crear el elemento. [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) le permite realizar cambios en el formato que se aplican a todo el texto, como la alineación del texto. Si desea aplicar formato a intervalos de caracteres específicos, debe hacerlo mediante un **IDWriteTextLayout**.

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) proporciona métodos para establecer la alineación del texto, la dirección del flujo, la tabulación incremental, el interlineado, la alineación del párrafo, el recorte y el ajuste de línea. Estas propiedades se pueden cambiar en cualquier momento después de la creación del objeto **IDWriteTextFormat** .

## <a name="idwritetextlayout"></a>IDWriteTextLayout

La interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , a diferencia de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), representa un bloque de texto y el formato asociado. **IDWriteTextFormat** representa la información de formato inicial. En el ejemplo siguiente se muestra cómo crear un objeto **IDWriteTextLayout** mediante [**IDWriteFactory:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).


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



El texto de un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) no se puede cambiar una vez creado el objeto. Para cambiar el texto, debe eliminar el objeto existente y crear un nuevo objeto **IDWriteTextLayout** .

Puede usar un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) para dar formato a los intervalos de texto especificados. **IDWriteTextLayout** también proporciona métodos para cambiar el estilo y el peso de la fuente, y para agregar características de fuentes OpenType y pruebas de posicionamiento. Para obtener más información y una lista completa de los métodos, vea la página de referencia de [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

### <a name="formatting-a-range-of-text"></a>Aplicar formato a un intervalo de texto

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) proporciona varios métodos para dar formato a los intervalos de texto. Cada uno de estos métodos toma una estructura de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) como un parámetro para especificar la posición del texto inicial dentro de la cadena y la longitud del intervalo al que se va a dar formato. En el ejemplo siguiente se muestra cómo establecer el espesor de fuente de un intervalo de texto en negrita.


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a>Opciones de representación

El texto con formato descrito por solo un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se puede representar con [Direct2D](../direct2d/direct2d-portal.md); sin embargo, hay algunas opciones más para representar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

La cadena descrita por un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) se puede representar mediante los métodos siguientes.

1.  Se [representa mediante Direct2D](rendering-by-using-direct2d.md).
2.  Se [representa mediante un representador de texto personalizado](how-to-implement-a-custom-text-renderer.md).
3.  [Se representan en una superficie de GDI](render-to-a-gdi-surface.md).

 

 