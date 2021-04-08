---
title: 'Información general sobre las geometrías '
description: Describe los aspectos básicos de las geometrías de Direct2D, los objetos que se pueden usar para representar, manipular y analizar formas.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Información general sobre las geometrías de Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797079"
---
# <a name="geometries-overview"></a>Información general sobre las geometrías 

En esta información general se describe cómo crear y usar objetos [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) para definir y manipular figuras 2D. Contiene las siguientes secciones:

## <a name="what-is-a-direct2d-geometry"></a>¿Qué es una geometría de Direct2D?

Una geometría de Direct2D es un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) . Este objeto puede ser una geometría simple ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)o [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), una geometría de trazado ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) o una geometría compuesta ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) y [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)).

Las geometrías de Direct2D permiten describir figuras bidimensionales y ofrecer muchos usos, como definir regiones de prueba de posicionamiento, regiones de recorte e incluso rutas de animación.

Las geometrías de Direct2D son recursos inmutables y independientes del dispositivo creados por [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory). Por lo general, debe crear geometrías una vez y mantenerlas mientras dure la aplicación, o hasta que tengan que cambiarse. Para obtener más información sobre los recursos independientes del dispositivo y dependientes del dispositivo, consulte la [información general](resources-and-resource-domains.md)sobre los recursos.

En las secciones siguientes se describen los diferentes tipos de geometrías.

## <a name="simple-geometries"></a>Geometrías simples

Las geometrías simples incluyen objetos [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)y [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , y se pueden usar para crear figuras geométricas básicas, como rectángulos, rectángulos redondeados, círculos y elipses.

Para crear una geometría simple, use uno de los métodos [**ID2D1Factory:: create<*GeometryType*>Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) . Estos métodos crean un objeto del tipo especificado. Por ejemplo, para crear un rectángulo, llame a [**ID2D1Factory:: CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), que devuelve un objeto [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) ; para crear un rectángulo redondeado, llame a [**ID2D1Factory:: CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry)), que devuelve un objeto [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) , etc.

En el ejemplo de código siguiente se llama al método [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) , pasando una estructura de elipse con el *Centro* establecido en (100, 100), *x-RADIUS* a 100 e y *-RADIUS* a 50. A continuación, llama a [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry), pasando la geometría de la elipse devuelta, un puntero a un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)negro y un ancho del trazo de 5. En la ilustración siguiente se muestra el resultado del ejemplo de código.

![Ilustración de una elipse](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



Para dibujar el contorno de cualquier geometría, use el método [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) . Para pintar su interior, use el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) .

## <a name="path-geometries"></a>Geometrías de ruta de acceso

La interfaz [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) representa las geometrías de ruta de acceso. Estos objetos se pueden usar para describir figuras geométricas complejas que se componen de segmentos como arcos, curvas y líneas. En la ilustración siguiente se muestra un dibujo creado con la geometría de la ruta de acceso.

![Ilustración de un río, montañas y el sol](images/path-geo-mnts.png)

Para obtener más información y ejemplos, vea [información general sobre las geometrías de ruta de acceso](path-geometries-overview.md).

## <a name="composite-geometries"></a>Geometrías compuestas

Una geometría compuesta es una geometría agrupada o combinada con otro objeto Geometry o con una transformación. Las geometrías compuestas incluyen objetos [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) y [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) .

### <a name="geometry-groups"></a>Grupos de geometría

Los grupos de geometría son una manera cómoda de agrupar varias geometrías al mismo tiempo, por lo que todas las figuras de varias geometrías distintas se concatenan en una. Para crear un [**objeto ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , llame al método [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) en el objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , pasando el *fillMode* con los valores posibles del [**modo de relleno D2D1 \_ \_ \_ alternativo**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternativo) y del **\_ \_ modo de relleno \_ D2D1**, una matriz de objetos Geometry para agregar al grupo Geometry y el número de elementos de esta matriz.

En el ejemplo de código siguiente se declara primero una matriz de objetos Geometry. Estos objetos son cuatro círculos concéntricos que tienen los radios siguientes: 25, 50, 75 y 100. Después, llame a [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) en el objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , pasando el [**modo de relleno D2D1 \_ \_ \_ alternativo**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), una matriz de objetos Geometry que se van a agregar al grupo Geometry y el número de elementos de esta matriz.


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

En la ilustración siguiente se muestran los resultados de la representación de las dos geometrías de grupo del ejemplo.

![Ilustración de dos conjuntos de cuatro círculos concéntricos, uno con anillos alternados y otro con todos los anillos rellenos](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>Geometrías transformadas

Hay varias maneras de transformar una geometría. Puede usar el método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) de un destino de representación para transformar todo lo que dibuja el destino de representación, o puede asociar una transformación directamente a una geometría mediante el método [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) para crear un [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)).

