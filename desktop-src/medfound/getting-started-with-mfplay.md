---
description: MFPlay es una API para crear aplicaciones de reproducción multimedia en C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Tareas iniciales con MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2afb0b20189501530116c252a4d11a9b3e2d8d0dff07482b1998b73400071e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063503"
---
# <a name="getting-started-with-mfplay"></a>Tareas iniciales con MFPlay

\[MFPlay está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. \]

MFPlay es una API para crear aplicaciones de reproducción multimedia en C++.

Este tema contiene las siguientes secciones:

-   [Requisitos](#requirements)
-   [Acerca de MFPlay](#about-mfplay)
-   [Reproducir un archivo multimedia](#playing-a-media-file)
-   [Controlar la reproducción](#controlling-playback)
-   [Recepción de eventos del reproductor](#receiving-events-from-the-player)
-   [Obtener información sobre un archivo multimedia](#getting-information-about-a-media-file)
-   [Administración de la reproducción de vídeo](#managing-video-playback)
-   [Limitaciones de MFPlay](#limitations-of-mfplay)
-   [Temas relacionados](#related-topics)

## <a name="requirements"></a>Requisitos

MFPlay requiere Windows 7.

## <a name="about-mfplay"></a>Acerca de MFPlay

MFPlay tiene un modelo de programación simple, al tiempo que proporciona el conjunto básico de características que la mayoría de las aplicaciones de reproducción necesitan. Una aplicación crea un objeto *player* que controla la reproducción. Para reproducir un archivo multimedia, el objeto de reproductor crea un elemento multimedia *,* que se puede usar para obtener información sobre el contenido del archivo multimedia. La aplicación controla la reproducción a través de métodos en la interfaz [**DESPMediaPlayer del**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) objeto player. Opcionalmente, la aplicación puede obtener notificaciones de eventos a través de una interfaz de devolución de llamada El siguiente diagrama ilustra este proceso.

![diagrama conceptual: la aplicación y el reproductor apuntan entre sí, ambos apuntan al elemento multimedia, que apunta al archivo multimedia](images/mfplay.png)

## <a name="playing-a-media-file"></a>Reproducir un archivo multimedia

Para reproducir un archivo multimedia, llame a la [**función MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)


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



La [**función MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) crea una nueva instancia del objeto de reproductor MFPlay. La función toma los parámetros siguientes:

-   El primer parámetro es la dirección URL del archivo que se va a abrir. Puede ser un archivo local o un archivo en un servidor multimedia.
-   El segundo parámetro especifica si la reproducción se inicia automáticamente. Al establecer este parámetro en **TRUE,** el archivo se reproducirá en cuanto MFPlay lo cargue.
-   El tercer parámetro establece varias opciones. Para las opciones predeterminadas, pase cero (0).
-   El cuarto parámetro es un puntero a una interfaz de devolución de llamada opcional. Este parámetro puede ser **NULL,** como se muestra. La devolución de llamada se describe en la sección [Recepción de eventos del reproductor](#receiving-events-from-the-player).
-   El quinto parámetro es un identificador de la ventana de la aplicación. Si el archivo multimedia contiene una secuencia de vídeo, el vídeo aparecerá dentro del área cliente de esta ventana. Para la reproducción de solo audio, este parámetro puede ser **NULL.**

El último parámetro recibe un puntero a la interfaz [**DESPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) del objeto player.

Antes de que se cierre la aplicación, asegúrese de liberar el puntero [**DE LANPTMediaPlayer.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) Puede hacerlo en el controlador de **mensajes WM \_ CLOSE.**


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> En este ejemplo se usa [la función SafeRelease para](saferelease.md) liberar punteros de interfaz.

 

Para una reproducción de vídeo sencilla, es todo el código que necesita. En el resto de este tutorial se muestra cómo agregar más características, empezando por cómo controlar la reproducción.

## <a name="controlling-playback"></a>Controlar la reproducción

El código que se muestra en la sección anterior reproducirá el archivo multimedia hasta que llegue al final del archivo. Puede detener e iniciar la reproducción llamando a los métodos siguientes en la interfaz [**DEPMediaPlayer:**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)

-   [**IMFPMediaPlayer::P ause pausa**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) la reproducción. Mientras la reproducción está en pausa, se muestra el fotograma de vídeo más reciente y el audio es silencioso.
-   [**IMFPMediaPlayer::Stop detiene la**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) reproducción. No se muestra ningún vídeo y la posición de reproducción se restablece al inicio del archivo.
-   [**IMFPMediaPlayer::P lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) reanuda la reproducción después de detener o pausar.

El código siguiente pausa o reanuda la reproducción al presionar la **BARRA ESPACIADORA**.


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



En este ejemplo se llama al método [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) para obtener el estado de reproducción actual (en pausa, detenido o en reproducción) y se pausa o se reanuda en consecuencia.

## <a name="receiving-events-from-the-player"></a>Recepción de eventos del reproductor

MFPlay usa una interfaz de devolución de llamada para enviar eventos a la aplicación. Hay dos razones para esta devolución de llamada:

-   La reproducción se produce en un subproceso independiente. Durante la reproducción, pueden producirse determinados eventos, como llegar al final del archivo. MFPlay usa la devolución de llamada para notificar a la aplicación del evento.
-   Muchos de los [**métodos DEPTPMediaPlayer son**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) asincrónicos, lo que significa que devuelven antes de que se complete la operación. Los métodos asincrónicos permiten iniciar una operación desde el subproceso de interfaz de usuario que puede tardar mucho tiempo en completarse, sin que esto provoco que la interfaz de usuario se bloquee. Una vez completada la operación, MFPlay señala la devolución de llamada.

Para recibir notificaciones de devolución de llamada, implemente [**la interfaz IMFPMediaPlayerCallback.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) Esta interfaz hereda **IUnknown y** define un único método, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Para configurar la devolución de llamada, pase un puntero a la implementación **de IMFPMediaPlayerCallback** en el *parámetro pCallback* de la [**función MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)

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



El [**método OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) tiene un único parámetro, que es un puntero a la [**estructura EVENT HEADER \_ \_ de MFP.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) El **miembro eEventType** de esta estructura indica qué evento se ha producido. Por ejemplo, cuando se inicia la reproducción, MFPlay envía el **evento \_ MFP EVENT \_ TYPE \_ PLAY.**

Cada tipo de evento tiene una estructura de datos correspondiente que contiene información para ese evento. Cada una de estas estructuras comienza con una [**estructura \_ EVENT HEADER \_ de MFP.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) En la devolución de llamada, convierte el **puntero \_ EVENT HEADER \_ de MFP** a la estructura de datos específica del evento. Por ejemplo, si el tipo de evento es **MFP \_ PLAY \_ EVENT**, la estructura de datos es [**MFP \_ PLAY \_ EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event). El código siguiente muestra cómo controlar este evento en la devolución de llamada.


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



En este ejemplo se usa el [**evento \_ GET PLAY \_ \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) de MFP para convertir el *puntero pEventHeader* a una [**estructura MFP PLAY \_ \_ EVENT.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) El **valor HRESULT** de la operación que desencadenó el evento se almacena en el **campo hrEvent** de la estructura .

Para obtener una lista de todos los tipos de eventos y las estructuras de datos correspondientes, vea [**MFP \_ EVENT \_ TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).

Nota sobre el subprocesamiento: de forma predeterminada, MFPlay invoca la devolución de llamada del mismo subproceso que llamó [**a MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer). Este subproceso debe tener un bucle de mensajes. Como alternativa, puede pasar la marca DE DEVOLUCIÓN DE LLAMADA FREE **\_ \_ \_ \_ THREADED** DE MFP OPTION en el parámetro *creationOptions* **de MFPCreateMediaPlayer**. Esta marca hace que MFPlay invoque devoluciones de llamada desde un subproceso independiente. Cualquiera de las opciones tiene implicaciones para la aplicación. La opción predeterminada significa que la devolución de llamada no puede hacer nada que espere en el bucle de mensajes, como esperar una acción de interfaz de usuario, porque eso bloqueará el procedimiento de la ventana. La opción de subproceso libre significa que debe usar secciones críticas para proteger los datos a los que tiene acceso en la devolución de llamada. En la mayoría de los casos, la opción predeterminada es más sencilla.

## <a name="getting-information-about-a-media-file"></a>Obtener información sobre un archivo multimedia

Al abrir un archivo multimedia en MFPlay, el reproductor crea un objeto denominado elemento *multimedia* que representa el archivo multimedia. Este objeto expone la interfaz [**IMFPMediaItem,**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) que puede usar para obtener información sobre el archivo multimedia. Muchas de las estructuras de eventos MFPlay contienen un puntero al elemento multimedia actual. También puede obtener el elemento multimedia actual mediante una llamada [**a IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) en el reproductor.

Dos métodos especialmente útiles [**son IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) y [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio). Estos métodos consultan si el origen multimedia contiene vídeo o audio.

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



Si el archivo de origen contiene una secuencia de vídeo seleccionada para la reproducción, *bHasVideo* y *bIsSelected* se establecen en **TRUE.**

## <a name="managing-video-playback"></a>Administración de la reproducción de vídeo

Cuando MFPlay reproduce un archivo de vídeo, dibuja el vídeo en la ventana que especificó en la [**función MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) Esto sucede en un subproceso independiente que pertenece a la canalización de Microsoft Media Foundation reproducción. En su mayor parte, la aplicación no necesita administrar este proceso. Sin embargo, hay dos situaciones en las que la aplicación debe notificar a MFPlay que actualice el vídeo.

-   Si la reproducción está en pausa o detenida, se debe notificar a MFPlay cada vez que la ventana de vídeo de la aplicación recibe un mensaje WM \_ PAINT. Esto permite a MFPlay volver a dibujar la ventana.
-   Si se cambia el tamaño de la ventana, se debe notificar a MFPlay para que pueda escalar el vídeo para que coincida con el nuevo tamaño de la ventana.

El [**método IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) controla ambos casos. Llame a este método dentro de los controladores de mensajes WM PAINT y \_ WM SIZE para la ventana de \_ vídeo.

> [!IMPORTANT]
> Llame a la función **BeginPaint de** GDI antes de llamar [**a UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).

 


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



A menos que especifique lo contrario, MFPlay muestra el vídeo con la relación de aspecto correcta, mediante la conversión de letras si es necesario. Si no desea conservar la relación de aspecto, llame a [**MFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) con la marca **MFVideoARMode \_ None.** Esto hará que MFPlay es mejore el vídeo para rellenar todo el rectángulo, sin necesidad de usar el cuadro de texto. Normalmente, debe usar la configuración predeterminada y dejar que MFPlay cree una caja de texto en el vídeo. El color predeterminado del cuadro de letras es negro, pero puede cambiarlo llamando a [**ALFMEDIAPlayer::SetBorderColor.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor)

## <a name="limitations-of-mfplay"></a>Limitaciones de MFPlay

La versión actual de MFPlay tiene las siguientes limitaciones:

-   MFPlay no admite contenido protegido por DRM.
-   De forma predeterminada, MFPlay no admite protocolos de streaming de red. Para obtener más información, [**vea IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).
-   MFPlay no admite listas de reproducción del lado servidor (SSPL) u otros tipos de origen que reproducen más de un segmento. En términos técnicos, MFPlay detiene la reproducción después de la primera presentación y omite los eventos [MENewPresentation](menewpresentation.md) del origen multimedia.
-   MFPlay no admite transiciones perfectas entre orígenes multimedia.
-   MFPlay no admite la combinación de varias secuencias de vídeo.
-   MFPlay solo admite los formatos multimedia Media Foundation de forma nativa. (Esto incluye componentes de Media Foundation de terceros que podrían estar instalados en el sistema).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



