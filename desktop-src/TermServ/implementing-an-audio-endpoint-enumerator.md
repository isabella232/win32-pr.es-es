---
title: Implementación de un enumerador de punto de conexión de audio personalizado
description: A partir de Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor de protocolo Escritorio remoto.
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105676519"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a><span data-ttu-id="ed3c1-103">Implementación de un enumerador de punto de conexión de audio personalizado</span><span class="sxs-lookup"><span data-stu-id="ed3c1-103">Implementing a Custom Audio Endpoint Enumerator</span></span>

<span data-ttu-id="ed3c1-104">A partir de Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor de protocolo Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-104">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span> <span data-ttu-id="ed3c1-105">Un proveedor de protocolo de Escritorio remoto puede utilizar un enumerador de punto de conexión de audio personalizado para recuperar una colección de puntos de conexión de audio que tienen un conjunto específico de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-105">A Remote Desktop protocol provider can use a custom audio endpoint enumerator to retrieve a collection of audio endpoints that have a specific set of capabilities.</span></span>

<span data-ttu-id="ed3c1-106">**Para implementar un enumerador de punto de conexión de audio remoto personalizado**</span><span class="sxs-lookup"><span data-stu-id="ed3c1-106">**To implement a custom remote audio endpoint enumerator**</span></span>

1.  <span data-ttu-id="ed3c1-107">La solución de enumerador de punto de conexión personalizada debe implementar cuatro tipos principales de objetos: objetos de enumerador de dispositivos, objetos de colección de dispositivos, objetos de dispositivo y objetos de almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-107">Your custom endpoint enumerator solution should implement four main types of objects: device enumerator objects, device collection objects, device objects, and property store objects.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="ed3c1-108">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="ed3c1-108">Object type</span></span></th>
    <th><span data-ttu-id="ed3c1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed3c1-109">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="ed3c1-110">Objeto de enumerador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ed3c1-110">Device enumerator object</span></span><br/></td>
    <td><span data-ttu-id="ed3c1-111">Un objeto de enumerador de dispositivo proporciona la funcionalidad de enumerador de extremo.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-111">A device enumerator object provides the endpoint enumerator functionality.</span></span> <span data-ttu-id="ed3c1-112">Expone métodos que devuelven un punto de conexión predeterminado y colecciones de extremos especificadas.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-112">It exposes methods that return a default endpoint and specified collections of endpoints.</span></span> <span data-ttu-id="ed3c1-113">Por ejemplo, en función de los criterios especificados, el enumerador puede devolver puntos de conexión de comunicación, puntos de conexión de reproducción o puntos de conexión de captura.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-113">For example, depending on the criteria specified, the enumerator can return communication endpoints, playback endpoints, or capture endpoints.</span></span> <span data-ttu-id="ed3c1-114">El objeto de enumerador de dispositivos debe implementar la interfaz <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed3c1-114">The device enumerator object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ed3c1-115">Objeto de colección de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ed3c1-115">Device collection object</span></span><br/></td>
    <td><span data-ttu-id="ed3c1-116">Un objeto de colección de dispositivos representa una colección de dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-116">A device collection object represents a collection of audio devices.</span></span> <span data-ttu-id="ed3c1-117">Debe implementar la interfaz <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed3c1-117">It must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="ed3c1-118">Objeto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ed3c1-118">Device object</span></span><br/></td>
    <td><span data-ttu-id="ed3c1-119">Un objeto de dispositivo representa un dispositivo de audio determinado.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-119">A device object represents a particular audio device.</span></span> <span data-ttu-id="ed3c1-120">Proporciona acceso al almacén de propiedades del dispositivo de audio y expone las interfaces de captura y reproducción de audio disponibles en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-120">It provides access to the audio device's property store and exposes the audio playback and capture interfaces available on the device.</span></span> <span data-ttu-id="ed3c1-121">El objeto de dispositivo debe implementar las interfaces <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> y <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed3c1-121">The device object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> and <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> interfaces.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="ed3c1-122">Objeto de almacén de propiedades</span><span class="sxs-lookup"><span data-stu-id="ed3c1-122">Property store object</span></span><br/></td>
    <td><span data-ttu-id="ed3c1-123">Un objeto de almacén de propiedades expone las propiedades asociadas a un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-123">A property store object exposes the properties associated with an audio device.</span></span> <span data-ttu-id="ed3c1-124">El sistema utiliza algunas de estas propiedades, pero las aplicaciones también pueden almacenar propiedades arbitrarias con el punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-124">Some of these properties are used by the system, but applications can store arbitrary properties with the audio endpoint as well.</span></span><br/> <span data-ttu-id="ed3c1-125">Todos los dispositivos de audio tienen las tres propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="ed3c1-125">All audio devices have the following three properties:</span></span><br/>
    <ul>
    <li><span data-ttu-id="ed3c1-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed3c1-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span></span></li>
    <li><span data-ttu-id="ed3c1-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed3c1-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span></span></li>
    <li><span data-ttu-id="ed3c1-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed3c1-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span></span></li>
    </ul>
