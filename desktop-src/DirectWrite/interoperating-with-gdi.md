---
title: Interoperar con GDI
description: DirectWrite proporciona una ruta de migración desde, y alguna interoperabilidad con, modelo de fuente de GDI, así como interfaces para representar texto en un mapa de bits que se puede dibujar en una ventana.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, interoperación GDI
- DirectWrite, interoperabilidad
- interoperabilidad
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077794"
---
# <a name="interoperating-with-gdi"></a>Interoperar con GDI

[DirectWrite](direct-write-portal.md) proporciona una ruta de migración desde, y alguna interoperabilidad con, modelo de fuente de GDI, así como interfaces para representar texto en un mapa de bits que se puede dibujar en una ventana.

Esta información general contiene las siguientes partes:

-   [Introducción](#introduction)
-   [Parte 1: IDWriteGdiInterop](#part-1-idwritegdiinterop)
-   [Parte 2: objetos de fuente](#part-2-font-objects)
-   [Parte 3: representación](#part-3-rendering)

## <a name="introduction"></a>Introducción

[DirectWrite](direct-write-portal.md) proporciona métodos para la conversión entre la estructura LOGFONT de GDI y las interfaces de fuente de DirectWrite. Esto le permite usar GDI para algunas o todas las enumeraciones y selección de fuentes, a la vez que aprovecha la funcionalidad mejorada y el rendimiento de DirectWrite. DirectWrite también tiene interfaces para representar en un mapa de bits si desea mostrar texto en una superficie de GDI.

## <a name="part-1-idwritegdiinterop"></a>Parte 1: IDWriteGdiInterop

La interfaz [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) se usa para convertir entre estructuras de fuentes de GDI e interfaces de fuente de [DirectWrite](direct-write-portal.md) , y también para crear un objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) . Obtenga un objeto **IDWriteGdiInterop** mediante el método [**IDWriteFactory:: GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , como se muestra en el código siguiente.


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a>Parte 2: objetos de fuente

GDI utiliza la estructura LOGFONT para almacenar información sobre la fuente y el estilo del texto. El método [**IDWriteGdiInterop:: CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) convertirá una estructura LOGFONT en un objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , como se aprecia en el código siguiente.


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



Sin embargo, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) no encapsula toda la información que realiza un LogFont. Una estructura LOGFONT contiene el tamaño de fuente, el peso, el estilo, el subrayado, el tachado, el nombre de la fuente y otro tipo de información. Los objetos **IDWriteFont** contienen información sobre una fuente y su peso y estilo, pero no el tamaño de fuente, el subrayado, etc. Con [DirectWrite](direct-write-portal.md), los elementos de información de formato, como estos, se encapsulan con un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o, para rangos de texto concretos, un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

Tiene la opción de convertir un [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) en LOGFONT mediante [**IDWriteGdiInterop:: ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).

## <a name="part-3-rendering"></a>Parte 3: representación

Para representar el texto de DirectWrite en una superficie de GDI, se usa un representador de texto personalizado. Vea el tema [representar en una superficie de GDI](render-to-a-gdi-surface.md) .

 

 