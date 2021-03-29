---
title: 'Información general sobre los pinceles '
description: Describe los diferentes tipos de pinceles que proporciona Direct2D.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104421585"
---
# <a name="brushes-overview"></a>Información general sobre los pinceles 

En esta información general se describe cómo crear y usar los objetos [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)y [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para pintar áreas con colores sólidos, degradados y mapas de bits. Contiene las siguientes secciones:

## <a name="prerequisites"></a>Requisitos previos

En esta información general se supone que está familiarizado con la estructura de una aplicación básica de Direct2D, tal como se describe en [creación de una aplicación sencilla de direct2d](direct2d-quickstart.md).

## <a name="brush-types"></a>Tipos de pincel

Un pincel "pinta" un área con su salida. Distintos pinceles tienen tipos de salida diferentes. Direct2D proporciona cuatro tipos de pincel: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta un área con un color sólido, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) con un degradado lineal, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) con un degradado radial y [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con un mapa de bits.

> [!NOTE]  
> A partir de Windows 8, también puede usar [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), que es similar a un pincel de mapa de bits, pero también puede usar primitivas.

Todos los pinceles se heredan de [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) y comparten un conjunto de características comunes (estableciendo y obteniendo la opacidad y transformando los pinceles); se crean mediante [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y son recursos dependientes del dispositivo: la aplicación debe crear pinceles después de inicializar el destino de representación con el que se usarán los pinceles y volver a crear los pinceles cada vez que sea necesario volver a crear el destino de representación. (Para obtener más información acerca de los recursos, consulte [información general sobre recursos](resources-and-resource-domains.md)).

En la ilustración siguiente se muestran ejemplos de cada uno de los distintos tipos de pincel.

![Ilustración de los efectos visuales de los pinceles de color sólido, pinceles de degradado lineal, pinceles de degradado radial y pinceles de mapa de bits](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a>Conceptos básicos de color

Antes de pintar con un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o un pincel de degradado, debe elegir colores. En Direct2D, los colores se representan mediante la estructura de [**\_ color \_ F de D2D1**](d2d1-color-f.md) (que, en realidad, es simplemente un nombre nuevo para la estructura que usa Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).

Antes de Windows 8, [**el \_ color \_ F de D2D1**](d2d1-color-f.md) usa la codificación sRGB. la codificación sRGB divide los colores en cuatro componentes: rojo, verde, azul y alfa. Cada componente se representa mediante un valor de punto flotante con un intervalo normal de 0,0 a 1,0. Un valor de 0,0 indica la ausencia completa de ese color, mientras que un valor de 1,0 indica que el color está completamente presente. Para el componente alfa, 0,0 representa un color completamente transparente y 1,0 representa un color totalmente opaco.

A partir de Windows 8, el [**\_ color \_ F de D2D1**](d2d1-color-f.md) también acepta la codificación ScRGB. scRGB es un superconjunto de que permite valores de color por encima de 1,0 y por debajo de 0,0.

Para definir un color, puede usar la estructura [**D2D1 de \_ color \_ F**](d2d1-color-f.md) e inicializar sus campos usted mismo, o bien puede usar la clase [**D2D1:: ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para ayudarle a crear el color. La clase **ColorF** proporciona varios constructores para definir colores. Si el valor alfa no se especifica en los constructores, se toma como valor predeterminado 1,0.

-   Use el constructor [**ColorF (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) para especificar un color predefinido y un valor de canal alfa. Un valor de canal alfa oscila entre 0,0 y 1,0, donde 0,0 representa un color completamente transparente y 1,0 representa un color totalmente opaco. En la ilustración siguiente se muestran varios colores predefinidos y sus equivalentes hexadecimales. Para obtener una lista completa de los colores predefinidos, vea la sección de constantes de color de la clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

    ![Ilustración de los colores predefinidos](images/brushes-ovw-colors.png)

    En el ejemplo siguiente se crea un color predefinido y se usa para especificar el color de un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   Use el constructor [**ColorF (float, Float, Float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) para especificar un color en la secuencia de un rojo, verde, azul y alfa, donde cada elemento tiene un valor entre 0,0 y 1,0.

    En el ejemplo siguiente se especifican los valores rojo, verde, azul y alfa de un color.

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   Use el constructor [**ColorF (UINT32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) para especificar el valor hexadecimal de un color y un valor alfa, tal y como se muestra en el ejemplo siguiente.
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a>Modos alfa

Independientemente del modo alfa del destino de representación con el que se usa un pincel, los valores de [**\_ color \_ F de D2D1**](d2d1-color-f.md) siempre se interpretan como alfa recto.

## <a name="using-solid-color-brushes"></a>Usar pinceles de color sólido

Para crear un pincel de color sólido, llame al método [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , que devuelve un valor HRESULT y un objeto [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) . En la ilustración siguiente se muestra un cuadrado con trazos con un pincel de color negro y pintado con un pincel de color sólido que tiene el valor de color de 0x9ACD32.

![Ilustración de un cuadrado pintado con un pincel de color sólido](images/brushes-ovw-solidcolor.png)

En el código siguiente se muestra cómo crear y usar un pincel de color negro y un pincel con un valor de color de 0x9ACD32 para rellenar y dibujar este cuadrado.


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



A diferencia de otros pinceles, la creación de una [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) es una operación relativamente económica. Puede crear objetos **ID2D1SolidColorBrush** cada vez que represente con poco o ningún impacto en el rendimiento. Este enfoque no se recomienda para los pinceles de degradado o de mapa de bits.

## <a name="using-linear-gradient-brushes"></a>Usar pinceles de degradado lineal

Un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pinta un área con un degradado lineal definido a lo largo de una línea, el eje de degradado. Los colores del degradado y su ubicación se especifican a lo largo del eje de degradado mediante objetos [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) . También puede modificar el eje de degradado, que le permite crear un degradado horizontal y vertical, e invertir la dirección del degradado. Para crear un pincel de degradado lineal, llame al método [**ID2D1RenderTarget:: CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .

En la ilustración siguiente se muestra un cuadrado que se pinta con un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que tiene dos colores predefinidos: "Yellow" y "ForestGreen".

![Ilustración de un cuadrado pintado con un pincel de degradado lineal de amarillo y verde de bosque](images/brushes-ovw-lineargradient.png)

Para crear el degradado que se muestra en la ilustración anterior, siga estos pasos:

1.  Declare dos objetos de delimitador de [**\_ \_ degradado D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Cada delimitador de degradado especifica un color y una posición. Una posición de 0,0 indica el principio del degradado, mientras que una posición de 1,0 indica el final del degradado.

    En el código siguiente se crea una matriz de dos objetos de delimitador de [**\_ \_ degradado D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . La primera parada especifica el color "Yellow" en la posición 0 y el segundo valor de STOP especifica el color "ForestGreen" en la posición 1.

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  Cree un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection). En el ejemplo siguiente se llama a [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), pasando la matriz de objetos de delimitador de [**\_ degradado \_ D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , el número de delimitadores de degradado (2), [**D2D1 \_ gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) para la interpolación y [**D2D1 la \_ \_ \_ abrazadera del modo Extend**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) para el modo Extend.

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  Cree el [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). En el ejemplo siguiente se llama al método [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) y se le pasan las propiedades de pincel de degradado lineal que contienen el punto inicial en (0,0) y el punto final en (150, 150) y los delimitadores de degradado creados en el paso anterior.
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  Use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). En el siguiente ejemplo de código se usa el pincel para relleno un rectángulo.
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a>Más información sobre los delimitadores de degradado

El delimitador de [**\_ degradado \_ D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) es el bloque de creación básico de un pincel de degradado. Un delimitador de degradado especifica el color y la posición a lo largo del eje de degradado. El valor de la posición del degradado oscila entre 0,0 y 1,0. Cuanto más se acerque a 0,0, más próximo será el color al inicio del degradado. cuanto más se acerque a 1,0, más próximo será el color al final del degradado.

En la ilustración siguiente se resaltan los delimitadores de degradado. El círculo marca la posición de los delimitadores de degradado y una línea discontinua muestra el eje de degradado.

![Ilustración de un pincel de degradado lineal con cuatro paradas a lo largo del eje](images/4stoplineargradient.png)

El primer delimitador de degradado especifica el color amarillo en una posición de 0,0. El segundo delimitador de degradado especifica el color rojo en una posición de 0,25. De izquierda a derecha a lo largo del eje de degradado, los colores entre estos dos se detienen gradualmente de amarillo a rojo. El tercer delimitador de degradado especifica el color azul en una posición de 0,75. Los colores entre el segundo y el tercer delimitador de degradado cambian gradualmente de rojo a azul. El cuarto delimitador de degradado especifica verde lima en una posición de 1,0. Los colores entre el tercer y cuarto delimitador de degradado cambian gradualmente de azul a verde lima.

## <a name="the-gradient-axis"></a>El eje de degradado

Como se mencionó anteriormente, los puntos de degradado de un pincel de degradado lineal se colocan a lo largo de una línea, el eje de degradado. Puede especificar la orientación y el tamaño de la línea mediante los campos **startPoint** y **endPoint** de la estructura [**D2D1 \_ linear \_ gradiente \_ Brush \_ Properties**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) al crear un pincel de degradado lineal. Después de crear un pincel, puede ajustar el eje de degradado llamando a los métodos [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) y [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) del pincel. Manipulando el punto inicial y el punto final del pincel, puede crear degradados horizontales y verticales, invertir la dirección del degradado, etc.

Por ejemplo, en la siguiente ilustración, el punto inicial se establece en (0, 0) y el punto final en (150, 50); Esto crea un degradado diagonal que comienza en la esquina superior izquierda y se extiende a la esquina inferior derecha del área que se está pintando. Al establecer el punto inicial en (0, 25) y el punto final en (150, 25), se crea un degradado horizontal. Del mismo modo, si se establece el punto inicial en (75, 0) y el punto final en (75, 50), se crea un degradado vertical. Al establecer el punto inicial en (0, 50) y el punto final en (150, 0), se crea un degradado diagonal que comienza en la esquina inferior izquierda y se extiende hasta la esquina superior derecha del área que se está pintando.

![Ilustración de cuatro ejes de degradado diferentes en el mismo rectángulo](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a>Usar pinceles de degradado radial

A diferencia de un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), que combina dos o más colores a lo largo de un eje de degradado, una [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) pinta un área con un degradado radial que combina dos o más colores a través de una elipse. Mientras que un **ID2D1LinearGradientBrush** define su eje de degradado con un punto inicial y un punto final, un **ID2D1RadialGradientBrush** define su elipse de degradado especificando un centro, radios horizontales y verticales, y un desplazamiento de origen del degradado.

Al igual que un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) usa un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) para especificar los colores y las posiciones del degradado.

En la ilustración siguiente se muestra un círculo pintado con un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush). El círculo tiene dos delimitadores de degradado: el primero especifica un color predefinido "Yellow" en la posición 0,0 y el segundo especifica un color predefinido "ForestGreen" en una posición de 1,0. El degradado tiene un centro de (75, 75), un desplazamiento de origen del degradado de (0,0) y un radio x e y de 75.

![Ilustración de un círculo pintado con un pincel de degradado radial](images/brushes-ovw-radials.png)

En los siguientes ejemplos de código se muestra cómo pintar este círculo con un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que tiene dos delimitadores de color: "Yellow" en la posición 0,0 y "ForestGreen" en una posición de 1,0. De forma similar a la creación de un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), en el ejemplo se llama a [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para crear un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de una matriz de delimitadores de degradado.


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



Para crear un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use el método [**ID2D1RenderTarget:: CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) . **CreateRadialGradientBrush** toma tres parámetros. El primer parámetro, una [**\_ propiedad de \_ \_ pincel de \_ degradado radial D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) especifica el centro, el desplazamiento del origen del degradado y los radios horizontal y vertical del degradado. El segundo parámetro es un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) que describe los colores y sus posiciones en el degradado, y el tercer parámetro es la dirección del puntero que recibe la nueva referencia de **ID2D1RadialGradientBrush** . Algunas sobrecargas toman un parámetro adicional, una estructura de [**\_ \_ propiedades de pincel D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) que especifica un valor de opacidad y una transformación que se va a aplicar al nuevo pincel.

En el ejemplo siguiente se llama a [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), se pasa la matriz de delimitadores de degradado y las propiedades de pincel de degradado radial que tienen el valor *central* establecido en (75, 75), el *gradientOriginOffset* establecido en (0,0) y *radiusX* y *RADIUS* , ambos establecidos en 75.


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



En el último ejemplo se usa el pincel para rellenar una elipse.


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a>Configuración de un degradado radial

Los distintos valores de *Center*, *gradientOriginOffset*, *radiusX* y/o *RADIUS* generan degradados diferentes. En la ilustración siguiente se muestran varios degradados radiales con distintos desplazamientos de origen de degradado, lo que crea la apariencia de la luz que ilumina los círculos de distintos ángulos.

![Ilustración del mismo círculo pintado con pinceles de degradado radial con desplazamientos de origen diferentes](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a>Usar pinceles de mapa de bits

Un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pinta un área con un mapa de bits (representado por un objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).

En la ilustración siguiente se muestra un cuadrado pintado con un mapa de bits de una planta.

![Ilustración de un cuadrado pintado con un mapa de bits de planta](images/brushes-ovw-bitmap.png)

En los ejemplos siguientes se muestra cómo pintar este cuadrado con un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).

En el primer ejemplo se inicializa un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) para su uso con el pincel. El **ID2D1Bitmap** se proporciona mediante un método auxiliar, LoadResourceBitmap, que se define en otra parte del ejemplo.


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



Para crear el pincel de mapa de bits, llame al método [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) y especifique el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con el que desea pintar. El método devuelve un **valor HRESULT** y un objeto [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) . Algunas sobrecargas de **CreateBitmapBrush** permiten especificar opciones adicionales mediante la aceptación de [**\_ \_ las propiedades de pincel de D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) y una estructura de [**\_ \_ \_ propiedades de pincel de mapa de bits de D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



En el ejemplo siguiente se usa el pincel para rellenar un rectángulo.


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a>Configurar modos de extensión

A veces, el degradado de un pincel de degradado o el mapa de bits para un pincel de mapa de bits no rellena completamente el área que se está pintando.

-   Cuando esto sucede en un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D usa la configuración de modo de extensión horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) y vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) del pincel para determinar cómo rellenar el área restante.

-   Cuando esto sucede en un pincel de degradado, Direct2D determina cómo rellenar el área restante mediante el valor del parámetro de [**\_ \_ modo de extensión D2D1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) que especificó al llamar a [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para crear el [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)del pincel de degradado.

En la ilustración siguiente se muestran los resultados de cada combinación posible de los modos de extensión para [**una \_ \_ \_ abrazadera en modo de extensión**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) de [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): D2D1 (clamp), **D2D1 \_ Extend \_ Mode \_ Wrap** (Wrap) y **D2D1 \_ Extend \_ Mirror** (Mirror).

![Ilustración de una imagen original y las imágenes resultantes de varios modos de extensión](images/bitmapwrap-clamp-mirror.png)

En el ejemplo siguiente se muestra cómo establecer los modos x-e y-Extend del pincel de mapa de bits en [**D2D1 \_ extender \_ Mirror**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode). A continuación, pinta el rectángulo con el [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



Genera la salida como se muestra en la siguiente ilustración.

![Ilustración de una imagen original y la imagen resultante después de reflejar las direcciones x e y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a>Transformación de pinceles

Cuando se pinta con un pincel, pinta en el espacio de coordenadas del destino de representación. Los pinceles no se colocan automáticamente para alinearse con el objeto que se está dibujando; de forma predeterminada, empiezan a pintar en el origen (0,0) del destino de representación.

Puede "desplace" el degradado definido por un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) a un área de destino estableciendo el punto inicial y el punto final. Del mismo modo, puede trasladar el degradado definido por un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) cambiando su centro y radios.

Para alinear el contenido de un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con el área que se está dibujando, puede usar el método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) para traducir el mapa de bits a la ubicación deseada. Esta transformación solo afecta al pincel; no afecta a ningún otro contenido dibujado por el destino de representación.

En las ilustraciones siguientes se muestra el efecto de usar un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para rellenar un rectángulo ubicado en (100, 100). En la ilustración de la ilustración izquierda se muestra el resultado de llenar el rectángulo sin transformar el pincel: el mapa de bits se dibuja en el origen del destino de representación. Como resultado, solo aparece una parte del mapa de bits en el rectángulo. En la ilustración de la derecha se muestra el resultado de transformar el **ID2D1BitmapBrush** para que su contenido se desplace 50 píxeles hacia la derecha y 50 píxeles hacia abajo. El mapa de bits ahora rellena el rectángulo.

![Ilustración de un cuadrado pintado con un pincel de mapa de bits sin transformar el pincel y transformando el pincel](images/brushes-ovw-transform.png)

En el código siguiente se muestra cómo hacerlo. En primer lugar, aplique una traducción al [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moviendo el pincel 50 píxeles a lo largo del eje x y 50 píxeles hacia abajo a lo largo del eje y. A continuación, use **ID2D1BitmapBrush** para rellenar el rectángulo que tiene la esquina superior izquierda en (100, 100) y la esquina inferior derecha en (200, 200).


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a>Temas relacionados

* [Referencia de Direct2D](reference.md)
* [Cómo crear un pincel de color sólido](how-to-create-a-solid-color-brush.md)
* [Cómo crear un pincel de degradado lineal](how-to-create-a-linear-gradient-brush.md)
* [Cómo crear un pincel de degradado radial](how-to-create-a-radial-gradient-brush.md)
* [Cómo crear un pincel de mapa de bits](how-to-create-a-bitmap-brush.md)
