---
description: Propiedades de dispositivos
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Propiedades de dispositivo (API de audio Core)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659312"
---
# <a name="device-properties-core-audio-apis"></a><span data-ttu-id="bfaf6-103">Propiedades de dispositivo (API de audio Core)</span><span class="sxs-lookup"><span data-stu-id="bfaf6-103">Device Properties (Core Audio APIs)</span></span>

<span data-ttu-id="bfaf6-104">Durante el proceso de enumeración de los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md), una aplicación cliente puede consultar los objetos de punto de conexión para sus propiedades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-104">During the process of enumerating [audio endpoint devices](audio-endpoint-devices.md), a client application can interrogate the endpoint objects for their device properties.</span></span> <span data-ttu-id="bfaf6-105">Las propiedades del dispositivo se exponen en la implementación de la API de MMDevice de la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-105">The device properties are exposed in MMDevice API's implementation of the **IPropertyStore** interface.</span></span> <span data-ttu-id="bfaf6-106">Dada una referencia a la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de un objeto de punto de conexión, un cliente puede obtener una referencia al almacén de propiedades del objeto de extremo llamando al método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-106">Given a reference to the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an endpoint object, a client can obtain a reference to the endpoint object's property store by calling the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method.</span></span>

<span data-ttu-id="bfaf6-107">El objeto de almacén de propiedades expone una interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-107">The property-store object exposes an **IPropertyStore** interface.</span></span> <span data-ttu-id="bfaf6-108">Los dos métodos principales de esta interfaz son **IPropertyStore:: GetValue**, que obtiene un valor de propiedad de dispositivo y **IPropertyStore:: SetValue**, que establece un valor de propiedad de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-108">The two primary methods in this interface are **IPropertyStore::GetValue**, which gets a device property value, and **IPropertyStore::SetValue**, which sets a device property value.</span></span> <span data-ttu-id="bfaf6-109">Para obtener más información sobre **IPropertyStore**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-109">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="bfaf6-110">La implementación de la API de MMDevice del almacén de propiedades es diferente del objeto de almacén de propiedades de Shell estándar.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-110">The MMDevice API's implementation of the property store is different from the standard shell property store object.</span></span> <span data-ttu-id="bfaf6-111">Para cambiar un valor de propiedad, la aplicación cliente debe llamar al método **IPropertyStore:: SetValue** .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-111">To change a property value, the client application must call the **IPropertyStore::SetValue** method.</span></span> <span data-ttu-id="bfaf6-112">Durante esta llamada, los nuevos valores se establecen y se escriben en el registro.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-112">During this call, the new values are set and written in the registry.</span></span> <span data-ttu-id="bfaf6-113">Por lo tanto, la aplicación no necesita llamar al método **IPropertyStore:: commit** después de la llamada a **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-113">Therefore, the application does not need to call the **IPropertyStore::Commit** method after the **SetValue** call.</span></span> <span data-ttu-id="bfaf6-114">El identificador del registro solo se cierra cuando el cliente libera el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-114">The handle to the registry is closed only when the client releases the interface pointer.</span></span>

<span data-ttu-id="bfaf6-115">Normalmente, las aplicaciones cliente de terceros llaman al método **GetValue** , pero no al método **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-115">Typically, third-party client applications call the **GetValue** method but not the **SetValue** method.</span></span> <span data-ttu-id="bfaf6-116">El administrador de puntos de conexión establece las propiedades básicas del dispositivo para los puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-116">The endpoint manager sets the basic device properties for endpoints.</span></span> <span data-ttu-id="bfaf6-117">Endpoint Manager es el componente de Windows Vista responsable de detectar la presencia de dispositivos de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-117">The endpoint manager is the Windows Vista component that is responsible for detecting the presence of audio endpoint devices.</span></span>

