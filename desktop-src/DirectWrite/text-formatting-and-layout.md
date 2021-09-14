---
title: Formato y diseño de texto
description: DirectWrite proporciona dos interfaces para dar formato al texto IDWriteTextFormat e IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite,formato de texto
- DirectWrite,layout
- DirectWrite,IDWriteTextFormat (interfaz)
- DirectWrite,interfaz IDWriteTextLayout
- Interfaz IDWriteTextFormat
- Interfaz IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e5790742a3d3caf7f962a6b5e2b3111c626f28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069969"
---
# <a name="text-formatting-and-layout"></a>Formato y diseño de texto

[DirectWrite](direct-write-portal.md) proporciona dos interfaces para dar formato al texto: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextFormat** solo describe el formato de texto y se usa en casos en los que una cadena completa debe tener el mismo tamaño de fuente, estilo, peso, entre otros. Por otro lado, **IDWriteTextLayout** encapsula una cadena de texto y el formato de los intervalos especificados de la cadena. En este documento se describe cada interfaz y sus usos. Para obtener más información sobre la creación y los métodos de estas interfaces, vea las páginas de referencia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) [**e IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Este documento contiene las siguientes partes:

-   [IDWriteTextFormat](#modifying-an-idwritetextformat)
    -   [Modificar un IDWriteTextFormat](#modifying-an-idwritetextformat)
-   [IDWriteTextLayout](#idwritetextlayout)
    -   [Aplicar formato a un intervalo de texto](#formatting-a-range-of-text)
    -   [Opciones de representación](#rendering-options)

## <a name="idwritetextformat"></a>IDWriteTextFormat

Un [**objeto IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se usa para:

-   Describa el formato de una cadena completa al representarla. Para representar una cadena con varios formatos, use [**un objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
-   Especifique el formato de texto predeterminado al crear un [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Para crear un objeto [**IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) use el método [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) y especifique la familia de fuentes, la colección de fuentes, el grosor de la fuente, el tamaño de fuente (en DIP), el nombre de la configuración regional.

### <a name="modifying-an-idwritetextformat"></a>Modificar un IDWriteTextFormat

Una vez creada una interfaz [**IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) no se pueden cambiar algunos valores: la familia de fuentes, la colección, el peso y el tamaño, así como el nombre de la configuración regional. Para cambiar estos valores, se debe crear un nuevo objeto **IDWriteTextFormat.**

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) permite cambiar las propiedades anteriores sin volver a crear nada. [**IDWriteTextFormat permite**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) realizar cambios de formato que se aplican a todo el texto, como la alineación de texto. Si desea aplicar formato a intervalos de caracteres específicos, debe hacerlo mediante un **IDWriteTextLayout**.

[**IDWriteTextFormat proporciona métodos**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) para establecer la alineación del texto, la dirección del flujo, el tabulador incremental, el espaciado de línea, la alineación de párrafos, el recorte y el ajuste de palabras. Estas propiedades se pueden cambiar en cualquier momento después de la creación del **objeto IDWriteTextFormat.**

## <a name="idwritetextlayout"></a>IDWriteTextLayout

La [**interfaz IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) a diferencia [**de IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)representa un bloque de texto y el formato asociado. **IDWriteTextFormat representa** la información de formato inicial. En el ejemplo siguiente se muestra cómo crear un **objeto IDWriteTextLayout** mediante [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).


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



El texto de un [**objeto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) no se puede cambiar una vez creado el objeto. Para cambiar el texto, debe eliminar el objeto existente y crear un nuevo **objeto IDWriteTextLayout.**

Puede usar un [**IDWriteTextLayout para**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) dar formato a los intervalos de texto especificados. **IDWriteTextLayout también** proporciona métodos para cambiar el estilo y el peso de la fuente, y agregar características de fuente OpenType y pruebas de acceso. Para obtener más información y una lista completa de métodos, vea la [**página de referencia de IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

### <a name="formatting-a-range-of-text"></a>Aplicar formato a un intervalo de texto

[**IDWriteTextLayout proporciona**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) varios métodos para dar formato a intervalos de texto. Cada uno de estos métodos toma una estructura [**DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) como parámetro para especificar la posición inicial del texto dentro de la cadena y la longitud del intervalo al que se va a dar formato. En el ejemplo siguiente se muestra cómo establecer el grosor de fuente de un intervalo de texto en negrita.


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a>Opciones de representación

El texto con formato descrito por solo un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) se puede representar con [Direct2D;](../direct2d/direct2d-portal.md)sin embargo, hay algunas opciones más para representar un objeto [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

La cadena descrita por un [**objeto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) se puede representar mediante los métodos siguientes.

1.  [Representar mediante Direct2D.](rendering-by-using-direct2d.md)
2.  [Representar mediante un representador de texto personalizado.](how-to-implement-a-custom-text-renderer.md)
3.  [Representar en una superficie GDI.](render-to-a-gdi-surface.md)

 

 
