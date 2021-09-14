---
description: Uso de sensores lógicos
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: Uso de sensores lógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0493cfe8ff3a489e926792f9a101eb5d9db6b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265140"
---
# <a name="using-logical-sensors"></a>Uso de sensores lógicos

Para crear una instancia de un nodo de dispositivo para un sensor lógico o volver a conectarse a un nodo de dispositivo de sensor lógico existente, una aplicación o servicio debe llamar a [**ILogicalSensorManager::Conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)). El *parámetro pPropertyStore* para este método requiere un puntero a una interfaz [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que contiene los id. a los que se conectarán los controladores del sensor. Esto significa que debe crear un almacén de propiedades y agregar estos datos al almacén antes de llamar a este método.

### <a name="connecting-to-the-logical-sensor"></a>Conexión al sensor lógico

Para conectarse a un sensor lógico, debe proporcionar, como mínimo, un identificador de hardware, tal como se define en el archivo .inf del controlador del sensor, y un **GUID** lógico que identifique el sensor. La plataforma usa este **GUID para** identificar el sensor cuando decide desconectarse del nodo del dispositivo del sensor o desinstalarlo.

El código de ejemplo siguiente crea un método auxiliar que se conecta a un sensor lógico especificado. Los parámetros de método reciben el identificador de hardware del sensor y un **GUID único** para identificar el sensor.


```C++
HRESULT ConnectToLogicalSensor(PCWSTR* wszHardwareID, GUID guidLogicalID)
{
    HRESULT hr = S_OK;
    
    ILogicalSensorManager* pLSM = NULL;
    IPropertyStore* pStore = NULL;
    PROPVARIANT pv = {};

    // Create the property store.
    hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pStore));

    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    // Fill in the values.
    if(SUCCEEDED(hr))
    {
        hr = InitPropVariantFromStringVector(wszHardwareID, 1, &pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_HardwareIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_CompatibleIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        // Connect to the logical sensor.
        hr = pLSM->Connect(guidLogicalID, pStore);
    }

    SafeRelease(&pStore);
    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="disconnecting-from-a-logical-sensor"></a>Desconexión de un sensor lógico

Para desconectarse de un sensor lógico, debe proporcionar el mismo identificador lógico que usó al llamar a [**Conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

El código de ejemplo siguiente crea una función auxiliar que se desconecta de un sensor lógico.


```C++
HRESULT DisconnectFromLogicalSensor(GUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM = NULL;
 
    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    if(SUCCEEDED(hr))
    {
        hr = pLSM->Disconnect(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="uninstalling-a-logical-sensor"></a>Desinstalación de un sensor lógico

Para desinstalar un sensor lógico, debe proporcionar el mismo identificador lógico que usó al llamar a [**Conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).

El código de ejemplo siguiente crea una función auxiliar que desinstala un sensor lógico.


```C++
HRESULT UninstallLogicalSensor(REFGUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM;
 
    // Create the logical sensor manager.
    hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_PPV_ARGS(&pLSM));
 
    if(SUCCEEDED(hr))
    {
        hr = pLSM->Uninstall(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los sensores lógicos](about-logical-sensors.md)
</dt> </dl>

 

 
