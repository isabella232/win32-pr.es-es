---
description: Microsoft Media Foundation usa una combinación de construcciones COM, pero no es una API totalmente basada en COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation y COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb7d05bac6a3f4deef2c004c6980ef1351c3823
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721350"
---
# <a name="media-foundation-and-com"></a>Media Foundation y COM

Microsoft Media Foundation usa una combinación de construcciones COM, pero no es una API totalmente basada en COM. En este tema se describe la interacción entre COM y Media Foundation. También define algunos procedimientos recomendados para desarrollar componentes de complemento de Media Foundation. Estos procedimientos pueden ayudarle a evitar algunos errores de programación comunes pero sutiles.

-   [Prácticas recomendadas para aplicaciones](#best-practices-for-applications)
-   [Prácticas recomendadas para componentes de Media Foundation](#best-practices-for-media-foundation-components)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

## <a name="best-practices-for-applications"></a>Prácticas recomendadas para aplicaciones

En Media Foundation, las [colas de trabajo](work-queues.md)controlan el procesamiento asincrónico y las devoluciones de llamada. Las colas de trabajo siempre tienen subprocesos de Apartamento multiproceso (MTA), por lo que una aplicación tendrá una implementación más sencilla si se ejecuta también en un subproceso MTA. Por lo tanto, se recomienda llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con la marca de **COinit \_ multithreaded** .

Media Foundation no calcula los objetos de contenedor uniproceso (STA) para los subprocesos de la cola de trabajo. Tampoco garantiza que se mantengan las invariantes de STA. Por lo tanto, una aplicación STA debe tener cuidado de no pasar objetos STA o proxies a Media Foundation API. Los objetos que son solo STA no se admiten en Media Foundation.

Si tiene un proxy STA a un objeto MTA o de subprocesamiento libre, el objeto se puede serializar en un proxy MTA mediante una devolución de llamada de cola de trabajo. La función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) puede devolver un puntero sin formato o un proxy STA, dependiendo del modelo de objetos definido en el registro para ese CLSID. Si se devuelve un proxy STA, no debe pasar el puntero a una API de Media Foundation.

Por ejemplo, supongamos que desea pasar un puntero **IPropertyStore** al método [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) . Puede llamar a **PSCreateMemoryPropertyStore** para crear el puntero **IPropertyStore** . Si llama a desde un STA, debe serializar el puntero antes de pasarlo a **BeginCreateObjectFromURL**.

En el código siguiente se muestra cómo calcular las referencias de un proxy STA a una API de Media Foundation.


```C++
class CCreateSourceMarshalCallback
    : public IMFAsyncCallback
{
public:
    CCreateSourceMarshalCallback(
        LPCWSTR szURL, 
        IMFSourceResolver* pResolver, 
        IPropertyStore* pSourceProps, 
        IMFAsyncCallback* pCompletionCallback, 
        HRESULT& hr
        )
        : m_szURL(szURL), 
          m_pResolver(pResolver), 
          m_pCompletionCallback(pCompletionCallback),
          m_pGIT(NULL),
          m_cRef(1)
    {
        hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable, NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGIT));

        if(SUCCEEDED(hr))
        {
            hr = m_pGIT->RegisterInterfaceInGlobal(
                pSourceProps, IID_IPropertyStore, &m_dwInterfaceCookie);
        }
    }
    ~CCreateSourceMarshalCallback()
    {
        SafeRelease(&m_pResolver);
        SafeRelease(&m_pCompletionCallback);
        SafeRelease(&m_pGIT);
    }


    STDMETHOD_(ULONG, AddRef)()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHOD_(ULONG, Release)()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (0 == cRef)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHOD(QueryInterface)(REFIID riid, LPVOID* ppvObject)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCreateSourceMarshalCallback, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppvObject);

    }

    STDMETHOD(GetParameters)(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHOD(Invoke)(IMFAsyncResult* pResult)
    {
        IPropertyStore *pSourceProps = NULL;

        HRESULT hr = m_pGIT->GetInterfaceFromGlobal(
            m_dwInterfaceCookie, 
            IID_PPV_ARGS(&pSourceProps)
            );

        if(SUCCEEDED(hr))
        {
            hr = m_pResolver->BeginCreateObjectFromURL(
                m_szURL, MF_RESOLUTION_MEDIASOURCE, pSourceProps, NULL, 
                m_pCompletionCallback, NULL);
        }

        SafeRelease(&pSourceProps);
        return hr;
    }

private:
    LPCWSTR m_szURL;
    IMFSourceResolver *m_pResolver;
    IMFAsyncCallback *m_pCompletionCallback;
    IGlobalInterfaceTable *m_pGIT;
    DWORD m_dwInterfaceCookie;
    LONG m_cRef;
};
```



Para obtener más información acerca de la tabla de la interfaz global, vea [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Si usa Media Foundation en proceso, los objetos devueltos de Media Foundation métodos y funciones son punteros directos al objeto. En el caso de Media Foundation entre procesos, estos objetos pueden ser proxies MTA y se deben calcular las referencias en un subproceso STA si es necesario. Del mismo modo, los objetos que se obtienen dentro de una devolución de llamada (por ejemplo, una topología del evento [MESessionTopologyStatus](mesessiontopologystatus.md) ) son punteros directos cuando Media Foundation se usa en proceso, pero son proxies MTA cuando Media Foundation se usa entre procesos.

> [!Note]  
> El escenario más común para el uso de Media Foundation entre procesos es con la ruta de acceso a los [medios protegidos](protected-media-path.md) (PMP). Sin embargo, estas notas se aplican a cualquier situación cuando se usan Media Foundation API a través de RPC.

 

Todas las implementaciones de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) deben ser compatibles con MTA. No es necesario que estos objetos sean objetos COM. Pero si son, no se pueden ejecutar en el STA. La función [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) se invocará en un subproceso MTA workqueue y el objeto [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) proporcionado será un puntero de objeto directo o un proxy MTA.

## <a name="best-practices-for-media-foundation-components"></a>Prácticas recomendadas para componentes de Media Foundation

Hay dos categorías de objetos de Media Foundation que deben preocuparse de COM. Algunos componentes, como las transformaciones o los controladores de secuencias de bytes, son objetos COM completos creados por CLSID. Estos objetos deben seguir las reglas de los apartamentos COM, tanto en el proceso como en el Media Foundation entre procesos. Otros componentes Media Foundation no son objetos COM completos, pero necesitan proxies COM para la reproducción entre procesos. Los objetos de esta categoría incluyen orígenes de medios y objeto de activación. Estos objetos pueden omitir los problemas de apartamento si solo se van a utilizar para Media Foundation en proceso.

Aunque no todos los objetos Media Foundation son objetos COM, todas las interfaces de Media Foundation derivan de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Por lo tanto, todos los objetos Media Foundation deben implementar **IUnknown** de acuerdo con las especificaciones com, incluidas las reglas para el recuento de referencias y [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Todos los objetos contables de referencia también deben asegurarse de que [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) no permitirá que el módulo se descargue mientras los objetos persisten.

Los componentes de Media Foundation no pueden ser objetos STA. Muchos objetos Media Foundation no necesitan ser objetos COM. Pero si son, no se pueden ejecutar en el STA. Todos los componentes de Media Foundation deben ser seguros para subprocesos. Algunos objetos Media Foundation deben ser de subprocesamiento libre o independiente. En la tabla siguiente se especifican los requisitos para las implementaciones de interfaz personalizadas:



| Interfaz                                                          | Category            | Apartamento obligatorio       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Proxy entre procesos | Subproceso libre o neutro |
| [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | Objeto COM          | MTA                      |
| [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Proxy entre procesos | Subproceso libre o neutro |
| [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | Objeto COM          | Subproceso libre o neutro |
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Proxy entre procesos | Subproceso libre o neutro |
| [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | Objeto COM          | MTA                      |
| [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | Objeto COM          | Subproceso libre o neutro |
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | Objeto COM          | MTA                      |



 

Puede haber requisitos adicionales en función de la implementación. Por ejemplo, si un receptor de medios implementa otra interfaz que permite que la aplicación realice llamadas de función directas al receptor, el receptor tendría que ser de subprocesamiento libre o neutro, de modo que pueda controlar llamadas directas entre procesos. Cualquier objeto puede ser de subprocesamiento libre; en esta tabla se especifican los requisitos mínimos.

La manera recomendada de implementar objetos independientes o de subprocesos libres es agregando el contador de referencias de subprocesamiento libre. Para obtener más información, consulte la documentación de MSDN en [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). De acuerdo con el requisito de no pasar objetos STA o proxies a Media Foundation API, no es necesario que los objetos de subprocesamiento libre tengan que preocuparse por la serialización de punteros de entrada STA en componentes de subprocesamiento libre.

Los componentes que utilizan la cola de trabajo de función larga (**\_ \_ \_ \_ función Long de cola de devolución de llamada MFASYNC**) deben tener más cuidado. Los subprocesos de la función Long workqueue crean su propio STA. Los componentes que utilizan la función Long workqueue para las devoluciones de llamada deberían evitar la creación de objetos COM en estos subprocesos y deben tener cuidado de calcular las referencias de los servidores proxy en el STA según sea necesario.

## <a name="summary"></a>Resumen

Las aplicaciones tendrán un tiempo más sencillo si interactúan con Media Foundation desde un subproceso MTA, pero es posible que tenga cuidado al usar Media Foundation desde un subproceso STA. Media Foundation no controla los componentes STA y las aplicaciones deben tener cuidado de no pasar objetos STA a Media Foundation API. Algunos objetos tienen requisitos adicionales, especialmente objetos que se ejecutan en una situación entre procesos. Seguir estas instrucciones le ayudará a evitar errores COM, interbloqueos y retrasos inesperados en el procesamiento de medios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de Media Foundation Platform](media-foundation-platform-apis.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 
