---
title: Información general de DWriteCore
description: DWriteCore es la implementación project-project de DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 1ebb85ae2628a2c9abce86e0ce146c0d24828267
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925696"
---
# <a name="dwritecore-overview"></a>Información general de DWriteCore

DWriteCore es la implementación [project-project de](/windows/apps/project-reunion/) [DirectWrite](./direct-write-portal.md) (DirectWrite es la API de DirectX para la representación de texto de alta calidad, fuentes de contorno independientes de la resolución y compatibilidad completa con texto Unicode y diseño). DWriteCore es una forma de DirectWrite que se ejecuta en versiones de Windows hasta Windows 8, y que le permite su uso en varias plataformas.

En este tema introductorio se describe qué es DWriteCore y se muestra cómo instalarlo en el entorno de desarrollo y programar con él.

## <a name="the-value-proposition-of-dwritecore"></a>La propuesta de valor de DWriteCore

[DirectWrite](./direct-write-portal.md) admite una amplia gama de características que la convierten en la herramienta de representación de fuentes preferida en Windows para la mayoría de las aplicaciones, ya sea a través de llamadas directas o a través de &mdash; [Direct2D.](../direct2d/direct2d-portal.md) DirectWrite incluye un sistema de diseño de texto independiente del dispositivo, representación de texto [de Microsoft ClearType](/typography/cleartype/) de subpíxeles de alta calidad, texto acelerado por hardware, texto de formato múltiple, características avanzadas de [tipografía OpenType®](/typography/opentype/) compatibilidad con lenguaje ancho y representación compatible con [GDI.](../gdi/windows-gdi.md) DirectWrite ha estado disponible desde Windows Vista SP2 y ha evolucionado a lo largo de los años para incluir características más avanzadas, como las fuentes variables, que le permiten aplicar estilos, pesos y otros atributos a una fuente con un solo recurso de fuente.

Sin embargo, debido a la larga duración de DirectWrite, los avances en el desarrollo tienden a dejar atrás las versiones anteriores de Windows. Además, el estado de DirectWrite como tecnología de representación de texto premier solo se limita a Windows, lo que deja que las aplicaciones multiplataforma escriban su propia pila de representación de texto o que se basen en soluciones de terceros.

DWriteCore resuelve los problemas fundamentales de la característica de versión huérfana y la compatibilidad multiplataforma mediante la eliminación de la biblioteca del sistema y el destino de todos los posibles puntos de conexión admitidos. Con ese fin, hemos integrado DWriteCore en ProjectPlataforma con una API pública que se admite en todos los puntos de conexión de Windows hasta Windows 8 y abre la puerta para que la use multiplataforma.

El valor principal que DWriteCore proporciona, como desarrollador, en Project Hacer es que proporciona acceso a todas las características actuales de DirectWrite hasta el Windows 8. Todas las características de DWriteCore funcionarán igual en todas las versiones de nivel inferior. En otras palabras, todas las características actuales funcionarán en Windows 8, 8.1 y todas las versiones de Windows 10, sin ninguna disparidad con respecto a qué características podrían funcionar en qué versiones.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>La aplicación de demostración DWriteCore &mdash; DWriteCoreGallery

DWriteCore se muestra a través de la aplicación de ejemplo [DWriteCoreGallery,](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) que ahora está disponible para su descarga y estudio.

## <a name="get-started-with-dwritecore"></a>Introducción a DWriteCore

DWriteCore forma parte del [proyecto Deserción 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0) En esta sección se describe cómo configurar el entorno de desarrollo para la programación con DWriteCore.

### <a name="install-the-project-reunion-05-vsix"></a>Instalación del VSIX de Project Alsa 0.5

En Visual Studio, haga clic en **Extensiones**  >  **Administrar extensiones,** busque *Project Desenván y* descargue la extensión Project Extension. Cierre y vuelva a Visual Studio y siga las indicaciones para instalar la extensión.

