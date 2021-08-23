---
description: Microsoft Media Foundation usa una combinación de construcciones COM, pero no es una API totalmente basada en COM.
ms.assetid: d58ca46f-8f3a-4a12-b948-1ea7ab568788
title: Media Foundation y COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb43fa29063da453a17275fca0b5c441e89f75aab8016a1abcf1702f5433fd71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974223"
---
# <a name="media-foundation-and-com"></a>Media Foundation y COM

Microsoft Media Foundation usa una combinación de construcciones COM, pero no es una API totalmente basada en COM. En este tema se describe la interacción entre COM y Media Foundation. También define algunos procedimientos recomendados para desarrollar Media Foundation componentes de complemento. Seguir estos procedimientos puede ayudarle a evitar algunos errores de programación comunes pero sutiles.

-   [Procedimientos recomendados para aplicaciones](#best-practices-for-applications)
-   [Procedimientos recomendados para Media Foundation componentes](#best-practices-for-media-foundation-components)
-   [Resumen](#summary)
-   [Temas relacionados](#related-topics)

## <a name="best-practices-for-applications"></a>Procedimientos recomendados para aplicaciones

En Media Foundation, las colas de trabajo controlan el procesamiento asincrónico y las devoluciones [de llamada.](work-queues.md) Las colas de trabajo siempre tienen subprocesos de apartamento multiproceso (MTA), por lo que una aplicación tendrá una implementación más sencilla si también se ejecuta en un subproceso MTA. Por lo tanto, se recomienda llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con la **marca COINIT \_ MULTITHREADED.**

Media Foundation serializa objetos de apartamento de un solo subproceso (STA) para los subprocesos de cola de trabajo. Tampoco garantiza que se mantengan los invariables de STA. Por lo tanto, una aplicación STA debe tener cuidado de no pasar objetos STA ni servidores proxy a Media Foundation API. Los objetos que son solo STA no se admiten en Media Foundation.

Si tiene un proxy STA a un objeto MTA o de subproceso libre, el objeto se puede serializar a un proxy MTA mediante una devolución de llamada de cola de trabajo. La [**función CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) puede devolver un puntero sin formato o un proxy STA, en función del modelo de objetos definido en el Registro para ese CLSID. Si se devuelve un proxy STA, no debe pasar el puntero a una MEDIA FOUNDATION API.

Por ejemplo, supongamos que desea pasar un puntero **IPropertyStore** al método [**IMFSourceResolver::BeginCreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) Puede llamar a **PSCreateMemoryPropertyStore para** crear el **puntero IPropertyStore.** Si está llamando a desde un STA, debe serializar el puntero antes de pasarlo a **BeginCreateObjectFromURL**.

En el código siguiente se muestra cómo serializar un proxy STA a Media Foundation API.


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



Para obtener más información sobre la tabla de interfaz global, vea [**IGlobalInterfaceTable**](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).

Si usa un Media Foundation en proceso, los objetos devueltos desde Media Foundation métodos y funciones son punteros directos al objeto. En el caso de Media Foundation proceso, estos objetos pueden ser servidores proxy MTA y se deben serializar en un subproceso STA si es necesario allí. De forma similar, los objetos obtenidos dentro de una devolución de llamada (por ejemplo, una topología del evento [MESessionTopologyStatus)](mesessiontopologystatus.md) son punteros directos cuando Media Foundation se usa en proceso, pero son servidores proxy MTA cuando Media Foundation se usa entre procesos.

> [!Note]  
> El escenario más común para usar Media Foundation entre procesos es con la [ruta de acceso](protected-media-path.md) multimedia protegida (PMP). Sin embargo, estos comentarios se aplican a cualquier situación en la que Media Foundation API se usan a través de RPC.

 

Todas las implementaciones de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) deben ser compatibles con MTA. No es necesario que estos objetos sean objetos COM. Pero si lo están, no se pueden ejecutar en el STA. La [**función IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) se invocará en un subproceso de la cola de trabajo MTA y el objeto [**DEASYNCResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) proporcionado será un puntero de objeto directo o un proxy MTA.

## <a name="best-practices-for-media-foundation-components"></a>Procedimientos recomendados para Media Foundation componentes

Hay dos categorías de objetos Media Foundation que deben preocuparse por COM. Algunos componentes, como transformaciones o controladores de flujo de bytes, son objetos COM completos creados por CLSID. Estos objetos deben seguir las reglas para los alojamientos COM, tanto en proceso como entre procesos Media Foundation. Otros Media Foundation componentes no son objetos COM completos, pero necesitan servidores proxy COM para la reproducción entre procesos. Los objetos de esta categoría incluyen orígenes multimedia y objeto de activación. Estos objetos pueden pasar por alto los problemas de apartamento si solo se usarán para los objetos en Media Foundation.

Aunque no todos los Media Foundation son objetos COM, todas las interfaces Media Foundation derivan de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Por lo tanto, todos los Media Foundation deben implementar **IUnknown** según las especificaciones COM, incluidas las reglas para el recuento de referencias [**y QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Todos los objetos con recuento de referencias también deben asegurarse de [**que DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) no permitirá que el módulo se descargue mientras los objetos persisten.

Media Foundation componentes no pueden ser objetos STA. Muchos Media Foundation no necesitan ser objetos COM. Pero si lo están, no se pueden ejecutar en el STA. Todos Media Foundation componentes deben ser seguros para subprocesos. Algunos Media Foundation objetos deben ser de subproceso libre o neutros en el apartamento también. En la tabla siguiente se especifican los requisitos para las implementaciones de interfaz personalizada:



| Interfaz                                                          | Category            | Apartamento necesario       |
|--------------------------------------------------------------------|---------------------|--------------------------|
| [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)                                 | Proxy entre procesos | Libre de subprocesos o neutro |
| [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)               | Objeto COM          | MTA                      |
| [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) | Proxy entre procesos | Libre de subprocesos o neutro |
| [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)                     | Objeto COM          | Libre de subprocesos o neutro |
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                           | Proxy entre procesos | Libre de subprocesos o neutro |
| [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)                       | Objeto COM          | MTA                      |
| [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)                             | Objeto COM          | Libre de subprocesos o neutro |
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                               | Objeto COM          | MTA                      |



 

Puede haber requisitos adicionales en función de la implementación. Por ejemplo, si un receptor multimedia implementa otra interfaz que permite a la aplicación realizar llamadas de función directas al receptor, el receptor tendría que ser de subproceso libre o neutro, para que pudiera controlar las llamadas directas entre procesos. Cualquier objeto puede ser de subproceso libre; esta tabla especifica los requisitos mínimos.

La manera recomendada de implementar objetos sin subprocesos o neutros es agregando el serializador de subproceso libre. Para obtener más información, vea la documentación de MSDN [**sobre CoCreateFreeThreadedMarsthread**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler). De acuerdo con el requisito de no pasar objetos STA o servidores proxy a las API de Media Foundation, los objetos de subproceso libre no tienen que preocuparse de serializar punteros de entrada STA en componentes de subproceso libre.

Los componentes que usan la cola de trabajo de función larga **(MFASYNC \_ CALLBACK \_ QUEUE LONG \_ \_ FUNCTION)** deben tener más cuidado. Los subprocesos de la cola de trabajo de función larga crean su propio STA. Los componentes que usan la cola de trabajo de función larga para las devoluciones de llamada deben evitar la creación de objetos COM en estos subprocesos y deben tener cuidado para serializar los servidores proxy al STA según sea necesario.

## <a name="summary"></a>Resumen

Las aplicaciones tendrán un tiempo más fácil si interactúan con Media Foundation desde un subproceso MTA, pero es posible con cierto cuidado usar Media Foundation desde un subproceso STA. Media Foundation no controla los componentes sta, y las aplicaciones deben tener cuidado de no pasar objetos STA a Media Foundation API. Algunos objetos tienen requisitos adicionales, especialmente los objetos que se ejecutan en una situación entre procesos. Seguir estas directrices le ayudará a evitar errores COM, interbloqueos y retrasos inesperados en el procesamiento de medios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation PLATFORM API](media-foundation-platform-apis.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 