<span data-ttu-id="bfaf6-118">Cada \_ identificador de propiedad PKEY XXX de la lista siguiente es una constante de tipo **PROPERTYKEY** que se define en el archivo de encabezado Functiondiscoverykeys \_ devpkey. h.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-118">Each PKEY\_Xxx property identifier in the following list is a constant of type **PROPERTYKEY** that is defined in header file Functiondiscoverykeys\_devpkey.h.</span></span> <span data-ttu-id="bfaf6-119">Todos los dispositivos de punto de conexión de audio tienen estas tres propiedades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-119">All audio endpoint devices have these three device properties.</span></span>



| <span data-ttu-id="bfaf6-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bfaf6-120">Property</span></span>                                                                         | <span data-ttu-id="bfaf6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfaf6-121">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfaf6-122">**PKEY \_ DeviceInterface \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="bfaf6-122">**PKEY\_DeviceInterface\_FriendlyName**</span></span>](pkey-deviceinterface-friendlyname.md) | <span data-ttu-id="bfaf6-123">El nombre descriptivo del adaptador de audio al que está conectado el dispositivo de extremo (por ejemplo, "adaptador de audio XYZ").</span><span class="sxs-lookup"><span data-stu-id="bfaf6-123">The friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span> <span data-ttu-id="bfaf6-124">El miembro **VT** de **PROPVARIANT** se establece en VT \_ LPWStr y el miembro **pwszVal** apunta a una cadena de caracteres anchos terminada en null que contiene el nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-124">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span> |
| [<span data-ttu-id="bfaf6-125">**\_DeviceDesc de dispositivo PKEY \_**</span><span class="sxs-lookup"><span data-stu-id="bfaf6-125">**PKEY\_Device\_DeviceDesc**</span></span>](pkey-device-devicedesc.md)                       | <span data-ttu-id="bfaf6-126">La descripción del dispositivo de extremo (por ejemplo, "altavoces").</span><span class="sxs-lookup"><span data-stu-id="bfaf6-126">The device description of the endpoint device (for example, "Speakers").</span></span> <span data-ttu-id="bfaf6-127">El miembro **VT** de **PROPVARIANT** se establece en VT \_ LPWStr y el miembro **pwszVal** apunta a una cadena de caracteres anchos terminada en null que contiene la descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-127">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the device description.</span></span>                                       |
| [<span data-ttu-id="bfaf6-128">**PKEY el \_ dispositivo \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="bfaf6-128">**PKEY\_Device\_FriendlyName**</span></span>](pkey-device-friendlyname.md)                   | <span data-ttu-id="bfaf6-129">El nombre descriptivo del dispositivo de extremo (por ejemplo, "altavoces (adaptador de audio XYZ)").</span><span class="sxs-lookup"><span data-stu-id="bfaf6-129">The friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span> <span data-ttu-id="bfaf6-130">El miembro **VT** de **PROPVARIANT** se establece en VT \_ LPWStr y el miembro **pwszVal** apunta a una cadena de caracteres anchos terminada en null que contiene el nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-130">**PROPVARIANT** member **vt** is set to VT\_LPWSTR and member **pwszVal** points to a null-terminated, wide-character string that contains the friendly name.</span></span>                             |



 

<span data-ttu-id="bfaf6-131">Algunos dispositivos de punto de conexión de audio pueden tener propiedades adicionales que no aparecen en la lista anterior.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-131">Some audio endpoint devices might have additional properties that do not appear in the preceding list.</span></span> <span data-ttu-id="bfaf6-132">Para obtener más información acerca de las propiedades adicionales, consulte [propiedades de punto de conexión de audio](audio-endpoint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bfaf6-132">For more information about additional properties, see [Audio Endpoint Properties](audio-endpoint-properties.md).</span></span> <span data-ttu-id="bfaf6-133">Para obtener más información acerca de **PROPERTYKEY**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-133">For more information about **PROPERTYKEY**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="bfaf6-134">En el ejemplo de código siguiente se imprimen los nombres para mostrar de todos los dispositivos de punto de conexión de representación de audio en el sistema:</span><span class="sxs-lookup"><span data-stu-id="bfaf6-134">The following code example prints the display names of all audio-rendering endpoint devices in the system:</span></span>


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



<span data-ttu-id="bfaf6-135">La macro FAILed en el ejemplo de código anterior se define en el archivo de encabezado Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-135">The FAILED macro in the preceding code example is defined in header file Winerror.h.</span></span>

