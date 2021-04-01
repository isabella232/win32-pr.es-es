---
title: Introducción a DirectWrite
description: Las personas se comunican con texto todo el tiempo en sus vidas diarias.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, acerca de
- DirectWrite, características tipográficas
- tipografía
- DirectWrite, texto internacional
- Fuentes de DirectWrite, OpenType
- Fuentes OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, información general sobre API
- DirectWrite, IDWriteFontFace
- IDWriteFontFace
- DirectWrite, representación de texto
- DirectWrite, modos de representación
- DirectWrite, interoperación GDI
- DirectWrite, interoperabilidad
- interoperabilidad, DirectWrite
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904797"
---
# <a name="introducing-directwrite"></a>Introducción a DirectWrite

Las personas se comunican con texto todo el tiempo en sus vidas diarias. Es la forma principal de que los usuarios consuman un volumen de información cada vez mayor. En el pasado, solía usarse el contenido impreso, principalmente documentos, periódicos, libros, etc. Cada vez es un contenido en línea en su equipo Windows. Un usuario de Windows típico emplea mucho tiempo en leer la pantalla del equipo. Es posible que estén explorando la web, examinando el correo electrónico, redactando un informe, rellenando una hoja de cálculo o escribiendo software, pero lo que realmente está haciendo es leer. Aunque el texto y las fuentes conforman casi todas las partes de la experiencia del usuario en Windows, para la mayoría de los usuarios, la lectura en la pantalla no es tan agradable como leer la salida impresa.

En el caso de los desarrolladores de aplicaciones de Windows, la escritura de código de control de texto es un desafío debido a los mayores requisitos para mejorar la legibilidad, el sofisticado formato y el control de diseño, y la compatibilidad con los distintos idiomas que debe mostrar la aplicación. Incluso el sistema de control de texto más básico debe permitir la entrada de texto, el diseño, la visualización, la edición y la copia y el pegado. Normalmente, los usuarios de Windows esperan más de estas características básicas, por lo que requieren editores sencillos para admitir varias fuentes, varios estilos de párrafo, imágenes incrustadas, revisión ortográfica y otras características. El diseño de interfaz de usuario moderno también ya no se limita al formato único, texto sin formato, pero debe presentar una mejor experiencia con fuentes enriquecidas y diseños de texto.

Se trata de una introducción a cómo [DirectWrite](direct-write-portal.md) permite a las aplicaciones Windows mejorar la experiencia de texto para la interfaz de usuario y los documentos.

## <a name="improving-the-text-experience"></a>Mejorar la experiencia de texto

Las aplicaciones modernas de Windows tienen requisitos sofisticados para el texto en la interfaz de usuario y los documentos. Esto incluye una mejor legibilidad, compatibilidad con una gran variedad de lenguajes y scripts, y un rendimiento de representación superior. Además, la mayoría de las aplicaciones existentes requieren una forma de llevar a cabo inversiones existentes en la base de código WindowsWin32.

[DirectWrite](direct-write-portal.md) proporciona las tres características siguientes que permiten a los desarrolladores de aplicaciones Windows mejorar la experiencia de texto dentro de sus aplicaciones: independencia del sistema de representación, tipografía de alta calidad y varios niveles de funcionalidad.

## <a name="rendering-system-independence"></a>Independencia Rendering-System

[DirectWrite](direct-write-portal.md) es independiente de cualquier tecnología de gráficos determinada. Las aplicaciones pueden usar la tecnología de representación que mejor se adapte a sus necesidades. Esto proporciona a las aplicaciones la flexibilidad de seguir representando algunas partes de su aplicación a través de GDI y otras partes a través de Direct3D o [Direct2D](../direct2d/direct2d-portal.md). De hecho, una aplicación podría optar por representar DirectWrite a través de una pila de representación de propiedad.

## <a name="high-quality-typography"></a>Tipografía de High-Quality

[DirectWrite](direct-write-portal.md) aprovecha los avances de la tecnología de fuentes [OpenType](../intl/opentype-font-format.md) para habilitar la tipografía de alta calidad en una aplicación Windows. El sistema de fuentes DirectWrite proporciona servicios para trabajar con la enumeración de fuentes, la reserva de fuentes y el almacenamiento en caché de fuentes, que son necesarios para las aplicaciones de control de fuentes.

