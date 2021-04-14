---
title: Información general de DWriteCore
description: DWriteCore es la implementación de la reunión del proyecto de DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361806"
---
# <a name="dwritecore-overview"></a>Información general de DWriteCore

DWriteCore es la implementación de la [reunión del proyecto](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.

En este tema introductorio se describe qué es DWriteCore y se muestra cómo instalarlo en el entorno de desarrollo y programar con él.

## <a name="the-value-proposition-of-dwritecore"></a>La propuesta de valor de DWriteCore

[DirectWrite](./direct-write-portal.md) es compatible con una amplia gama de características que lo convierte en la herramienta de representación de fuentes preferida en Windows para la mayoría de las aplicaciones &mdash; , ya sea a través de llamadas directas o a través de [Direct2D](../direct2d/direct2d-portal.md). DirectWrite incluye un sistema de diseño de texto independiente del dispositivo, representación de texto de [Microsoft ClearType](/typography/cleartype/) de alta calidad, texto con aceleración de hardware, texto multiforma, características avanzadas de tipografía de [® OpenType](/typography/opentype/) , compatibilidad con idiomas amplio y diseño y representación compatibles con [GDI](../gdi/windows-gdi.md). DirectWrite ha estado disponible desde Windows Vista SP2 y ha evolucionado a lo largo de los años para incluir características más avanzadas, como fuentes variables, lo que permite a los desarrolladores aplicar estilos, pesos y otros atributos a una fuente con un solo recurso de fuente.

Debido a la larga duración de DirectWrite, sin embargo, los avances en el desarrollo han dado la idea de dejar versiones anteriores de Windows detrás. Además, el estado de DirectWrite como la tecnología de representación de texto Premier solo está limitado a Windows, lo que deja que las aplicaciones multiplataforma escriban su propia pila de representación de texto o que se basen en soluciones de terceros.

DWriteCore resuelve los problemas fundamentales de la característica de versión huérfana y la compatibilidad entre plataformas mediante la eliminación de la biblioteca del sistema y el destino de todos los puntos de conexión admitidos. Para ello, hemos integrado DWriteCore en la reunión de proyectos con una API pública que es compatible con todos los puntos de conexión de Windows hasta Windows 8 y abre la puerta para que la use entre plataformas.

El valor principal que DWriteCore le proporciona, como desarrollador, en Project reunion es que proporciona acceso a todas las características de DirectWrite actuales hasta el nivel inferior a Windows 8. Todas las características de DWriteCore funcionarán igual en todas las versiones de nivel inferior; en otras palabras, todas las características actuales funcionarán en Windows 8, 8,1 y todas las versiones de Windows 10, sin ninguna disparidad con respecto a las características que podrían funcionar en cada versión.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>Aplicación de demostración de DWriteCore &mdash; DWriteCoreGallery

DWriteCore se muestra por medio de la aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que ahora está disponible para su descarga y estudio.

## <a name="get-started-with-dwritecore"></a>Introducción a DWriteCore

En la versión preliminar de Project reunion 0,1, actualmente no se admite la instalación del paquete de NuGet de reunión del proyecto en sus propios proyectos. En su lugar, la opción admitida actualmente para su propia programación con DWriteCore es comenzar con el proyecto de aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) y basar el desarrollo en ese proyecto.

Después, puede quitar cualquier código fuente (o archivos) existente del proyecto de ejemplo y agregar cualquier nuevo código fuente (o archivos) al proyecto. Para obtener más información sobre la programación con DWriteCore, consulte la sección [programación con DWriteCore](#programming-with-dwritecore) más adelante en este tema.

## <a name="the-release-phases-of-dwritecore"></a>Fases de versión de DWriteCore

La migración de DirectWrite a DWriteCore es un proyecto suficientemente grande para abarcar varios ciclos de versión de Windows. Ese proyecto se divide en fases, cada una de las cuales corresponde a un fragmento de funcionalidad entregado en una versión.

### <a name="features-in-the-current-release-of-dwritecore"></a>Características de la versión actual de DWriteCore

La versión de DWriteCore disponible actualmente contiene las herramientas básicas que usted, como desarrollador, necesitan para consumir DWriteCore, incluidas las siguientes características.

- Enumeración de fuentes.
- API de fuentes.
- Forma.
- API de representación de bajo nivel. Esto es parcial en la fase actual &mdash; DWriteCore no interopera con [Direct2D](../direct2d/direct2d-portal.md), pero puede usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) y [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).
- Funcionalidad básica de diseño de texto.
- API de representación de texto.
- Destino de representación de mapa de bits.
- Fuentes de color.
- Optimizaciones misceláneas (limpieza de la caché de fuentes, cargador de fuentes en memoria, etc.).

La característica de pancarta en esta fase es fuentes de color. Las fuentes de color permiten representar las fuentes con una funcionalidad de color más sofisticada más allá de los simples colores sencillos. Por ejemplo, las fuentes de color son lo que impulsa la capacidad de representar las fuentes de Emoji y de los iconos de la barra de herramientas (por ejemplo, la última usada por Office). Las fuentes de color se introdujeron por primera vez en Windows 8.1, pero la característica se amplió mucho en Windows 10, versión 1607 (actualización de aniversario).

El trabajo de limpieza de la memoria caché de fuentes y el cargador de fuentes en memoria permiten una carga más rápida de fuentes y mejoras en la memoria.

