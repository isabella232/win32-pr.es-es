---
title: Interoperación con GDI
description: DirectWrite proporciona una ruta de migración del modelo de fuente de GDI y cierta interoperabilidad con él, así como interfaces para representar texto en un mapa de bits que se puede dibujar en una ventana.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite,interoperación GDI
- DirectWrite,interoperabilidad
- interoperabilidad
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274916"
---
# <a name="interoperating-with-gdi"></a>Interoperación con GDI

[DirectWrite](direct-write-portal.md) proporciona una ruta de migración a partir del modelo de fuente de GDI y cierta interoperabilidad con él, así como interfaces para representar texto en un mapa de bits que se puede dibujar en una ventana.

Esta información general contiene las siguientes partes:

-   [Introducción](#introduction)
-   [Parte 1: IDWriteGdiInterop](#part-1-idwritegdiinterop)
-   [Parte 2: Objetos de fuente](#part-2-font-objects)
-   [Parte 3: Representación](#part-3-rendering)

## <a name="introduction"></a>Introducción

[DirectWrite](direct-write-portal.md) proporciona métodos para convertir entre la estructura LOGFONT de GDI y DirectWrite interfaces de fuente. Esto le permite usar GDI para algunas o todas las enumeraciones y selecciones de fuentes, al tiempo que aprovecha la funcionalidad y el rendimiento mejorados de DirectWrite. DirectWrite interfaces para representar un mapa de bits si desea mostrar texto en una superficie GDI.

## <a name="part-1-idwritegdiinterop"></a>Parte 1: IDWriteGdiInterop

La [**interfaz IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) se usa para convertir entre estructuras de fuentes GDI e interfaces de fuente [DirectWrite,](direct-write-portal.md) y también para crear un objeto [**IDWriteBitmapRenderTarget.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) Obtenga un **objeto IDWriteGdiInterop** mediante el método [**IDWriteFactory::GetGdiInterop,**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) como se muestra en el código siguiente.


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a>Parte 2: Objetos de fuente

GDI usa la estructura LOGFONT para almacenar información sobre la fuente y el estilo del texto. El [**método IDWriteGdiInterop::CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) convertirá una estructura LOGFONT en un objeto [**IDWriteFont,**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) como se muestra en el código siguiente.


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



Sin embargo, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) no encapsula toda la misma información que un LOGFONT. Una estructura LOGFONT contiene el tamaño de fuente, el peso, el estilo, el subrayado, el tachón, el nombre de la cara de fuente y otra información. **Los objetos IDWriteFont** contienen información sobre una fuente y su peso y estilo, pero no el tamaño de fuente, el subrayado, y así sucesivamente. Con [DirectWrite](direct-write-portal.md), los elementos de información de formato como estos se encapsulan mediante un objeto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o, para intervalos específicos de texto, un [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Tiene la opción de convertir [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) en LOGFONT mediante [**IDWriteGdiInterop::ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).

## <a name="part-3-rendering"></a>Parte 3: Representación

Para representar DirectWrite texto en una superficie GDI, use un representador de texto personalizado. Consulte el tema Render to a GDI Surface (Representar [en una superficie GDI).](render-to-a-gdi-surface.md)

 

 