La compatibilidad con [OpenType](../intl/opentype-font-format.md) proporcionada por [DirectWrite](direct-write-portal.md) permite a los desarrolladores agregar a sus aplicaciones características tipográficas avanzadas y compatibilidad con texto internacional.

## <a name="support-for-advanced-typographic-features"></a>Compatibilidad con características tipográficas avanzadas

[DirectWrite](direct-write-portal.md) permite a los desarrolladores de aplicaciones desbloquear las características de las fuentes OpenType que no se pueden usar en WINFORMS o GDI. El objeto [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) de DirectWrite expone muchas de las características avanzadas de las fuentes OpenType, como alternativas estilísticas y caracteres floreados. El kit de desarrollo de software (SDK) de Microsoft Windows proporciona un conjunto de fuentes [OpenType](../intl/opentype-font-format.md) de ejemplo diseñadas con características enriquecidas, como las fuentes Pericles y pescadero. Para obtener más información sobre las características de OpenType, consulte [características de fuentes OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).

## <a name="support-for-international-text"></a>Compatibilidad con texto internacional

[DirectWrite](direct-write-portal.md) usa fuentes [OpenType](../intl/opentype-font-format.md) para permitir una amplia compatibilidad con texto internacional. Se admiten características Unicode como suplentes, BIDI, salto de línea y UVS. La función de los scripts guiados por el lenguaje, la sustitución de números y la forma de glifos garantizan que el texto de cualquier script tenga el diseño y la representación correctos.

Actualmente se admiten los siguientes scripts:

> [!Note]  
> En el caso de los scripts marcados con, no hay \* fuentes del sistema predeterminadas. Las aplicaciones deben instalar las fuentes que admiten estos scripts.

 

-   Árabe
-   Armenio
-   Bengala
-   Bopomofo
-   Pantallas\*
-   Canadiense indígena silábico
-   Cheroqui
-   Chino (simplificado & tradicional)
-   Cirílico
-   Copto\*
-   Devanagari
-   Dígito
-   Georgiano
-   Letra\*
-   Griego
-   Gujarati
-   Gurmukhi
-   Hebreo
-   Japonés
-   Canarés
-   Jemer
-   Coreano
-   Lao
-   Latín
-   Malayalam
-   Mongol
-   Myanmar
-   Nuevo tai lue moderno
-   Ogham\*
-   Odia
-   ' Phags-pa
-   Rúnica\*
-   Cingalés
-   Siríaco
-   Tai le
-   Tamil
-   Telugu
-   Thaana
-   Tailandés
-   Tibetano
-   Yi

## <a name="multiple-layers-of-functionality"></a>Varios niveles de funcionalidad

[DirectWrite](direct-write-portal.md) proporciona capas de funcionalidad factorizadas, donde cada capa interactúa sin problemas con el siguiente. El diseño de la API permite a los desarrolladores de aplicaciones tener libertad y flexibilidad para adoptar capas individuales en función de sus necesidades y programación. En el diagrama siguiente se muestra la relación entre estas capas.

![diagrama de capas de directwrite y cómo se comunican con una aplicación o marco de interfaz de usuario y la API de gráficos](images/intro-01.png)

La API de diseño de texto proporciona la funcionalidad de nivel más alto disponible en [DirectWrite](direct-write-portal.md). Proporciona servicios para que la aplicación mida, muestre e interactúe con cadenas de texto con formato enriquecido. Esta API de texto se puede usar en aplicaciones que actualmente usan Win32 DrawText para compilar una interfaz de usuario moderna con texto con formato enriquecido.

Las aplicaciones con un uso intensivo de texto que implementan su propio motor de diseño pueden usar la siguiente capa hacia abajo: el procesador de scripts. El procesador de scripts divide un fragmento de texto en bloques de scripts y controla la asignación entre representaciones Unicode a la representación de glifo adecuada en la fuente, por lo que el texto del script puede mostrarse correctamente en el idioma correcto. El sistema de diseño utilizado por el nivel de API de diseño de texto se basa en el sistema de procesamiento de fuentes y scripts.

