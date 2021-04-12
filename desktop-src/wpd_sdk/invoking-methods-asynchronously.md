---
description: Invocar métodos de servicio de forma asincrónica
ms.assetid: d3072e34-65f2-4eeb-bcfa-e2db2d34e680
title: Invocar métodos de servicio de forma asincrónica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d312cc76cf8cb737136629c1e2c8135d1b7bd1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277762"
---
# <a name="invoking-service-methods-asynchronously"></a>Invocar métodos de servicio de forma asincrónica

La aplicación WpdServiceApiSample incluye código que muestra cómo una aplicación puede invocar los métodos de servicio de forma asincrónica. Este ejemplo utiliza las interfaces siguientes.



|                                                                                         |                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaz                                                                               | Descripción                                                                                                                                                             |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                                | Se utiliza para recuperar la interfaz **IPortableDeviceServiceMethods** para invocar métodos en un servicio determinado.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                  | Se utiliza para invocar un método de servicio.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                                  | Se usa para contener los parámetros del método de salida y los resultados del método de entrada. Puede ser **null** si el método no requiere ningún parámetro o devuelve ningún resultado. |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback) | Implementado por la aplicación para recibir los resultados del método cuando se ha completado un método.                                                                               |



 

Cuando el usuario elige la opción "10" en la línea de comandos, la aplicación invoca el método **InvokeMethodsAsync** que se encuentra en el módulo ServiceMethods. cpp. Tenga en cuenta que antes de invocar los métodos, la aplicación de ejemplo abre un servicio de contactos en un dispositivo conectado.

Los métodos de servicio encapsulan la funcionalidad que cada servicio define e implementa. Son únicos para cada tipo de servicio y se representan mediante un GUID. Por ejemplo, el servicio contactos define un método **BeginSync** que las aplicaciones llaman para preparar el dispositivo para la sincronización de objetos de contacto y un método **EndSync** para notificar al dispositivo que se ha completado la sincronización. Las aplicaciones ejecutan un método de servicio de dispositivo portátil mediante una llamada a [**IPortableDeviceServiceMethods:: Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

Los métodos de servicio no deben confundirse con los comandos de WPD. Los comandos de WPD forman parte de la interfaz de controlador de dispositivo (DDI) de WPD estándar y son el mecanismo para la comunicación entre una aplicación de WPD y el controlador. Los comandos están predefinidos, agrupados por categorías (por ejemplo, la **categoría de WPD \_ \_ común**) y se representan mediante una estructura **PROPERTYKEY** . Una aplicación envía comandos al controlador de dispositivo mediante una llamada a [**IPortableDeviceService:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Para obtener más información, vea el tema comandos.

El método **InvokeMethodsAsync** invoca [**IPortableDeviceService:: Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una interfaz [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Mediante esta interfaz, invoca la función auxiliar **InvokeMethodAsync** dos veces; una vez para el método **BeginSync** y otra para el método **EndSync** . En este ejemplo, **InvokeMethodAsync** espera indefinidamente a que se señalice un evento global cuando se llama a [**IPortableDeviceServiceMethodCallback:: alcomplete**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethodcallback-oncomplete) .

En el código siguiente se usa el método **InvokeMethodsAsync** .


```C++
// Invoke methods on the Contacts Service asynchornously.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethodsAsync(IPortableDeviceService* pService)
{
    HRESULT hr = S_OK;
    CComPtr<IPortableDeviceServiceMethods> pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceMethods interface from the IPortableDeviceService interface to
    // invoke methods.
    hr = pService->Methods(&pMethods);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceMethods from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Invoke the BeginSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_BeginSync);

        // This method does not take any parameters, so we pass in NULL
        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_BeginSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        printf("Invoking %ws asynchronously...\n",NAME_FullEnumSyncSvc_EndSync);

        hr = InvokeMethodAsync(pMethods, METHOD_FullEnumSyncSvc_EndSync, NULL);
        if (FAILED(hr))
        {
            printf("! Failed to invoke %ws asynchronously, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
    }
}
```



La función auxiliar **InvokeMethodAsync** realiza lo siguiente para cada método que invoca:

-   Crea un identificador de evento global que supervisa para determinar la finalización del método.
-   Crea un objeto **CMethodCallback** que se proporciona como argumento para [**IPortableDeviceServiceMethods: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync).
-   Llama al método **IPortableDeviceServiceMethods:: InvokeAsync** para invocar el método especificado.
-   Supervisa el identificador global de eventos para su finalización.
-   Realiza la limpieza.

La clase **CMethodCallback** muestra cómo una aplicación puede implementar [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback). La implementación de **Alcompletar** en esta clase señaliza un evento para notificar a la aplicación que el método de servicio se ha completado. Además del método **Alcompletar** , esta clase implementa **AddRef**, **QueryInterface** y **Release**, que se usan para mantener el recuento de referencias del objeto y las interfaces que implementa.


```C++
class CMethodCallback : public IPortableDeviceServiceMethodCallback
{
public:
   CMethodCallback () : m_cRef(1)
   {
   }

   ~CMethodCallback ()
   {
   }

public:
    // IPortableDeviceServiceMethodCallback::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE OnComplete(
        HRESULT                 hrStatus,
        IPortableDeviceValues*  /*pResults*/) // We are ignoring results as our methods will not return any results
    {
        printf("** Method completed, status HRESULT = 0x%lx **\n", hrStatus);

        if (g_hMethodCompleteEvent != NULL)
        {
            SetEvent(g_hMethodCompleteEvent);
        }          
        return S_OK;
    }

    // IUnknown::AddRef
    virtual ULONG STDMETHODCALLTYPE AddRef(void)
    {
        InterlockedIncrement((long*) &m_cRef);
        return m_cRef;
    }

    // IUnknown::QueryInterface
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(
        REFIID  riid,
        LPVOID* ppvObj)
    {
        HRESULT hr = S_OK;
        if (ppvObj == NULL)
        {
            hr = E_INVALIDARG;
            return hr;
        }

        if ((riid == IID_IUnknown) ||
            (riid == IID_IPortableDeviceServiceMethodCallback))
        {
            AddRef();
            *ppvObj = this;
        }
        else
        {
            *ppvObj = NULL;
            hr = E_NOINTERFACE;
        }
        return hr;
    }

    // IUnknown::Release
    virtual ULONG STDMETHODCALLTYPE Release(void)
    {
        ULONG ulRefCount = m_cRef - 1;

        if (InterlockedDecrement((long*) &m_cRef) == 0)
        {
            delete this;
            return 0;
        }
        return ulRefCount;
    }

private:
    DWORD   m_cRef;
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 
