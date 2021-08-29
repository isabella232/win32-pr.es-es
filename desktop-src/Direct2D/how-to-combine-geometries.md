---
title: Cómo combinar geometrías
description: Muestra cómo combinar dos geometrías mediante Direct2D.
ms.assetid: c5413e59-ae73-4797-b4ad-3a78ad700634
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1baa10b78b1829da292656f44160c444e4441b5ef89b52b38a17efd375415b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259585"
---
# <a name="how-to-combine-geometries"></a>Cómo combinar geometrías

En este tema se describe cómo combinar dos geometrías. Direct2D admite cuatro modos para combinar geometrías: Unión, Intersección, XOR y Excluir. Estos modos se especifican en el tipo [**de enumeración D2D1 \_ COMBINE \_ MODE.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)

**Para combinar dos geometrías mediante cualquiera de los cuatro modos**

1.  Declare una geometría de ruta de acceso: una variable de tipo [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) que almacenará el resultado de la combinación de geometría.
2.  Declare un receptor de geometría: una variable de tipo [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) que almacenará la geometría de ruta de acceso.
3.  Cree el objeto geometry de ruta de acceso llamando al [**método ID2D1Factory::CreatePathGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry)
4.  Abra el objeto de receptor geometry llamando al [**método ID2D1PathGeometry::Open.**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open)
5.  Use uno de los cuatro modos para combinar las dos geometrías llamando al método [**ID2D1VelopseGeometry::CombineWithGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))
6.  Cierre el objeto de receptor geometry.

El código siguiente declara las variables de tipo [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e **ID2D1GeometrySink**.


```C++
    ID2D1PathGeometry *m_pPathGeometryUnion;
    ID2D1PathGeometry *m_pPathGeometryIntersect;
    ID2D1PathGeometry *m_pPathGeometryXOR;
    ID2D1PathGeometry *m_pPathGeometryExclude;
```



El código siguiente usa cada uno de los cuatro modos para combinar los dos objetos [**ID2D1VelopseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) y realiza las siguientes acciones:

-   Crea dos puntos suspensivos, m \_ spPelpseGeometryOne y m \_ spPelpseGeometryTwo.
-   Crea un objeto geometry de ruta de acceso.
-   Abre un objeto de receptor geometry.
-   Combina los dos puntos suspensivos.
-   Cierra el objeto de receptor geometry.


```C++
HRESULT DemoApp::CreateGeometryResources()
{
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

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
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

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
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

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
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

    return hr;
}
```



Este código genera la salida que se muestra en la ilustración siguiente.

![ilustración de dos geometrías y cuatro modos para combinar las geometrías (unión, intersección, xor y exclusión)](images/combine-modes.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MODO DE COMBINACIÓN D2D1 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)
</dt> <dt>

[**ID2D1VelopseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)
</dt> <dt>

[**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)
</dt> <dt>

**ID2D1GeometrySink**
</dt> </dl>

 

 