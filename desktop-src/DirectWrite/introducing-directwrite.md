---
title: Presentación de DirectWrite
description: Las personas se comunican con texto todo el tiempo de su vida diaria.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite,about
- DirectWrite, características tipográficas
- tipografía
- DirectWrite,texto internacional
- DirectWrite,fuentes OpenType
- Fuentes OpenType
- DirectWrite,ClearType
- ClearType
- DirectWrite,introducción a la API
- DirectWrite,IDWriteFontFace
- IDWriteFontFace
- DirectWrite,representación de texto
- DirectWrite, modos de representación
- DirectWrite,interoperación GDI
- DirectWrite,interoperabilidad
- interoperabilidad, DirectWrite
- interoperabilidad, Interfaz de dispositivo gráfico (GDI)
- Interfaz de dispositivo gráfico (GDI)
- GDI (Interfaz de dispositivo gráfico)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fc0ef18287c5e3b923e42e585556f69a3186453ed2bfc205438f74bf50a449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130874"
---
# <a name="introducing-directwrite"></a>Presentación de DirectWrite

Las personas se comunican con texto todo el tiempo de su vida diaria. Es la manera principal de que los usuarios consuman un volumen creciente de información. En el pasado, solía estar a través de contenido impreso, principalmente documentos, periódicos, libros, entre otros. Cada vez más, es contenido en línea en su Windows PC. Un usuario Windows pasa mucho tiempo leyendo desde la pantalla de su equipo. Es posible que no usen la Web, que escriban correo electrónico, que creen un informe, que rellenen una hoja de cálculo o que escriban software, pero lo que realmente hacen es leer. Aunque el texto y las fuentes permean casi todas las partes de la experiencia del usuario en Windows, para la mayoría de los usuarios, leer en la pantalla no es tan divertido como leer la salida impresa.

Para Windows desarrolladores de aplicaciones, escribir código de control de texto es un desafío debido al aumento de los requisitos para mejorar la legibilidad, el formato sofisticado y el control de diseño, y la compatibilidad con los distintos idiomas que debe mostrar la aplicación. Incluso el sistema de control de texto más básico debe permitir la entrada de texto, el diseño, la presentación, la edición, la copia y el pegar. Windows usuarios normalmente esperan incluso más que estas características básicas, lo que requiere incluso editores sencillos para admitir varias fuentes, varios estilos de párrafo, imágenes incrustadas, revisión ortográfica y otras características. El diseño moderno de la interfaz de usuario ya no se limita a un solo formato, texto sin formato, pero debe presentar una mejor experiencia con fuentes y diseños de texto enriquecidos.

Esta es una introducción a [cómo](direct-write-portal.md) DirectWrite permite Windows aplicaciones para mejorar la experiencia de texto para la interfaz de usuario y los documentos.

## <a name="improving-the-text-experience"></a>Mejora de la experiencia de texto

Las Windows modernas tienen requisitos sofisticados para el texto en su interfaz de usuario y documentos. Estos incluyen una mejor legibilidad, compatibilidad con una gran variedad de lenguajes y scripts, y un rendimiento de representación superior. Además, la mayoría de las aplicaciones existentes requieren una manera de llevar adelante las inversiones existentes en la base de código WindowsWin32.

[DirectWrite](direct-write-portal.md) proporciona las tres características siguientes que permiten a los desarrolladores de aplicaciones de Windows mejorar la experiencia de texto dentro de sus aplicaciones: independencia del sistema de representación, tipografía de alta calidad y varias capas de funcionalidad.

## <a name="rendering-system-independence"></a>Rendering-System independencia

[DirectWrite](direct-write-portal.md) es independiente de cualquier tecnología de gráficos determinada. Las aplicaciones pueden usar la tecnología de representación más adecuada para sus necesidades. Esto ofrece a las aplicaciones la flexibilidad de seguir representando algunas partes de su aplicación a través de GDI y otras a través de Direct3D [o Direct2D.](../direct2d/direct2d-portal.md) De hecho, una aplicación podría optar por representar DirectWrite a través de una pila de representación propietaria.

## <a name="high-quality-typography"></a>High-Quality tipografía