<span data-ttu-id="bfaf6-136">En el ejemplo de código anterior, el cuerpo del bucle **for** de la función PrintEndpointNames llama al método [**IMMDevice:: getId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener la [cadena de identificador de punto de conexión](endpoint-id-strings.md) para el dispositivo de punto de conexión de audio representado por la instancia de la interfaz **IMMDevice** .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-136">In the preceding code example, the **for**-loop body in the PrintEndpointNames function calls the [**IMMDevice::GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method to obtain the [endpoint ID string](endpoint-id-strings.md) for the audio endpoint device that is represented by the **IMMDevice** interface instance.</span></span> <span data-ttu-id="bfaf6-137">La cadena identifica de forma única el dispositivo con respecto a todos los demás dispositivos de punto de conexión de audio del sistema.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-137">The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system.</span></span> <span data-ttu-id="bfaf6-138">Un cliente puede usar la cadena de identificador de punto de conexión para crear una instancia del dispositivo de punto de conexión de audio más adelante o en un proceso diferente llamando al método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-138">A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="bfaf6-139">Los clientes deben tratar el contenido de la cadena de ID. de punto de conexión como opaco.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-139">Clients should treat the contents of the endpoint ID string as opaque.</span></span> <span data-ttu-id="bfaf6-140">Es decir, los clientes no deben intentar analizar el contenido de la cadena para obtener información sobre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-140">That is, clients should not attempt to parse the contents of the string to obtain information about the device.</span></span> <span data-ttu-id="bfaf6-141">La razón es que el formato de la cadena no está definido y puede cambiar de una implementación de la API de MMDevice al siguiente.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-141">The reason is that the string format is undefined and might change from one implementation of the MMDevice API to the next.</span></span>

<span data-ttu-id="bfaf6-142">Los nombres descriptivos de los dispositivos y las cadenas de ID. de punto de conexión obtenidos por la función PrintEndpointNames en el ejemplo de código anterior son idénticos a los nombres descriptivos de los dispositivos y las cadenas de identificador de punto de conexión que proporciona DirectSound durante la enumeración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-142">The friendly device names and endpoint ID strings that are obtained by the PrintEndpointNames function in the preceding code example are identical to the friendly device names and endpoint ID strings that are provided by DirectSound during device enumeration.</span></span> <span data-ttu-id="bfaf6-143">Para obtener más información, consulte [eventos de audio para aplicaciones de audio heredadas](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="bfaf6-143">For more information, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

<span data-ttu-id="bfaf6-144">En el ejemplo de código anterior, la función PrintEndpointNames llama a la función **CoCreateInstance** para crear un enumerador para los dispositivos de punto de conexión de audio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-144">In the preceding code example, the PrintEndpointNames function calls the **CoCreateInstance** function to create an enumerator for the audio endpoint devices in the system.</span></span> <span data-ttu-id="bfaf6-145">A menos que el programa de llamada previamente haya llamado a la función **CoInitialize** o **CoInitializeEx** para inicializar la biblioteca com, se producirá un error en la llamada a **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="bfaf6-145">Unless the calling program previously called either the **CoInitialize** or **CoInitializeEx** function to initialize the COM library, the **CoCreateInstance** call will fail.</span></span> <span data-ttu-id="bfaf6-146">Para obtener más información sobre **CoCreateInstance**, **CoInitialize** y **CoInitializeEx**, vea la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bfaf6-146">For more information about **CoCreateInstance**, **CoInitialize**, and **CoInitializeEx**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="bfaf6-147">Para obtener más información sobre las interfaces **IMMDeviceEnumerator**, **IMMDeviceCollection** y **IMMDevice** , vea [API de MMDevice](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="bfaf6-147">For more information about the **IMMDeviceEnumerator**, **IMMDeviceCollection**, and **IMMDevice** interfaces, see [MMDevice API](mmdevice-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfaf6-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfaf6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfaf6-149">Dispositivos de punto de conexión de audio</span><span class="sxs-lookup"><span data-stu-id="bfaf6-149">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