Para obtener más información, [vea ProjectUwp 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)y [Build desktop Windows apps with ProjectUwp 0.5](/windows/apps/project-reunion/#set-up-your-development-environment)(Compilación de aplicaciones de escritorio de Windows con Project Hacer 0.5).

### <a name="create-a-new-project"></a>Crear un proyecto nuevo

En Visual Studio, cree un proyecto a partir de la plantilla de proyecto Aplicación vacía **empaquetada (WinUI 3 en** el escritorio). Puede encontrar esa plantilla de proyecto eligiendo el lenguaje: *C++*; platform: *ProjectPlataforma*; tipo de proyecto: *Escritorio.*

Para obtener más información, consulta [Plantillas de proyecto para WinUI 3.](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3)

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>Instalación del paquete NuGet Microsoft.ProjectReunion.DWrite

En Visual Studio, haga  clic en Project Manage NuGet Packages... Browse (Administrar proyectos paquetes NuGet... Examinar), escriba o pegue \>  \>  **Microsoft.ProjectReunion.DWrite**  en el cuadro de búsqueda, seleccione el elemento en los resultados de la búsqueda y, a continuación, haga clic en Instalar para instalar el paquete para ese proyecto.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>Como alternativa, comience con la aplicación de ejemplo DWriteCoreGallery.

Como alternativa, puede programar con DWriteCore empezando por el proyecto de aplicación de ejemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) y basar el desarrollo en ese proyecto. A continuación, puede quitar cualquier código fuente (o archivos) existente de ese proyecto de ejemplo y agregar cualquier nuevo código fuente (o archivos) al proyecto.

### <a name="use-dwritecore-in-your-project"></a>Uso de DWriteCore en el proyecto

Para obtener más información sobre la programación con DWriteCore, vea la sección Programming with DWriteCore (Programación con [DWriteCore)](#programming-with-dwritecore) más adelante en este tema.

## <a name="the-release-phases-of-dwritecore"></a>Fases de lanzamiento de DWriteCore

La porción de DirectWrite a DWriteCore es un proyecto lo suficientemente grande como para abarcar varios ciclos de versión de Windows. Ese proyecto se divide en fases, cada una de las cuales corresponde a un fragmento de funcionalidad entregado en una versión.

### <a name="features-in-the-current-release-of-dwritecore"></a>Características de la versión actual de DWriteCore

La versión de DWriteCore disponible actualmente forma parte de [Project Hacer 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0) Contiene las herramientas básicas que, como desarrollador, necesita para consumir DWriteCore, incluidas las siguientes características.

- Enumeración de fuentes.
- API de fuente.
- Formar.
- API de representación de bajo nivel. Esto es parcial en la fase actual DWriteCore no interopera con &mdash; [Direct2D,](../direct2d/direct2d-portal.md)pero puede usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)
- Funcionalidad básica de diseño de texto.
- API de representación de texto.
- Destino de representación de mapa de bits.
- Fuentes de color.
- Optimizaciones varias (limpieza de caché de fuentes, cargador de fuentes en memoria, entre otras).

Una característica de banner son las fuentes de color. Las fuentes de color permiten representar las fuentes con una funcionalidad de color más sofisticada más allá de colores simples. Por ejemplo, las fuentes de color es lo que potencia la capacidad de representar fuentes de icono de emoji y barra de herramientas (la última de las cuales la usa Office, por ejemplo). Las fuentes de color se introdujeron por primera vez en Windows 8.1, pero la característica se expandió mucho en Windows 10, versión 1607 (actualización de aniversario).

El trabajo de limpieza de la caché de fuentes y el cargador de fuentes en memoria permiten una carga más rápida de fuentes y mejoras en la memoria.

Con estas características, puede empezar a aprovechar inmediatamente algunas de las funcionalidades básicas modernas de DirectWrite, como las fuentes variables de nivel inferior &mdash; &mdash; a Windows 8. Las fuentes variables son una de las características más importantes para los clientes de DirectWrite. se introdujeron en Windows 10, versión 1709 (Fall Creators Update), por lo que acceder a ellos en versiones anteriores es una ventaja importante para usted como desarrollador.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Nuestra invitación para usted como desarrollador de DirectWrite

