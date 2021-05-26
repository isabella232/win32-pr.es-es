---
description: Invocación de los métodos de servicio
ms.assetid: 3a2796c8-1a39-49eb-98e1-c9e06c61f397
title: Invocación de los métodos de servicio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b9540cf7378e13d56af2611d6216897c6750f6
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424205"
---
# <a name="invoking-service-methods"></a>Invocación de los métodos de servicio

La aplicación WpdServicesApiSample incluye código que muestra cómo una aplicación puede invocar los métodos admitidos por un servicio Contacts determinado de forma sincrónica. En este ejemplo se usan las interfaces siguientes



| Interfaz    | Descripción    |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)               | Se usa para recuperar la **interfaz IPortableDeviceServiceMethods** para invocar métodos en un servicio determinado.                                                                  |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods) | Se usa para invocar un método de servicio.                                                                                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                 | Se usa para contener los parámetros del método saliente y los resultados del método entrante. Puede ser **NULL si** el método no requiere parámetros ni devuelve ningún resultado. |



 

Cuando el usuario elige la opción "9" en la línea de comandos, la aplicación invoca el método **InvokeMethods** que se encuentra en el módulo ServiceMethods.cpp. Tenga en cuenta que antes de invocar los métodos, la aplicación de ejemplo abre un servicio Contactos en un dispositivo conectado.

Los métodos de servicio encapsulan la funcionalidad que cada servicio define e implementa. Son únicos para cada tipo de servicio y se representan mediante un GUID. Por ejemplo, el servicio Contacts define un método **BeginSync** al que llaman las aplicaciones para preparar el dispositivo para sincronizar objetos Contact y un método **EndSync** para notificar al dispositivo que se ha completado la sincronización. Las aplicaciones ejecutan un método mediante una [**llamada a IPortableDeviceServiceMethods::Invoke**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invoke).

Los métodos de servicio no deben confundirse con los comandos de WPD. Los comandos WPD forman parte de la interfaz de controlador de dispositivos (DDI) WPD estándar y son el mecanismo para la comunicación entre una aplicación WPD y el controlador. Los comandos están predefinidos, agrupados por categorías, por ejemplo, **WPD \_ CATEGORY \_ COMMON** y se representan mediante una **estructura PROPERTYKEY.** Una aplicación envía comandos al controlador de dispositivo mediante una llamada [**a IPortableDeviceService::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand). Para obtener más información, vea el tema Comandos.

El **método InvokeMethods** invoca el método [**IPortableDeviceService::Methods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar una [**interfaz IPortableDeviceServiceMethods.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Con esta interfaz, invoca los métodos **BeginSync** y **EndSync** llamando al método [**IPortableDeviceServiceMethods::Invoke.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) Cada vez que llama a **Invoke**, la aplicación proporciona el REFGUID para el método que se invoca.

En el código siguiente se usa **el método InvokeMethods.**


```C++
// Invoke methods on the Contacts Service.
// BeginSync and EndSync are methods defined by the FullEnumerationSync Device Service.
void InvokeMethods(IPortableDeviceService* pService)
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

    // Invoke() the BeginSync method
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_BeginSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_BeginSync, hr);
        }
    }

    // Invoke the EndSync method asynchronously
    if (SUCCEEDED(hr))
    {
        // This method does not take any parameters or results, so we pass in NULL
        hr = pMethods->Invoke(METHOD_FullEnumSyncSvc_EndSync, NULL, NULL);
        if (SUCCEEDED(hr))
        {
            printf("%ws called, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        }
        else
        {
            printf("! Failed to invoke %ws, hr = 0x%lx\n",NAME_FullEnumSyncSvc_EndSync, hr);
        } 
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



