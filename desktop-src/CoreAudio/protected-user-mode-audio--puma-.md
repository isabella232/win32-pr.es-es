---
description: Windows Vista introdujo el audio en modo de usuario protegido (PEM), el motor de audio en modo de usuario en el entorno protegido (PE) que proporciona un entorno más seguro para el procesamiento y la representación de audio.
ms.assetid: 27a50026-9e48-48b1-9249-7528a97333c9
title: Audio en modo de usuario protegido (IAM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f119094440297c90ae67c46d5a6b39b1ba6e2e9931b43b4bdda17393d0273dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077459"
---
# <a name="protected-user-mode-audio-puma"></a>Audio en modo de usuario protegido (IAM)

Windows Vista introdujo el audio en modo de usuario protegido (PEM), el motor de audio en modo de usuario en el entorno protegido (PE) que proporciona un entorno más seguro para el procesamiento y la representación de audio. Permite habilitar solo las salidas de audio aceptables y garantiza que las salidas se deshabilitan de forma confiable. Para obtener más información acerca de LA... , [vea Output Content Protection and Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).

SE HA ACTUALIZADO PARA WINDOWS 7 para proporcionar las siguientes características:

-   Establecer bits del Sistema de administración de copia en serie (SCMS) en puntos de conexión S/PDIF y bits de Content Protection digital de ancho de banda alto (HDCP) en puntos de conexión de la interfaz multimedia de High-Definition (HDMI).
-   Habilitación de controles de protección SCMS y HDMI fuera de un entorno protegido (PE).

## <a name="drm-protection-in-audio-drivers"></a>Protección DRM en controladores de audio

Digital Rights Management (DRM) proporciona la capacidad de empaquetar datos multimedia en un contenedor seguro y adjuntar reglas de uso al contenido. Por ejemplo, el proveedor  de contenido podría usar la protección de copia o la deshabilitación de salida **digital** para deshabilitar las copias digitales directas o la transmisión fuera del sistema de PC.

La pila de audio de determinados productos de Microsoft admite DRM mediante la implementación de las reglas de uso que rigen la reproducción del contenido de audio. Para reproducir el contenido protegido, el controlador de audio subyacente debe ser un *controlador de confianza*; Es decir, el controlador debe estar certificado con el logotipo para DRMLevel 1300. Para obtener información sobre el desarrollo de controladores de confianza, puede usar interfaces definidas en el Kit de desarrollo de controladores de Windows 2000 ("DDK") o posterior. Los controladores desarrollados con DDK implementarán las interfaces necesarias para DRM. Para obtener más información, vea [Digital Rights Management](/windows-hardware/drivers/audio/digital-rights-management).

Para representar el contenido protegido, el  controlador de confianza debe comprobar si la protección de copia y la deshabilitación de salida **digital** están establecidas en el contenido que fluye a través de la pila de audio y responder a la configuración en consecuencia.

### <a name="copy-protection-rule"></a>Regla de protección de copia

**La protección contra** copia indica que no se permiten copias digitales directas en el sistema. La prueba B del acuerdo de pruebas de WHQL se ha actualizado para reflejar las nuevas expectativas y requisitos de un controlador cuando **se** establece la protección de copia en el contenido. Para Windows 7, el controlador de clase de audio HD integrado cumple los requisitos más recientes.

Además de asegurarse de que el contenido no puede pasar a otro componente o almacenarse en cualquier medio de almacenamiento no  volátil que no esté autenticado por el sistema DRM, el controlador de audio realiza las siguientes tareas cuando se establece la protección de copia:

-   El controlador habilita HDCP en los puntos de conexión de HDMI.
-   Para las interfaces S/PDIF, el controlador valida que la combinación de bits L, Cp y Código de categoría indica un estado SCMS de "Copiar nunca", tal como se define en IEC 60958.
-   El bit L se establece en 0 y el código de categoría se establece en "Digital Signal Mixer".

La **estructura DRMRIGHTS,** que usan los controladores de audio de confianza, especifica los derechos de contenido drm asignados a un pin de audio KS o al objeto de secuencia de un controlador de clase de puerto. El **miembro CopyProtect** indica si la **protección de copia** está establecida en el contenido de audio.

Para Windows 7, el uso de **CopyProtect** es más estricto. El controlador garantiza que los controles de protección se establecen en las interfaces de audio, HDCP se establece para la salida HDMI y SCMS se establece para la salida S/PDIF estableciendo el estado en "Copiar nunca".

### <a name="digital-output-disable-rule"></a>Regla de deshabilitación de salida digital

**Digital Output Disable** indica que el contenido no se puede transmitir fuera del sistema. En Windows 7, el controlador de clase de audio HD integrado responde a esta configuración habilitando HDCP en puntos de conexión HDMI. Esto es similar a la respuesta del controlador a la configuración **de protección de** copia.

## <a name="enabling-content-protection-mechanisms-outside-of-a-protected-environment"></a>Habilitar mecanismos de protección de contenido fuera de un entorno protegido

RESIDE en un proceso independiente en el entorno protegido (PE). En Windows Vista, para usar los controles de protección de contenido de audio ofrecidos por PEM, una aplicación multimedia debe estar en un PE. Dado que Media Foundation API pueden interactuar con un PE, los controles de protección de contenido se limitan a las aplicaciones que usan Media Foundation API para transmitir contenido de audio.

En Windows 7, cualquier aplicación puede tener acceso a los controles de protección de contenido proporcionados por la autoridad de confianza de salida (OTA) de KPI, independientemente de si están en un PE o mediante las API de Media Foundation para la reproducción de audio.

## <a name="implementation-instructions"></a>Instrucciones de implementación

Los pasos siguientes son necesarios para que una aplicación de audio controle la protección de contenido de SCMS o HDCP en un punto de conexión de audio. Las API de audio admitidas DirectShow, DirectSound y WASAPI.

Este código de ejemplo usa las interfaces siguientes.

-   [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)
-   [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
-   [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)
-   [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)

La aplicación multimedia debe realizar las siguientes tareas.

1.  Configure el entorno de desarrollo.
    -   Haga referencia a las interfaces necesarias e incluya los encabezados que se muestran en el código siguiente.
        ```cpp
        #include <MMdeviceapi.h>        // Device endpoint definitions
        #include <Mfidl.h>              // OTA interface definitions
        ```

        

    -   Vínculo a Mfuuid.lib para usar las interfaces OTA.
    -   Deshabilite el depurador del kernel y el comprobador de controladores para evitar errores de comprobación de autenticación.
2.  Enumere todos los puntos de conexión del sistema y seleccione el punto de conexión de destino de la colección de puntos de conexión, como se muestra en el código siguiente. Para obtener más información sobre la enumeración de dispositivos, [vea Enumerar dispositivos de audio.](/previous-versions//ms678716(v=vs.85))
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

    

3.  Use el [**puntero IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) al punto de conexión devuelto por el proceso de enumeración para activar la API de streaming de audio deseada y prepararse para el streaming. Las distintas API de audio requieren una preparación ligeramente diferente.
    -   Para DShow audio applications (Mostrar aplicaciones de audio):
        1.  Cree un DirectShow COM llamando a [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) y especificando \_ IID IBaseFilter como identificador de interfaz.
            ```cpp
            IUnknown *pDShowFilter = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IBaseFilter,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDShowFilter));
            ```

            

        2.  Cree un DirectShow de filtro con este objeto COM activado por el dispositivo. Para obtener más información sobre este proceso, consulte "Building the Filter Graph" (Creación del filtro DirectShow sdk).
    -   Para las aplicaciones de audio D Sound:
        1.  Cree un objeto COM DSound llamando a [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) y especificando \_ IID IDirectSound8 como identificador de interfaz.
            ```cpp
            IDirectSound8  *pDSSound8;
            ...
            hr = pDevice->Activate (
                              IID_IDirectSound8,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDSSound8));
            ```

            

        2.  Use el objeto DSound creado anteriormente para programar DSound para el consumo de agua. Para obtener más información sobre este proceso, [vea DirectSound](/previous-versions//bb219818(v=vs.85)) en MSDN.
    -   Para WASAPI:
        1.  Cree un objeto COM [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) llamando a [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) y especificando \_ IID IAudioClient como identificador de interfaz.
            ```cpp
            IAudioClient *pIAudioClient = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IAudioClient,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pIAudioClient));
            ```

            

        2.  Abra la secuencia de audio.
            ```cpp
            hr = pIAudioClient->Initialize(...);
            ```

            
4.  Inicie el streaming de audio.
5.  Establezca la directiva de protección en la secuencia.
    1.  Para los clientes WASAPI, obtenga una referencia a la interfaz [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) del objeto de autoridad de confianza de salida (OTA) para la secuencia llamando a [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) y especificando IID IMFTrustedOutput como identificador de \_ interfaz.
        ```cpp
        IMFTrustedOutput*       pTrustedOutput = NULL;
        hr = pIAudioClient>GetService(
                       __uuidof(IMFTrustedOutput),
                       (void**)& pTrustedOutput);
        ```

        

    2.  Obtenga un recuento de los objetos OTA disponibles mediante una llamada a [**IMFTrustedOutput::GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).
        ```cpp
        hr = pTrustedOutput->GetOutputTrustAuthorityCount(&m_dwCountOTA);
        ```

        

    3.  Enumerar la colección OTA y obtener una referencia al objeto OTA que admite la acción PEACTION \_ PLAY. Todas las OTA exponen [**la interfaz IMFOutputTrustAuthority.**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority)
        ```cpp
        hr = pMFTrustedOutput->GetOutputTrustAuthorityByIndex(I, &pMFOutputTrustAuthority);
        hr = pMFOutputTrustAuthority->GetAction(&action) 
        ```

        

    4.  Use la [**interfaz IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) para establecer la directiva de protección en la secuencia.

        ```cpp
        hr = pTrustedOutput ->SetPolicy(&pPolicy, nPolicy, &pbTicket, &cbTicket);
        ```

        

        > [!Note]
        > Si usa evr, [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) genera el evento [MEPolicySet](../medfound/mepolicyset.md) y devuelve MF S WAIT FOR POLICY SET para indicar que el OTA aplicará la directiva de forma \_ \_ \_ \_ \_ asincrónica. Sin embargo, en este código de ejemplo, la aplicación es un cliente WASAPI directo que recuperó el objeto OTA del cliente de audio (paso 5 a). A diferencia de EVR, un cliente de audio y otros objetos WASAPI no implementan generadores de eventos multimedia. Sin los generadores de eventos multimedia, **MFTrustedOutput::SetPolicy** no devuelve MF \_ S WAIT FOR POLICY \_ \_ \_ \_ SET.
        >
        > La configuración de la directiva de audio debe establecerse después de que se inicie el streaming de audio; de lo contrario, SE PRODUCE un error [**en LAPÓSTERTrustedOutput::GetOutputTrustAuthorityByIndex.**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) Además, para admitir esta característica, el controlador de audio subyacente debe ser un *controlador de confianza.*

         

        En el código de ejemplo, *pPolicy* es un puntero a la interfaz [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) de un objeto de directiva implementado por el cliente. Para más información, consulte la [documentación Media Foundation SDK.](../medfound/microsoft-media-foundation-sdk.md)

        En la implementación del método [**IMFOutputPolicy::GenerateRequiredSchemas,**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) se debe generar una colección de los sistemas de protección de salida (esquemas) que el OTA debe aplicar. Cada esquema se identifica mediante un GUID y contiene datos de configuración para el sistema de protección. Asegúrese de que los sistemas de protección de la colección están restringidos al uso de controladores de audio de confianza. Esta restricción se identifica mediante el GUID, **MFPROTECTION \_ TRUSTEDAUDIODRIVERS**, DISABLE o CONSTRICTAUDIO. Si se usa MFPROTECTION \_ TRUSTEDAUDIODRIVERS, los datos de configuración de este esquema son DWORD. Para obtener más información sobre los esquemas y los datos de configuración relacionados, consulte la documentación del SDK del entorno protegido.

        El cliente también debe proporcionar la definición de esquema mediante la implementación de la [**interfaz IMFOutputSchema.**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) [**MFOutputSchema::GetSchemaType recupera**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) **MFPROTECTION \_ TRUSTEDAUDIODRIVERS como** GUID del esquema. [**IMFOutputSchema::GetConfigurationData devuelve**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) un puntero a los datos de configuración del esquema.

6.  Continuar el streaming de audio.
7.  Asegúrese de que la directiva de protección está clara antes de detener el streaming.

    Libere las referencias de interfaz de directiva relacionadas anteriores.

    Las llamadas de versión borran la configuración de directiva establecida anteriormente.

    > [!Note]  
    > Cada vez que se reinicia una secuencia, la directiva de protección debe establecerse de nuevo en la secuencia. El procedimiento se describe en el paso 5-d.

    ```cpp
    pMFOutputTrustAuthority->Release()
    pMFTrustedOutput->Release()
    ```
  

En los ejemplos de código siguientes se muestra una implementación de ejemplo de los objetos de esquema y directiva.


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



## <a name="related-topics"></a>Temas relacionados

[Guía de programación](programming-guide.md)

[Componentes de audio en modo de usuario](user-mode-audio-components.md)