La capa de representación de glifos es el nivel más bajo de funcionalidad y proporciona la funcionalidad de representación de glifos para las aplicaciones que implementan su propio motor de diseño de texto. La capa de representación del glifo también es útil para las aplicaciones que implementan un representador personalizado para modificar el comportamiento del dibujo de glifos a través de la función de devolución de llamada en la API de formato de texto de [DirectWrite](direct-write-portal.md) .

El sistema de fuentes [directwrite](direct-write-portal.md) está disponible para todos los niveles funcionales de directwrite y permite que una aplicación tenga acceso a la información de fuentes y glifos. Está diseñado para administrar tecnologías de fuentes y formatos de datos comunes. El modelo de fuente DirectWrite sigue la práctica tipográfica común de admitir cualquier número de pesos, estilos y estirados de la misma familia de fuentes. Este modelo, el mismo modelo seguido de WPF y CSS, especifica que las fuentes que difieren solo en peso (negrita, luz, etc.), estilo (vertical, cursiva u oblicuo) o Stretch (estrecho, condensado, ancho, etc.) se consideran miembros de una sola familia de fuentes.

### <a name="improved-text-rendering-with-cleartype"></a>Representación de texto mejorada con ClearType

Mejorar la legibilidad en la pantalla es un requisito clave para todas las aplicaciones de Windows. La evidencia de Research en la psicología cognitiva indica que es necesario poder reconocer cada letra con precisión y que incluso el espaciado entre las letras es fundamental para el procesamiento rápido. Las letras y palabras que no son simétricas se perciben como feo y degradan la experiencia de lectura. Kevin Larson, el grupo de tecnologías avanzadas de lectura de Microsoft, escribió un artículo sobre el asunto que se publicó en el espectro IEEE. El artículo se denomina "tecnología de texto" ( https://www.spectrum.ieee.org/print/5049) .

El texto en [DirectWrite](direct-write-portal.md) se representa con Microsoft ClearType, lo que mejora la claridad y la legibilidad del texto. ClearType aprovecha el hecho de que las pantallas LCD modernas tienen bandas RGB para cada píxel que se pueden controlar individualmente. DirectWrite usa las últimas mejoras de ClearType, que se incluyen primero en Windows Vista con Windows Presentation Foundation, que le permite evaluar no solo las letras individuales, sino también el espaciado entre las letras. Antes de estas mejoras de ClearType, el texto con un tamaño de "lectura" de 10 o 12 puntos era difícil de mostrar: podríamos colocar 1 píxel entre letras, que a menudo era demasiado pequeño o 2 píxeles, lo que a menudo era demasiado grande. El uso de la resolución adicional en los subpíxeles nos proporciona el espaciado fraccionario, lo que mejora la simetría y la simetría de toda la página.

En la ilustración siguiente se muestra cómo los glifos pueden comenzar en cualquier límite de subpíxeles cuando se usa el posicionamiento de subpíxeles.

La siguiente ilustración se representa mediante la versión de GDI del representador ClearType, que no empleaba el posicionamiento de subpíxeles.

![Ilustración de "tecnología" representada sin posicionamiento de subpíxeles](images/intro-03.png)

La siguiente ilustración se representa mediante la versión de [DirectWrite](direct-write-portal.md) del representador ClearType, que usa el posicionamiento de subpíxeles.

![Ilustración de "tecnología" representada con posicionamiento de subpíxeles](images/intro-04.png)

Tenga en cuenta que el espaciado entre las letras h y n es más incluso en la segunda imagen y la letra o se espacia más allá de la letra n, incluso con la letra l. Tenga en cuenta también cómo el tallo de las letras l es más natural.

La posición de ClearType de subpíxeles ofrece el espaciado más preciso de los caracteres en la pantalla, especialmente en tamaños pequeños en los que la diferencia entre un subpíxel y un píxel entero representa una proporción significativa del ancho del glifo. Permite medir el texto en el espacio de resolución ideal y representarlo en su posición natural en la franja de color LCD, con granularidad de subpíxeles. El texto que se mide y se representa mediante esta tecnología es, por definición, independiente de la resolución, lo que significa que se consigue el mismo diseño de texto en el intervalo de varias resoluciones de pantalla.

A diferencia de cualquier tipo de representación de GDI de GDI, ClearType de subpíxel ofrece el ancho de caracteres más preciso.

La API de cadena de texto adopta la representación de texto de subpíxeles de forma predeterminada, lo que significa que mide el texto en su resolución ideal independiente de la resolución de pantalla actual y genera el resultado de posicionamiento del glifo en función de los anchos de avance del glifo realmente escalados y los desplazamientos de posición.

En el caso de texto de tamaño grande, [DirectWrite](direct-write-portal.md) también habilita el suavizado de contorno a lo largo del eje y para que los bordes sean más suaves y representaciones como el diseñador de fuentes previsto. En la ilustración siguiente se muestra el suavizado de contorno de la dirección y.

![Ilustración de "ClearType" representada como texto GDI y como texto de directwrite con suavizado de contorno de la dirección y](images/intro-05.png)

Aunque el texto de [DirectWrite](direct-write-portal.md) se coloca y se representa con ClearType de subpíxeles de forma predeterminada, hay disponibles otras opciones de representación. Muchas aplicaciones existentes usan GDI para representar la mayor parte de su interfaz de usuario y algunas aplicaciones usan controles de edición del sistema que siguen usando GDI para la representación de texto. Al agregar texto de DirectWrite a estas aplicaciones, puede que sea necesario sacrificar las mejoras de la experiencia de lectura proporcionadas por ClearType de subpíxeles para que el texto tenga una apariencia coherente en toda la aplicación.

Para cumplir estos requisitos, [DirectWrite](direct-write-portal.md) también admite las siguientes opciones de representación:

-   ClearType de subpíxel (valor predeterminado).
-   ClearType de subpíxel con suavizado de contorno en las dimensiones horizontal y vertical.
-   Texto con alias.
-   El ancho natural de GDI (usado por Microsoft Word Vista de lectura, por ejemplo).
-   Compatible con GDI: ancho (incluido mapa de bits incrustado de Asia oriental).

Cada uno de estos modos de representación se puede ajustar a través de la API de DirectWrite y a través del nuevo sintonizador ClearType de bandeja de entrada de Windows 7.

> [!Note]  
> A partir de Windows 8, debe usar el suavizado de contorno de texto de la grisización en la mayoría de los casos. Consulte la siguiente sección para más información.

 

### <a name="support-for-natural-layout"></a>Compatibilidad con el diseño natural

El diseño natural es independiente de la resolución, por lo que el espaciado de los caracteres no cambia a medida que se acerca o aleja, o en función de los PPP de la pantalla. Una ventaja secundaria es que el espaciado es cierto para el diseño de la fuente. El diseño natural es posible gracias a la compatibilidad de DirectWrite con la representación natural, lo que significa que los glifos individuales se pueden colocar en una fracción de un píxel.

Aunque el diseño natural es el valor predeterminado, algunas aplicaciones necesitan representar texto con el mismo espaciado y apariencia que GDI. Para estas aplicaciones, DirectWrite proporciona modos de medida natural GDI clásico y GDI y los modos de representación correspondientes.

Cualquiera de los modos de representación anteriores se puede combinar con cualquiera de los dos modos de suavizado de contorno: ClearType o escala de grises. El suavizado de contorno de ClearType simula una resolución más alta al manipular individualmente los valores de color rojo, verde y azul de cada píxel. El suavizado de escala de grises calcula solo un valor de cobertura (o alfa) para cada píxel. ClearType es el valor predeterminado, pero se recomienda el suavizado de escala de grises para las aplicaciones de la tienda Windows porque es más rápido y es compatible con el suavizado de contorno estándar, mientras que sigue siendo muy legible.

## <a name="api-overview"></a>Información general acerca de la API

La interfaz [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) es el punto de partida para usar la funcionalidad de DirectWrite. El generador es el objeto raíz que crea un conjunto de objetos que se pueden usar juntos.

La operación de formato y diseño es un requisito previo para las operaciones, ya que el texto debe tener el formato correcto y estar diseñado para un conjunto especificado de restricciones antes de que se pueda dibujar o probar la prueba de posicionamiento. Dos objetos clave que se pueden crear con un [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para este propósito son [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). Un objeto **IDWriteTextFormat** representa la información de formato para un párrafo de texto. La función [**IDWriteFactory:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) toma la cadena de entrada, las restricciones asociadas, como la dimensión del espacio que se va a rellenar y el objeto **IDWriteTextFormat** , y coloca el resultado analizado y con formato completo en **IDWriteTextLayout** para usarlo en operaciones posteriores.

A continuación, la aplicación puede representar el texto mediante la función [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) proporcionada por [Direct2D](../direct2d/direct2d-portal.md) o implementando una función de devolución de llamada que puede usar GDI, Direct2D u otros sistemas de gráficos para representar los glifos. Para un solo formato de texto, la función [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) en Direct2D proporciona una manera más sencilla de dibujar texto sin tener que crear primero un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a>Aplicar formato y dibujar "Hola mundo" con DirectWrite

En el ejemplo de código siguiente se muestra cómo una aplicación puede dar formato a un solo párrafo mediante [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y dibujarlo mediante la función [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) de [Direct2D](../direct2d/direct2d-portal.md).


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a>Acceder al sistema de fuentes

Además de especificar un nombre de familia de fuentes para la cadena de texto mediante la interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) en el ejemplo anterior, [DirectWrite](direct-write-portal.md) proporciona a las aplicaciones un mayor control sobre la selección de fuentes a través de la enumeración de fuentes y la capacidad de crear una colección de fuentes personalizada basada en fuentes de documentos incrustadas.

El objeto [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) es una colección de familias de fuentes. DirectWrite proporciona acceso al conjunto de fuentes instaladas en el sistema a través de una colección de fuentes especial denominada colección de fuentes del sistema. Esto se obtiene llamando al método [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) del objeto [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) . Una aplicación también puede crear una colección de fuentes personalizada a partir de un conjunto de fuentes enumeradas por una devolución de llamada definida por la aplicación, es decir, fuentes privadas instaladas por una aplicación o fuentes incrustadas en un documento.

A continuación, la aplicación puede llamar a [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) para obtener un objeto FontFamily específico dentro de la colección y, a continuación, llamar a [**IDWriteFontFamily:: GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) para obtener un objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) específico. El objeto **IDWriteFont** representa una fuente de una colección de fuentes y expone propiedades y algunas métricas de fuente básicas.

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) es otro objeto que representa una fuente y expone un conjunto completo de métricas en una fuente. El **IDWriteFontFace** se puede crear directamente a partir de un nombre de fuente; una aplicación no tiene que obtener una colección de fuentes para tener acceso a ella. Resulta útil para una aplicación de diseño de texto como Microsoft Word que necesita consultar los detalles de una fuente específica.