[DirectWrite](direct-write-portal.md) aprovecha los avances de la tecnología [OpenType](../intl/opentype-font-format.md) Font para habilitar la tipografía de alta calidad dentro de una Windows aplicación. El DirectWrite fuente proporciona servicios para trabajar con la enumeración de fuentes, la reserva de fuentes y el almacenamiento en caché de fuentes, que todas las aplicaciones necesitan para controlar las fuentes.

La [compatibilidad con OpenType](../intl/opentype-font-format.md) proporcionada por [DirectWrite](direct-write-portal.md) permite a los desarrolladores agregar a sus aplicaciones características tipográficas avanzadas y compatibilidad con texto internacional.

## <a name="support-for-advanced-typographic-features"></a>Compatibilidad con características tipográficas avanzadas

[DirectWrite](direct-write-portal.md) permite a los desarrolladores de aplicaciones desbloquear las características de las fuentes OpenType que no podían usar en WinForms o GDI. El DirectWrite [**objeto IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) expone muchas de las características avanzadas de las fuentes OpenType, como las alternativas estilísticas y los bañadores. El Kit de desarrollo de software (SDK) de Microsoft Windows proporciona un conjunto de fuentes [OpenType](../intl/opentype-font-format.md) de ejemplo que están diseñadas con características enriquecidas, como las fuentes Pericles y Querdero. Para obtener más información sobre las características de OpenType, vea [Características de fuente OpenType.](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85))

## <a name="support-for-international-text"></a>Compatibilidad con texto internacional

[DirectWrite](direct-write-portal.md) usa [fuentes OpenType](../intl/opentype-font-format.md) para permitir una amplia compatibilidad con texto internacional. Se admiten características Unicode como suplentes, BIDI, salto de línea y UVS. La caracterización de scripts guiados por el lenguaje, la sustitución de números y el modelado de glifos garantizan que el texto de cualquier script tenga el diseño y la representación correctos.

Actualmente se admiten los siguientes scripts:

> [!Note]  
> Para los scripts marcados con \* , no hay fuentes predeterminadas del sistema. Las aplicaciones deben instalar fuentes que admitan estos scripts.

 

-   Árabe
-   Armenio
-   Bengala
-   Bopomofo
-   Braille\*
-   Sílabas aborígenes canadienses
-   Cheroqui
-   Chino (tradicional & simplificado)
-   Cirílico
-   Copto\*
-   Devanagari
-   Etíope
-   Georgiano
-   Glagolitic\*
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
-   Nuevo Tai Lue
-   Ogham\*
-   Odia
-   'Phags-pa
-   Rúnico\*
-   Cingalés
-   Siríaco
-   Tai Le
-   Tamil
-   Telugu
-   Thaana
-   Tailandés
-   Tibetano
-   Yi

## <a name="multiple-layers-of-functionality"></a>Varias capas de funcionalidad

[DirectWrite](direct-write-portal.md) proporciona capas factoradas de funcionalidad, y cada capa interactúa sin problemas con la siguiente. El diseño de API ofrece a los desarrolladores de aplicaciones la libertad y flexibilidad para adoptar capas individuales en función de sus necesidades y programación. En el diagrama siguiente se muestra la relación entre estas capas.

![diagrama de capas de directwrite y cómo se comunican con una aplicación o marco de interfaz de usuario y la API de gráficos](images/intro-01.png)

La API de diseño de texto proporciona la funcionalidad de nivel más alto disponible [en DirectWrite](direct-write-portal.md). Proporciona servicios para que la aplicación mida, muestre e interactúe con cadenas de texto con formato enriquecido. Esta API de texto se puede usar en aplicaciones que actualmente usan DrawText de Win32 para crear una interfaz de usuario moderna con texto con formato enriquecido.

Las aplicaciones de uso intensivo de texto que implementan su propio motor de diseño pueden usar la siguiente capa hacia abajo: el procesador de scripts. El procesador de scripts divide un fragmento de texto en bloques de script y controla la asignación entre representaciones Unicode a la representación de glifo adecuada en la fuente para que el texto del script se pueda mostrar correctamente en el idioma correcto. El sistema de diseño utilizado por la capa de API de diseño de texto se basa en el sistema de procesamiento de fuentes y scripts.

