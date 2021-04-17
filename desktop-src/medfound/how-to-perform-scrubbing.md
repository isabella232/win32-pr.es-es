---
description: Cómo realizar la limpieza
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Cómo realizar la limpieza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543606"
---
# <a name="how-to-perform-scrubbing"></a><span data-ttu-id="545ba-103">Cómo realizar la limpieza</span><span class="sxs-lookup"><span data-stu-id="545ba-103">How to Perform Scrubbing</span></span>

<span data-ttu-id="545ba-104">La limpieza se realiza para buscar de forma instantánea puntos específicos dentro de un archivo interactuando con una representación visual del tiempo, como una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="545ba-104">Scrubbing is performed to instantaneously seek to specific points within a file by interacting with a visual representation of time, such as a scrollbar.</span></span> <span data-ttu-id="545ba-105">En Media Foundation, la limpieza significa buscar en un archivo y obtener un marco actualizado.</span><span class="sxs-lookup"><span data-stu-id="545ba-105">In Media Foundation, scrubbing means seeking on a file and getting one updated frame.</span></span>

<span data-ttu-id="545ba-106">Para obtener información acerca de la limpieza, vea [About Rate Control](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="545ba-106">For information about scrubbing, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-perform-scrubbing"></a><span data-ttu-id="545ba-107">Para realizar la limpieza</span><span class="sxs-lookup"><span data-stu-id="545ba-107">To perform scrubbing</span></span>

1.  <span data-ttu-id="545ba-108">Llame a [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obtener la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) de la [sesión multimedia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="545ba-108">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the [Media Session](media-session.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="545ba-109">No obtenga la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) desde el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="545ba-109">Do not get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the media source.</span></span> <span data-ttu-id="545ba-110">Obtenga siempre la interfaz de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="545ba-110">Always get the interface from the Media Session.</span></span>

     

2.  <span data-ttu-id="545ba-111">Llame a [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para establecer la velocidad de reproducción en cero.</span><span class="sxs-lookup"><span data-stu-id="545ba-111">Call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) to set the playback rate to zero.</span></span> <span data-ttu-id="545ba-112">Para obtener más información sobre cómo llamar a este método, vea [cómo establecer la velocidad de reproducción en la sesión multimedia](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="545ba-112">For more information about calling this method, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>
3.  <span data-ttu-id="545ba-113">Cree una posición de búsqueda en un **PROPVARIANT** especificando el tiempo de presentación que se va a buscar en un tipo de **MFTIME** .</span><span class="sxs-lookup"><span data-stu-id="545ba-113">Create a seek position in a **PROPVARIANT** by specifying the presentation time to seek to in a **MFTIME** type.</span></span>
4.  <span data-ttu-id="545ba-114">Llame a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) con la posición de búsqueda para iniciar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="545ba-114">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the seek position to start playback.</span></span>
5.  <span data-ttu-id="545ba-115">Cuando se completa la operación de limpieza, la sesión multimedia envía un evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="545ba-115">When the scrub operation is complete, the Media Session sends an [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event.</span></span> <span data-ttu-id="545ba-116">Espere a que este evento antes de llamar a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) de nuevo para otra operación de limpieza.</span><span class="sxs-lookup"><span data-stu-id="545ba-116">Wait for this event before calling [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) again for another scrubbing operation.</span></span>

## <a name="example"></a><span data-ttu-id="545ba-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="545ba-117">Example</span></span>

<span data-ttu-id="545ba-118">En el ejemplo de código siguiente se muestra cómo realizar la limpieza.</span><span class="sxs-lookup"><span data-stu-id="545ba-118">The following code example shows how to perform scrubbing.</span></span>


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



<span data-ttu-id="545ba-119">Una operación de limpieza correcta genera el evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) después de que todos los receptores de flujo se actualicen con el nuevo marco y la operación de limpieza se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="545ba-119">A successful scrubbing operation generates the [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event after all the stream sinks are updated with the new frame and the scrubbing operation completes successfully.</span></span> <span data-ttu-id="545ba-120">Al limpiar un archivo de vídeo se muestra el fotograma en el que se ha buscado, pero no se genera una salida de audio.</span><span class="sxs-lookup"><span data-stu-id="545ba-120">Scrubbing a video file displays the frame that was seeked to, but does not generate an audio output.</span></span>

<span data-ttu-id="545ba-121">La aplicación puede realizar la ejecución paso a paso estableciendo la velocidad de reproducción en cero y, a continuación, pasando un **PROPVARIANT** que se establece en **VT \_ vacío** en la llamada a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="545ba-121">The application can perform frame stepping by setting the playback rate to zero and then passing a **PROPVARIANT** that is set to **VT\_EMPTY** in the call to [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

## <a name="related-topics"></a><span data-ttu-id="545ba-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="545ba-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="545ba-123">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="545ba-123">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="545ba-124">Control de tasa</span><span class="sxs-lookup"><span data-stu-id="545ba-124">Rate Control</span></span>](rate-control.md)
</dt> </dl>

 

 