DWriteCore, junto con otros componentes de Project Components, se desarrollará con apertura a los comentarios de los desarrolladores. Le invitamos a empezar a explorar DWriteCore y a proporcionar información o solicitudes sobre el desarrollo de características en nuestro repositorio de [GitHub Project GitHub.](https://github.com/microsoft/ProjectReunion/)

## <a name="programming-with-dwritecore"></a>Programación con DWriteCore

Al igual que [con DirectWrite,](./direct-write-portal.md)programa con DWriteCore a través de su API ligera COM, a través de la [**interfaz IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)

Para usar DWriteCore, es necesario incluir el archivo `dwrite_core.h` de encabezado.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

El `dwrite_core.h` archivo de encabezado define primero el token *DWRITE_CORE* y, a continuación, incluye el archivo `dwrite_3.h` de encabezado. El *DWRITE_CORE* es importante, ya que dirige los encabezados incluidos posteriormente para que todas las API de DirectWrite estén disponibles para usted. Una vez que el proyecto haya incluido , puede continuar y escribir `dwrite_core.h` código, compilar y ejecutar.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>API nuevas o diferentes para DWriteCore

La superficie de la API DWriteCore es prácticamente la misma que para [DirectWrite.](/windows/win32/api/_directwrite/) Pero hay un pequeño número de NUEVAS API que solo están en DWriteCore en la actualidad.

#### <a name="create-a-factory-object"></a>Creación de un objeto de generador

La [**función gratuita DWriteCoreCreateFactory**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) crea un objeto de generador que se usa para la posterior creación de objetos DWriteCore individuales.

**DWriteCoreCreateFactory es** funcionalmente igual que la función [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada por la versión del sistema de DirectWrite. La función DWriteCore tiene un nombre diferente para evitar ambigüedades.

#### <a name="create-a-restricted-factory-object"></a>Creación de un objeto de generador restringido

La [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeración tiene una nueva &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, que indica un generador restringido. Una fábrica restringida está más bloqueada que una factoría aislada. No interactúa con una caché de fuentes persistentes ni entre procesos de ninguna manera. Además, la colección de fuentes del sistema devuelta desde este generador incluye solo fuentes conocidas. Aquí se muestra cómo  puede usar DWRITE_FACTORY_TYPE_ISOLATED2 para crear un objeto de generador restringido al llamar a la función **gratuita DWriteCoreCreateFactory.**

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

Si pasa **DWRITE_FACTORY_TYPE_ISOLATED2** a una versión anterior de DirectWrite que no la **admite,** **DWriteCreateFactory** devuelve E_INVALIDARG .

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Dibujar glifos en un mapa de bits de memoria del sistema

DirectWrite tiene una interfaz de destino de representación de mapa de bits que admite la representación de glifos en un mapa de bits en la memoria del sistema. Sin embargo, actualmente la única manera de obtener acceso a los datos de píxel subyacentes es pasar por GDI, por lo que la API no se puede usar entre plataformas. Esto se corrige fácilmente agregando un método para recuperar los datos de píxeles.

Por lo tanto, DWriteCore presenta la interfaz [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) y su método [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md). Ese método toma un parámetro de tipo (puntero a) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), que es un nuevo struct.

La aplicación crea un destino de representación de mapa de bits mediante una [llamada a IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). En Windows, un destino de representación de mapa de bits encapsula un controlador de dominio de memoria GDI con un mapa de bits independiente del dispositivo (DIB) GDI seleccionado en él. [IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) representa glifos en la DIB. DirectWrite representa los glifos sin pasar por GDI. A continuación, la aplicación puede obtener **el HDC** del destino de representación de mapa de bits y usar [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar los píxeles en una **ventana HDC.**

En plataformas que no son de Windows, la aplicación todavía puede crear un destino de representación de mapa de bits, pero simplemente encapsula una matriz de memoria del sistema sin **HDC** ni DIB. Sin un **HDC**, debe haber otra manera de que la aplicación obtenga los píxeles de mapa de bits para poder copiarlos o usarlos de otro modo. Incluso en Windows, a veces resulta útil obtener los datos de píxeles reales y mostramos la manera actual de hacerlo en el ejemplo de código siguiente.

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

Hay algunas API que son solo código auxiliar o se comportan de forma ligeramente diferente en plataformas que no son de Windows. Por ejemplo, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) devuelve **E_NOTIMPL** en plataformas que no son de Windows, ya que no hay nada como **un HDC** sin [GDI.](../gdi/windows-gdi.md)

Y, por último, hay ciertas otras API de Windows que normalmente se usan junto con DirectWrite (Direct2D es un ejemplo importante). Sin embargo, actualmente, Direct2D y DWriteCore no interoperan. Por ejemplo, si crea un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mediante DWriteCore y lo pasa a [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), se producirá un error en esa llamada.