<span data-ttu-id="ed3c1-129">El objeto de almacén de propiedades debe implementar la interfaz <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> .</span><span class="sxs-lookup"><span data-stu-id="ed3c1-129">The property store object must implement the <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="ed3c1-130">El enumerador de punto de conexión personalizado debe implementarse en un archivo DLL que se pueda cargar en el sistema de audio y en otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-130">The custom endpoint enumerator must be implemented in a DLL that can be loaded into the audio system and other applications.</span></span> <span data-ttu-id="ed3c1-131">La DLL debe estar firmada para que los procesos seguros puedan cargarla.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-131">The DLL must be signed so that secure processes can load it.</span></span> <span data-ttu-id="ed3c1-132">El archivo DLL debe implementar y exportar la función [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) , que actúa como punto de entrada para el enumerador de punto de conexión personalizado.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-132">The DLL must implement and export the [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) function, which acts as an entry point to the custom endpoint enumerator.</span></span>

<span data-ttu-id="ed3c1-133">El servicio Servicios de Escritorio remoto llama al método [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) y establece el parámetro *QueryType* en la **consulta de WTS \_ \_ AUDIOENUM \_ dll** para recuperar el nombre del objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-133">The Remote Desktop Services service calls the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) method and sets the *QueryType* parameter to **WTS\_QUERY\_AUDIOENUM\_DLL** to retrieve the name of the enumerator object.</span></span>

<span data-ttu-id="ed3c1-134">Los objetos de enumerador personalizados usan interfaces de tipo COM y un mecanismo de recuento de referencias COM, pero no son objetos COM verdaderos.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-134">Custom enumerator objects use COM-like interfaces and a COM-like reference counting mechanism, but they are not true COM objects.</span></span> <span data-ttu-id="ed3c1-135">El enumerador de punto de conexión personalizado debe tener la capacidad de trabajar con las interfaces de audio heredadas que usan las aplicaciones que no admiten COM.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-135">The custom endpoint enumerator must have the ability to work with legacy audio interfaces used by applications that do not support COM.</span></span> <span data-ttu-id="ed3c1-136">Por esta razón, el enumerador de punto de conexión personalizado no debe basarse en el mecanismo de administración del ciclo de vida de COM.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-136">For this reason, the custom endpoint enumerator must not rely on COM's life cycle management mechanism.</span></span> <span data-ttu-id="ed3c1-137">Los consumidores del enumerador de punto de conexión de audio, como MMDevAPI.dll, cargan el archivo DLL del enumerador de punto de conexión personalizado cuando lo requieren las aplicaciones de usuario y no descargan el enumerador mientras el enumerador contiene una referencia a un objeto de enumerador de dispositivo, objeto de colección de dispositivos, objeto de dispositivo o objeto de almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-137">Consumers of your audio endpoint enumerator, such as MMDevAPI.dll, load the custom endpoint enumerator DLL when required by user applications, and they will not unload the enumerator while the enumerator holds a reference to a device enumerator object, device collection object, device object, or property store object.</span></span> <span data-ttu-id="ed3c1-138">No obstante, no es posible que estos consumidores realicen un seguimiento de las referencias a otros tipos de objetos propiedad del enumerador de extremo personalizado.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-138">It is not possible, however, for these consumers to track references to other types of objects owned by the custom endpoint enumerator.</span></span> <span data-ttu-id="ed3c1-139">En consecuencia, se recomienda que el enumerador de punto de conexión personalizado no cree ningún objeto que durar más estos cuatro tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-139">Accordingly, we recommend that your custom endpoint enumerator not create any objects that could outlive these four types of objects.</span></span>