En el diagrama siguiente se ilustra la relación entre estos objetos.

![diagrama de la relación entre una colección de fuentes, una familia de fuentes y una fuente](images/fontcollection.png)

### <a name="idwritefontface"></a>IDWriteFontFace

El objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) representa una fuente y proporciona información más detallada sobre la fuente que el objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) . Las métricas de fuente y glifo de **IDWriteFontFace** son útiles para las aplicaciones que implementan el diseño de texto.

La mayoría de las aplicaciones principales no usarán estas API directamente y, en su lugar, utilizará [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) o especificará el nombre de la familia de fuentes directamente.

En la tabla siguiente se resumen los escenarios de uso de los dos objetos.



| Category                                                                                                         | [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| API para admitir la interacción del usuario, como una interfaz de usuario del selector de fuentes: Descripción y otras API informativas | Sí                                        | No                                                 |
| API para admitir la asignación de fuentes: familia, estilo, peso, stretch, cobertura de caracteres                                 | Sí                                        | No                                                 |
| DrawText API                                                                                                     | Sí                                        | No                                                 |
| API usadas para la representación                                                                                          | No                                         | Sí                                                |
| API utilizadas para el diseño de texto: métricas del glifo, etc.                                                              | No                                         | Sí                                                |
| API para el control de la interfaz de usuario y el diseño de texto: métricas de toda la fuente                                                           | Sí                                        | Sí                                                |



 

A continuación se muestra una aplicación de ejemplo que enumera las fuentes de la colección de fuentes del sistema.


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a>Representación de texto

Las API de representación de texto permiten que los glifos de una fuente [DirectWrite](direct-write-portal.md) se representen en una superficie de [Direct2D](../direct2d/direct2d-portal.md) o en un mapa de bits independiente del dispositivo GDI o que se conviertan en esquemas o mapas de bits. La representación de ClearType en DirectWrite admite el posicionamiento de subpíxeles con una nitidez y un contraste mejorados en comparación con las implementaciones anteriores en Windows. DirectWrite también admite texto en blanco y negro con alias para admitir escenarios en los que intervienen fuentes asiáticas Orientales con mapas de bits incrustados o en los que el usuario ha deshabilitado el suavizado de fuentes de cualquier tipo.

Todas las opciones son ajustables por todos los botones ClearType disponibles a los que se puede acceder a través de las API de [DirectWrite](direct-write-portal.md) y también se exponen a través del nuevo applet del panel de control de Windows 7 ClearType Tuner.

Hay dos API disponibles para la representación de glifos, una que proporciona una representación acelerada mediante hardware a través de [Direct2D](../direct2d/direct2d-portal.md) y la otra que proporciona la representación de software a un mapa de bits de GDI. Una aplicación que usa [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e implementa la devolución de llamada [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) puede llamar a cualquiera de estas funciones como respuesta a una devolución de llamada [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) . Además, las aplicaciones que implementan su propio diseño o tratan los datos de nivel de glifo pueden utilizar estas API.

1.  [**ID2DRenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    Las aplicaciones pueden usar la API de [Direct2D](../direct2d/direct2d-portal.md) [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) para proporcionar aceleración de hardware para la representación de texto mediante la GPU. La aceleración de hardware afecta a todas las fases de la canalización de representación de texto: desde combinar glifos en ejecuciones de glifos y filtrar el mapa de bits de ejecución de glifos, para aplicar el algoritmo de mezcla ClearType a la salida mostrada final. Esta es la API recomendada para obtener el mejor rendimiento de representación.

2.  [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    Las aplicaciones pueden usar el método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para realizar una representación de software de una ejecución de glifos en un mapa de bits 32-bpp. El objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsula un mapa de bits y un contexto de dispositivo de memoria que se puede usar para representar glifos. Esta API es útil si desea permanecer en GDI porque tiene una base de código existente que se representa en GDI.

Si tiene una aplicación que tiene código de diseño de texto existente que usa GDI y desea conservar su código de diseño existente, pero usar [DirectWrite](direct-write-portal.md) solo para el paso final de los glifos de representación, [**IDWriteGdiInterop:: CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) proporciona el puente entre las dos API. Antes de llamar a esta función, la aplicación usará la función **IDWriteGdiInterop:: CreateFontFaceFromHdc** para obtener una referencia de fuente a partir de un contexto de dispositivo.

> [!Note]  
> En la mayoría de los escenarios, es posible que las aplicaciones no tengan que usar estas API de representación de glifos. Después de que una aplicación haya creado un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , puede utilizar el método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) para representar el texto.

 

## <a name="custom-rendering-modes"></a>Modos de representación personalizados

Varios parámetros afectan a la representación de texto, como gamma, nivel de ClearType, geometría de píxeles y contraste mejorado. Los parámetros de representación se encapsulan mediante un objeto, que implementa la interfaz [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) pública. El objeto de parámetros de representación se inicializa automáticamente en función de las propiedades de hardware o las preferencias de usuario especificadas mediante el applet de panel de control ClearType en Windows 7. Por lo general, si un cliente usa la API de diseño de [directwrite](direct-write-portal.md) , directwrite seleccionará automáticamente un modo de representación que se corresponda con el modo de medición especificado.

Las aplicaciones que desean más control pueden usar [**IDWriteFactory:: CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) para implementar las distintas opciones de representación. Esta función también se puede usar para establecer la gamma, la geometría de píxeles y el contraste mejorado.

A continuación se muestran las diversas opciones de representación disponibles:

-   Suavizado de contorno de subpíxeles

    La aplicación establece el parámetro *renderingMode* en el \_ modo de representación de DWRITE \_ \_ natural para especificar la representación con suavizado de contorno solo en la dimensión horizontal.

-   Suavizado de contorno de subpíxeles en dimensiones horizontales y verticales.

    La aplicación establece el parámetro *renderingMode* en el \_ modo de representación de DWRITE \_ \_ \_ simétrico natural para especificar la representación con suavizado de contorno en las dimensiones horizontal y vertical. Esto hace que las curvas y las líneas diagonales parezcan más suaves a costa de cierta suavidad y se suelen usar en tamaños superiores a 16 PPEM.

-   Texto con alias

    La aplicación establece el parámetro *renderingMode* en el \_ modo de representación de DWRITE \_ \_ con alias para especificar el texto con alias.

-   Texto en escala de grises

    La aplicación establece el parámetro *pixelGeometry* en DWRITE \_ píxeles \_ Geometry \_ Flat para especificar el texto de escala de grises.

-   Compatible con GDI: ancho (incluido mapa de bits incrustado de Asia oriental)

    La aplicación establece el parámetro *renderingMode* en el \_ modo de representación de DWRITE \_ \_ GDI \_ clásico para especificar el suavizado de contorno de ancho compatible con GDI.

-   Ancho natural de GDI

    La aplicación establece el parámetro *renderingMode* en el modo de representación de DWRITE de \_ \_ \_ GDI \_ natural para especificar el suavizado de contorno compatible de ancho natural de GDI.

-   Texto de esquema

    Para la representación en tamaños grandes, es posible que un desarrollador de aplicaciones prefiera representar con el contorno de fuente en lugar de rasterizarlo en un mapa de bits. La aplicación establece el parámetro *renderingMode* en **el \_ esquema del \_ modo \_ de representación DWRITE** para especificar que la representación debe omitir el rasterizador y utilizar los contornos directamente.

## <a name="gdi-interoperability"></a>Interoperabilidad con GDI

La interfaz [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) proporciona interoperabilidad con GDI. Esto permite a las aplicaciones continuar su inversión existente en las bases de código GDI y usar de forma selectiva [DirectWrite](direct-write-portal.md) para la representación o el diseño.

A continuación se muestran las API que permiten a una aplicación migrar a o desde el sistema de fuentes de GDI:

-   [**CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    Crea un objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) que coincide con las propiedades especificadas por la estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

-   [**ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    Inicializa una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basada en las propiedades compatibles con GDI del [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)especificado.

-   [**ConvertFontFaceToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    Inicializa una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basada en las propiedades compatibles con GDI del [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)especificado.

-   [**CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    Crea un objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) que corresponde al **HFONT** seleccionado actualmente.

## <a name="conclusion"></a>Conclusión

Mejorar la experiencia de lectura es de gran valor para los usuarios, ya sea en la pantalla o en papel. [DirectWrite](direct-write-portal.md) proporciona la facilidad de uso y el modelo de programación por capas para que los desarrolladores de aplicaciones mejoren la experiencia de texto en sus aplicaciones Windows. Las aplicaciones pueden usar DirectWrite para representar texto con formato enriquecido para su interfaz de usuario y sus documentos con la API de diseño. En escenarios más complejos, una aplicación puede trabajar directamente con glifos, fuentes de acceso, etc., y aprovechar la potencia de DirectWrite para ofrecer tipografía de alta calidad.

Las capacidades de interoperabilidad de [DirectWrite](direct-write-portal.md) permiten a los desarrolladores de aplicaciones llevar adelante sus códigos base de Win32 existentes y adoptar DirectWrite de manera selectiva dentro de sus aplicaciones.

 

 