Con estas características, puede empezar a aprovechar de inmediato algunas de las funcionalidades de núcleo moderno de DirectWrite, como las &mdash; fuentes variables de &mdash; nivel inferior a Windows 8. Esta iteración de la biblioteca también se puede consumir en [Android](https://www.android.com/)y **Linux**. Las fuentes variables son una de las características más importantes para los clientes de DirectWrite; se introdujeron en Windows 10, versión 1709 (Fall Creators Update), por lo que tener acceso a ellos en versiones anteriores es una gran ayuda como desarrollador.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Nuestra invitación a usted como desarrollador de DirectWrite

DWriteCore, junto con otros componentes de la reunión del proyecto, se desarrollarán con la apertura de los comentarios de los desarrolladores. Le invitamos a empezar a explorar DWriteCore y a proporcionar información o solicitudes en el desarrollo de características en nuestro [repositorio de github](https://github.com/microsoft/ProjectReunion/)de la Unión del proyecto.

## <a name="programming-with-dwritecore"></a>Programar con DWriteCore

Como ya se mencionó, para la versión preliminar del proyecto reunion 0,1, la opción admitida actualmente para su propia programación con DWriteCore es comenzar con el proyecto de aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

Al igual que con [DirectWrite](./direct-write-portal.md), puede programar con DWriteCore a través de su API de com-Light, a través de la interfaz [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .

**DWriteCoreGallery** ya incluye el `dwrite_core.h` archivo de encabezado. Dicho encabezado define primero el token *DWRITE_CORE* y, a continuación, lo incluye `dwrite_3.h` . El token *DWRITE_CORE* es importante, ya que dirige los encabezados incluidos posteriormente para que todas las API de DirectWrite estén disponibles. Una vez incluido un proyecto `dwrite_core.h` , puede continuar y escribir código, compilar y ejecutar.

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>API nuevas o diferentes para DWriteCore

La superficie de la API de DWriteCore es lo más grande que para [DirectWrite](/windows/win32/api/_directwrite/). Pero hay un pequeño número de API nuevas que solo están en DWriteCore en el momento actual.

#### <a name="create-a-restricted-factory-object"></a>Crear un objeto de generador restringido

La enumeración [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) tiene una nueva constante &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED**. Un generador restringido está más bloqueado que un generador aislado. No interactúa de ningún modo con una memoria caché de fuentes entre procesos ni persistentes. Además, la colección de fuentes del sistema devuelta desde este generador solo incluye fuentes conocidas. Aquí se muestra cómo se puede usar **DWRITE_FACTORY_TYPE_RESTRICTED** para crear un objeto de generador restringido cuando se llama a la función Free de [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

Si pasa **DWRITE_FACTORY_TYPE_RESTRICTED** a una versión anterior de DirectWrite que no lo admite, **DWriteCreateFactory** devuelve **E_INVALIDARG**.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Dibujar glifos en un mapa de bits de memoria del sistema

DirectWrite tiene una interfaz de destino de representación de mapas de bits que admite la representación de glifos en un mapa de bits en la memoria del sistema. Sin embargo, actualmente, la única manera de obtener acceso a los datos de píxeles subyacentes es pasar a través de GDI, por lo que la API no se puede usar entre plataformas. Esto se soluciona fácilmente agregando un método para recuperar los datos de píxeles.

Por lo tanto, DWriteCore introduce la interfaz [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) y su método [**IDWriteBitmapRenderTarget2:: GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md). Ese método toma un parámetro de tipo (puntero a) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), que es un nuevo struct.

La aplicación crea un destino de representación de mapa de bits llamando a [IDWriteGdiInterop:: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). En Windows, un destino de representación de mapas de bits encapsula un DC de memoria de GDI con un mapa de bits independiente del dispositivo GDI (DIB) seleccionado en él. [IDWriteBitmapRenderTarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) representa glifos en el Dib. DirectWrite representa los glifos en sí sin pasar por GDI. A continuación, la aplicación puede obtener la **HDC** del destino de representación del mapa de bits y usar [bitblt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar los píxeles en una ventana **HDC**.

En plataformas que no son de Windows, la aplicación puede seguir creando un destino de representación de mapa de bits, pero simplemente encapsula una matriz de memoria del sistema sin **HDC** y sin Dib. Sin una **HDC**, debe haber otra manera de que la aplicación obtenga los píxeles del mapa de bits para que pueda copiarlos, o bien usarlos. Incluso en Windows, a veces resulta útil obtener los datos de píxeles reales y se muestra la manera actual de hacerlo en el ejemplo de código siguiente.

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Otras diferencias de API entre DWriteCore y DirectWrite

Hay algunas API que son solo códigos auxiliares o que se comportan de manera ligeramente diferente en plataformas que no son de Windows. Por ejemplo, [IDWriteGdiInterop:: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) devuelve **E_NOTIMPL** en plataformas que no son de Windows, ya que no hay nada como **HDC** sin [GDI](../gdi/windows-gdi.md).

Y, por último, hay algunas otras API de Windows que se suelen usar junto con DirectWrite (Direct2D es un ejemplo importante). Sin embargo, actualmente, Direct2D y DWriteCore no interoperan. Por ejemplo, si crea un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) con DWriteCore y lo pasa a [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), se producirá un error en esa llamada.