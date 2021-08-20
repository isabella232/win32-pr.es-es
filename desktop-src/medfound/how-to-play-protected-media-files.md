---
description: Cómo reproducir archivos que contienen medios protegidos con DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Cómo reproducir archivos multimedia protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20a2b525f8acc3a602bcaae2630726d01269881beec07ac214f4d0bd02ee1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942345"
---
# <a name="how-to-play-protected-media-files"></a>Cómo reproducir archivos multimedia protegidos

Un archivo multimedia protegido es cualquier archivo multimedia que tenga reglas asociadas para usar el contenido. En algunos casos, un archivo multimedia protegido se cifra mediante algún tipo de cifrado de administración de derechos digitales (DRM). Para reproducir un archivo multimedia protegido, la reproducción debe realizarse dentro de la ruta de acceso multimedia protegida (PMP). Además, es posible que el usuario tenga que adquirir derechos sobre el contenido.

El término adquisición de derechos hace referencia a cualquier acción que la aplicación debe realizar antes de que el usuario pueda reproducir el contenido. El ejemplo más común es obtener una licencia DRM, pero Media Foundation define un mecanismo genérico que puede admitir otros tipos de adquisición de derechos. La [**interfaz IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) define este mecanismo genérico.

La adquisición de derechos debe realizarse fuera del PMP, desde el proceso de aplicación. La sesión multimedia notifica a la aplicación a través de [**la interfaz IMFContentProtectionManager,**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) que implementa la aplicación. La sesión multimedia usa la **interfaz IMFContentProtectionManager** para reenviar un objeto habilitador de contenido a la aplicación. Los habilitadores de contenido implementan [**la interfaz IMFContentEnabler.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) La aplicación usa esta interfaz para adquirir los derechos necesarios.

Un habilitador de contenido podría admitir la adquisición automática de derechos, en cuyo caso el habilitador de contenido implementa todo el proceso y la aplicación simplemente supervisa el estado. De lo contrario, la aplicación debe usar la adquisición de derechos no silenciosos, que es un proceso en el que la aplicación envía datos HTTP POST a una dirección URL proporcionada por el habilitador de contenido.

Para reproducir medios protegidos, una aplicación sigue los mismos pasos que se indican en el tema [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), con los siguientes pasos adicionales:

1.  Consulta si el origen multimedia contiene contenido protegido. (Opcional).
2.  Cree la sesión multimedia en el proceso PMP, en lugar del proceso de aplicación.
3.  Realice la adquisición de derechos, si la sesión multimedia le notifica que lo haga. La aplicación realiza esta operación de forma asincrónica.
4.  Complete la operación asincrónica.

## <a name="query-for-protected-content"></a>Consulta de contenido protegido

Para consultar si un origen multimedia contiene contenido protegido, llame a la función [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) en el descriptor de presentación del origen multimedia. Si la función devuelve S \_ OK, debe usar el PMP para reproducir el contenido. Si la función devuelve S \_ FALSE, el PMP no es necesario y puede crear la sesión multimedia en el proceso de aplicación. Como alternativa, puede usar el PMP para reproducir ambos tipos de contenido, protegidos y desprotegidos. Si lo hace, no es necesario llamar a **MFRequireProtectedEnvironment**.

Para obtener más información sobre los descriptores de presentación, vea [Descriptores de presentación](presentation-descriptors.md).

## <a name="create-the-pmp-media-session"></a>Creación de la sesión multimedia de PMP

Para crear la sesión multimedia en el PMP, llame a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Esta función es similar a [**MFCreateMediaSession,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)pero en lugar de crear la sesión multimedia en el proceso de la aplicación, crea la sesión multimedia en el proceso PMP. La aplicación recibe un puntero a un objeto proxy para la sesión multimedia. La aplicación llama [**a los métodos IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) en el objeto proxy, tal como lo haría en la sesión multimedia. El objeto proxy reenvía las llamadas a la sesión multimedia a través del límite del proceso.

Cree la sesión de medios PMP como se muestra a continuación:

1.  Cree un nuevo almacén de atributos mediante una [**llamada a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Establezca el [**atributo MF SESSION CONTENT PROTECTION \_ \_ \_ \_ MANAGER**](mf-session-content-protection-manager-attribute.md) en el almacén de atributos. El valor de este atributo es un puntero a la implementación de LA APLICACIÓN de [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager). Llame [**a IMFAttributes::SetUnknown para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) establecer el atributo.
3.  Llame [**a MFCreatePMPMediaSession para**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) crear la sesión multimedia en el proceso PMP. El *parámetro pConfiguration* es un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) del almacén de atributos.


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



