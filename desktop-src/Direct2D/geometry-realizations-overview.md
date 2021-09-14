---
title: Información general sobre las realizaciones de geometría
description: En este tema se describe cómo usar las realizaciones de geometría de Direct2D para mejorar el rendimiento de la representación de geometría de la aplicación en determinados escenarios.
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b903e047ee58a803a7584aaca407281fc803e30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163254"
---
# <a name="geometry-realizations-overview"></a>Información general sobre las realizaciones de geometría

En este tema se describe cómo usar las realizaciones de geometría de [Direct2D](direct2d-portal.md) para mejorar el rendimiento de la representación de geometría de la aplicación en determinados escenarios.

Contiene las secciones siguientes:

-   [¿Qué son las realizaciones de geometría?](#what-are-geometry-realizations)
-   [¿Por qué usar realizaciones de geometría?](#why-use-geometry-realizations)
-   [Cuándo usar realizaciones de geometría](#when-to-use-geometry-realizations)
-   [Creación de realizaciones de geometría](#creating-geometry-realizations)
-   [Realizaciones de geometría de dibujo](#drawing-geometry-realizations)
-   [Escalado de realizaciones de geometría](#scaling-geometry-realizations)
    -   [Uso de realizaciones de geometría en aplicaciones que no se escalan](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [Uso de realizaciones de geometría en aplicaciones que se escalan en una pequeña cantidad](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [Uso de realizaciones de geometría en aplicaciones que escalan en gran medida](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [Temas relacionados](#related-topics)

## <a name="what-are-geometry-realizations"></a>¿Qué son las realizaciones de geometría?

Las realizaciones de geometría, introducidas en Windows 8.1, son un nuevo tipo de primitiva de dibujo que facilita a las aplicaciones [de Direct2D](direct2d-portal.md) mejorar el rendimiento de la representación de geometría en determinados casos. Las realizaciones de geometría se representan mediante la [**interfaz ID2D1GeometryRealization.**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

## <a name="why-use-geometry-realizations"></a>¿Por qué usar realizaciones de geometría?

Cuando [Direct2D](direct2d-portal.md) representa un objeto [**ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) debe convertir esa geometría en una forma que el hardware gráfico entienda a través de un proceso denominado teselación. Normalmente, Direct2D debe cambiar la geometría de cada marco que se dibuja, aunque no cambie. Si la aplicación representa la misma geometría en cada fotograma, la teselación repetida representa el esfuerzo de cálculo desperdiciado. Es más eficaz desde el punto de vista computacional almacenar en caché la teselación, o incluso la rasterización completa, de la geometría, y dibujar esa representación en caché de cada fotograma en lugar de volver a tesonear repetidamente.

Una manera común de que los desarrolladores resuelvan este problema es almacenar en caché la rasterización completa de la geometría. En concreto, es habitual crear un mapa de bits, rasterizar la geometría a ese mapa de bits y, a continuación, dibujar ese mapa de bits en la escena según sea necesario. (Este enfoque se describe en la sección [Representación de geometría](improving-direct2d-performance.md) de Mejora del rendimiento de las aplicaciones de Direct2D). Aunque este enfoque es muy eficaz a nivel computacional, tiene algunas desventajas:

-   El mapa de bits almacenado en caché es sensible a los cambios en la transformación aplicada a la escena. Por ejemplo, el escalado de la rasterización puede dar lugar a artefactos de escalado perceptibles. La mitigación de estos artefactos con algoritmos de escalado de alta calidad puede ser costosa desde el punto de conexión computacional.
-   El mapa de bits almacenado en caché consume una cantidad significativa de memoria, especialmente si se rasteriza a una alta resolución.

Las realizaciones de geometría proporcionan una manera alternativa de almacenar en caché la geometría que evita los inconvenientes anteriores. Las realizaciones de geometría no se representan mediante píxeles (como es el caso con una rasterización completa), sino por puntos en un plano matemático. Por esta razón, son menos sensibles que las rasterizaciones completa para el escalado y otra manipulación, y consumen significativamente menos memoria.

## <a name="when-to-use-geometry-realizations"></a>Cuándo usar realizaciones de geometría

Considere la posibilidad de usar realizaciones de geometría cuando la aplicación represente geometrías complejas cuyas formas cambian con poca frecuencia, pero que pueden estar sujetas a transformaciones cambiantes.

Por ejemplo, considere una aplicación de asignación que muestra un mapa estático, pero que permite al usuario acercar y alejar. Esta aplicación puede beneficiarse del uso de realizaciones de geometría. Puesto que las geometrías que se representan permanecen estáticas, resulta útil almacenarlas en caché para guardar el trabajo de teselación. Pero dado que los mapas se escalan cuando el usuario se acerca, el almacenamiento en caché de una rasterización completa no es ideal, debido al escalado de artefactos. El almacenamiento en caché de las realizaciones de geometría permitiría a la aplicación evitar el trabajo de teselación al tiempo que se mantiene una alta calidad visual durante el escalado.

Por otro lado, considere una aplicación de aidoscope con geometría animada que cambia continuamente. Es probable que esta aplicación no se beneficie del uso de realizaciones de geometría. Dado que las propias formas cambian de marco a marco, no resulta útil almacenar en caché sus teselaciones. El mejor enfoque para esta aplicación es dibujar [**objetos ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) directamente.

## <a name="creating-geometry-realizations"></a>Creación de realizaciones de geometría

Se debe crear un objeto [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) a partir de un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) existente. Para crear una realización de geometría, llame al método [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) o al método [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) y pase el **ID2D1Geometry** que se va a realizar.

-   [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) crea una realización del interior de la forma: la región que se dibujaría llamando a [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry).
-   [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) crea una realización del trazo de la forma: la región que se dibujaría llamando a [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry).

Ambos tipos de realización de geometría se representan mediante la [**interfaz ID2D1GeometryRealization.**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

Al crear una realización de geometría, [Direct2D](direct2d-portal.md) debe aplanar las curvas de la geometría proporcionada a aproximaciones poligonales. Debe proporcionar un parámetro de tolerancia de aplanamiento al método de creación, que especifica la distancia máxima, en píxeles independientes del dispositivo (DIP), entre la curva verdadera de la geometría y su aproximación poligonal. Cuanto menor sea la tolerancia de aplanado que proporcione, mayor será la fidelidad del objeto de realización de geometría resultante. De forma similar, proporcionar una mayor tolerancia de aplanado produce una realización de geometría de baja fidelidad. Tenga en cuenta que las realizaciones de geometría de mayor fidelidad son más costosas de dibujar que las de menor fidelidad, pero se pueden escalar aún más antes de introducir artefactos visibles. Para obtener instrucciones sobre el uso de tolerancias de aplanado, consulte [Escalado de las realizaciones de geometría a](#scaling-geometry-realizations) continuación.

> [!Note]  
> Los objetos de realización de geometría están asociados a un dispositivo gráfico determinado: son recursos dependientes del dispositivo.

 

## <a name="drawing-geometry-realizations"></a>Realizaciones de geometría de dibujo

Dibujar realizaciones de geometría es similar al dibujo de otras primitivas [de Direct2D,](direct2d-portal.md) como mapas de bits. Para ello, llame al [**método DrawGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) y pásle el objeto de realización de geometría que se va a dibujar y el pincel que se va a usar. Al igual que con otros métodos de dibujo de Direct2D, debe llamar a **DrawGeometryRealization** entre llamadas a [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) [**y EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="scaling-geometry-realizations"></a>Escalado de realizaciones de geometría

Las realizaciones de geometría, al igual que otras primitivas [de Direct2D,](direct2d-portal.md) respetan el conjunto de transformaciones en el contexto del dispositivo. Aunque las transformaciones de traducción y rotación no tienen ningún efecto en la calidad visual de las realizaciones de geometría, las transformaciones de escala pueden generar artefactos visuales.

En concreto, aplicar una escala lo suficientemente grande a cualquier realización de geometría puede revelar la aproximación poligonal de las curvas verdaderas. La imagen aquí muestra un par de realizaciones de geometría elíptica (relleno y trazo) que se han escalado verticalmente demasiado lejos. Los artefactos de aplanado de curva son visibles.

![un par de realizaciones de geometría elíptica (relleno y trazo) que se han escalado verticalmente demasiado lejos. Los artefactos de aplanado de curva son visibles.](images/zoomed-in.png)

Las aplicaciones que son sensibles a la calidad visual deben tomar medidas para asegurarse de que esto no sucede. La forma de controlar el escalado depende de las necesidades de la aplicación. A continuación se enumeran varios enfoques recomendados para varios tipos diferentes de aplicaciones.

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>Uso de realizaciones de geometría en aplicaciones que no se escalan

Si la aplicación no realiza ningún escalado en las realizaciones de geometría, es seguro crear las realizaciones solo una vez, mediante una única tolerancia de aplanado. (Las transformaciones sin escalado no afectan a la calidad visual de las realizaciones de geometría representados). Use la [**función ComputeFlatteningTolerance para**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) calcular la tolerancia de aplanado adecuada para el ppp:


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>Uso de realizaciones de geometría en aplicaciones que se escalan en una pequeña cantidad

Si la aplicación puede escalar verticalmente una realización de geometría solo en una pequeña cantidad (por ejemplo, hasta 2 o 3 veces), puede ser adecuado simplemente crear la realización de geometría una vez, con una tolerancia de aplanado proporcionalmente inferior a la predeterminada. Esto crea una realización de mayor fidelidad que se puede escalar verticalmente significativamente antes de incurrir en artefactos de escalado. La conclusión es que dibujar la realización de mayor fidelidad requiere más trabajo.

Por ejemplo, supongamos que sabe que la aplicación nunca escalará una realización de geometría más de 2 veces. La aplicación puede crear la realización de geometría mediante una tolerancia de aplanado que es la mitad del valor predeterminado y simplemente escalar la realización según sea necesario, hasta 2 veces. Use la [**función ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) para calcular la tolerancia de aplanado adecuada pasando 2,0 como *parámetro maxZoomFactor:*


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



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>Uso de realizaciones de geometría en aplicaciones que escalan en gran medida

Si la aplicación puede escalar o reducir verticalmente una realización de geometría en grandes cantidades (por ejemplo, 10 veces o más), es más complicado controlar el escalado adecuadamente.

En la mayoría de estas aplicaciones, el enfoque recomendado es volver a crear la realización de geometría con tolerancias de aplanación progresivamente inferiores a medida que la escena se escala verticalmente, con el fin de mantener la fidelidad visual y evitar el escalado de artefactos. Del mismo modo, a medida que la escena se escala verticalmente, la aplicación debe volver a crear las realizaciones de geometría con tolerancias de aplanación progresivamente mayores, con el fin de evitar la representación desaprobada de detalles que no son visibles. La aplicación no debe volver a crear las realizaciones de geometría cada vez que cambia la escala, ya que al hacerlo se contrae el propósito de almacenar en caché el trabajo de teselación. En su lugar, la aplicación debe volver a crear las realizaciones de geometría con menos frecuencia: por ejemplo, después de cada dos veces mayor o menor escala.

Cada vez que la escala cambia en una aplicación en respuesta a la interacción del usuario, la aplicación podría comparar la nueva escala con la escala en la que se crearon por última vez las realizaciones de geometría (almacenadas, por ejemplo, en un **miembro m \_ lastScale).** Si los dos valores están cerca (en este caso, dentro de un factor de 2), no se toma ninguna otra acción. Pero si los dos valores no están cerca, se vuelve a crear la realización de geometría. La [**función ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) se usa para calcular una tolerancia de aplanado adecuada para la nueva escala y **m \_ lastScale** se actualiza a la nueva escala.

Además, la aplicación siempre crea realizaciones con una tolerancia menor que la que se usaría normalmente para la nueva escala, pasando un valor de 2 como parámetro *maxZoomFactor* a [**ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)). Esto permite escalar verticalmente las nuevas realizaciones de geometría mediante un factor adicional de 2 sin incurrir en artefactos de escalado.

> [!Note]  
> El enfoque descrito aquí puede no ser adecuado para todas las aplicaciones. Por ejemplo, si la aplicación permite que la escena se escale por factores muy grandes muy rápidamente (por ejemplo, si contiene un control deslizante de "zoom" que se puede mover del 100 % al 1000 000 % en el intervalo de unos pocos fotogramas), este enfoque puede dar lugar a un trabajo excesivo al volver a crear las realizaciones de geometría en cada fotograma. Un enfoque alternativo es volver a crear las realizaciones de geometría solo después de que se haya completado cada manipulación de la escala de la escena (por ejemplo, después de que el usuario haya completado un gesto de reducir).

 

## <a name="related-topics"></a>Temas relacionados

[Información general sobre las geometrías](direct2d-geometries-overview.md)

[Mejora del rendimiento de las aplicaciones de Direct2D](improving-direct2d-performance.md)

[Directrices generales para representar contenido estático complejo](improving-direct2d-performance.md)

[**ID2D1DeviceContext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**Función ComputeFlatteningTolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))