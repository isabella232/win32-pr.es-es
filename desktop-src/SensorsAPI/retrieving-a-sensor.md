---
description: Para recuperar un objeto de sensor, se usa la interfaz ISensorManager. Esta interfaz se puede considerar como la interfaz raíz de la API del sensor. Para usar ISensorManager, debe llamar primero al método COM CoCreateInstance.
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: Recuperación de un objeto de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cda6ea04d1a0580c38aef5a0b9c4186b908300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001036"
---
# <a name="retrieving-a-sensor-object"></a><span data-ttu-id="0baf6-105">Recuperación de un objeto de sensor</span><span class="sxs-lookup"><span data-stu-id="0baf6-105">Retrieving a Sensor Object</span></span>

<span data-ttu-id="0baf6-106">Para recuperar un objeto de sensor, se usa la interfaz [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) .</span><span class="sxs-lookup"><span data-stu-id="0baf6-106">To retrieve a sensor object, you use the [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) interface.</span></span> <span data-ttu-id="0baf6-107">Esta interfaz se puede considerar como la interfaz raíz de la API del sensor.</span><span class="sxs-lookup"><span data-stu-id="0baf6-107">You can think of this interface as the root interface for the Sensor API.</span></span> <span data-ttu-id="0baf6-108">Para usar **ISensorManager**, debe llamar primero al método com **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="0baf6-108">To use **ISensorManager**, you must first call the COM **CoCreateInstance** method.</span></span>

<span data-ttu-id="0baf6-109">En el código de ejemplo siguiente se crea una instancia del administrador del sensor.</span><span class="sxs-lookup"><span data-stu-id="0baf6-109">The following example code creates an instance of the sensor manager.</span></span>


```C++
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
```



<span data-ttu-id="0baf6-110">Después de recuperar correctamente un puntero a [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), puede recuperar los sensores por categoría, tipo o identificador.</span><span class="sxs-lookup"><span data-stu-id="0baf6-110">After successfully retrieving a pointer to [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), you can retrieve sensors by category, type, or ID.</span></span> <span data-ttu-id="0baf6-111">Si recupera sensores por tipo o categoría, recibirá un puntero a una interfaz [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) que contiene todos los sensores disponibles que pertenecen a la categoría o tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="0baf6-111">If you retrieve sensors by type or category, you receive a pointer to an [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) interface that contains all the available sensors that belong to the requested category or type.</span></span> <span data-ttu-id="0baf6-112">Si recupera un sensor por su identificador, recibirá un puntero a una interfaz [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) que representa el sensor único que solicitó.</span><span class="sxs-lookup"><span data-stu-id="0baf6-112">If you retrieve a sensor by its ID, you receive a pointer to an [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface that represents the unique sensor you requested.</span></span>

<span data-ttu-id="0baf6-113">En el ejemplo de código siguiente se recupera una colección de sensores que pertenecen a la categoría denominada SAMPLE \_ sensor \_ Category \_ Date \_ Time.</span><span class="sxs-lookup"><span data-stu-id="0baf6-113">The following example code retrieves a collection of sensors that belong to the category named SAMPLE\_SENSOR\_CATEGORY\_DATE\_TIME.</span></span> <span data-ttu-id="0baf6-114">A continuación, el código recupera el primer sensor de la colección por su índice.</span><span class="sxs-lookup"><span data-stu-id="0baf6-114">The code then retrieves the first sensor in the collection by its index.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByCategory(SAMPLE_SENSOR_CATEGORY_DATE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested category.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



<span data-ttu-id="0baf6-115">Tenga en cuenta que puede recuperar todos los sensores disponibles mediante categoría de \_ sensor \_ ALL.</span><span class="sxs-lookup"><span data-stu-id="0baf6-115">Note that you can retrieve all of the available sensors by using SENSOR\_CATEGORY\_ALL.</span></span>

<span data-ttu-id="0baf6-116">De forma similar, puede recuperar sensores de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="0baf6-116">In a similar way, you can retrieve sensors of a particular type.</span></span>

<span data-ttu-id="0baf6-117">En el código de ejemplo siguiente se recupera una colección de sensores del tipo denominado SAMPLE \_ sensor \_ Type \_ Time.</span><span class="sxs-lookup"><span data-stu-id="0baf6-117">The following example code retrieves a collection of sensors of the type named SAMPLE\_SENSOR\_TYPE\_TIME.</span></span> <span data-ttu-id="0baf6-118">A continuación, el código recupera el primer sensor de la colección por su índice.</span><span class="sxs-lookup"><span data-stu-id="0baf6-118">The code then retrieves the first sensor in the collection by its index.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested type.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



<span data-ttu-id="0baf6-119">Para recuperar un sensor por su identificador, debe conocer el identificador único para el sensor.</span><span class="sxs-lookup"><span data-stu-id="0baf6-119">To retrieve a sensor by its ID, you must know the unique ID for the sensor.</span></span> <span data-ttu-id="0baf6-120">Normalmente, los sensores generan este identificador cuando se conecta por primera vez para que pueda identificar varios sensores de la misma marca y modelo.</span><span class="sxs-lookup"><span data-stu-id="0baf6-120">Sensors usually generate this ID when first connected to enable you to identify multiple sensors of the same make and model.</span></span> <span data-ttu-id="0baf6-121">Esto significa que probablemente no conocerá el ID. de sensor de antemano.</span><span class="sxs-lookup"><span data-stu-id="0baf6-121">This means that you probably will not know the sensor ID in advance.</span></span> <span data-ttu-id="0baf6-122">Sin embargo, si ha almacenado una copia de un identificador de sensor determinado que recuperó anteriormente, por ejemplo llamando a [**ISensor:: getId**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), puede que desee volver a recuperar el mismo sensor.</span><span class="sxs-lookup"><span data-stu-id="0baf6-122">However, if you have stored a copy of a particular sensor ID that you previously retrieved, for example by calling [**ISensor::GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), you may want to retrieve the same sensor again.</span></span>

<span data-ttu-id="0baf6-123">En el ejemplo de código siguiente se muestra cómo recuperar un sensor mediante su identificador.</span><span class="sxs-lookup"><span data-stu-id="0baf6-123">The following example code shows how to retrieve a sensor by using its ID.</span></span>


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



<span data-ttu-id="0baf6-124">También puede recuperar los sensores cuando estén disponibles mediante la recepción de un evento desde el administrador del sensor.</span><span class="sxs-lookup"><span data-stu-id="0baf6-124">You can also retrieve sensors when they become available by receiving an event from the sensor manager.</span></span> <span data-ttu-id="0baf6-125">Para obtener más información, vea [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span><span class="sxs-lookup"><span data-stu-id="0baf6-125">For more information, see [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0baf6-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0baf6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0baf6-127">**ISensorManagerEvents::OnSensorEnter**</span><span class="sxs-lookup"><span data-stu-id="0baf6-127">**ISensorManagerEvents::OnSensorEnter**</span></span>](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
