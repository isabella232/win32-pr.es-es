---
description: Windows Vista presentó el audio en modo de usuario protegido (PUMA), el motor de audio de modo de usuario en el entorno protegido (PE), que proporciona un entorno más seguro para el procesamiento y la representación de audio.
ms.assetid: 27a50026-9e48-48b1-9249-7528a97333c9
title: Audio de modo de usuario protegido (PUMA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233dc82109feb66472e66e4235031696937d70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907449"
---
# <a name="protected-user-mode-audio-puma"></a><span data-ttu-id="55189-103">Audio de modo de usuario protegido (PUMA)</span><span class="sxs-lookup"><span data-stu-id="55189-103">Protected User Mode Audio (PUMA)</span></span>

<span data-ttu-id="55189-104">Windows Vista presentó el audio en modo de usuario protegido (PUMA), el motor de audio de modo de usuario en el entorno protegido (PE), que proporciona un entorno más seguro para el procesamiento y la representación de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-104">Windows Vista introduced Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE) that provides a safer environment for audio processing and rendering.</span></span> <span data-ttu-id="55189-105">Solo permite habilitar las salidas de audio aceptables y garantiza que las salidas estén deshabilitadas de forma confiable.</span><span class="sxs-lookup"><span data-stu-id="55189-105">It allows only the acceptable audio outputs to be enabled and ensures that the outputs are disabled reliably.</span></span> <span data-ttu-id="55189-106">Para obtener más información sobre el PUMA, consulte [Content Protection de salida y Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span><span class="sxs-lookup"><span data-stu-id="55189-106">For more information about PUMA, see [Output Content Protection and Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).</span></span>

<span data-ttu-id="55189-107">PUMA se ha actualizado para Windows 7 con el fin de proporcionar las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="55189-107">PUMA has been updated for Windows 7 to provide the following features:</span></span>

-   <span data-ttu-id="55189-108">Establecer bits del sistema de administración de copia en serie (SCMS) en puntos de conexión S/PDIF y bits de Content Protection digital (HDCP) de ancho de banda alto en los puntos de conexión de la interfaz multimedia High-Definition (HDMI).</span><span class="sxs-lookup"><span data-stu-id="55189-108">Setting Serial Copying Management System (SCMS) bits on S/PDIF endpoints and High-bandwidth Digital Content Protection (HDCP) bits on High-Definition Multimedia Interface (HDMI) endpoints.</span></span>
-   <span data-ttu-id="55189-109">Habilitación de los controles de protección SCMS y HDMI fuera de un entorno protegido (PE).</span><span class="sxs-lookup"><span data-stu-id="55189-109">Enabling SCMS and HDMI protection controls outside of a Protected Environment (PE).</span></span>

## <a name="drm-protection-in-audio-drivers"></a><span data-ttu-id="55189-110">Protección DRM en controladores de audio</span><span class="sxs-lookup"><span data-stu-id="55189-110">DRM Protection in Audio Drivers</span></span>

<span data-ttu-id="55189-111">Digital Rights Management (DRM) proporciona la capacidad de empaquetar datos multimedia en un contenedor seguro y adjuntar reglas de uso al contenido.</span><span class="sxs-lookup"><span data-stu-id="55189-111">Digital Rights Management (DRM) provides the ability to package media data in a secure container and attach usage rules to the content.</span></span> <span data-ttu-id="55189-112">Por ejemplo, el proveedor de contenido podría usar la **protección contra copia** o **deshabilitar la salida digital** para deshabilitar las copias digitales directas o la transmisión fuera del sistema de PC.</span><span class="sxs-lookup"><span data-stu-id="55189-112">For example, the content provider might use **Copy Protection** or **Digital Output Disable** to disable direct digital copies or transmission out of the PC system.</span></span>

<span data-ttu-id="55189-113">La pila de audio de determinados productos de Microsoft es compatible con DRM implementando las reglas de uso que rigen la reproducción del contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-113">The audio stack in certain Microsoft products supports DRM by implementing the usage rules that govern playback of the audio content.</span></span> <span data-ttu-id="55189-114">Para reproducir el contenido protegido, el controlador de audio subyacente debe ser un *controlador de confianza*; es decir, el controlador debe tener la certificación de logotipo para DRMLevel 1300.</span><span class="sxs-lookup"><span data-stu-id="55189-114">To play the protected content, the underlying audio driver must be a *trusted driver*; that is, the driver must be logo-certified for DRMLevel 1300.</span></span> <span data-ttu-id="55189-115">Para obtener información acerca del desarrollo de controladores de confianza, puede utilizar las interfaces que se definen en el kit de desarrollo de controladores de Windows 2000 ("DDK") o posterior.</span><span class="sxs-lookup"><span data-stu-id="55189-115">For information about developing trusted drivers, you can use interfaces that are defined in the Windows 2000 Driver Development Kit ("DDK") or later.</span></span> <span data-ttu-id="55189-116">Los controladores desarrollados con el DDK implementarán las interfaces necesarias para DRM.</span><span class="sxs-lookup"><span data-stu-id="55189-116">Drivers developed with the DDK will implement the necessary interfaces to DRM.</span></span> <span data-ttu-id="55189-117">Para obtener más información, vea [Rights Management digital](/windows-hardware/drivers/audio/digital-rights-management).</span><span class="sxs-lookup"><span data-stu-id="55189-117">For more information, see [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).</span></span>

<span data-ttu-id="55189-118">Para representar el contenido protegido, el controlador de confianza debe comprobar si la **protección contra copia** y la **deshabilitación de la salida digital** están configuradas en el contenido que fluye a través de la pila de audio y responder a la configuración según corresponda.</span><span class="sxs-lookup"><span data-stu-id="55189-118">To render the protected content, the trusted driver must check whether **Copy Protection** and **Digital Output Disable** are set on the content flowing through the audio stack, and respond to the settings accordingly.</span></span>

### <a name="copy-protection-rule"></a><span data-ttu-id="55189-119">Copiar regla de protección</span><span class="sxs-lookup"><span data-stu-id="55189-119">Copy Protection Rule</span></span>

<span data-ttu-id="55189-120">La **protección contra copia** indica que no se permiten copias digitales directas en el sistema.</span><span class="sxs-lookup"><span data-stu-id="55189-120">**Copy Protection** indicates that direct digital copies are not allowed on the system.</span></span> <span data-ttu-id="55189-121">El documento B del acuerdo de pruebas de WHQL se ha actualizado para reflejar las nuevas expectativas y requisitos de un controlador cuando se establece la **protección contra copia** en el contenido.</span><span class="sxs-lookup"><span data-stu-id="55189-121">Exhibit B to the WHQL Testing Agreement has been updated to reflect the new expectations and requirements of a driver when **Copy Protection** is set on the content.</span></span> <span data-ttu-id="55189-122">En Windows 7, el controlador de clase de audio HD integrado cumple los requisitos más recientes.</span><span class="sxs-lookup"><span data-stu-id="55189-122">For Windows 7, the built-in HD audio class driver complies with the latest requirements.</span></span>

<span data-ttu-id="55189-123">Además de garantizar que el contenido no se puede pasar a otro componente o almacenarse en un medio de almacenamiento no volátil que no esté autenticado por el sistema DRM, el controlador de audio realiza las siguientes tareas cuando se establece la **protección contra copia** :</span><span class="sxs-lookup"><span data-stu-id="55189-123">In addition to ensuring that content is not allowed to pass to another component or be stored on any nonvolatile storage medium that is not authenticated by the DRM system, the audio driver performs the following tasks when **Copy Protection** is set:</span></span>

-   <span data-ttu-id="55189-124">El controlador habilita HDCP en los puntos de conexión de HDMI.</span><span class="sxs-lookup"><span data-stu-id="55189-124">The driver enables HDCP on HDMI endpoints.</span></span>
-   <span data-ttu-id="55189-125">En el caso de las interfaces S/PDIF, el controlador valida que la combinación de los bits de código L, CP y categoría indica un estado SCMS de "Copy Never", tal como se define en IEC 60958.</span><span class="sxs-lookup"><span data-stu-id="55189-125">For S/PDIF interfaces, the driver validates that the combination of L, Cp and Category Code bits indicates an SCMS state of "Copy Never", as defined in IEC 60958.</span></span>
-   <span data-ttu-id="55189-126">El bit L se establece en 0 y el código de categoría se establece en "mezclador digital signal".</span><span class="sxs-lookup"><span data-stu-id="55189-126">The L bit is set to 0 and the Category Code is set to "Digital Signal Mixer".</span></span>

<span data-ttu-id="55189-127">La estructura **DRMRIGHTS** , usada por los controladores de audio de confianza, especifica los derechos de contenido DRM asignados a un PIN de audio de KS o a un objeto de secuencia de un controlador de clase de puerto.</span><span class="sxs-lookup"><span data-stu-id="55189-127">The **DRMRIGHTS** structure, used by trusted audio drivers, specifies the DRM content rights assigned to a KS audio pin or to a port-class driver's stream object.</span></span> <span data-ttu-id="55189-128">El miembro **CopyProtect** indica si la **protección contra copia** está establecida en el contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-128">The **CopyProtect** member indicates whether **Copy Protection** is set on the audio content.</span></span>

<span data-ttu-id="55189-129">En Windows 7, el uso de **CopyProtect** es más estricto.</span><span class="sxs-lookup"><span data-stu-id="55189-129">For Windows 7, the use of **CopyProtect** is stricter.</span></span> <span data-ttu-id="55189-130">El controlador garantiza que los controles de protección se establezcan en las interfaces de audio, se establezca HDCP para la salida de HDMI y SCMS se establezca para la salida S/PDIF estableciendo el estado en "copiar nunca".</span><span class="sxs-lookup"><span data-stu-id="55189-130">The driver ensures that the protection controls are set on the audio interfaces, HDCP is set for HDMI output, and SCMS is set for S/PDIF output by setting the state to "Copy Never".</span></span>

### <a name="digital-output-disable-rule"></a><span data-ttu-id="55189-131">Regla de deshabilitación de salida digital</span><span class="sxs-lookup"><span data-stu-id="55189-131">Digital Output Disable Rule</span></span>

<span data-ttu-id="55189-132">La **deshabilitación de salida digital** indica que el contenido no se puede transmitir fuera del sistema.</span><span class="sxs-lookup"><span data-stu-id="55189-132">**Digital Output Disable** indicates that the content is not allowed to be transmitted out of the system.</span></span> <span data-ttu-id="55189-133">En Windows 7, el controlador integrado de la clase HD Audio responde a esta configuración al habilitar HDCP en los puntos de conexión de HDMI.</span><span class="sxs-lookup"><span data-stu-id="55189-133">In Windows 7, the built-in HD audio class driver responds to this setting by enabling HDCP on HDMI endpoints.</span></span> <span data-ttu-id="55189-134">Esto es similar a la respuesta del controlador a la configuración de **protección contra copia** .</span><span class="sxs-lookup"><span data-stu-id="55189-134">This is similar to the driver's response to the **Copy Protection** setting.</span></span>

## <a name="enabling-content-protection-mechanisms-outside-of-a-protected-environment"></a><span data-ttu-id="55189-135">Habilitación de mecanismos de protección de contenido fuera de un entorno protegido</span><span class="sxs-lookup"><span data-stu-id="55189-135">Enabling Content-Protection Mechanisms Outside of a Protected Environment</span></span>

<span data-ttu-id="55189-136">PUMA reside en un proceso independiente en el entorno protegido (PE).</span><span class="sxs-lookup"><span data-stu-id="55189-136">PUMA resides in a separate process in the Protected Environment (PE).</span></span> <span data-ttu-id="55189-137">En Windows Vista, para usar los controles de protección de contenido de audio ofrecidos por PUMA, una aplicación multimedia debe estar en un archivo PE.</span><span class="sxs-lookup"><span data-stu-id="55189-137">In Windows Vista, to use the audio content protection controls offered by PUMA, a media application must be in a PE.</span></span> <span data-ttu-id="55189-138">Dado que solo Media Foundation API pueden interactuar con un PE, los controles de protección de contenido se limitan a las aplicaciones que usan Media Foundation API para transmitir contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-138">Because only Media Foundation APIs can interact with a PE, the content protection controls are limited to applications using Media Foundation APIs to stream audio content.</span></span>

<span data-ttu-id="55189-139">En Windows 7, cualquier aplicación puede acceder a los controles de protección de contenido que proporciona la autoridad de confianza de salida de PUMA (OTA), independientemente de si están en un PE o mediante Media Foundation API para la reproducción de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-139">In Windows 7, any application can access the content protection controls provided by the PUMA Output Trust Authority (OTA), regardless of whether they are in a PE or using Media Foundation APIs for audio playback.</span></span>

## <a name="implementation-instructions"></a><span data-ttu-id="55189-140">Instrucciones de implementación</span><span class="sxs-lookup"><span data-stu-id="55189-140">Implementation Instructions</span></span>

<span data-ttu-id="55189-141">Los pasos siguientes son necesarios para que una aplicación de audio controle la protección de contenido de SCMS o HDCP en un punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-141">The following steps are required for an audio application to control SCMS or HDCP content protection on an audio endpoint.</span></span> <span data-ttu-id="55189-142">Las API de audio compatibles son DirectShow, DirectSound y WASAPI.</span><span class="sxs-lookup"><span data-stu-id="55189-142">Supported Audio APIs are DirectShow, DirectSound, and WASAPI.</span></span>

<span data-ttu-id="55189-143">Este código de ejemplo utiliza las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="55189-143">This example code uses the following interfaces.</span></span>

-   [<span data-ttu-id="55189-144">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="55189-144">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="55189-145">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="55189-145">**IMMDevice**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="55189-146">**IAudioClient**</span><span class="sxs-lookup"><span data-stu-id="55189-146">**IAudioClient**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)
-   [<span data-ttu-id="55189-147">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="55189-147">**IMMDeviceCollection**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
-   [<span data-ttu-id="55189-148">**IMFTrustedOutput**</span><span class="sxs-lookup"><span data-stu-id="55189-148">**IMFTrustedOutput**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)
-   [<span data-ttu-id="55189-149">**IMFOutputPolicy**</span><span class="sxs-lookup"><span data-stu-id="55189-149">**IMFOutputPolicy**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)

<span data-ttu-id="55189-150">La aplicación multimedia debe realizar las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="55189-150">The media application must perform the following tasks.</span></span>

1.  <span data-ttu-id="55189-151">Configure el entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="55189-151">Set up the development environment.</span></span>
    -   <span data-ttu-id="55189-152">Haga referencia a las interfaces necesarias, incluya los encabezados que se muestran en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="55189-152">Reference the required interfaces, include the headers shown in the following code.</span></span>
        ```cpp
        #include <MMdeviceapi.h>        // Device endpoint definitions
        #include <Mfidl.h>              // OTA interface definitions
        ```

        

    -   <span data-ttu-id="55189-153">Vínculo a Mfuuid. lib para usar las interfaces de OTA.</span><span class="sxs-lookup"><span data-stu-id="55189-153">Link to the Mfuuid.lib to use the OTA interfaces.</span></span>
    -   <span data-ttu-id="55189-154">Deshabilite el depurador de kernel y el comprobador de controladores para evitar errores de comprobación de autenticación.</span><span class="sxs-lookup"><span data-stu-id="55189-154">Disable the kernel debugger and driver verifier to avoid any authentication checking errors.</span></span>
2.  <span data-ttu-id="55189-155">Enumere todos los extremos del sistema y seleccione el punto de conexión de destino de la colección de extremos, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="55189-155">Enumerate all endpoints in the system and select the target endpoint from the endpoint collection, as shown in the following code.</span></span> <span data-ttu-id="55189-156">Para obtener más información acerca de la enumeración de dispositivos, consulte [enumeración de dispositivos de audio](/previous-versions//ms678716(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="55189-156">For more information about enumerating devices, see [Enumerating Audio Devices](/previous-versions//ms678716(v=vs.85)).</span></span>
    ```cpp
    BOOL IsDigitalEndpoint(IMMDevice *pDevice)
    {
       PROPVARIANT         var;
       IPropertyStore      *pProperties = NULL;
       EndpointFormFactor  formfactor;
       BOOL                bResult = FALSE;
       HRESULT             hr = S_OK;
       PropVariantInit(&var);
       // Open endpoint properties
       hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
       IF_FAILED_JUMP(hr, Exit);

       // get form factor 
       hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
       IF_FAILED_JUMP(hr, Exit);
       formfactor = (EndpointFormFactor)var.uiVal;
       // DigitalAudioDisplayDevice is defined same as HDMI formfactor
       if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
       {
           bResult = TRUE;
       }

    Exit:
       PropVariantClear(&var);
       SAFE_RELEASE(pProperties);
       return bResult;
    }
    ```

    

    ```cpp
    /******************************************************************
    *                                                                 *
    *  GetDevice:  Selects an endpoint that meets the requirements.   *
    *                                                                 *
    *  ppDevice: Receives a pointer to an IMMDevice interface of      *
    *            the device's endpoint object                         *                                             *                                            *
    *                                                                 *
    ******************************************************************/
    HRESULT GetDevice(IMMDevice** ppDevice)
    {
       IMMDeviceEnumerator    *pEnumerator = NULL;
       IMMDevice              *pDevice = NULL;
       IMMDeviceCollection    *pEndpoints = NULL;
       UINT                    cEndpoints = 0;

       const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
       const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

       // Get enumerator for audio endpoint devices
       hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, 
           NULL,
           CLSCTX_ALL, 
           IID_IMMDeviceEnumerator,
           (void**)&pEnumerator));


       EXIT_ON_ERROR(hr)

       // Enumerate all active endpoints,
       hr = pEnumerator->EnumAudioEndpoints (
           eRender,
           DEVICE_STATE_ACTIVE,
           &pEndpoints);
       EXIT_ON_ERROR(hr)

       hr = pEndpoints->GetCount(&cEndpoints);
       EXIT_ON_ERROR(hr)

       for (UINT i = 0; i < cEndpoints; i++)
       {
           hr = pEndpoints->Item(i, &pDevice);
           IF_FAILED_JUMP(hr, Exit);
           {
               // Select the endpoint that meets the requirements.
               // For example, SPDIF analog output or HDMI
               if (IsDigitalEndpoint(pDevice))
               {
                   *(ppDevice) = pDevice;
                   (*ppDevice)->AddRef();
                   break;
               }
           }
           SAFE_RELEASE(pDevice);
       }
    Exit:
       if (FAILED(hr))
       {
           // Notify error.
           // Not Shown.
       }
       SAFE_RELEASE(pEndpoints);
       SAFE_RELEASE(pEnumerator);
    }
    ```

    

3.  <span data-ttu-id="55189-157">Use el puntero [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) al punto de conexión devuelto por el proceso de enumeración para activar la API de streaming de audio deseada y preparar la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="55189-157">Use the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) pointer to the endpoint returned by the enumeration process to activate the desired audio streaming API and prepare for streaming.</span></span> <span data-ttu-id="55189-158">Las distintas API de audio requieren una preparación ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="55189-158">Different audio APIs require slightly different preparation.</span></span>
    -   <span data-ttu-id="55189-159">Para las aplicaciones de audio de DShow:</span><span class="sxs-lookup"><span data-stu-id="55189-159">For DShow audio applications:</span></span>
        1.  <span data-ttu-id="55189-160">Cree un objeto COM de DirectShow llamando a [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) y especificando IID \_ IBaseFilter como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="55189-160">Create a DirectShow COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IBaseFilter as the interface identifier.</span></span>
            ```cpp
            IUnknown *pDShowFilter = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IBaseFilter,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDShowFilter));
            ```

            

        2.  <span data-ttu-id="55189-161">Cree un gráfico de filtros de DirectShow con este objeto COM activado por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55189-161">Build a DirectShow filter graph with this COM object activated by the device.</span></span> <span data-ttu-id="55189-162">Para obtener más información sobre este proceso, vea "Building the Filter Graph" en la documentación del SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="55189-162">For more information about this process, see "Building the Filter Graph" in DirectShow SDK documentation.</span></span>
    -   <span data-ttu-id="55189-163">Para las aplicaciones de DSound audio:</span><span class="sxs-lookup"><span data-stu-id="55189-163">For DSound audio applications:</span></span>
        1.  <span data-ttu-id="55189-164">Cree un objeto COM DSound llamando a [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) y especificando IID \_ IDirectSound8 como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="55189-164">Create a DSound COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IDirectSound8 as the interface identifier.</span></span>
            ```cpp
            IDirectSound8  *pDSSound8;
            ...
            hr = pDevice->Activate (
                              IID_IDirectSound8,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDSSound8));
            ```

            

        2.  <span data-ttu-id="55189-165">Use el objeto DSound creado anteriormente para el programa DSound para el streaming.</span><span class="sxs-lookup"><span data-stu-id="55189-165">Use DSound object created above to program DSound for steaming.</span></span> <span data-ttu-id="55189-166">Para obtener más información acerca de este proceso, consulte [DirectSound](/previous-versions//bb219818(v=vs.85)) en MSDN.</span><span class="sxs-lookup"><span data-stu-id="55189-166">For more information about this process, see [DirectSound](/previous-versions//bb219818(v=vs.85)) on MSDN.</span></span>
    -   <span data-ttu-id="55189-167">Para WASAPI:</span><span class="sxs-lookup"><span data-stu-id="55189-167">For WASAPI:</span></span>
        1.  <span data-ttu-id="55189-168">Cree un objeto com [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) llamando a [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) y especificando IID \_ IAudioClient como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="55189-168">Create an [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) COM object by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) and specifying IID\_IAudioClient as the interface identifier.</span></span>
            ```cpp
            IAudioClient *pIAudioClient = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IAudioClient,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pIAudioClient));
            ```

            

        2.  <span data-ttu-id="55189-169">Abra la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-169">Open the audio stream.</span></span>
            ```cpp
            hr = pIAudioClient->Initialize(...);
            ```

            
4.  <span data-ttu-id="55189-170">Inicie el streaming de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-170">Start audio streaming.</span></span>
5.  <span data-ttu-id="55189-171">Establezca la Directiva de protección en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="55189-171">Set the protection policy on the stream.</span></span>
    1.  <span data-ttu-id="55189-172">En el caso de los clientes de WASAPI, obtenga una referencia a la interfaz [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) del objeto de la autoridad de confianza de salida (OTA) para la secuencia llamando a [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) y especificando IID \_ IMFTrustedOutput como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="55189-172">For WASAPI clients, get a reference to the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface of the output trust authority (OTA) object for the stream by calling [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) and specifying IID\_IMFTrustedOutput as the interface identifier.</span></span>
        ```cpp
        IMFTrustedOutput*       pTrustedOutput = NULL;
        hr = pIAudioClient>GetService(
                       __uuidof(IMFTrustedOutput),
                       (void**)& pTrustedOutput);
        ```

        

    2.  <span data-ttu-id="55189-173">Obtiene un recuento de los objetos de OTA disponibles mediante una llamada a [**IMFTrustedOutput:: GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).</span><span class="sxs-lookup"><span data-stu-id="55189-173">Get a count of the available OTA objects by calling [**IMFTrustedOutput::GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).</span></span>
        ```cpp
        hr = pTrustedOutput->GetOutputTrustAuthorityCount(&m_dwCountOTA);
        ```

        

    3.  <span data-ttu-id="55189-174">Enumere la colección de OTA y obtenga una referencia al objeto de OTA que admite la acción PEACTION \_ Play.</span><span class="sxs-lookup"><span data-stu-id="55189-174">Enumerate the OTA collection and get a reference to the OTA object that supports the action PEACTION\_PLAY.</span></span> <span data-ttu-id="55189-175">Todos los OTAs exponen la interfaz [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) .</span><span class="sxs-lookup"><span data-stu-id="55189-175">All OTAs expose the [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) interface.</span></span>
        ```cpp
        hr = pMFTrustedOutput->GetOutputTrustAuthorityByIndex(I, &pMFOutputTrustAuthority);
        hr = pMFOutputTrustAuthority->GetAction(&action) 
        ```

        

    4.  <span data-ttu-id="55189-176">Use la interfaz [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) para establecer la Directiva de protección en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="55189-176">Use the [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) interface to set the protection policy on the stream.</span></span>

        ```cpp
        hr = pTrustedOutput ->SetPolicy(&pPolicy, nPolicy, &pbTicket, &cbTicket);
        ```

        

        > [!Note]
        > <span data-ttu-id="55189-177">Si usa EVR, [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) genera el evento [MEPOLICYSET](../medfound/mepolicyset.md) y devuelve MF \_ S \_ Wait \_ para \_ \_ que la Directiva se establezca para indicar que la OTA aplicará la Directiva de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="55189-177">If you are using the EVR, [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) raises the [MEPolicySet](../medfound/mepolicyset.md) event and returns MF\_S\_WAIT\_FOR\_POLICY\_SET to indicate that the OTA will enforce the policy asynchronously.</span></span> <span data-ttu-id="55189-178">Sin embargo, en este código de ejemplo, la aplicación es un cliente de WASAPI directo que recuperó el objeto de OTA del cliente de audio (paso 5 a).</span><span class="sxs-lookup"><span data-stu-id="55189-178">However, in this example code, the application is a direct WASAPI client that retrieved the OTA object from the audio client (Step 5 a).</span></span> <span data-ttu-id="55189-179">A diferencia de EVR, un cliente de audio y otros objetos WASAPI no implementan generadores de eventos multimedia.</span><span class="sxs-lookup"><span data-stu-id="55189-179">Unlike the EVR, an audio client and other WASAPI objects do not implement media event generators.</span></span> <span data-ttu-id="55189-180">Sin generadores de eventos multimedia, **IMFTrustedOutput:: SetPolicy** no devuelve MF \_ S \_ Wait \_ para el \_ conjunto de directivas \_ .</span><span class="sxs-lookup"><span data-stu-id="55189-180">Without media event generators, **IMFTrustedOutput::SetPolicy** does not return MF\_S\_WAIT\_FOR\_POLICY\_SET.</span></span>
        >
        > <span data-ttu-id="55189-181">La configuración de la Directiva de audio debe establecerse después de que se inicie el streaming de audio; de lo contrario, [**IMFTrustedOutput:: GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) produce un error</span><span class="sxs-lookup"><span data-stu-id="55189-181">The audio policy settings must be set after audio streaming starts, otherwise [**IMFTrustedOutput::GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) fails.</span></span> <span data-ttu-id="55189-182">Además, para admitir esta característica, el controlador de audio subyacente debe ser un *controlador de confianza*.</span><span class="sxs-lookup"><span data-stu-id="55189-182">Also, to support this feature, the underlying audio driver must be a *trusted driver*.</span></span>

         

        <span data-ttu-id="55189-183">En el código de ejemplo, *pPolicy* es un puntero a la interfaz [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) de un objeto de directiva implementado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="55189-183">In the example code, *pPolicy* is a pointer to the [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) interface of a client-implemented policy object.</span></span> <span data-ttu-id="55189-184">Para obtener más información, consulte la documentación del [SDK de Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .</span><span class="sxs-lookup"><span data-stu-id="55189-184">For information, see [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) documentation.</span></span>

        <span data-ttu-id="55189-185">En la implementación del método [**IMFOutputPolicy:: GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) , debe generarse una colección de los sistemas de protección de salida (esquemas) que debe aplicar la OTA.</span><span class="sxs-lookup"><span data-stu-id="55189-185">In the implementation of the [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) method, a collection of the output protection systems (schemas) must be generated that the OTA must enforce.</span></span> <span data-ttu-id="55189-186">Cada esquema se identifica mediante un GUID y contiene datos de configuración para el sistema de protección.</span><span class="sxs-lookup"><span data-stu-id="55189-186">Each schema is identified by a GUID and contains configuration data for the protection system.</span></span> <span data-ttu-id="55189-187">Asegúrese de que los sistemas de protección de la recopilación estén restringidos al uso de controladores de audio de confianza.</span><span class="sxs-lookup"><span data-stu-id="55189-187">Make sure that the protection systems in the collection are restricted to using trusted audio drivers.</span></span> <span data-ttu-id="55189-188">Esta restricción se identifica mediante el GUID, **MFPROTECTION \_ TRUSTEDAUDIODRIVERS**, Disable o CONSTRICTAUDIO.</span><span class="sxs-lookup"><span data-stu-id="55189-188">This restriction is identified by the GUID, **MFPROTECTION\_TRUSTEDAUDIODRIVERS**,DISABLE, or CONSTRICTAUDIO.</span></span> <span data-ttu-id="55189-189">Si \_ se usa MFPROTECTION TRUSTEDAUDIODRIVERS, los datos de configuración de este esquema son un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="55189-189">If MFPROTECTION\_TRUSTEDAUDIODRIVERS is used, the configuration data for this schema is a DWORD.</span></span> <span data-ttu-id="55189-190">Para obtener más información sobre los esquemas y los datos de configuración relacionados, vea la documentación del SDK de entorno protegido.</span><span class="sxs-lookup"><span data-stu-id="55189-190">For more information about the schemas and the related configuration data, see Protected Environment SDK documentation.</span></span>

        <span data-ttu-id="55189-191">El cliente también debe proporcionar la definición de esquema mediante la implementación de la interfaz [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="55189-191">The client must also provide the schema definition, by implementing the [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) interface.</span></span> <span data-ttu-id="55189-192">[**IMFOutputSchema:: GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) recupera **MFPROTECTION \_ TRUSTEDAUDIODRIVERS** como el GUID del esquema.</span><span class="sxs-lookup"><span data-stu-id="55189-192">[**IMFOutputSchema::GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) retrieves **MFPROTECTION\_TRUSTEDAUDIODRIVERS** as the schema GUID.</span></span> <span data-ttu-id="55189-193">[**IMFOutputSchema:: GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) devuelve un puntero a los datos de configuración del esquema.</span><span class="sxs-lookup"><span data-stu-id="55189-193">[**IMFOutputSchema::GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) returns a pointer to the schema's configuration data.</span></span>

6.  <span data-ttu-id="55189-194">Continúe con el streaming de audio.</span><span class="sxs-lookup"><span data-stu-id="55189-194">Continue audio streaming.</span></span>
7.  <span data-ttu-id="55189-195">Asegúrese de que la Directiva de protección esté clara antes de detener la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="55189-195">Make sure the protection policy is clear before stopping streaming.</span></span>

    <span data-ttu-id="55189-196">Libere las referencias de la interfaz de directiva relacionadas anteriores.</span><span class="sxs-lookup"><span data-stu-id="55189-196">Release the related policy interface references above.</span></span>

    <span data-ttu-id="55189-197">Las llamadas de versión borran la configuración de directiva establecida previamente.</span><span class="sxs-lookup"><span data-stu-id="55189-197">The release calls clear the previously set policy settings.</span></span>

    > [!Note]  
    > <span data-ttu-id="55189-198">Cada vez que se reinicia una secuencia, se debe volver a establecer la Directiva de protección en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="55189-198">Every time a stream is restarted, the protection policy must be set again on the stream.</span></span> <span data-ttu-id="55189-199">El procedimiento se describe en el paso 5-d.</span><span class="sxs-lookup"><span data-stu-id="55189-199">The procedure is described in step 5-d.</span></span>

    ```cpp
    pMFOutputTrustAuthority->Release()
    pMFTrustedOutput->Release()
    ```
  

<span data-ttu-id="55189-200">En los siguientes ejemplos de código se muestra una implementación de ejemplo de la Directiva y los objetos de esquema.</span><span class="sxs-lookup"><span data-stu-id="55189-200">The following code examples show a sample implementation of the policy and schema objects.</span></span>


```cpp
//OTADsoundSample.cpp
#include <stdio.h>
#include <tchar.h>
#include <initguid.h>
#include <windows.h>
#include <mmreg.h>
#include <dsound.h>

#include <mfidl.h>
#include <Mmdeviceapi.h>
#include <AVEndpointKeys.h>
#include "OTADSoundSample.h"

#define STATIC_KSDATAFORMAT_SUBTYPE_AC3\
    DEFINE_WAVEFORMATEX_GUID(WAVE_FORMAT_DOLBY_AC3_SPDIF)
DEFINE_GUIDSTRUCT("00000092-0000-0010-8000-00aa00389b71", KSDATAFORMAT_SUBTYPE_AC3);
#define KSDATAFORMAT_SUBTYPE_AC3 DEFINE_GUIDNAMED(KSDATAFORMAT_SUBTYPE_AC3)


HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy);
HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy);


const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

BOOL IsDigitalEndpoint(IMMDevice *pDevice)
{
    PROPVARIANT         var;
    IPropertyStore      *pProperties = NULL;
    EndpointFormFactor  formfactor;
    BOOL                bResult = FALSE;
    HRESULT             hr = S_OK;
    PropVariantInit(&var);

    // Open endpoint properties
    hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
    IF_FAILED_JUMP(hr, Exit);

    // get form factor 
    hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
    IF_FAILED_JUMP(hr, Exit);

    formfactor = (EndpointFormFactor)var.uiVal;
    if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
    {
        bResult = TRUE;
    }

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pProperties);

    return bResult;
}


HRESULT GetDigitalAudioEndpoint(IMMDevice** ppDevice)
{
    IMMDeviceEnumerator    *pEnumerator = NULL;
    IMMDevice              *pDevice = NULL;
    IMMDeviceCollection    *pEndpoints = NULL;
    UINT                    cEndpoints = 0;
    HRESULT hr = S_OK;

    *ppDevice = NULL;
    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator, NULL,
                          CLSCTX_ALL, IID_IMMDeviceEnumerator,
                          (void**)&pEnumerator);
    IF_FAILED_JUMP(hr, Exit);

    // Enumerate all active render endpoints, 
    hr = pEnumerator->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    hr = pEndpoints->GetCount(&cEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    for (UINT i = 0; i < cEndpoints; i++)
    {
        hr = pEndpoints->Item(i, &pDevice);
        IF_FAILED_JUMP(hr, Exit);
        // Select the endpoint that meets the requirements.
        // For example, SPDIF analog output or HDMI
        // Not Shown.
        if (IsDigitalEndpoint(pDevice))
        {
            *ppDevice = pDevice;
            (*ppDevice)->AddRef();
            break;
        }
        SAFE_RELEASE(pDevice);
    }
Exit:
    if (FAILED(hr))
    {
        // Notify error.
        // Not Shown.
    }
    SAFE_RELEASE(pEndpoints);
    SAFE_RELEASE(pEnumerator);
    return hr; 
}


//-------------------------------------------------------------------
int __cdecl wmain(int argc, char* argv[])
{
    IMMDevice *pEndpoint=NULL;
    HRESULT hr = S_OK;

    // DSound related variables
    IDirectSound8*          DSSound8 = NULL; 
    IDirectSoundBuffer*     DSBuffer = NULL; 
    DSBUFFERDESC            DSBufferDesc;
    WAVEFORMATEXTENSIBLE    wfext;
    WORD nChannels = 2;
    DWORD nSamplesPerSec = 48000;
    WORD wBitsPerSample = 16;

    // OTA related variables
    IMFTrustedOutput *pMFTrustedOutput=NULL;
    IMFOutputPolicy *pMFOutputPolicy=NULL;
    IMFOutputTrustAuthority *pMFOutputTrustAuthority=NULL;
    DWORD dwConfigData=0;

    // Initialize COM
    hr = CoInitialize(NULL);
    IF_FAILED_JUMP(hr, Exit);

    printf("OTA test app for DSound\n");

    hr = GetDigitalAudioEndpoint(&pEndpoint);
    IF_FAILED_JUMP(hr, Exit);

    if (pEndpoint)
    {
        printf("Found digital audio endpoint.\n");
    }
    //
    // Active DSound interface
    //
    hr = pEndpoint->Activate(IID_IDirectSound8, CLSCTX_INPROC_SERVER, NULL, reinterpret_cast<void **>(&DSSound8));
    IF_FAILED_JUMP(hr, Exit);

    nChannels = 2;
    nSamplesPerSec = 48000;
    wBitsPerSample = 16;

    ZeroMemory(&wfext, sizeof(wfext));
    wfext.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
    wfext.Format.nChannels = nChannels;
    wfext.Format.nSamplesPerSec = nSamplesPerSec;
    wfext.Format.wBitsPerSample = wBitsPerSample;
    wfext.Format.nBlockAlign = (nChannels * wBitsPerSample) / 8;
    wfext.Format.nAvgBytesPerSec = nSamplesPerSec * ((nChannels * wBitsPerSample) / 8);
    wfext.Format.cbSize = 22;
    wfext.Samples.wValidBitsPerSample = wBitsPerSample;
    wfext.dwChannelMask = 0x3;
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_PCM;
#if 1 
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_AC3;
#endif

    ZeroMemory(&DSBufferDesc, sizeof(DSBufferDesc));
    DSBufferDesc.dwSize = sizeof(DSBufferDesc);
    DSBufferDesc.dwFlags = DSBCAPS_GLOBALFOCUS | DSBCAPS_LOCSOFTWARE | DSBCAPS_GETCURRENTPOSITION2;
    DSBufferDesc.lpwfxFormat = (WAVEFORMATEX *)&wfext;
    DSBufferDesc.dwBufferBytes = wfext.Format.nAvgBytesPerSec / 100;

    HWND hwnd = GetForegroundWindow();
    hr = DSSound8->SetCooperativeLevel(hwnd, DSSCL_PRIORITY);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSSound8->CreateSoundBuffer(&DSBufferDesc, &DSBuffer, NULL);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    printf("Will set the following audio policy:\n");
    printf("Test Certificate Enable: %s\n", TRUE ? "True" : "False");
    printf("Copy OK: %s\n", FALSE ? "True" : "False");
    printf("Digital Output Disable: %s\n", FALSE ? "True" : "False");
    printf("DRM Level: %u\n", 1300);

    // Set policy when the stream is in RUN state
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    //
    // Perform all the necessary streaming operations here.
    //

    // stop audio streaming
    DSBuffer->Stop();

    // In order for the stream to restart successfully 
    // Need to release the following OutputTrust* interface to release audio endpoint
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // After above release operations, the following Play() will succeed without without device-in-use error message 0x8889000A
    DSBuffer->SetCurrentPosition(0);
    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    // Need to reset the new audio protection state because previous settings were gone with the ClearOTAPolicy call.
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    // Clean up setting before leaving your streaming app.
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    DSBuffer->SetCurrentPosition(0);

Exit:
    SAFE_RELEASE(DSBuffer);
    SAFE_RELEASE(DSSound8);

    SAFE_RELEASE(pEndpoint);

    CoUninitialize();

    return 0;
}
```




```cpp
//OTADSoundSample.h
// Macro defines
#define IF_FAILED_JUMP(_hresult, label)                         \
    if(FAILED(_hresult))                                        \
    {                                                           \
        goto label;                                             \
    }

#define SAFE_RELEASE(p) \
    if (NULL != p) { \
        (p)->Release(); \
        (p) = NULL; \
    }

#define IF_TRUE_ACTION_JUMP(condition, action, label)           \
    if(condition)                                               \
    {                                                           \
        action;                                                 \
        goto label;                                             \
    }
```




```cpp
// outputpolicy.h

class CTrustedAudioDriversOutputPolicy : public CMFAttributesImpl<IMFOutputPolicy> 
{
friend
    HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy);
private:
    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginator;
    IMFOutputSchema *m_pOutputSchema;
    
    CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr);
    ~CTrustedAudioDriversOutputPolicy();

public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(/* [in] */ REFIID riid,/* [out] */ LPVOID *ppvObject);
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();
    
    // IMFOutputPolicy methods
    HRESULT STDMETHODCALLTYPE
        GenerateRequiredSchemas( 
            /* [in] */ DWORD dwAttributes,
            /* [in] */ GUID guidOutputSubType,
            /* [in] */ GUID *rgGuidProtectionSchemasSupported,
            /* [in] */ DWORD cProtectionSchemasSupported,
            /* [annotation][out] */ 
            __out  IMFCollection **ppRequiredProtectionSchemas);

    HRESULT STDMETHODCALLTYPE GetOriginatorID(/* [annotation][out] */ __out  GUID *pguidOriginatorID);

    HRESULT STDMETHODCALLTYPE GetMinimumGRLVersion(/* [annotation][out] */ __out  DWORD *pdwMinimumGRLVersion);
}; // CTrustedAudioDriversOutputPolicy

class CTrustedAudioDriversOutputSchema : public CMFAttributesImpl<IMFOutputSchema> 
{

friend
    HRESULT CreateTrustedAudioDriversOutputSchema(
        DWORD dwConfigData,
        GUID guidOriginatorID,
        IMFOutputSchema **ppMFOutputSchema
    );

private:
    CTrustedAudioDriversOutputSchema(DWORD dwConfigData, GUID guidOriginatorID);
    ~CTrustedAudioDriversOutputSchema();

    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginatorID;
    
public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(
       /* [in] */ REFIID riid,
       /* [out] */ LPVOID *ppvObject
    );
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();

    // IMFOutputSchema methods
    HRESULT STDMETHODCALLTYPE GetConfigurationData(__out DWORD *pdwVal);
    HRESULT STDMETHODCALLTYPE GetOriginatorID(__out GUID *pguidOriginatorID);
    HRESULT STDMETHODCALLTYPE GetSchemaType(__out GUID *pguidSchemaType);

}; // CTrustedAudioDriversOutputSchema
```




```cpp
// outputpolicy.cpp

#include <windows.h>
#include <tchar.h>
#include <mfidl.h>
#include <atlstr.h>
#include <attributesbase.h>
#include "OTADSoundSample.h"

#include <Mmdeviceapi.h>
#include "OutputPolicy.h"

#define RETURN_INTERFACE(T, iid, ppOut) \
    if (IsEqualIID(__uuidof(T), (iid))) { \
        this->AddRef(); \
        *(ppOut) = static_cast<T *>(this); \
        return S_OK; \
    } else {} (void)0

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputPolicy
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputPolicy::CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr)
: m_cRefCount(1), m_dwConfigData(dwConfigData), m_pOutputSchema(NULL)
{
    hr = CoCreateGuid(&m_guidOriginator);
    IF_FAILED_JUMP(hr, Exit);

    hr = CreateTrustedAudioDriversOutputSchema(dwConfigData, m_guidOriginator, &m_pOutputSchema);
    IF_FAILED_JUMP(hr, Exit);

Exit:
    if (FAILED(hr))
    {
        printf("CreateTrustedAudioDriversOutputSchema failed: hr = 0x%08x", hr);
    }
    return;
}

// destructor
CTrustedAudioDriversOutputPolicy::~CTrustedAudioDriversOutputPolicy()
{
    if (NULL != m_pOutputSchema) 
    {
        m_pOutputSchema->Release();
    }
}


// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE
    CTrustedAudioDriversOutputPolicy::QueryInterface(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject)
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);

    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputPolicy, riid, ppvObject);    

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}

// IMFOutputPolicy::GenerateRequiredSchemas
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GenerateRequiredSchemas
( 
        /* [in] */ DWORD dwAttributes,
        /* [in] */ GUID guidOutputSubType,
        /* [in] */ GUID *rgGuidProtectionSchemasSupported,
        /* [in] */ DWORD cProtectionSchemasSupported,
        /* [annotation][out] */ 
        __out  IMFCollection **ppRequiredProtectionSchemas
)
{
    HRESULT hr = S_OK;
    bool bTrustedAudioDriversSupported = false;
    // if we've made it this far then the Output Trust Authority supports Trusted Audio Drivers
    // create a collection and put our output policy in it
    // then give that collection to the caller
    CComPtr<IMFCollection> pMFCollection;

    // sanity checks
    IF_TRUE_ACTION_JUMP((NULL == ppRequiredProtectionSchemas), hr = E_POINTER, Exit); 
    *ppRequiredProtectionSchemas = NULL;

    IF_TRUE_ACTION_JUMP((NULL == rgGuidProtectionSchemasSupported) && (0 != cProtectionSchemasSupported), 
                    hr = E_POINTER, Exit); 

    // log all the supported protection schemas
    for (DWORD i = 0; i < cProtectionSchemasSupported; i++) 
    {
        if (IsEqualIID(MFPROTECTION_TRUSTEDAUDIODRIVERS, rgGuidProtectionSchemasSupported[i])) 
        {
            bTrustedAudioDriversSupported = true;
        }
    }

    if (!bTrustedAudioDriversSupported) 
    {
        return HRESULT_FROM_WIN32(ERROR_RANGE_NOT_FOUND);
    }


    // create the collection
    hr = MFCreateCollection(&pMFCollection);
    if (FAILED(hr)) 
    {
        return hr;
    }

    // add our output policy to the collection
    hr = pMFCollection->AddElement(m_pOutputSchema);
    if (FAILED(hr)) 
    {
        return hr;
    }
Exit:
    // give the collection to the caller
    return pMFCollection.CopyTo(ppRequiredProtectionSchemas); // increments refcount
}// GenerateRequiredSchemas

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetOriginatorID(__out  GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) 
    {
        return E_POINTER;
    }
    *pguidOriginatorID = m_guidOriginator;
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetMinimumGRLVersion(__out  DWORD *pdwMinimumGRLVersion) 
{
    if (NULL == pdwMinimumGRLVersion) 
    {
        return E_POINTER;
    }
    *pdwMinimumGRLVersion = 0;
    return S_OK;
}

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputSchema
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputSchema::CTrustedAudioDriversOutputSchema
(    
    DWORD dwConfigData, 
    GUID guidOriginatorID
)
: m_cRefCount(1)
, m_dwConfigData(dwConfigData)
, m_guidOriginatorID(guidOriginatorID)
{}

// destructor
CTrustedAudioDriversOutputSchema::~CTrustedAudioDriversOutputSchema() {}

// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::QueryInterface
(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject
) 
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);
    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputSchema, riid, ppvObject);

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}
// IMFOutputSchema::GetConfigurationData
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetConfigurationData(__out DWORD *pdwVal) 
{
    if (NULL == pdwVal) { return E_POINTER; }
    *pdwVal = m_dwConfigData;
    return S_OK;
}

// IMFOutputSchema::GetOriginatorID
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetOriginatorID(__out GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) { return E_POINTER; }
    *pguidOriginatorID = m_guidOriginatorID;
    return S_OK;
}
// IMFOutputSchema::GetSchemaType
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetSchemaType(__out GUID *pguidSchemaType) 
{
    if (NULL == pguidSchemaType) { return E_POINTER; }
    *pguidSchemaType = MFPROTECTION_TRUSTEDAUDIODRIVERS;
    return S_OK;
}

//---------------------------------------------------------------------------------------------------
//
// Other subroutine declarations
//
//---------------------------------------------------------------------------------------------------
HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy) 
{
    if (NULL == ppMFOutputPolicy) 
    {
        return E_POINTER;
    }

    *ppMFOutputPolicy = NULL;

    HRESULT hr = S_OK;
    CTrustedAudioDriversOutputPolicy *pPolicy = new CTrustedAudioDriversOutputPolicy(dwConfigData, hr);
    if (NULL == pPolicy) 
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr)) 
    {
        delete pPolicy;
        return hr;
    }
    *ppMFOutputPolicy = static_cast<IMFOutputPolicy *>(pPolicy);
    return S_OK;
}// CreateTrustedAudioDriversOutputPolicy

HRESULT CreateTrustedAudioDriversOutputSchema
(
    DWORD dwConfigData,
    GUID guidOriginatorID,
    IMFOutputSchema **ppMFOutputSchema) 
{
    if (NULL == ppMFOutputSchema) 
    {
        return E_POINTER;
    }

    *ppMFOutputSchema = NULL;

    CTrustedAudioDriversOutputSchema *pSchema =
        new CTrustedAudioDriversOutputSchema(dwConfigData, guidOriginatorID);

    if (NULL == pSchema) 
    {
        return E_OUTOFMEMORY;
    }

    *ppMFOutputSchema = static_cast<IMFOutputSchema *>(pSchema);

    return S_OK;
}// CreateTrustedAudioDriversOutputSchema



HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy)
{
    HRESULT hr = S_OK;

    DWORD dwCountOfOTAs = 0;
    bool bRet = false;

    hr = CreateTrustedAudioDriversOutputPolicy(_dwConfigData, _ppMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // activate IMFTrustedOutput
    hr = _pMMDevice->Activate(__uuidof(IMFTrustedOutput), CLSCTX_ALL, NULL,
                             (void**)_ppMFTrustedOutput);
    IF_FAILED_JUMP(hr, Exit);

    // get count of Output Trust Authorities on this trusted output
    hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityCount(&dwCountOfOTAs);
    IF_FAILED_JUMP(hr, Exit);

    // sanity check - fail on endpoints with no output trust authorities
    IF_TRUE_ACTION_JUMP((0 == dwCountOfOTAs), hr = E_NOTFOUND, Exit);

    printf("dwCountOfOTAs = %d\n", dwCountOfOTAs);

     
    // loop over each output trust authority on the endpoint
    for (DWORD i = 0; i < dwCountOfOTAs; i++) 
    {
        // get the output trust authority
        hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityByIndex(i, ppMFOutputTrustAuthority);
        IF_FAILED_JUMP(hr, Exit);


        // log the purpose of the output trust authority
        MFPOLICYMANAGER_ACTION action;
        hr = (*ppMFOutputTrustAuthority)->GetAction(&action);
        if (FAILED(hr)) 
        {
            return hr;
        }

        printf(" It's %s.", (PEACTION_PLAY==action) ? "PEACTION_PLAY" :
                            (PEACTION_COPY==action) ? "PEACTION_COPY" :
                            "Others");
 
        // only PEACTION_PLAY Output Trust Authorities are relevant
        if (PEACTION_PLAY != action) 
        {
            printf("Skipping as the OTA action is not PEACTION_PLAY");
            SAFE_RELEASE(*ppMFOutputTrustAuthority);
            continue;
        }

        BYTE *pbTicket = NULL;
        DWORD cbTicket = 0;
        // audio ota does not support ticket, leaving it NULL is ok.
        hr = (*ppMFOutputTrustAuthority)->SetPolicy(_ppMFOutputPolicy, 1, &pbTicket, &cbTicket);
        IF_FAILED_JUMP(hr, Exit);
        printf("SetPolicy succeeded.\n");

        bRet = true;
        break;

    }// for each output trust authority

Exit:
    if (bRet)
    {
        hr = S_OK;
    }
    if (FAILED(hr))
    {
        printf("failure code is 0x%0x\n", hr);
        SAFE_RELEASE(*ppMFOutputTrustAuthority);
        SAFE_RELEASE(*_ppMFTrustedOutput);
        if (*_ppMFOutputPolicy)
        {
            delete (*_ppMFOutputPolicy);
        }
    }

    return hr;
}


HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy)
{
    SAFE_RELEASE(_pMFOutputTrustAuthority);
    SAFE_RELEASE(_pMFTrustedOutput);
    if (_pMFOutputPolicy)
    {
        delete _pMFOutputPolicy;
    }
    return S_OK;
}
```




```cpp
//OTADSoundSample.rc
#include "windows.h"

/////////////////////////////////////////////////////////////////////////////
// Version
#include <ntverp.h>

#define VER_FILETYPE                VFT_DLL
#define VER_FILESUBTYPE             VFT2_UNKNOWN
#define VER_FILEDESCRIPTION_STR     "Default Device Heuristic Dumper"
#define VER_INTERNALNAME_STR        "DefaultDeviceDump.exe"
#define VER_ORIGINALFILENAME_STR    "DefaultDeviceDump.exe"

#include "common.ver"
```




```cpp
Sources file:

TARGETNAME=OTADSoundSample
TARGETTYPE=PROGRAM
TARGET_DESTINATION=retail
UMTYPE=console
UMENTRY=wmain
UMBASE=0x1000000
#_NT_TARGET_VERSION=$(_NT_TARGET_VERSION_VISTA)
MSC_WARNING_LEVEL=$(MSC_WARNING_LEVEL) /WX
USE_ATL=1
ATL_VER=70
USE_NATIVE_EH=1
USE_MSVCRT=1
C_DEFINES=-DUNICODE -D_UNICODE
INCLUDES=$(INCLUDES);  

SOURCES=OTADSoundSample.cpp \
        OTADSoundSample.rc \
        outputpolicy.cpp\

TARGETLIBS=\
       $(SDK_LIB_PATH)\advapi32.lib         \
       $(SDK_LIB_PATH)\kernel32.lib         \
       $(SDK_LIB_PATH)\User32.lib           \
       $(SDK_LIB_PATH)\shlwapi.lib          \
       $(SDK_LIB_PATH)\ole32.lib            \
       $(SDK_LIB_PATH)\oleaut32.lib         \
       $(SDK_LIB_PATH)\rpcrt4.lib           \
       $(SDK_LIB_PATH)\strmiids.lib         \
       $(SDK_LIB_PATH)\uuid.lib             \
       $(SDK_LIB_PATH)\SetupAPI.lib         \
       $(SDK_LIB_PATH)\mfplat.lib \
```



## <a name="related-topics"></a><span data-ttu-id="55189-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55189-201">Related topics</span></span>

[<span data-ttu-id="55189-202">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="55189-202">Programming Guide</span></span>](programming-guide.md)

[<span data-ttu-id="55189-203">Componentes de audio de modo de usuario</span><span class="sxs-lookup"><span data-stu-id="55189-203">User-Mode Audio Components</span></span>](user-mode-audio-components.md)
