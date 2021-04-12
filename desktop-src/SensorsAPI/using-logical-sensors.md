---
description: Uso de sensores lógicos
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: Uso de sensores lógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0493cfe8ff3a489e926792f9a101eb5d9db6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154056"
---
# <a name="using-logical-sensors"></a><span data-ttu-id="c4324-103">Uso de sensores lógicos</span><span class="sxs-lookup"><span data-stu-id="c4324-103">Using Logical Sensors</span></span>

<span data-ttu-id="c4324-104">Para crear una instancia de un nodo de dispositivo para un sensor lógico o volver a conectarse a un nodo de dispositivo de sensor lógico existente, una aplicación o servicio debe llamar a [**ILogicalSensorManager:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4324-104">To instantiate a device node for a logical sensor, or to reconnect to an existing logical sensor device node, an application or service must call [**ILogicalSensorManager::Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span> <span data-ttu-id="c4324-105">El parámetro *pPropertyStore* para este método requiere un puntero a una interfaz [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que contenga los identificadores de los controladores de sensor a los que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="c4324-105">The *pPropertyStore* parameter for this method requires a pointer to an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface that contains the IDs for the sensor drivers to connect to.</span></span> <span data-ttu-id="c4324-106">Esto significa que debe crear un almacén de propiedades y agregar estos datos al almacén antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="c4324-106">This means that you must create a property store and add this data to the store before calling this method.</span></span>

### <a name="connecting-to-the-logical-sensor"></a><span data-ttu-id="c4324-107">Conexión al sensor lógico</span><span class="sxs-lookup"><span data-stu-id="c4324-107">Connecting to the Logical Sensor</span></span>

<span data-ttu-id="c4324-108">Para conectarse a un sensor lógico, debe proporcionar, como mínimo, un identificador de hardware, tal como se define en el archivo. inf del controlador del sensor, y un **GUID** lógico que identifica el sensor.</span><span class="sxs-lookup"><span data-stu-id="c4324-108">To connect to a logical sensor, you must provide, at a minimum, a hardware ID, as defined in the sensor driver's .inf file, and a logical **GUID** that identifies the sensor.</span></span> <span data-ttu-id="c4324-109">La plataforma usa este **GUID** para identificar el sensor cuando decide desconectarse del nodo de dispositivo de sensor o desinstalarlo.</span><span class="sxs-lookup"><span data-stu-id="c4324-109">The platform uses this **GUID** to identify the sensor when you choose to disconnect from, or uninstall, the sensor device node.</span></span>

<span data-ttu-id="c4324-110">En el código de ejemplo siguiente se crea un método auxiliar que se conecta a un sensor lógico especificado.</span><span class="sxs-lookup"><span data-stu-id="c4324-110">The following example code creates a helper method that connects to a specified logical sensor.</span></span> <span data-ttu-id="c4324-111">Los parámetros de método reciben el identificador de hardware del sensor y un **GUID** único para identificar el sensor.</span><span class="sxs-lookup"><span data-stu-id="c4324-111">The method parameters receive the sensor hardware ID and a unique **GUID** to identify the sensor.</span></span>


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



### <a name="disconnecting-from-a-logical-sensor"></a><span data-ttu-id="c4324-112">Desconectar de un sensor lógico</span><span class="sxs-lookup"><span data-stu-id="c4324-112">Disconnecting from a Logical Sensor</span></span>

<span data-ttu-id="c4324-113">Para desconectarse de un sensor lógico, debe proporcionar el mismo identificador lógico que utilizó cuando llamó a [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4324-113">To disconnect from a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="c4324-114">En el código de ejemplo siguiente se crea una función auxiliar que se desconecta de un sensor lógico.</span><span class="sxs-lookup"><span data-stu-id="c4324-114">The following example code creates a helper function that disconnects from a logical sensor.</span></span>


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



### <a name="uninstalling-a-logical-sensor"></a><span data-ttu-id="c4324-115">Desinstalación de un sensor lógico</span><span class="sxs-lookup"><span data-stu-id="c4324-115">Uninstalling a Logical Sensor</span></span>

<span data-ttu-id="c4324-116">Para desinstalar un sensor lógico, debe proporcionar el mismo identificador lógico que utilizó cuando llamó a [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4324-116">To uninstall a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="c4324-117">En el código de ejemplo siguiente se crea una función auxiliar que desinstala un sensor lógico.</span><span class="sxs-lookup"><span data-stu-id="c4324-117">The following example code creates a helper function that uninstalls a logical sensor.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c4324-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4324-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4324-119">Acerca de los sensores lógicos</span><span class="sxs-lookup"><span data-stu-id="c4324-119">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> </dl>

 

 
