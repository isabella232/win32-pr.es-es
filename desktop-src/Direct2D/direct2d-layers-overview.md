---
title: Información general sobre capas
description: Describe los conceptos básicos de las capas de Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, capas
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 027be097c5c21929f3ccdbaa169a1f3dac55b394
ms.sourcegitcommit: 698ce2d9ba2fa650f2875225d99623995fac246a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2021
ms.locfileid: "114231612"
---
# <a name="layers-overview"></a>Información general sobre capas

En esta introducción se describen los conceptos básicos del uso de capas de Direct2D. Contiene las siguientes secciones:

-   [¿Qué son las capas?](#what-are-layers)
-   [Capas en Windows 8 y versiones posteriores](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceContext y PushLayer](#id2d1devicecontext-and-pushlayer)
    -   [D2D1 \_ LAYER \_ PARAMETERS1 y D2D1 \_ LAYER \_ OPTIONS1](/windows)
    -   [Modos de fusión](#blend-modes)
    -   [Interoperación](#interoperation)
-   [Creación de capas](#creating-layers)
-   [Límites de contenido](#content-bounds)
-   [Máscaras geométricas](#geometric-masks)
-   [Máscaras de opacidad](#opacity-masks)
-   [Alternativas a las capas](#alternatives-to-layers)
-   [Recorte de una forma arbitraria](#clipping-an-arbitrary-shape)
    -   [Clips alineados en el eje](#axis-aligned-clips)
-   [Temas relacionados](#related-topics)

## <a name="what-are-layers"></a>¿Qué son las capas?

Las capas, representadas [**por objetos ID2D1Layer,**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) permiten a una aplicación manipular un grupo de operaciones de dibujo. Para usar una capa, "insertarla" en un destino de representación. Las operaciones de dibujo posteriores del destino de representación se dirigen a la capa. Cuando haya terminado con la capa, "resalte" la capa del destino de representación, que compone el contenido de la capa de nuevo al destino de representación.

Al igual que los pinceles, las capas son recursos dependientes del dispositivo creados por destinos de representación. Las capas se pueden usar en cualquier destino de representación en el mismo dominio de recursos que contiene el destino de representación que lo creó. Sin embargo, un recurso de capa solo puede ser utilizado por un destino de representación a la vez. Para obtener más información sobre los recursos, vea Información [general sobre recursos.](resources-and-resource-domains.md)

Aunque las capas ofrecen una técnica de representación eficaz para producir efectos interesantes, un número excesivo de capas en una aplicación puede afectar negativamente a su rendimiento, debido a los distintos costos asociados con la administración de capas y recursos de capas. Por ejemplo, existe el costo de rellenar o borrar la capa y, a continuación, combinarla de nuevo, especialmente en hardware de gama superior. A continuación, existe el costo de administrar los recursos de la capa. Si los resigna con frecuencia, los detenciones resultantes en la GPU serán el problema más importante. Al diseñar la aplicación, intente maximizar la utilización de recursos de capa.

## <a name="layers-in-windows-8-and-later"></a>Capas en Windows 8 y versiones posteriores

Windows 8 nuevas API relacionadas con capas que simplifican, mejoran el rendimiento de y agregan características a las capas.

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceContext y PushLayer

La interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) se deriva de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y es clave para mostrar contenido de Direct2D en Windows 8. Para obtener más información sobre esta interfaz, vea Dispositivos y [contextos de dispositivo.](devices-and-device-contexts.md) Con la interfaz de contexto del dispositivo, puede omitir la llamada al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y, a continuación, pasar NULL al [**método ID2D1DeviceContext::P ushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) Direct2D administra automáticamente el recurso de capa y puede compartir recursos entre capas y gráficos de efectos.

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>D2D1 \_ LAYER \_ PARAMETERS1 y D2D1 \_ LAYER \_ OPTIONS1

La [**estructura D2D1 \_ LAYER \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) es la misma que los PARÁMETROS DE CAPA [**D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), excepto que el miembro final de la estructura es ahora una [**enumeración D2D1 \_ LAYER \_ OPTIONS1.**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)

[**D2D1 \_ LAYER \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) no tiene ninguna opción ClearType y tiene dos opciones diferentes que puede usar para mejorar el rendimiento:

-   [**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE FROM \_ \_ BACKGROUND:**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)Direct2D representa primitivas en la capa sin borrarla con negro transparente. Este no es el valor predeterminado, pero en la mayoría de los casos da como resultado un mejor rendimiento.

-   [**D2D1 \_ OPCIONES \_ DE CAPA1 \_ OMITIR \_ ALFA:**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)si la superficie subyacente está establecida en [**D2D1 \_ ALPHA MODE \_ \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), esta opción permite a Direct2D evitar modificar el canal alfa de la capa. No lo use en otros casos.

### <a name="blend-modes"></a>Modos de fusión

A partir Windows 8, el contexto [](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) del dispositivo tiene un modo de combinación primitivo que determina cómo se combina cada primitivo con la superficie de destino. Este modo también se aplica a las capas cuando se llama al [**método PushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))

Por ejemplo, si usa una capa para recortar primitivas con transparencia, establezca el modo [**COPY \_ DE BLEND \_ \_ PRIMITIVO D2D1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) en el contexto del dispositivo para obtener los resultados adecuados. El modo de copia hace que el contexto del dispositivo interpola linealmente los 4 canales de color, incluido el canal alfa, de cada píxel con el contenido de la superficie de destino según la máscara geométrica de la capa.

### <a name="interoperation"></a>Interoperación

A partir Windows 8, Direct2D admite la interoperación con Direct3D y GDI mientras se inserta una capa o un clip. Se llama [**a ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) mientras se inserta una capa para interoperar con GDI. Se llama [**a ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) y, a continuación, se representa en la superficie subyacente para interoperar con Direct3D. Es su responsabilidad representar dentro de la capa o clip con Direct3D o GDI. Si intenta representar fuera de la capa o recortar los resultados no están definidos.

## <a name="creating-layers"></a>Creación de capas

El trabajo con capas requiere estar familiarizado con los métodos [**CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))y [**PopLayer,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) y la estructura DE PARÁMETROS DE CAPA [**D2D1, \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) que contiene un conjunto de datos paramétricos que definen cómo se puede usar la capa. En la lista siguiente se describen los métodos y la estructura.

-   Llame al [**método CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para crear un recurso de capa.
    > [!Note]  
    > A partir Windows 8, puede omitir la llamada al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y, a continuación, pasar NULL al método [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) en la [**interfaz ID2D1DeviceContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) Esto es más sencillo y permite que Direct2D administre automáticamente el recurso de capa y comparta recursos entre capas y gráficos de efectos.

     

-   Después de que el destino de representación haya empezado a dibujar (después de llamar a su [**método BeginDraw),**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) puede usar el [**método PushLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) El **método PushLayer** agrega la capa especificada al destino de representación, de modo que el destino recibe todas las operaciones de dibujo posteriores hasta que se llama a [**PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) Este método toma un [**objeto ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) devuelto llamando a [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y *a layerParameters* en la estructura DE PARÁMETROS [**DE \_ CAPA \_ D2D1.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) En la tabla siguiente se describen los campos de la estructura . 

    | Campo                 | Descripción|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **contentBounds**     | Límites de contenido de la capa. El contenido no se representará fuera de estos límites. Este parámetro tiene como valor predeterminado [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect). Cuando se usa el valor predeterminado, los límites de contenido se toman eficazmente como límites del destino de representación. |
    | **geometricMask**     | (Opcional) Área, definida por [**id2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)al que se debe recortar la capa. Establezca en **NULL** si la capa no se debe recortar a una geometría. |
    | **maskAntialiasMode** | Valor que especifica el modo de suavizado de contorno para la máscara geométrica especificada por el **campo geometricMask.** |
    | **maskTransform**     | Valor que especifica la transformación que se aplica a la máscara geométrica al componer la capa. Esto es relativo a la transformación del mundo.  |
    | **Opacidad**           | Valor de opacidad de la capa. La opacidad de cada recurso de la capa se multiplica con este valor al componer en el destino.  |
    | **opacityBrush**      | (Opcional) Pincel que se usa para modificar la opacidad de la capa. El pincel se asigna a la capa y el canal alfa de cada píxel de pincel asignado se multiplica con respecto al píxel de capa correspondiente. Establezca en **NULL** si la capa no debe tener una máscara de opacidad.   |
    | **layerOptions**      | Valor que especifica si la capa pretende representar texto con suavizado de contorno ClearType. El valor predeterminado de este parámetro es off. Activarlo permite que ClearType funcione correctamente, pero da como resultado una velocidad de representación ligeramente más lenta.    |

    

     

    > [!Note]  
    > A partir Windows 8, no se puede representar con ClearType en una capa, por lo que el parámetro **layerOptions** siempre debe establecerse en [**D2D1 \_ LAYER OPTIONS \_ \_ NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)

     

    Para mayor comodidad, Direct2D proporciona el método [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) para ayudarle a crear estructuras [**de PARÁMETROS DE CAPA D2D1. \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)

-   Para componer el contenido de la capa en el destino de representación, llame al [**método PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) Debe llamar al método **PopLayer** antes de llamar al [**método EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)

En el ejemplo siguiente se muestra cómo usar [**CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))y [**PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) Todos los campos de la estructura DE PARÁMETROS DE CAPA [**\_ \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) se establecen en sus valores predeterminados, excepto **opacityBrush**, que se establece en [**id2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



El código se ha omitido en este ejemplo.

Tenga en cuenta que cuando llame a [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) y [**PopLayer,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)asegúrese de que **cada PushLayer** tiene una llamada **a PopLayer correspondiente.** Si hay más llamadas **a PopLayer** que llamadas **pushLayer,** el destino de representación se coloca en un estado de error. Si se llama a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) antes de que se coloquen todas las capas pendientes, el destino de representación se coloca en un estado de error y devuelve un error. Para borrar el estado de error, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="content-bounds"></a>Límites de contenido

**ContentBounds establece** el límite de lo que se va a dibujar en la capa. Solo los elementos dentro de los límites de contenido se componen de nuevo en el destino de representación.

En el ejemplo siguiente se muestra cómo especificar **contentBounds** para que la imagen original se recorte a los límites de contenido con la esquina superior izquierda en (10, 108) y la esquina inferior derecha en (121, 177). En la ilustración siguiente se muestra la imagen original y el resultado de recortar la imagen a los límites de contenido.

![ilustración de límites de contenido en una imagen original y la imagen recortada resultante](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



El código se ha omitido en este ejemplo.

> [!Note]
>
> La imagen recortada resultante se ve afectada aún más si se especifica **una geometríaMask**. Consulte la [sección Máscaras geométricas](#geometric-masks) para obtener más información.

 

## <a name="geometric-masks"></a>Máscaras geométricas

Una máscara geométrica es un clip o un recorte, definido por un objeto [**ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) que enmascara una capa cuando se dibuja mediante un destino de representación. Puede usar el campo **geometryMask de** la estructura DE PARÁMETROS [**DE \_ CAPA \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para enmascarar los resultados en una geometría. Por ejemplo, si desea mostrar una imagen enmascarada por una letra de bloque "A", primero puede crear una geometría que represente la letra de bloque "A" y usar esa geometría como máscara geométrica para una capa. Después de insertar la capa, puede dibujar la imagen. Al hacer clic en la capa, la imagen se recorta a la forma "A" de la letra de bloque.

En el ejemplo siguiente se muestra cómo crear un [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) que contiene una forma de una montaña y, a continuación, pasar la geometría de ruta de acceso a [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)). A continuación, dibuja un mapa de bits y cuadrados. Si solo hay un mapa de bits en la capa que se va a representar, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con fijación para mejorar la eficacia. En la siguiente ilustración se muestra el resultado del ejemplo.

![ilustración de una imagen de una hoja y la imagen resultante después de aplicar una máscara geométrica de una montaña](images/layers-bitmapmask.png)

En el primer ejemplo se define la geometría que se va a usar como máscara.


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



En el ejemplo siguiente se usa la geometría como máscara para la capa.


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



El código se ha omitido en este ejemplo.

> [!Note]
>
> En general, si especifica una **geometríaMask**, puede usar el valor predeterminado, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), para **contentBounds**.
>
> Si **contentBounds** es NULL y **geometricMask** no es NULL, los límites de contenido son efectivamente los límites de la máscara geométrica después de aplicar la transformación de máscara.
>
> Si **contentBounds** no es NULL y **geometricMask** no es NULL, la máscara geométrica transformada se recorta eficazmente en los límites de contenido y se supone que los límites de contenido son infinitos.

 

## <a name="opacity-masks"></a>Máscaras de opacidad

Una máscara de opacidad es una máscara, descrita por un pincel o mapa de bits, que se aplica a otro objeto para que ese objeto sea parcial o completamente transparente. Permite usar el canal alfa de un pincel como máscara de contenido. Por ejemplo, puede definir un pincel de degradado radial que varíe de opaco a transparente para crear un efecto de viñeta.

En el ejemplo siguiente se usa [**id2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) como máscara de opacidad. A continuación, dibuja un mapa de bits y cuadrados. Si solo hay un mapa de bits en la capa que se va a representar, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con fijación para mejorar la eficacia. En la ilustración siguiente se muestra la salida de este ejemplo.

![ilustración de una imagen de árboles y la imagen resultante después de aplicar una máscara de opacidad](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



El código se ha omitido en este ejemplo.

> [!Note]  
> En este ejemplo se usa una capa para aplicar una máscara de opacidad a un solo objeto para que el ejemplo sea lo más sencillo posible. Al aplicar una máscara de opacidad a un solo objeto, es más eficaz usar los métodos [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) o [**FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) en lugar de una capa.

 

Para obtener instrucciones sobre cómo aplicar una máscara de opacidad sin usar una capa, vea La información general [sobre las máscaras de opacidad](opacity-masks-overview.md).

## <a name="alternatives-to-layers"></a>Alternativas a las capas

Como se mencionó anteriormente, un número excesivo de capas puede afectar negativamente al rendimiento de la aplicación. Para mejorar el rendimiento, evite usar capas siempre que sea posible; en su lugar, use sus alternativas. En el ejemplo de código siguiente se muestra cómo usar [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para recortar una región, como alternativa al uso de una capa con límites de contenido.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



De forma similar, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con fijación como alternativa al uso de una capa con una máscara de opacidad cuando solo hay un contenido en la capa que se va a representar, como se muestra en el ejemplo siguiente.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



Como alternativa al uso de una capa con una máscara geométrica, considere la posibilidad de usar una máscara de mapa de bits para recortar una región, como se muestra en el ejemplo siguiente.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Por último, si desea aplicar opacidad a una sola primitiva, debe multiplicar la opacidad en en el color del pincel y, a continuación, representar la primitiva. No necesita una capa ni un mapa de bits de máscara de opacidad.


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a>Recorte de una forma arbitraria

En la ilustración siguiente se muestra el resultado de aplicar un clip a una imagen.

![una imagen que muestra un ejemplo de una imagen antes y después de un clip.](images/clip.png)

Puede obtener este resultado mediante capas con una máscara de geometría o el [**método FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de opacidad.

Este es un ejemplo que usa una capa:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Este es un ejemplo que usa el [**método FillGeometry:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



En este ejemplo de código, cuando se llama al método PushLayer, no se pasa una capa creada por la aplicación. Direct2D crea una capa automáticamente. Direct2D puede administrar la asignación y destrucción de este recurso sin intervención de la aplicación. Esto permite a Direct2D reutilizar capas internamente y aplicar optimizaciones de administración de recursos.

> [!Note]  
> En Windows 8 se han realizado muchas optimizaciones para el uso de capas y se recomienda intentar usar las API de capa en lugar de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) siempre que sea posible.

 

### <a name="axis-aligned-clips"></a>Clips alineados en el eje

Si la región que se va a recortar está alineada con el eje de la superficie de dibujo, en lugar de arbitraria. Este caso es adecuado para usar un rectángulo de recorte en lugar de una capa. La ganancia de rendimiento es más para la geometría con alias que para la geometría suavizada. Para obtener más información sobre los clips alineados con el eje, vea el [**tema PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 