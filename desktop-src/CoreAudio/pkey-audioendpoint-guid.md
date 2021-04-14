---
description: La \_ propiedad GUID de PKEY AudioEndpoint \_ proporciona el identificador de dispositivo de DirectSound que corresponde al dispositivo de punto de conexión de audio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648169"
---
# <a name="pkey_audioendpoint_guid"></a><span data-ttu-id="3d872-103">GUID de PKEY \_ AudioEndpoint \_</span><span class="sxs-lookup"><span data-stu-id="3d872-103">PKEY\_AudioEndpoint\_GUID</span></span>

<span data-ttu-id="3d872-104">La **propiedad \_ \_ GUID de PKEY AudioEndpoint** proporciona el identificador de dispositivo de DirectSound que corresponde al dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="3d872-104">The **PKEY\_AudioEndpoint\_GUID** property supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span> <span data-ttu-id="3d872-105">El valor de propiedad es un GUID que el cliente puede proporcionar como identificador de dispositivo a la función **DirectSoundCreate** o **DIRECTSOUNDCAPTURECREATE** en la API de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="3d872-105">The property value is a GUID that the client can supply as the device identifier to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function in the DirectSound API.</span></span> <span data-ttu-id="3d872-106">Este valor identifica de forma única el dispositivo de punto de conexión de audio en todos los dispositivos de punto de conexión de audio del sistema.</span><span class="sxs-lookup"><span data-stu-id="3d872-106">This value uniquely identifies the audio endpoint device across all audio endpoint devices in the system.</span></span> <span data-ttu-id="3d872-107">Para obtener más información acerca de DirectSound, consulte la documentación del SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="3d872-107">For more information about DirectSound, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="3d872-108">El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="3d872-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="3d872-109">El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene un GUID que identifica el dispositivo de punto de conexión de audio en DirectSound.</span><span class="sxs-lookup"><span data-stu-id="3d872-109">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the audio endpoint device in DirectSound.</span></span>

