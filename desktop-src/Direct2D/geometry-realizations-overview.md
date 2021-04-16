---
title: Información general sobre las realizaciones de geometría
description: En este tema se describe cómo usar la realización de geometrías de Direct2D para mejorar el rendimiento de representación de la geometría de la aplicación en ciertos escenarios.
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b903e047ee58a803a7584aaca407281fc803e30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656361"
---
# <a name="geometry-realizations-overview"></a>Información general sobre las realizaciones de geometría

En este tema se describe cómo usar la realización de geometrías de [Direct2D](direct2d-portal.md) para mejorar el rendimiento de representación de la geometría de la aplicación en ciertos escenarios.

Contiene las secciones siguientes:

-   [¿Qué ocurre con Geometry?](#what-are-geometry-realizations)
-   [¿Por qué se tiene que usar Geometry?](#why-use-geometry-realizations)
-   [Cuándo usar la realización de geometría](#when-to-use-geometry-realizations)
-   [Crear la realización de geometría](#creating-geometry-realizations)
-   [Dibujo de la geometría de dibujo](#drawing-geometry-realizations)
-   [Escalado de geometría](#scaling-geometry-realizations)
    -   [Uso de la realización de geometría en aplicaciones que no se escalan](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [Uso de geometría en aplicaciones que se escalan en una cantidad pequeña](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [Uso de geometría en aplicaciones que se escalan en gran medida](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [Temas relacionados](#related-topics)

## <a name="what-are-geometry-realizations"></a>¿Qué ocurre con Geometry?

La realización de geometrías, introducida en Windows 8.1, es un nuevo tipo de primitiva de dibujo que facilita a las aplicaciones de [Direct2D](direct2d-portal.md) mejorar el rendimiento de la representación de geometría en determinados casos. La interfaz [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) representa la realización de la geometría.

## <a name="why-use-geometry-realizations"></a>¿Por qué se tiene que usar Geometry?

Cuando [Direct2D](direct2d-portal.md) representa un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , debe convertir esa geometría en una forma que el hardware gráfico comprenda a través de un proceso denominado teselación. Normalmente, Direct2D debe dividirlas geometría cada fotograma que se dibuja, incluso si la geometría no cambia. Si la aplicación representa la misma geometría en cada fotograma, la reteselación repetida representa el esfuerzo de cálculo desperdiciado. Es más eficaz en la memoria caché la teselación, o incluso la rasterización completa, de la geometría, y para dibujar esa representación almacenada en caché en cada fotograma en lugar de volver a teselar repetidamente.

Una forma habitual de que los desarrolladores resuelvan este problema es almacenar en caché la rasterización completa de la geometría. En concreto, es habitual crear un nuevo mapa de bits, rasterizar la geometría a ese mapa de bits y, a continuación, dibujar dicho mapa de bits en la escena según sea necesario. (Este enfoque se describe en la sección de [representación de geometría](improving-direct2d-performance.md) de cómo mejorar el rendimiento de las aplicaciones de Direct2D). Aunque este enfoque es muy eficaz, tiene algunas desventajas:

-   El mapa de bits almacenado en caché es sensible a los cambios en la transformación aplicada a la escena. Por ejemplo, el escalado de la rasterización puede dar lugar a artefactos de escalado perceptible. Mitigar estos artefactos con algoritmos de escalado de alta calidad puede ser costoso.
-   El mapa de bits almacenado en caché consume una cantidad significativa de memoria, especialmente si se rasteriza con una resolución alta.

Las conversiones de geometría proporcionan una manera alternativa de almacenar en caché la geometría que evita las desventajas anteriores. Los cálculos de geometría se representan no por píxeles (como es el caso con una rasterización completa), sino en lugar de puntos en un plano matemático. Por esta razón, son menos sensibles que las rasterizaciones completas para el escalado y otras manipulaciones, y consumen mucha menos memoria.

## <a name="when-to-use-geometry-realizations"></a>Cuándo usar la realización de geometría

Considere la posibilidad de usar geometría cuando la aplicación representa geometrías complejas cuyas formas cambian con poca frecuencia, pero que pueden estar sujetas a cambios de transformaciones.

Por ejemplo, imagine una aplicación de asignación que muestra una asignación estática pero que permite al usuario acercar y alejar. Esta aplicación se puede beneficiar del uso de la realización de geometría. Puesto que las geometrías que se representan siguen siendo estáticas, resulta útil almacenarlas en caché para ahorrar trabajo de teselación. Sin embargo, dado que las asignaciones se escalan cuando el usuario amplía, el almacenamiento en caché de una rasterización completa no es ideal, debido a los artefactos de escalado. Almacenar en caché las supuestos de geometría permitiría a la aplicación evitar el trabajo de reteselación manteniendo una calidad visual elevada durante el escalado.

Por otro lado, considere la posibilidad de usar una aplicación Kaleidoscope con geometría animada que cambia continuamente. Esta aplicación probablemente no se beneficiaría del uso de la realización de geometría. Dado que las formas cambian de fotograma a fotograma, no es útil almacenar en caché sus teselaciones. El mejor enfoque para esta aplicación es dibujar objetos de [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) directamente.

## <a name="creating-geometry-realizations"></a>Crear la realización de geometría

Se debe crear un objeto [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) a partir de un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) existente. Para crear una realización de geometría, llame al método [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) o al método [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) y pase la **ID2D1Geometry** que se va a realizar.

-   [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) crea una realización del interior de la forma: la región que se dibujaría llamando a [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry).
-   [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) crea una realización del trazo de la forma: la región que se dibujaría llamando a [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry).

Ambos tipos de la realización de geometría se representan mediante la interfaz [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) .

Al crear una realización de geometría, [Direct2D](direct2d-portal.md) debe acoplar las curvas de la geometría proporcionada a las aproximaciones poligonales. Debe proporcionar un parámetro de tolerancia de acoplamiento al método de creación; esto especifica la distancia máxima, en píxeles independientes del dispositivo (DIP), entre la curva verdadera de la geometría y su aproximación poligonal. Cuanto menor sea la tolerancia de acoplamiento que proporcione, mayor será la fidelidad del objeto de realización de geometría resultante. De forma similar, si se proporciona una tolerancia de acoplamiento superior, se consigue una geometría de menor fidelidad. Tenga en cuenta que las conversiones de geometría de mayor fidelidad son más costosas de dibujar que las de menor fidelidad, pero se pueden escalar más antes de introducir artefactos visibles. Para obtener instrucciones sobre el uso de las tolerancias de acoplamiento, consulte el [escalado de geometría](#scaling-geometry-realizations) a continuación.

> [!Note]  
> Los objetos de realización de geometría están asociados a un dispositivo de gráficos determinado: son recursos dependientes del dispositivo.

 

## <a name="drawing-geometry-realizations"></a>Dibujo de la geometría de dibujo

El dibujo de las supuestos de geometría es similar al de dibujar otras primitivas de [Direct2D](direct2d-portal.md) , como los mapas de bits. Para ello, llame al método [**DrawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) y pásele el objeto de la realización de geometría que se va a dibujar y el pincel que se va a usar. Como con otros métodos de dibujo de Direct2D, debe llamar a **DrawGeometryRealization** entre las llamadas a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="scaling-geometry-realizations"></a>Escalado de geometría

La realización de geometrías, al igual que otras primitivas de [Direct2D](direct2d-portal.md) , respetan la transformación establecida en el contexto del dispositivo. Aunque las transformaciones de traslación y rotación no tienen ningún efecto en la calidad visual de realización de geometría, las transformaciones de escalado pueden generar artefactos visuales.

En concreto, si se aplica una escala suficientemente grande a cualquier geometría, se puede revelar la aproximación poligonal de las curvas verdaderas. En la imagen siguiente se muestra un par de realización de geometría elíptica (relleno y trazo) que se ha escalado verticalmente. Los artefactos de alisado de curva son visibles.

![se lleva a cabo un par de geometría elíptica (relleno y trazo) que se ha escalado verticalmente. los artefactos de alisado de curva son visibles.](images/zoomed-in.png)

Las aplicaciones que son sensibles a la calidad visual deben tomar medidas para asegurarse de que esto no suceda. La forma de controlar el escalado depende de las necesidades de la aplicación. A continuación se muestran varios enfoques recomendados para varios tipos diferentes de aplicaciones.

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>Uso de la realización de geometría en aplicaciones que no se escalan

Si la aplicación no realiza ningún ajuste de escala en el rendimiento de la geometría, es seguro crear la realización solo una vez, mediante una única tolerancia de acoplamiento. (Las transformaciones que no son de escala no afectan a la calidad visual de realización de geometría representada). Utilice la función [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) para calcular la tolerancia de aplanamiento adecuada para el PPP:


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>Uso de geometría en aplicaciones que se escalan en una cantidad pequeña

Si la aplicación puede escalar una medida de geometría solo en una cantidad pequeña (por ejemplo, hasta el 2x o el 3x), puede ser adecuado simplemente crear el objeto Geometry una vez, en una tolerancia de acoplamiento proporcionalmente inferior a la predeterminada. Esto crea una realización de mayor fidelidad que se puede escalar considerablemente antes de incurrir en artefactos de escalado. la desventaja es que dibujar la realización de la mayor fidelidad requiere más trabajo.

Por ejemplo, supongamos que sabe que la aplicación no escalará nunca una realización de geometría superior al 2x. La aplicación puede crear la realización de la geometría mediante una tolerancia de acoplamiento que sea la mitad del valor predeterminado y simplemente escale la realización según sea necesario, hasta el doble. Use la función [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) para calcular la tolerancia de aplanamiento adecuada pasando 2,0 como parámetro *maxZoomFactor* :


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);
    
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY,                           // vertical DPI
        2.0f                            // realization can be scaled by an additional 2x
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>Uso de geometría en aplicaciones que se escalan en gran medida

Si la aplicación puede escalar o reducir verticalmente una geometría de gran cantidad (por ejemplo, 10 veces o más), el control de escalado de forma adecuada es más complicado.

Para la mayoría de estas aplicaciones, el enfoque recomendado consiste en volver a crear el objeto Geometry en las tolerancias de acoplamiento progresivamente inferiores a medida que la escena se escale verticalmente, con el fin de mantener la fidelidad visual y evitar el escalado de los artefactos. Del mismo modo, a medida que la escena se reduce verticalmente, la aplicación debe volver a crear la geometría con tolerancias de acoplamiento progresivamente superior, con el fin de evitar la representación de los detalles que no son visibles. La aplicación no debe volver a crear la geometría cada vez que cambie la escala, ya que esto impide el almacenamiento en caché del trabajo de teselación. En su lugar, la aplicación debe volver a crear la geometría con menos frecuencia: por ejemplo, después de cada 2x aumento o disminución de la escala.

Cada vez que cambia el escalado de una aplicación en respuesta a la interacción del usuario, la aplicación podría comparar la nueva escala con la escala en la que se creó la geometría por última vez (almacenada, por ejemplo, en un miembro **m \_ lastScale** ). Si los dos valores son cercanos (en este caso, dentro de un factor de 2), no se realiza ninguna otra acción. Pero si los dos valores no se cierran, se vuelven a crear las geometrías. La función [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) se usa para calcular una tolerancia de acoplamiento adecuada para la nueva escala y **m \_ lastScale** se actualiza a la nueva escala.

Además, la aplicación siempre crea la realización con una tolerancia menor que la que se utilizaría normalmente para la nueva escala, pasando un valor de 2 como el parámetro *maxZoomFactor* a [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)). Esto permite que la nueva geometría se escale verticalmente mediante un factor adicional de 2 sin incurrir en artefactos de escalado.

> [!Note]  
> El enfoque descrito aquí puede no ser adecuado para todas las aplicaciones. Por ejemplo, si la aplicación permite que la escena se escale con factores muy grandes de manera muy rápida (por ejemplo, si contiene un control deslizante "zoom" que se puede pasar del 100% al 1 millón% en el intervalo de unos cuantos fotogramas), este enfoque puede provocar un exceso de trabajo mediante la recreación de la geometría de cada fotograma. Un enfoque alternativo consiste en volver a crear el objeto Geometry solo después de que se haya completado cada manipulación de la escala de la escena (por ejemplo, después de que el usuario haya completado un gesto de pinch).

 

## <a name="related-topics"></a>Temas relacionados

[Información general sobre las geometrías](direct2d-geometries-overview.md)

[Mejorar el rendimiento de las aplicaciones de Direct2D](improving-direct2d-performance.md)

[Directrices generales para la representación de contenido estático complejo](improving-direct2d-performance.md)

[**ID2D1DeviceContext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**ComputeFlatteningTolerance función)**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))