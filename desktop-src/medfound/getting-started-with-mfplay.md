---
description: MFPlay es una API para crear aplicaciones de reproducción multimedia en C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Introducción con MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9e0405d3138a22e0d20e94849d416b29d62945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496799"
---
# <a name="getting-started-with-mfplay"></a>Introducción con MFPlay

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

MFPlay es una API para crear aplicaciones de reproducción multimedia en C++.

Este tema contiene las siguientes secciones:

-   [Requisitos](#requirements)
-   [Acerca de MFPlay](#about-mfplay)
-   [Reproducir un archivo multimedia](#playing-a-media-file)
-   [Controlar la reproducción](#controlling-playback)
-   [Recibir eventos del reproductor](#receiving-events-from-the-player)
-   [Obtención de información acerca de un archivo multimedia](#getting-information-about-a-media-file)
-   [Administrar la reproducción de vídeo](#managing-video-playback)
-   [Limitaciones de MFPlay](#limitations-of-mfplay)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="about-mfplay"></a>Acerca de MFPlay

MFPlay tiene un modelo de programación simple, a la vez que proporciona el conjunto principal de características que necesitan la mayoría de las aplicaciones de reproducción. Una aplicación crea un objeto de *reproductor* que controla la reproducción. Para reproducir un archivo multimedia, el objeto reproductor crea un *elemento multimedia*, que se puede utilizar para obtener información sobre el contenido del archivo multimedia. La aplicación controla la reproducción a través de métodos en la interfaz [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) del objeto Player. Opcionalmente, la aplicación puede obtener notificaciones de eventos a través de una interfaz de devolución de llamada. el siguiente diagrama ilustra este proceso.

![diagrama conceptual: la aplicación y el jugador apuntan entre sí, ambos apuntan al elemento multimedia, que apunta a un archivo multimedia](images/mfplay.png)

## <a name="playing-a-media-file"></a>Reproducir un archivo multimedia

Para reproducir un archivo multimedia, llame a la función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .


```C++
// Global variables
IMFPMediaPlayer *g_pPlayer = NULL;

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

HRESULT PlayVideo(HWND hwnd, const WCHAR* sURL)
{
    // Create the player object and play a video file.

    return MFPCreateMediaPlayer(
        sURL,
        TRUE,   // Start playback automatically?
        0,      // Flags.
        NULL,   // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



La función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) crea una nueva instancia del objeto MFPlay Player. La función toma los parámetros siguientes:

-   El primer parámetro es la dirección URL del archivo que se va a abrir. Puede ser un archivo local o un archivo en un servidor multimedia.
-   El segundo parámetro especifica si la reproducción se inicia automáticamente. Al establecer este valor de parámetros en **true**, el archivo se reproducirá en cuanto MFPlay lo cargue.
-   El tercer parámetro establece varias opciones. Para las opciones predeterminadas, pase cero (0).
-   El cuarto parámetro es un puntero a una interfaz de devolución de llamada opcional. Este parámetro puede ser **null**, como se muestra. La devolución de llamada se describe en la sección [recepción de eventos del reproductor](#receiving-events-from-the-player).
-   El quinto parámetro es un identificador de la ventana de la aplicación. Si el archivo multimedia contiene una secuencia de vídeo, el vídeo aparecerá dentro del área de cliente de esta ventana. Para la reproducción de solo audio, este parámetro puede ser **null**.

El último parámetro recibe un puntero a la interfaz [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) del objeto Player.

Antes de que se cierre la aplicación, asegúrese de liberar el puntero [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) . Puede hacerlo en el controlador de mensajes de **\_ cierre de WM** .


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> En este ejemplo se usa la función [SafeRelease](saferelease.md) para liberar punteros de interfaz.

 

Para una reproducción de vídeo sencilla, todo el código que necesita. En el resto de este tutorial se muestra cómo agregar más características, empezando por el modo de controlar la reproducción.

## <a name="controlling-playback"></a>Controlar la reproducción

El código mostrado en la sección anterior reproducirá el archivo multimedia hasta que llegue al final del archivo. Puede detener e iniciar la reproducción llamando a los métodos siguientes en la interfaz [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) :

-   [**IMFPMediaPlayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pone en pausa la reproducción. Mientras se pausa la reproducción, se muestra el fotograma de vídeo más reciente y el audio es silencioso.
-   [**IMFPMediaPlayer:: Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) detiene la reproducción. No se muestra ningún vídeo y la posición de reproducción se restablece al inicio del archivo.
-   [**IMFPMediaPlayer::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) se reanuda la reproducción después de detenerse o pausarse.

El código siguiente pausa o reanuda la reproducción al presionar la **barra espaciadora**.


```C++
//-------------------------------------------------------------------
// OnKeyDown
//
// Handles the WM_KEYDOWN message.
//-------------------------------------------------------------------

void OnKeyDown(HWND hwnd, UINT vk, BOOL fDown, int cRepeat, UINT flags)
{
    HRESULT hr = S_OK;

    switch (vk)
    {
    case VK_SPACE:

        // Toggle between playback and paused/stopped.
        if (g_pPlayer)
        {
            MFP_MEDIAPLAYER_STATE state = MFP_MEDIAPLAYER_STATE_EMPTY;
            
            g_pPlayer->GetState(&state);

            if (state == MFP_MEDIAPLAYER_STATE_PAUSED ||  
                state == MFP_MEDIAPLAYER_STATE_STOPPED)
            {
                g_pPlayer->Play();
            }
            else if (state == MFP_MEDIAPLAYER_STATE_PLAYING)
            {
                g_pPlayer->Pause();
            }
        }
        break;
    }
}
```



En este ejemplo se llama al método [**IMFPMediaPlayer:: GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) para obtener el estado de reproducción actual (en pausa, detenido o en reproducción) y se pone en pausa o se reanuda en consecuencia.

## <a name="receiving-events-from-the-player"></a>Recibir eventos del reproductor

MFPlay usa una interfaz de devolución de llamada para enviar eventos a la aplicación. Existen dos razones para esta devolución de llamada:

-   La reproducción se produce en un subproceso independiente. Durante la reproducción, pueden producirse ciertos eventos, como alcanzar el final del archivo. MFPlay utiliza la devolución de llamada para notificar a la aplicación el evento.
-   Muchos de los métodos [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) son asincrónicos, lo que significa que devuelven antes de que se complete la operación. Los métodos asincrónicos permiten iniciar una operación desde el subproceso de interfaz de usuario que puede tardar mucho tiempo en completarse, sin que provoque que la interfaz de usuario se bloquee. Una vez finalizada la operación, MFPlay señala la devolución de llamada.

Para recibir notificaciones de devolución de llamada, implemente la interfaz [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . Esta interfaz hereda **IUnknown** y define un método único, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Para configurar la devolución de llamada, pase un puntero a la implementación de **IMFPMediaPlayerCallback** en el parámetro *pCallback* de la función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .

Este es el primer ejemplo de este tutorial, modificado para incluir la devolución de llamada.


```
// Global variables.
IMFPMediaPlayer *g_pPlayer = NULL;
IMFPMediaPlayerCallback *g_pCallback = NULL;

// Call an application-defined function to create the callback object.
hr = CreateMyCallback(&g_pCallback);

// Create the player object and play a video file.

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

if (SUCCEEDED(hr))
{
    hr = MFPCreateMediaPlayer(
        sURL,
        TRUE,        // Start playback automatically?
        0,           // Flags.
        g_pCallback, // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



El método [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) tiene un único parámetro, que es un puntero a la estructura de [**\_ \_ encabezado del evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . El miembro **eEventType** de esta estructura indica qué evento se ha producido. Por ejemplo, cuando se inicia la reproducción, MFPlay envía el evento de **\_ reproducción del \_ tipo \_ de evento MFP** .

Cada tipo de evento tiene una estructura de datos correspondiente que contiene información para ese evento. Cada una de estas estructuras comienza con una estructura de [**\_ \_ encabezado de evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . En la devolución de llamada, convierta el puntero de **\_ \_ encabezado de evento MFP** en la estructura de datos específica del evento. Por ejemplo, si el tipo de evento es el **\_ \_ evento de reproducción de MFP**, la estructura de datos es el [**\_ \_ evento de reproducción de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event). En el código siguiente se muestra cómo controlar este evento en la devolución de llamada.


```
void STDMETHODCALLTYPE MediaPlayerCallback::OnMediaPlayerEvent(
    MFP_EVENT_HEADER *pEventHeader
    )
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY:
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    // Other event types (not shown).

    }
}

// Function to handle the event.
void OnPlay(MFP_PLAY_EVENT *pEvent)
{
    if (FAILED(pEvent->header.hrEvent))
    {  
        // Error occurred during playback.
    }  
}
```



En este ejemplo se usa el evento de [**\_ \_ \_ evento MFP Get Play**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) para convertir el puntero *PEventHeader* en una estructura de [**\_ \_ evento MFP Play**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) . El **valor HRESULT** de la operación que desencadenó el evento se almacena en el campo **hrEvent** de la estructura.

Para obtener una lista de todos los tipos de evento y las estructuras de datos correspondientes, vea [**\_ \_ tipo de evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).

Nota sobre el subprocesamiento: de forma predeterminada, MFPlay invoca la devolución de llamada del mismo subproceso que llamó a [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer). Este subproceso debe tener un bucle de mensajes. Como alternativa, puede pasar la **opción MFP \_ \_ Free \_ threaded \_ callback** Flag en el parámetro *creationOptions* de **MFPCreateMediaPlayer**. Esta marca hace que MFPlay invoque devoluciones de llamada desde un subproceso independiente. Ambas opciones tienen implicaciones en la aplicación. La opción predeterminada significa que la devolución de llamada no puede hacer nada que espere en el bucle de mensajes, como esperar una acción de la interfaz de usuario, porque bloqueará el procedimiento de ventana. La opción de subprocesamiento libre significa que es necesario usar secciones críticas para proteger los datos a los que se tiene acceso en la devolución de llamada. En la mayoría de los casos, la opción predeterminada es más sencilla.

## <a name="getting-information-about-a-media-file"></a>Obtención de información acerca de un archivo multimedia

Al abrir un archivo multimedia en MFPlay, el reproductor crea un objeto denominado *elemento multimedia* que representa el archivo multimedia. Este objeto expone la interfaz [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que puede usar para obtener información sobre el archivo multimedia. Muchas de las estructuras de eventos MFPlay contienen un puntero al elemento multimedia actual. También puede obtener el elemento multimedia actual llamando a [**IMFPMediaPlayer:: GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) en el reproductor.

Dos métodos especialmente útiles son [**IMFPMediaItem:: HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) y [**IMFPMediaItem:: HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio). Estos métodos consultan si el origen multimedia contiene vídeo o audio.

Por ejemplo, el código siguiente comprueba si el archivo multimedia actual contiene una secuencia de vídeo.


```
IMFPMediaItem *pItem;
BOOL bHasVideo = FALSE;
BOOL bIsSelected = FALSE;

hr = g_pPlayer->GetMediaItem(TRUE, &pItem);
if (SUCCEEDED(hr))
{
    hr = pItem->HasVideo(&bHasVideo, &bIsSelected);
    pItem->Release();
}
```



Si el archivo de origen contiene una secuencia de vídeo seleccionada para la reproducción, *bHasVideo* y *bIsSelected* se establecen en **true**.

## <a name="managing-video-playback"></a>Administrar la reproducción de vídeo

Cuando MFPlay reproduce un archivo de vídeo, lo dibuja en la ventana que especificó en la función [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) . Esto sucede en un subproceso independiente propiedad de la canalización de reproducción Microsoft Media Foundation. En su mayor parte, no es necesario que la aplicación administre este proceso. Sin embargo, hay dos situaciones en las que la aplicación debe notificar a MFPlay para actualizar el vídeo.

-   Si la reproducción está en pausa o se detiene, se debe notificar a MFPlay cada vez que la ventana de vídeo de la aplicación recibe un mensaje de dibujo de WM \_ . Esto permite que MFPlay vuelva a dibujar la ventana.
-   Si se cambia el tamaño de la ventana, se debe notificar a MFPlay para que pueda escalar el vídeo para que coincida con el nuevo tamaño de la ventana.

El método [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) controla ambos casos. Llame a este método dentro de los \_ \_ controladores de mensajes de tamaño de WM y de WM para la ventana de vídeo.

> [!IMPORTANT]
> Llame a la función **BeginPaint** de GDI antes de llamar a [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).

 


```
IMFPMediaPlayer *g_pPlayer;   // MFPlay player object

void OnSize(HWND hwnd, UINT state, int cx, int cy)
{
    HDC hdc;
    PAINTSTRUCT ps;

    if (g_pPlayer && (state == SIZE_RESTORED))
    {
        hdc = BeginPaint(hwnd, &ps);
        g_pPlayer->UpdateVideo();
         EndPaint(hwnd, &ps);
    }
}

void OnPaint(HWND hwnd)
{
    HDC hdc;
    PAINTSTRUCT ps;

    hdc = BeginPaint(hwnd, &ps);
    if (g_pPlayer)
    {
        g_pPlayer->UpdateVideo();
    }
      EndPaint(hwnd, &ps);
}
```



A menos que especifique lo contrario, MFPlay muestra el vídeo con la relación de aspecto correcta, mediante el uso de la panorámica si es necesario. Si no desea conservar la relación de aspecto, llame a [**IMFPMediaPlayer:: SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) con la marca **MFVideoARMode \_ None** . Esto hará que MFPlay estire el vídeo para rellenar todo el rectángulo, sin ninguna panorámica. Normalmente, debe usar la configuración predeterminada y dejar que MFPlay la panorámica del vídeo. El color de pantalla ancha predeterminado es negro, pero puede cambiarlo llamando a [**IMFPMediaPlayer:: SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).

## <a name="limitations-of-mfplay"></a>Limitaciones de MFPlay

La versión actual de MFPlay tiene las siguientes limitaciones:

-   MFPlay no admite contenido protegido con DRM.
-   De forma predeterminada, MFPlay no admite protocolos de transmisión por secuencias de red. Para obtener más información, vea [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).
-   MFPlay no admite listas de reproducción del lado servidor (SSPLs) ni otros tipos de origen que reproduzcan más de un segmento. En términos técnicos, MFPlay detiene la reproducción después de la primera presentación y omite cualquier evento [MENewPresentation](menewpresentation.md) del origen de medios.
-   MFPlay no admite transiciones sin problemas entre orígenes de medios.
-   MFPlay no admite la combinación de varias secuencias de vídeo.
-   MFPlay solo admite formatos multimedia compatibles de forma nativa en Media Foundation. (Esto incluye componentes de Media Foundation de terceros que podrían estar instalados en el sistema).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



