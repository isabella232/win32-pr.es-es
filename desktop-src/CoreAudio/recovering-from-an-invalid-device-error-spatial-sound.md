---
description: Recuperación de un error de Invalid-Device (sonido espacial)
title: Recuperación de un error de Invalid-Device (sonido espacial)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153399"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a><span data-ttu-id="13a1d-103">Recuperación de un error de Invalid-Device (sonido espacial)</span><span class="sxs-lookup"><span data-stu-id="13a1d-103">Recovering from an Invalid-Device Error (Spatial Sound)</span></span>

<span data-ttu-id="13a1d-104">Muchos de los métodos de la API de audio espacial de Microsoft, como [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)y [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), devuelven códigos de error si el dispositivo de punto de conexión de audio que utiliza la aplicación cliente deja de ser válido o se cambia el formato de representación de audio espacial en el extremo.</span><span class="sxs-lookup"><span data-stu-id="13a1d-104">Many of the methods of the Microsoft Spatial Audio API, such as [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream), and [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), return error codes if the audio endpoint device that the client application is using becomes invalid or the spatial audio rendering format is changed on the endpoint.</span></span> <span data-ttu-id="13a1d-105">Estos códigos de error indican que el dispositivo de punto de conexión se ha desconectado, o que el hardware de audio o los recursos de hardware asociados se han reconfigurado, deshabilitado, quitado, el modo de audio espacial cambia o no está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="13a1d-105">These error codes indicates that the endpoint device has been unplugged, or that the audio hardware or associated hardware resources have been reconfigured, disabled, removed, spatial audio mode is changed or otherwise made unavailable for use.</span></span> <span data-ttu-id="13a1d-106">Con frecuencia, la aplicación puede recuperarse de este error.</span><span class="sxs-lookup"><span data-stu-id="13a1d-106">Frequently, the application can recover from this error.</span></span>

<span data-ttu-id="13a1d-107">Los códigos de error que indican un error de dispositivo no válido incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="13a1d-107">Error codes that indicate an invalid-device error include the following:</span></span>

- <span data-ttu-id="13a1d-108">SPTLAUDCLNT_E_DESTROYED</span><span class="sxs-lookup"><span data-stu-id="13a1d-108">SPTLAUDCLNT_E_DESTROYED</span></span>
- <span data-ttu-id="13a1d-109">AUDCLNT_E_DEVICE_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="13a1d-109">AUDCLNT_E_DEVICE_INVALIDATED</span></span>
- <span data-ttu-id="13a1d-110">AUDCLNT_E_RESOURCES_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="13a1d-110">AUDCLNT_E_RESOURCES_INVALIDATED</span></span>
- <span data-ttu-id="13a1d-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span><span class="sxs-lookup"><span data-stu-id="13a1d-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span></span>
- <span data-ttu-id="13a1d-112">SPTLAUDCLNT_E_INTERNAL</span><span class="sxs-lookup"><span data-stu-id="13a1d-112">SPTLAUDCLNT_E_INTERNAL</span></span>

## <a name="strategies-for-handling-invalid-device-errors"></a><span data-ttu-id="13a1d-113">Estrategias para el control de errores de dispositivo no válidos</span><span class="sxs-lookup"><span data-stu-id="13a1d-113">Strategies for handling invalid-device errors</span></span>

<span data-ttu-id="13a1d-114">La estrategia recomendada para recuperarse de un error de dispositivo no válido depende de si la aplicación selecciona automáticamente un dispositivo específico según los requisitos internos o permite al usuario seleccionar explícitamente un dispositivo en una lista de dispositivos disponibles.</span><span class="sxs-lookup"><span data-stu-id="13a1d-114">The recommended strategy for recovering from an invalid-device error depends on whether the application automatically selects a specific device based on internal requirements or it allows the user to explicitly select a device from a list of available devices.</span></span> 

### <a name="default-audio-device"></a><span data-ttu-id="13a1d-115">Dispositivo de audio predeterminado</span><span class="sxs-lookup"><span data-stu-id="13a1d-115">Default audio device</span></span>

<span data-ttu-id="13a1d-116">Si la aplicación selecciona automáticamente el dispositivo predeterminado, siga estos pasos para realizar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="13a1d-116">If the application automatically selects the default device, use the following steps to recover.</span></span>

1. <span data-ttu-id="13a1d-117">Libere la interfaz [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) y [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) y las demás interfaces de audio espacial que se usen para la representación.</span><span class="sxs-lookup"><span data-stu-id="13a1d-117">Release the [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) and [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interface and any other spatial audio interfaces that are used for rendering.</span></span> 
1. <span data-ttu-id="13a1d-118">Llame a [IMMDeviceEnumerator:: GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener el dispositivo de audio predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="13a1d-118">Call [IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the current default audio device.</span></span>
1. <span data-ttu-id="13a1d-119">Intente activar **ISpatialAudioClient** en el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="13a1d-119">Attempt to activate **ISpatialAudioClient** on the audio device.</span></span>
1. <span data-ttu-id="13a1d-120">Active **ISpatialAudioObjectRenderStream**.</span><span class="sxs-lookup"><span data-stu-id="13a1d-120">Activate **ISpatialAudioObjectRenderStream**.</span></span> 

### <a name="specifically-selected-audio-device"></a><span data-ttu-id="13a1d-121">Dispositivo de audio seleccionado específicamente</span><span class="sxs-lookup"><span data-stu-id="13a1d-121">Specifically selected audio device</span></span>

<span data-ttu-id="13a1d-122">Si la aplicación selecciona un dispositivo de audio específico, siga estos pasos para realizar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="13a1d-122">If the application selects a specific audio device, use the following steps to recover.</span></span>

1. <span data-ttu-id="13a1d-123">Libere la interfaz ISpatialAudioObjectRenderStream y cualquier otra interfaz de audio espacial que se use para la representación, pero no publique **ISpatialAudioClient**.</span><span class="sxs-lookup"><span data-stu-id="13a1d-123">Release the ISpatialAudioObjectRenderStream interface and any other spatial audio interfaces that are used for rendering, but don't release **ISpatialAudioClient**.</span></span>
1. <span data-ttu-id="13a1d-124">Use la instancia actual de **ISpatialAudioClient** para activar **ISpatialAudioObjectRenderStream**.</span><span class="sxs-lookup"><span data-stu-id="13a1d-124">Use the current **ISpatialAudioClient** instance to activate **ISpatialAudioObjectRenderStream**.</span></span>

<span data-ttu-id="13a1d-125">Tenga en cuenta que para ambas estrategias mencionadas anteriormente, se pueden aplicar los mismos pasos a las aplicaciones que usan las interfaces [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) o [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) .</span><span class="sxs-lookup"><span data-stu-id="13a1d-125">Note that for both strategies listed above, the same steps can be applied to applications that use the [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) or [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) interfaces.</span></span> <span data-ttu-id="13a1d-126">Simplemente reemplace **ISpatialAudioObjectRenderStream** en los pasos anteriores con las interfaces Metadata o HRTF.</span><span class="sxs-lookup"><span data-stu-id="13a1d-126">Simply replace **ISpatialAudioObjectRenderStream** in the above steps with the metadata or Hrtf interfaces.</span></span>


## <a name="related-topics"></a><span data-ttu-id="13a1d-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13a1d-127">Related topics</span></span>

<dl> <span data-ttu-id="13a1d-128"><dt>
[Recuperación de un error](recovering-from-an-invalid-device-error.md) 
 de Invalid-Device [Administración de flujos](stream-management.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="13a1d-128"><dt>
[Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md)
[Stream Management](stream-management.md)
</dt> </span></span></dl>

 

 