El método que debe usar depende del efecto que desee. Cuando se usa el destino de representación para transformar y después representar una geometría, la transformación afecta a todo lo relacionado con la geometría, incluido el ancho de cualquier trazo que se haya aplicado. Por otro lado, cuando se usa un [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry), la transformación solo afecta a las coordenadas que describen la forma. La transformación no afectará al grosor del trazo cuando se dibuje la geometría.

> [!Note]  
> A partir de Windows 8, la transformación del mundo no afectará al grosor del trazo de los trazos con el [**\_ tipo de transformación trazo D2D1 \_ \_ \_ fijo**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)o el [**tipo de \_ transformación trazo D2D1 \_ \_ \_ fino**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type). Debe usar estos tipos de transformación para obtener trazos independientes de transformación.

 

En el ejemplo siguiente se crea una [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)y, a continuación, se dibuja sin transformarla. Genera la salida que se muestra en la ilustración siguiente.

![Ilustración de un rectángulo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



En el ejemplo siguiente se usa el destino de representación para escalar la geometría en un factor de 3 y, a continuación, se dibuja. En la ilustración siguiente se muestra el resultado de dibujar el rectángulo sin la transformación y con la transformación. Observe que el trazo es más grueso después de la transformación, aunque el grosor del trazo sea 1.

![Ilustración de un rectángulo más pequeño dentro de un rectángulo más grande con un trazo más grueso](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



En el ejemplo siguiente se usa el método [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) para escalar la geometría en un factor de 3 y, a continuación, se dibuja. Genera la salida que se muestra en la ilustración siguiente. Observe que, aunque el rectángulo es mayor, su trazo no ha aumentado.

![Ilustración de un rectángulo más pequeño dentro de un rectángulo más grande con el mismo grosor de trazo](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a>Geometrías como máscaras

Puede usar un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) como máscara geométrica al llamar al método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) . La máscara geométrica especifica el área de la capa que se compone en el destino de representación. Para obtener más información, consulte la sección máscaras geométricas de la [información general sobre capas](direct2d-layers-overview.md).

## <a name="geometric-operations"></a>Operaciones geométricas

La interfaz [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) proporciona varias operaciones geométricas que puede usar para manipular y medir figuras geométricas. Por ejemplo, puede usarlos para calcular y devolver sus límites, comparar para ver cómo una geometría está relacionada espacialmente con otra (útil para la prueba de posicionamiento), calcular las áreas y longitudes, etc. En la tabla siguiente se describen las operaciones geométricas comunes.



| Operación                                                   | Método                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Combinar                                                     | [**CombineWithGeometry**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| Límites/límites ampliados/recuperar límites, actualización de región sucia | [**Wide**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)                             |
| Pruebas de posicionamiento                                                 | [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md), [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                             |
| Carrera                                                      | [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| De comparación                                                  | [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| Simplificación (quita arcos y curvas Bézier cuadráticas)   | [**Simplificar**](id2d1geometry-simplify.md)                                                                                                                                 |
| Teselación                                                | [**Dividirlas**](id2d1geometry-tessellate.md)                                                                                                                             |
| Esquema (quitar intersección)                               | [**Esquema**](id2d1geometry-outline.md)                                                                                                                                   |
| Calcular el área o la longitud de una geometría                  | [**ComputeArea**](id2d1geometry-computearea.md), [**ComputeLength**](id2d1geometry-computelength.md), [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> A partir de Windows 8, puede usar el método [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) en [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) para calcular el área o la longitud de una geometría.

 

### <a name="combining-geometries"></a>Combinar geometrías

Para combinar una geometría con otra, llame al método [**ID2D1Geometry:: CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) . Al combinar las geometrías, se especifica una de las cuatro maneras de realizar la operación de combinación: [**D2D1 \_ combine \_ Mode \_ Union**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Unión), [**D2D1 \_ combine \_ Mode \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**D2D1 \_ combine \_ Mode \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) y [**D2D1 \_ combine \_ Mode \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Exclude). En el ejemplo de código siguiente se muestran dos círculos que se combinan mediante el modo de combinación Union, donde el primer círculo tiene el punto central de (75, 75) y el radio de 50, y el segundo círculo tiene el punto central de (125, 75) y el radio de 50.


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



En la ilustración siguiente se muestran dos círculos combinados con un modo de combinación de Union.

![Ilustración de dos círculos superpuestos combinados en una Unión](images/combine-mode-union.png)

Para ver las ilustraciones de todos los modos de combinación, consulte la [**\_ \_ enumeración del modo de combinación de D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).

### <a name="widen"></a>Ancha

El método [**Wide**](id2d1geometry-widen.md) genera una nueva geometría cuyo relleno es equivalente a contornear la geometría existente y, a continuación, escribe el resultado en el objeto [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) especificado. En el ejemplo de código siguiente se llama a [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) en el objeto [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Si **Open** se realiza correctamente, llama a **Widening** en el objeto Geometry.


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a>Dividirlas

El método [**dividirlas**](id2d1geometry-tessellate.md) crea un conjunto de triángulos de rebobinado en el sentido de las agujas del reloj que cubren la geometría después de que se transforme utilizando la matriz especificada y plana con la tolerancia especificada. En el ejemplo de código siguiente se usa **dividirlas** para crear una lista de triángulos que representan *pPathGeometry*. Los triángulos se almacenan en un [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pmesh* y, a continuación, se transfieren a un miembro de clase, *m \_ pStrokeMesh*, para su uso posterior al representarse.


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a>FillContainsPoint y StrokeContainsPoint

El método [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md) indica si el área rellenada por la geometría contiene el punto especificado. Puede utilizar este método para realizar la prueba de posicionamiento. En el ejemplo de código siguiente se llama a **FillContainsPoint** en un objeto [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) , pasando un punto en (0,0) y una matriz de [**identidad**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) .


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



El método [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md) determina si el trazo de la geometría contiene el punto especificado. Puede utilizar este método para realizar la prueba de posicionamiento. En el ejemplo de código siguiente se usa **StrokeContainsPoint**.


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a>Simplificación de 

El método [**simplificar**](id2d1geometry-simplify.md) quita los arcos y las curvas Bézier cuadráticas de una geometría especificada. Por lo tanto, la geometría resultante contiene solo líneas y, opcionalmente, curvas Bézier cúbicas. En el ejemplo de código siguiente se usa la **simplificación** para transformar una geometría con curvas Bézier en una geometría que solo contiene segmentos de línea.


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a>ComputeLength y ComputeArea

El método [**ComputeLength**](id2d1geometry-computelength.md) calcula la longitud de la geometría especificada si cada segmento se desscribió en una línea. Esto incluye el segmento de cierre implícito si la geometría está cerrada. En el ejemplo de código siguiente se usa **ComputeLength** para calcular la longitud de un círculo especificado (**m \_ pCircleGeometry1**).


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



El método [**ComputeArea**](id2d1geometry-computearea.md) calcula el área de la geometría especificada. En el ejemplo de código siguiente se usa **ComputeArea** para calcular el área de un círculo especificado (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>CompareWithGeometry

El método [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md) describe la intersección entre la geometría que llama a este método y la geometría especificada. Entre los valores posibles para la intersección se incluye la [**\_ relación de geometría \_ \_ D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (disunion), la **relación de \_ geometría D2D1 \_ \_ está \_ contenida** (está contenida), la **relación de geometría de D2D1 \_ \_ \_ contiene** (Contains) y la coincidencia de la **relación de geometría de D2D1 \_ \_ \_** (superposición). "disunion" significa que dos rellenos de geometría no forman una intersección. "está contenido" significa que la geometría está totalmente contenida en la geometría especificada. "Contains" significa que la geometría contiene por completo la geometría especificada y "superposición" significa que las dos geometrías se superponen, pero ninguna contiene por completo.

En el ejemplo de código siguiente se muestra cómo comparar dos círculos que tienen el mismo radio de 50 pero que están desplazados por 50.


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a>Esquema

El método de [**contorno**](id2d1geometry-outline.md) calcula el contorno de la geometría (una versión de la geometría en la que ninguna figura cruza o cualquier otra figura) y escribe el resultado en un [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). En el ejemplo de código siguiente se usa **Outline** para construir una geometría equivalente sin ninguna de las intersecciones. Usa la tolerancia de acoplamiento predeterminada.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a>GetBounds y GetWidenedBounds

El método [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) recupera los límites de la geometría. En el ejemplo de código siguiente se usa **GetBounds** para recuperar los límites de un círculo especificado (**m \_ pCircleGeometry1**).


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



El método [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md) recupera los límites de la geometría después de que se amplíe según el ancho del trazo y el estilo especificados y transformados por la matriz especificada. En el ejemplo de código siguiente se usa **GetWidenedBounds** para recuperar los límites de un círculo especificado (**m \_ pCircleGeometry1**) después de que se amplíe según el ancho del trazo especificado.


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a>ComputePointAtLength

El método [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) calcula el vector de punto y tangente a la distancia especificada a lo largo de la geometría. En el ejemplo de código siguiente se usa **ComputePointAtLength**.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre las geometrías de ruta](path-geometries-overview.md)
</dt> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 