La capa de representación de glifos es la capa más baja de funcionalidad y proporciona funcionalidad de representación de glifos para las aplicaciones que implementan su propio motor de diseño de texto. La capa de representación de glifos también es útil para las aplicaciones que implementan [](direct-write-portal.md) un representador personalizado para modificar el comportamiento del dibujo de glifos a través de la función de devolución de llamada en DirectWrite API de formato de texto.

El [DirectWrite](direct-write-portal.md) fuente está disponible para todas las capas DirectWrite funcionales y permite que una aplicación acceda a la información de fuentes y glifos. Está diseñado para controlar tecnologías de fuentes comunes y formatos de datos. El DirectWrite de fuente sigue la práctica tipográfica común de admitir cualquier número de pesos, estilos y stretches en la misma familia de fuentes. Este modelo, el mismo modelo seguido de WPF y CSS, especifica que las fuentes difieren solo en peso (negrita, luz, entre otras), estilo (vertical, cursiva u oblicuo) o stretch (estrecho, condensado, ancho, entre otros) se consideran miembros de una sola familia de fuentes.

### <a name="improved-text-rendering-with-cleartype"></a>Representación de texto mejorada con ClearType

Mejorar la legibilidad en la pantalla es un requisito clave para todas Windows aplicaciones. La evidencia de la investigación en la cognitiva cognitiva indica que es necesario poder reconocer cada letra con precisión y que el espaciado uniforme entre las letras es fundamental para un procesamiento rápido. Las letras y palabras que no son simétricas se perciben como feas y degradan la experiencia de lectura. Kevin Larson, del grupo Microsoft Advanced Reading Technologies, escribió un artículo sobre el tema que se publicó en Spectrum IEEE. El artículo se denomina "La tecnología del texto" ( https://www.spectrum.ieee.org/print/5049) .

El texto [DirectWrite](direct-write-portal.md) se representa mediante Microsoft ClearType, lo que mejora la claridad y la legibilidad del texto. ClearType aprovecha el hecho de que las pantallas modernas de RGB tienen franjas RGB para cada píxel que se pueden controlar individualmente. DirectWrite usa las últimas mejoras de ClearType, incluidas primero con Windows Vista con Windows Presentation Foundation, que le permite evaluar no solo las letras individuales, sino también el espaciado entre letras. Antes de estas mejoras de ClearType, el texto con un tamaño de "lectura" de 10 o 12 puntos era difícil de mostrar: podíamos colocar 1 píxel entre letras, que a menudo era demasiado pequeño, o 2 píxeles, que a menudo era demasiado. El uso de la resolución adicional en los subpíxeles proporciona espaciado fraccional, lo que mejora la paridad y simetría de toda la página.

En las dos ilustraciones siguientes se muestra cómo los glifos pueden comenzar en cualquier límite de subpíxeles cuando se usa el posicionamiento de subpíxeles.

La ilustración siguiente se representa mediante la versión GDI del representador ClearType, que no empleaba el posicionamiento de subpíxeles.

![ilustración de la "tecnología" que se representa sin posición de subpíxeles](images/intro-03.png)

La siguiente ilustración se [](direct-write-portal.md) representa mediante la DirectWrite del representador ClearType, que usa el posicionamiento de subpíxeles.

![ilustración de la "tecnología" que se representa con el posicionamiento de subpíxeles](images/intro-04.png)

Tenga en cuenta que el espaciado entre las letras h y n es más par en la segunda imagen y la letra o se separa más de la letra n, más incluso con la letra l. Observe también cómo los lemates de las letras l tienen un aspecto más natural.

El posicionamiento clearType de subpíxel ofrece el espaciado más preciso de caracteres en la pantalla, especialmente en tamaños pequeños donde la diferencia entre un subpíxel y un píxel entero representa una proporción significativa del ancho del glifo. Permite que el texto se mida en el espacio de resolución ideal y se represente en su posición natural en la franja de color DE LA FOTO, con granularidad de subpíxel. El texto medido y representado con esta tecnología es, por definición, independiente de la resolución, lo que significa que el mismo diseño exacto del texto se logra en el intervalo de distintas resoluciones de pantalla.

A diferencia de cualquier tipo de representación clearType de GDI, ClearType de subpíxeles ofrece el ancho de caracteres más preciso.

Text String API adopta la representación de texto de subpíxeles de forma predeterminada, lo que significa que mide el texto en su resolución ideal independientemente de la resolución de visualización actual y genera el resultado de la posición del glifo en función de los anchos de avance del glifo realmente escalados y los desplazamientos de posición.

En el caso del texto de gran [tamaño, DirectWrite](direct-write-portal.md) también permite suavizar los alias a lo largo del eje Y para que los bordes se suavizan y representen las letras según lo previsto en el diseñador de fuentes. En la ilustración siguiente se muestra el suavizado de alias de dirección Y.

![ilustración de "cleartype" representado como texto gdi y como texto de directwrite con suavizado de contorno de dirección Y](images/intro-05.png)

Aunque [DirectWrite](direct-write-portal.md) texto se coloca y se representa mediante ClearType de subpíxeles de forma predeterminada, hay otras opciones de representación disponibles. Muchas aplicaciones existentes usan GDI para representar la mayor parte de su interfaz de usuario, y algunas aplicaciones usan controles de edición del sistema que siguen usando GDI para la representación de texto. Al agregar DirectWrite texto a estas aplicaciones, puede ser necesario sacrificar las mejoras de la experiencia de lectura proporcionadas por ClearType de subpíxeles para que el texto tenga una apariencia coherente en toda la aplicación.

Para cumplir estos requisitos, [DirectWrite](direct-write-portal.md) también admite las siguientes opciones de representación:

-   ClearType de subpíxeles (valor predeterminado).
-   ClearType de subpíxeles con suavizado de alias en dimensiones horizontales y verticales.
-   Texto con alias.
-   Ancho natural de GDI (utilizado por Microsoft Word Vista de lectura, por ejemplo).
-   Ancho compatible con GDI (incluido el mapa de bits incrustado de Asia Oriental).

Cada uno de estos modos de representación se puede ajustar a través de la API DirectWrite y a través del nuevo Windows de entrada ClearType 7.

> [!Note]  
> A partir Windows 8, debe usar el suavizado de contorno de texto de escala de grises en la mayoría de los casos. Consulte la siguiente sección para más información.

 

### <a name="support-for-natural-layout"></a>Compatibilidad con el diseño natural

El diseño natural es independiente de la resolución, por lo que el espaciado de los caracteres no cambia a medida que se acerca o se aleja, o según el ppp de la pantalla. Una ventaja secundaria es que el espaciado se aplica al diseño de la fuente. El diseño natural es posible gracias a DirectWrite la representación natural, lo que significa que los glifos individuales se pueden colocar en una fracción de píxel.

Aunque el diseño natural es el predeterminado, algunas aplicaciones deben representar texto con el mismo espaciado y apariencia que GDI. Para estas aplicaciones, DirectWrite modos de medición natural GDI clásico y GDI y los modos de representación correspondientes.

Cualquiera de los modos de representación anteriores se puede combinar con cualquiera de los dos modos de suavizado de contorno: ClearType o escala de grises. El suavizado de contorno ClearType simula una resolución más alta mediante la manipulación individual de los valores de color rojo, verde y azul de cada píxel. El suavizado de contorno de escala de grises calcula solo un valor de cobertura (o alfa) para cada píxel. ClearType es el valor predeterminado, pero se recomienda el suavizado de contorno de escala de grises para las aplicaciones de la Tienda Windows porque es más rápido y es compatible con el suavizado de contorno estándar, a la vez que sigue siendo muy legible.

## <a name="api-overview"></a>Información general acerca de la API

La [**interfaz IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) es el punto de partida para usar DirectWrite funcionalidad. El generador es el objeto raíz que crea un conjunto de objetos que se pueden usar juntos.

La operación de formato y diseño es un requisito previo para las operaciones, ya que el texto debe tener el formato y la disposición adecuados para un conjunto especificado de restricciones antes de que se pueda dibujar o probar. Dos objetos clave que puede crear con [**idWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para este propósito son [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) Un **objeto IDWriteTextFormat** representa la información de formato de un párrafo de texto. La función [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) toma la cadena de entrada, las restricciones asociadas, como la dimensión del espacio que se va a rellenar, y el objeto **IDWriteTextFormat,** y coloca el resultado totalmente analizado y con formato en **IDWriteTextLayout** para usarlo en operaciones posteriores.

Después, la aplicación puede representar el texto mediante la función [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) proporcionada por [Direct2D](../direct2d/direct2d-portal.md) o mediante la implementación de una función de devolución de llamada que puede usar GDI, Direct2D u otros sistemas gráficos para representar los glifos. Para un único texto de formato, la función [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) en Direct2D proporciona una manera más sencilla de dibujar texto sin tener que crear primero un [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a>Aplicar formato y dibujar "Hola mundo" mediante DirectWrite

En el ejemplo de código siguiente se muestra cómo una aplicación puede dar formato a un único párrafo mediante [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y dibujarlo mediante la función [**DrawText de**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [Direct2D.](../direct2d/direct2d-portal.md)


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



## <a name="accessing-the-font-system"></a>Acceso al sistema de fuentes

Además de especificar un nombre de familia de fuentes para la cadena de texto mediante la interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) del ejemplo anterior, DirectWrite proporciona [a](direct-write-portal.md) las aplicaciones un mayor control sobre la selección de fuentes a través de la enumeración de fuentes y la capacidad de crear una colección de fuentes personalizada basada en fuentes de documento incrustadas.

El [**objeto IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) es una colección de familias de fuentes. DirectWrite proporciona acceso al conjunto de fuentes instalado en el sistema a través de una colección de fuentes especial denominada colección de fuentes del sistema. Esto se obtiene llamando al [**método GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) del [**objeto IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) Una aplicación también puede crear una colección de fuentes personalizada a partir de un conjunto de fuentes enumeradas por una devolución de llamada definida por la aplicación, es decir, fuentes privadas instaladas por una aplicación o fuentes incrustadas en un documento.

Después, la aplicación puede llamar a [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) para obtener un objeto FontFamily específico dentro de la colección y, a continuación, llamar a [**IDWriteFontFamily::GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) para obtener un objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) específico. El **objeto IDWriteFont** representa una fuente en una colección de fuentes y expone propiedades y algunas métricas de fuentes básicas.

[**IDWriteFontFace es**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) otro objeto que representa una fuente y expone un conjunto completo de métricas en una fuente. **IdWriteFontFace** se puede crear directamente a partir de un nombre de fuente; una aplicación no tiene que obtener una colección de fuentes para acceder a ella. Es útil para una aplicación de diseño de texto como Microsoft Word que necesita consultar los detalles de una fuente específica.

En el diagrama siguiente se muestra la relación entre estos objetos.

![diagrama de la relación entre una colección de fuentes, una familia de fuentes y una cara de fuente](images/fontcollection.png)

### <a name="idwritefontface"></a>IDWriteFontFace

El [**objeto IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) representa una fuente y proporciona información más detallada sobre la fuente que el [**objeto IDWriteFont.**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) Las métricas de fuente y glifo de **IDWriteFontFace** son útiles para las aplicaciones que implementan el diseño de texto.

La mayoría de las aplicaciones estándar no usarán estas API directamente y, en su lugar, usarán [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) o especificarán el nombre de familia de fuentes directamente.

En la tabla siguiente se resumen los escenarios de uso de los dos objetos.



| Category                                                                                                         | [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| API para admitir la interacción del usuario, como una interfaz de usuario que elige fuentes: descripción y otras API de información. | Sí                                        | No                                                 |
| API para admitir la asignación de fuentes: familia, estilo, peso, stretch, cobertura de caracteres                                 | Sí                                        | No                                                 |
| DrawText API                                                                                                     | Sí                                        | No                                                 |
| API usadas para la representación                                                                                          | No                                         | Sí                                                |
| API usadas para el diseño de texto: métricas de glifo, y así sucesivamente                                                              | No                                         | Sí                                                |
| API para el control de interfaz de usuario y el diseño de texto: métricas para toda la fuente                                                           | Sí                                        | Sí                                                |



 

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

Las API de representación de texto permiten que los glifos de una fuente DirectWrite se represente en una superficie de [Direct2D](../direct2d/direct2d-portal.md) o en un mapa de bits independiente del dispositivo GDI, o que se [conviertan en](direct-write-portal.md) contornos o mapas de bits. La representación ClearType en DirectWrite admite el posicionamiento de subpíxeles con mayor niguidad y contraste en comparación con las implementaciones anteriores de Windows. DirectWrite también admite texto en blanco y en blanco con alias para admitir escenarios que implican fuentes de Asia Oriental con mapas de bits incrustados, o donde el usuario ha deshabilitado el suavizado de fuentes de cualquier tipo.

Todas las opciones se pueden ajustar mediante todos los botones ClearType disponibles a los que se puede acceder a través de las API de [DirectWrite](direct-write-portal.md) y también se exponen a través del nuevo applet del panel de control de Windows 7 ClearType.

Hay dos API disponibles para representar glifos, una que proporciona una representación acelerada por hardware a través de [Direct2D](../direct2d/direct2d-portal.md) y otra que proporciona representación de software a un mapa de bits de GDI. Una aplicación que usa [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e implementa la devolución de llamada [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) puede llamar a cualquiera de estas funciones en respuesta a una devolución de llamada [**DrawGlyphRun.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Además, las aplicaciones que implementan su propio diseño o tratan con datos de nivel de glifo pueden usar estas API.

1.  [**ID2DRenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    Las aplicaciones pueden usar [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) de la API de [Direct2D](../direct2d/direct2d-portal.md) para proporcionar aceleración de hardware para la representación de texto mediante la GPU. La aceleración de hardware afecta a todas las fases de la canalización de representación de texto, desde la combinación de glifos en ejecuciones de glifos y el filtrado del mapa de bits de ejecución de glifos hasta la aplicación del algoritmo de combinación ClearType a la salida final mostrada. Esta es la API recomendada para obtener el mejor rendimiento de representación.

2.  [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    Las aplicaciones pueden usar el método [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para realizar una representación de software de una ejecución de glifos en un mapa de bits de 32 bpp. El [**objeto IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsula un mapa de bits y un contexto de dispositivo de memoria que se puede usar para representar glifos. Esta API es útil si desea permanecer con GDI porque tiene una base de código existente que se representa en GDI.

Si tiene una aplicación que tiene código de diseño de texto existente que usa GDI y desea conservar su código de diseño existente pero usar [DirectWrite solo](direct-write-portal.md) para el paso final de representación de glifos, [**IDWriteGdiInterop::CreateFontFaceFromHdc proporciona**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) el puente entre las dos API. Antes de llamar a esta función, la aplicación usará la función **IDWriteGdiInterop::CreateFontFaceFromHdc** para obtener una referencia de fuente-cara de un contexto de dispositivo.

> [!Note]  
> En la mayoría de los escenarios, es posible que las aplicaciones no necesiten usar estas API de representación de glifos. Una vez que una aplicación ha creado un objeto [**IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) puede usar el método [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) para representar el texto.

 

## <a name="custom-rendering-modes"></a>Modos de representación personalizados

Varios parámetros afectan a la representación de texto, como gamma, nivel ClearType, geometría de píxeles y contraste mejorado. Los parámetros de representación se encapsulan mediante un objeto , que implementa la interfaz [**pública IDWriteRenderingParams.**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) El objeto de parámetros de representación se inicializa automáticamente en función de las propiedades de hardware o las preferencias del usuario especificadas a través del applet del panel de control ClearType Windows 7. Por lo general, si [](direct-write-portal.md) un cliente usa la API de diseño DirectWrite, DirectWrite seleccionará automáticamente un modo de representación que se corresponda con el modo de medición especificado.

Las aplicaciones que desean más control pueden usar [**IDWriteFactory::CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) para implementar las distintas opciones de representación. Esta función también se puede usar para establecer el gamma, la geometría de píxeles y el contraste mejorado.

Estas son las distintas opciones de representación disponibles:

-   Suavizado de alias de subpíxeles

    La aplicación establece el parámetro *renderingMode* en DWRITE RENDERING MODE NATURAL para especificar la representación con suavizado de \_ alias solo en la dimensión \_ \_ horizontal.

-   Suavizado de alias de subpíxeles en dimensiones horizontales y verticales.

    La aplicación establece el parámetro *renderingMode* en DWRITE RENDERING MODE NATURAL SYMMETRIC para especificar la representación con suavizado de alias en \_ dimensiones \_ \_ \_ horizontales y verticales. Esto hace que las curvas y las líneas diagonales parezcan más fluidas a costa de cierta subilidad, y normalmente se usa en tamaños superiores a 16 ppem.

-   Texto con alias

    La aplicación establece el parámetro *renderingMode* en DWRITE \_ RENDERING MODE \_ \_ ALIASED para especificar texto con alias.

-   Texto de escala de grises

    La aplicación establece el *parámetro pixelGeometry* en DWRITE \_ PIXEL GEOMETRY FLAT para especificar texto de escala de \_ \_ grises.

-   Ancho compatible con GDI (incluido el mapa de bits incrustado de Asia Oriental)

    La aplicación establece el parámetro *renderingMode* en DWRITE RENDERING MODE GDI CLASSIC para especificar el suavizado de alias de ancho \_ compatible con \_ \_ \_ GDI.

-   Ancho natural de GDI

    La aplicación establece el parámetro *renderingMode* en DWRITE RENDERING MODE GDI NATURAL para especificar el suavizado de alias compatible con ancho \_ natural de \_ \_ \_ GDI.

-   Texto de esquema

    Para la representación en tamaños grandes, es posible que un desarrollador de aplicaciones prefiera representar mediante el contorno de fuente en lugar de rasterizar en un mapa de bits. La aplicación establece el parámetro *renderingMode* en **DWRITE \_ RENDERING MODE \_ \_ OUTLINE** para especificar que la representación debe omitir el rasterizador y usar los contornos directamente.

## <a name="gdi-interoperability"></a>Interoperabilidad de GDI

La [**interfaz IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) proporciona interoperabilidad con GDI. Esto permite a las aplicaciones continuar su inversión existente en bases de código GDI y usar de forma [selectiva](direct-write-portal.md) DirectWrite representación o diseño.

Estas son las API que permiten que una aplicación migre hacia o desde el sistema de fuentes GDI:

-   [**CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    Crea un [**objeto IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) que coincide con las propiedades especificadas por la [**estructura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

-   [**ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    Inicializa una estructura [**LOGFONT basada**](/windows/win32/api/wingdi/ns-wingdi-logfonta) en las propiedades compatibles con GDI del [**IDWriteFont especificado.**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)

-   [**ConvertFontFaceToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    Inicializa una estructura [**LOGFONT basada**](/windows/win32/api/wingdi/ns-wingdi-logfonta) en las propiedades compatibles con GDI del [**IDWriteFontFace especificado.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)

-   [**CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    Crea un [**objeto IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) que corresponde al **objeto HFONT seleccionado actualmente.**

## <a name="conclusion"></a>Conclusión

Mejorar la experiencia de lectura es de gran valor para los usuarios, ya sea en pantalla o en papel. [DirectWrite](direct-write-portal.md) proporciona la facilidad de uso y el modelo de programación por capas para que los desarrolladores de aplicaciones mejoren la experiencia de texto para sus Windows aplicaciones. Las aplicaciones pueden usar DirectWrite para representar texto con formato enriquecido para su interfaz de usuario y documentos con la API de diseño. En escenarios más complejos, una aplicación puede trabajar directamente con glifos, acceder a fuentes, etc., y aprovechar la eficacia de DirectWrite para ofrecer tipografía de alta calidad.

Las funcionalidades de interoperabilidad de [DirectWrite](direct-write-portal.md) permiten a los desarrolladores de aplicaciones llevar a cabo sus códigos base de Win32 existentes y adoptar DirectWrite de forma selectiva dentro de sus aplicaciones.

 

 