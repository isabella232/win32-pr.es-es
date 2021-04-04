---
title: Cómo recuperar datos de geometría extendiendo ID2D1SimplifiedGeometrySink
description: Muestra cómo recuperar datos de geometría extendiendo la interfaz ID2D1SimplifiedGeometrySink.
ms.assetid: c6777b11-6d4e-409e-9c30-da1e060c9aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba3670eb8d0152cc1dae8fbcc164bd8a6167630
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078173"
---
# <a name="how-to-retrieve-geometry-data-by-extending-id2d1simplifiedgeometrysink"></a>Cómo recuperar datos de geometría extendiendo ID2D1SimplifiedGeometrySink

Aunque un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) es inmutable, hay casos en los que es necesario manipular los datos de geometría en un objeto de geometría de trazado. Direct2D le permite hacerlo proporcionando una interfaz extensible denominada [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). En la ilustración de concepto, en este tema se describe cómo extender esta interfaz para recuperar los datos de geometría de un objeto de geometría de trazado.

**Para extender la interfaz ID2D1SimplifiedGeometrySink**

1.  Implemente una clase que herede de [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).
2.  Cree una instancia de esa clase y pásela a [**ID2D1Geometry:: simplifique**](id2d1geometry-simplify.md).

En el ejemplo de código siguiente se muestra cómo implementar una clase denominada SpecializedSink que hereda de la interfaz [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . En la ilustración simplicidad de concepto, el método **AddLines** extendido recupera los datos de geometría y los muestra en la ventana de la consola. puede personalizar este método para satisfacer sus necesidades de datos específicas.


```C++
class SpecializedSink : public ID2D1SimplifiedGeometrySink
{
    public:
        SpecializedSink()
            : m_cRef(1)
        {
        }

        STDMETHOD_(ULONG, AddRef)(THIS)
        {
            return InterlockedIncrement(reinterpret_cast<LONG volatile *>(&m_cRef));
        }

        STDMETHOD_(ULONG, Release)(THIS)
        {
            ULONG cRef = static_cast<ULONG>(
            InterlockedDecrement(reinterpret_cast<LONG volatile *>(&m_cRef)));

            if(0 == cRef)
            {
                delete this;
            }

            return cRef;
        }

        STDMETHOD(QueryInterface)(THIS_ REFIID iid, void** ppvObject)
        {
            HRESULT hr = S_OK;

            if (__uuidof(IUnknown) == iid)
            {
                *ppvObject = static_cast<IUnknown*>(this);
                AddRef();
            }
            else if (__uuidof(ID2D1SimplifiedGeometrySink) == iid)
            {
                *ppvObject = static_cast<ID2D1SimplifiedGeometrySink*>(this);
                AddRef();
            }
            else
            {
                *ppvObject = NULL;
                hr = E_NOINTERFACE;
            }

            return hr;
        }

        STDMETHOD_(void, AddBeziers)(const D2D1_BEZIER_SEGMENT * /*beziers*/,
                                     UINT /*beziersCount*/)
        {
            // Customize this method to meet your specific data needs.
        }

        STDMETHOD_(void, AddLines)(const D2D1_POINT_2F *points, UINT pointsCount)
        {
            // Customize this method to meet your specific data needs.
            printf("\n\nRetrieving geometry data from a derived ID2D1SimplifiedGeometrySink object:\n");
            for (UINT i = 0; i < pointsCount; ++i)
            {
                printf("%.0f, %.0f\n", points[i].x, points[i].y);
            }
        }

        STDMETHOD_(void, BeginFigure)(D2D1_POINT_2F startPoint,
                                      D2D1_FIGURE_BEGIN figureBegin)
        {
        }

        STDMETHOD_(void, EndFigure)(D2D1_FIGURE_END figureEnd)
        {
        }

        STDMETHOD_(void, SetFillMode)(D2D1_FILL_MODE fillMode)
        {
        }

        STDMETHOD_(void, SetSegmentFlags)(D2D1_PATH_SEGMENT vertexFlags)
        {
        }

        STDMETHOD(Close)()
        {
            return S_OK;
        }

    private:
        UINT m_cRef;
};
```



A continuación, en el ejemplo se usa un conjunto de datos (182, 209), (211, 251), (251, 226), (392, 360) y (101, 360) para crear una geometría de trazado rellena (**m \_ pGeometry**) donde se pueden recuperar los datos.


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pGeometry);
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;

    hr = m_pGeometry->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

        pSink->BeginFigure(
            D2D1::Point2F(101,360),
            D2D1_FIGURE_BEGIN_FILLED
            );
        D2D1_POINT_2F points[5] = {
           D2D1::Point2F(182,209),
           D2D1::Point2F(211,251),
           D2D1::Point2F(251,226),
           D2D1::Point2F(392,360),
           D2D1::Point2F(101,360),
           };

        printf("Adding the following geometry data to an ID2D1GeometrySink object:\n");
        printf("182, 209\n");
        printf("211, 251\n");
        printf("251, 226\n");
        printf("392, 360\n");
        printf("101, 360\n");

        pSink->AddLines(points, ARRAYSIZE(points));
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
        pSink->Release();
```



Por último, en el ejemplo se crea un objeto SpecializedSink y, a continuación, se llama al método [**ID2D1Geometry:: simplifique**](id2d1geometry-simplify.md) , pasando el objeto SpecializedSink y el parámetro de líneas de la [**\_ \_ \_ opción \_ de simplificación de geometría D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option) , que hace que las curvas se acoplen en segmentos de línea.


```C++
        SpecializedSink *pSpecializedSink = NULL;

        if (SUCCEEDED(hr))
        {
            pSpecializedSink = new SpecializedSink();
            if (!pSpecializedSink)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        if (SUCCEEDED(hr))
        {
            hr = m_pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES, // This causes any curves to be flattened into line segments.
                    NULL, // world transform
                    pSpecializedSink
                    );


            if (SUCCEEDED(hr))
            {
                hr = pSpecializedSink->Close();
            }

            pSpecializedSink->Release();
        }
```



El programa crea salidas como se muestra en la siguiente captura de pantalla.

![captura de pantalla de una ventana de consola con salida sobre la adición y la recuperación de datos de geometría](images/specializedgeometrysink.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct2D](reference.md)
</dt> </dl>

 

 