A continuación, cree una topología de reproducción y ponerla en cola en la sesión multimedia, como se describe en [Creación de topologías de reproducción.](creating-playback-topologies.md)

## <a name="perform-rights-acquisition"></a>Realización de la adquisición de derechos

Si la reproducción requiere la adquisición de derechos, la sesión multimedia llama [**a IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). El *parámetro pEnablerActivate de* este método es un puntero a la interfaz [**IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Use esta interfaz para crear el objeto de habilitador de contenido, que expone la [**interfaz IMFContentEnabler.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) A continuación, use el habilitador de contenido para realizar el paso de adquisición de derechos.

Para crear el habilitador de contenido, llame [**a IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



Consulte el puntero [**DESCONTENTENABLER devuelto**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para la [**interfaz IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Use esta interfaz para obtener eventos del objeto habilitador de contenido. Para obtener más información sobre los eventos, vea [Generadores de eventos multimedia](media-event-generators.md).

Para averiguar si el habilitador de contenido admite la adquisición automática, llame a [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported). Si este método devuelve el valor **TRUE**, la aplicación debe usar la adquisición automática. De lo contrario, use la adquisición no silenciosa.

El [**método BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) es asincrónico. La aplicación debe realizar el paso de adquisición en el subproceso de la aplicación. Un enfoque es publicar un mensaje de ventana privada en la ventana principal de la aplicación y notificar al subproceso de la aplicación que realice la adquisición. Mientras la operación está pendiente, la aplicación debe almacenar el puntero de devolución de llamada y el objeto de estado que recibió en los parámetros *pCallback* *ystate* de **BeginEnableContent**. Se usarán para completar la operación asincrónica.

### <a name="automatic-acquisition"></a>Adquisición automática

Para realizar la adquisición automática, llame [**a IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable). Este método es asincrónico. Cuando se completa la operación, el habilitador de contenido envía un [evento MEEnablerCompleted.](meenablercompleted.md) El código de estado del evento indica si la operación se ha realizado correctamente. Si el código de estado del evento MEEnablerCompleted es NS \_ E \_ DRM LICENSE \_ NOTACQUIRED, la aplicación debe intentar usar la adquisición no \_ silenciosa.

Mientras la operación de adquisición está en curso, el objeto habilitador podría enviar el evento [MEEnablerProgress](meenablerprogress.md) para indicar el progreso de la operación. Para cancelar la operación, llame [**a IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).

### <a name="non-silent-acquisition"></a>Adquisición no silenciosa

Si el método [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) devuelve **FALSE** o el método [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) produce un error con el código de error NS \_ E DRM LICENSE \_ \_ NOTACQUIRED, la aplicación debe realizar una adquisición no silenciosa como se describe en los pasos \_ siguientes:

1.  Llame [**a IMFContentEnabler::GetEnableURL para**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) obtener la dirección URL de la adquisición de derechos. Este método también devuelve una marca que indica si la dirección URL es de confianza.
2.  Llame [**a IMFContentEnabler::GetEnableData para**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) obtener los datos HTTP POST.
3.  Llame [**a IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable). Este método hace que el habilitador de contenido supervise el progreso de la acción de adquisición de derechos.

4.  Envíe los datos a la dirección URL de adquisición de derechos mediante una acción HTTP POST. Puede usar el control Internet Explorer o las API Windows Internet (WinINet).

En el código siguiente se muestran los pasos 1 a 3. El paso 4 depende de los requisitos concretos de la aplicación.


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



Cuando se completa la operación, el habilitador de contenido envía un [evento MEEnablerCompleted.](meenablercompleted.md)

## <a name="complete-the-asynchronous-operation"></a>Completar la operación asincrónica

Cuando se completa la adquisición de derechos, correctamente o de otro modo, la aplicación debe notificar a la sesión multimedia, invocando el puntero de devolución de llamada dado en el [**método BeginEnableContent.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)

1.  Cree un objeto de resultado asincrónico mediante una [**llamada a MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).
2.  Invoque la devolución de llamada de la sesión multimedia llamando [**a MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).
3.  La sesión multimedia llamará [**a IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent). En la implementación de este método, libere los punteros o recursos que asignó dentro [**de BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Devuelve un **valor HRESULT** que indica el éxito general de la operación. Si se produjo un error en la adquisición de derechos o el usuario canceló antes de que se completara, devuelva un código de error.

El código siguiente muestra cómo crear el resultado asincrónico e invocar la devolución de llamada.


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> </dl>

 

 