## <a name="to-implement-a-custom-audio-endpoint"></a><span data-ttu-id="ed3c1-140">Para implementar un punto de conexión de audio personalizado</span><span class="sxs-lookup"><span data-stu-id="ed3c1-140">To implement a custom audio endpoint</span></span>

<span data-ttu-id="ed3c1-141">Para implementar un enumerador de dispositivo de audio personalizado, debe implementar un punto de conexión de audio personalizado.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-141">To implement a custom audio device enumerator, you must implement a custom audio endpoint.</span></span> <span data-ttu-id="ed3c1-142">La forma en que se vinculan los dispositivos de audio personalizados es mediante el uso de las dos instrucciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ed3c1-142">The way that your custom audio devices are linked is by using the following two statements:</span></span>

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

<span data-ttu-id="ed3c1-143">No esperamos implementar la lista completa de interfaces [**IMMDevice:: Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) en el enumerador de dispositivos de audio personalizado.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-143">We do not expect you to implement the full list of [**IMMDevice::Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) interfaces in your custom audio device enumerator.</span></span> <span data-ttu-id="ed3c1-144">En su lugar, debe implementar [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) y [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="ed3c1-144">Instead, you should implement [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) and [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="ed3c1-145">Opcionalmente, puede implementar algunos más, como [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span><span class="sxs-lookup"><span data-stu-id="ed3c1-145">You can optionally implement a few more, such as [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span></span> <span data-ttu-id="ed3c1-146">Para cualquier interfaz que no implemente, debe devolver **E \_ nointerface** (debe usar este código de error específico).</span><span class="sxs-lookup"><span data-stu-id="ed3c1-146">For any interface you do not implement, you should return **E\_NOINTERFACE** (you must use this specific failure code).</span></span> <span data-ttu-id="ed3c1-147">A continuación, Windows revierte a una implementación estándar de la interfaz (por ejemplo, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span><span class="sxs-lookup"><span data-stu-id="ed3c1-147">Windows will then fall back to a stock implementation of the interface (for example, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span></span>

<span data-ttu-id="ed3c1-148">Para obtener documentación de referencia adicional sobre cómo implementar y registrar puntos de conexión de audio, vea [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span><span class="sxs-lookup"><span data-stu-id="ed3c1-148">For additional reference documentation about how to implement and register audio endpoints, see [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="ed3c1-149">Para ver un diagrama que muestra cómo funciona WASAPI, consulte [componentes de audio de modo de usuario](/windows/desktop/CoreAudio/user-mode-audio-components).</span><span class="sxs-lookup"><span data-stu-id="ed3c1-149">For a diagram that shows how WASAPI works, see [User-Mode Audio Components](/windows/desktop/CoreAudio/user-mode-audio-components).</span></span> <span data-ttu-id="ed3c1-150">Tenga en cuenta que todo el audio de modo usuario es nuevo a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ed3c1-150">Note that all of user-mode audio is new beginning with Windows Server 2008.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed3c1-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed3c1-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed3c1-152">Creación de un proveedor de Protocolo de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="ed3c1-152">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="ed3c1-153">**GetTSAudioEndpointEnumeratorForSession**</span><span class="sxs-lookup"><span data-stu-id="ed3c1-153">**GetTSAudioEndpointEnumeratorForSession**</span></span>](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[<span data-ttu-id="ed3c1-154">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="ed3c1-154">**IMMDevice**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="ed3c1-155">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="ed3c1-155">**IMMDeviceCollection**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[<span data-ttu-id="ed3c1-156">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="ed3c1-156">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[<span data-ttu-id="ed3c1-157">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="ed3c1-157">**IMMEndpoint**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[<span data-ttu-id="ed3c1-158">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="ed3c1-158">IPropertyStore</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>