<span data-ttu-id="3d872-110">Como se explicó anteriormente, la [API de MMDevice](mmdevice-api.md) admite roles de [dispositivo](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="3d872-110">As explained previously, the [MMDevice API](mmdevice-api.md) supports [device roles](device-roles.md).</span></span> <span data-ttu-id="3d872-111">Aunque DirectSound no admite directamente roles de dispositivo, un cliente de DirectSound puede usar la \_ propiedad GUID de PKEY AudioEndpoint \_ para seleccionar un dispositivo de representación o captura de DirectSound en función de su rol de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d872-111">Although DirectSound does not directly support device roles, a DirectSound client can use the PKEY\_AudioEndpoint\_GUID property to select a DirectSound rendering or capture device based on its device role.</span></span>

<span data-ttu-id="3d872-112">Por ejemplo, una aplicación DirectSound realiza los pasos siguientes para crear un dispositivo DirectSound que se corresponda con el dispositivo de punto de conexión de representación al que el usuario ha asignado el rol eMultimedia:</span><span class="sxs-lookup"><span data-stu-id="3d872-112">For example, a DirectSound application performs the following steps to create a DirectSound device that corresponds to the rendering endpoint device that the user has assigned the eMultimedia role to:</span></span>

1.  <span data-ttu-id="3d872-113">Llame al método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo de punto de conexión de representación que tiene el rol eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="3d872-113">Call the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to get the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the rendering endpoint device that has the eMultimedia role.</span></span>
2.  <span data-ttu-id="3d872-114">Llame al método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para obtener la interfaz **IPropertyStore** del dispositivo eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="3d872-114">Call the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to obtain the **IPropertyStore** interface of the eMultimedia device.</span></span> <span data-ttu-id="3d872-115">Para obtener más información sobre **IPropertyStore**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3d872-115">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>
3.  <span data-ttu-id="3d872-116">Llame al método **IPropertyStore:: GetValue** para obtener el valor de la \_ propiedad GUID de PKEY AudioEndpoint \_ .</span><span class="sxs-lookup"><span data-stu-id="3d872-116">Call the **IPropertyStore::GetValue** method to obtain the PKEY\_AudioEndpoint\_GUID property value.</span></span>
4.  <span data-ttu-id="3d872-117">Convierta el valor de propiedad de un GUID en formato de cadena en una estructura GUID de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="3d872-117">Convert the property value from a GUID in string format to a 16-byte GUID structure.</span></span>
5.  <span data-ttu-id="3d872-118">Llame a la función **DirectSoundCreate** con el GUID para crear el dispositivo con el rol eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="3d872-118">Call the **DirectSoundCreate** function with the GUID to create the device with the eMultimedia role.</span></span>

> [!Note]  
> <span data-ttu-id="3d872-119">**PKEY \_ El \_ GUID de AudioEndpoint** es una propiedad de solo lectura independientemente del modo de acceso al almacenamiento solicitado por la aplicación en [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span><span class="sxs-lookup"><span data-stu-id="3d872-119">**PKEY\_AudioEndpoint\_GUID** is a read-only property regardless of the storage-access mode requested by the application in [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span></span> <span data-ttu-id="3d872-120">Si una aplicación intenta establecer un valor mediante **IPropertyStore:: SetValue**, se produce un error en esta llamada con el \_ código de error E ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="3d872-120">If an application attempts to set a value by using **IPropertyStore::SetValue**, this call fails with the E\_ACCESSDENIED error code.</span></span>

 

<span data-ttu-id="3d872-121">Tenga en cuenta que el GUID de 16 bytes generado en el paso 4 coincide con el GUID del dispositivo que identifica el dispositivo durante la enumeración de dispositivos DirectSound.</span><span class="sxs-lookup"><span data-stu-id="3d872-121">Note that the 16-byte GUID generated in step 4 matches the device GUID that identifies the device during DirectSound device enumeration.</span></span> <span data-ttu-id="3d872-122">La función **DirectSoundEnumerate** enumera los dispositivos de punto de conexión de representación y la función **DirectSoundCaptureEnumerate** enumera los dispositivos de punto de conexión de captura.</span><span class="sxs-lookup"><span data-stu-id="3d872-122">The **DirectSoundEnumerate** function enumerates rendering endpoint devices, and the **DirectSoundCaptureEnumerate** function enumerates capture endpoint devices.</span></span> <span data-ttu-id="3d872-123">En cualquier caso, el GUID del dispositivo es el primer parámetro que se pasa a la función de devolución de llamada de enumeración.</span><span class="sxs-lookup"><span data-stu-id="3d872-123">In either case, the device GUID is the first parameter passed to the enumeration callback function.</span></span> <span data-ttu-id="3d872-124">Para obtener más información acerca de la enumeración de DirectSound, consulte la documentación del SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="3d872-124">For more information about DirectSound enumeration, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="3d872-125">Para ver un ejemplo de código que usa \_ la \_ propiedad GUID de PKEY AudioEndpoint, consulte [roles de dispositivo para aplicaciones DirectSound](device-roles-for-directsound-applications.md).</span><span class="sxs-lookup"><span data-stu-id="3d872-125">For a code example that uses the PKEY\_AudioEndpoint\_GUID property, see [Device Roles for DirectSound Applications](device-roles-for-directsound-applications.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d872-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d872-126">Requirements</span></span>



| <span data-ttu-id="3d872-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d872-127">Requirement</span></span> | <span data-ttu-id="3d872-128">Value</span><span class="sxs-lookup"><span data-stu-id="3d872-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d872-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d872-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3d872-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3d872-130">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3d872-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d872-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3d872-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d872-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d872-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d872-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d872-134"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d872-134"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d872-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d872-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d872-136">**Propiedades de punto de conexión de audio**</span><span class="sxs-lookup"><span data-stu-id="3d872-136">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="3d872-137">Propiedades de audio principales</span><span class="sxs-lookup"><span data-stu-id="3d872-137">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




