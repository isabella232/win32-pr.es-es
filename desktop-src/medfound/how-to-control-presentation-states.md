---
description: Cómo controlar los Estados de la presentación
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Cómo controlar los Estados de la presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696662"
---
# <a name="how-to-control-presentation-states"></a><span data-ttu-id="fc3be-103">Cómo controlar los Estados de la presentación</span><span class="sxs-lookup"><span data-stu-id="fc3be-103">How to Control Presentation States</span></span>

<span data-ttu-id="fc3be-104">La sesión multimedia proporciona control de transporte, como cambiar los Estados de presentación (reproducir, pausar y detener en un escenario de reproducción de estilo de lista de reproducción).</span><span class="sxs-lookup"><span data-stu-id="fc3be-104">The Media Session provides transport control such as changing presentation states (Play, Pause, and Stop in a playlist-style playback scenario).</span></span> <span data-ttu-id="fc3be-105">En este tema se describen los métodos de sesión multimedia a los que una aplicación debe llamar para cambiar el estado de reproducción.</span><span class="sxs-lookup"><span data-stu-id="fc3be-105">This topic describes Media Session methods that an application should call to change the playback state.</span></span>

<span data-ttu-id="fc3be-106">En la tabla siguiente se muestran las transiciones de estado de presentación válidas.</span><span class="sxs-lookup"><span data-stu-id="fc3be-106">The following table shows the valid presentation state transitions.</span></span>



| <span data-ttu-id="fc3be-107">Transición de estado</span><span class="sxs-lookup"><span data-stu-id="fc3be-107">State transition</span></span> | <span data-ttu-id="fc3be-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc3be-108">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3be-109">Reproducir-> pausar</span><span class="sxs-lookup"><span data-stu-id="fc3be-109">Play -> Pause</span></span> | <span data-ttu-id="fc3be-110">El reloj de la presentación se inmoviliza.</span><span class="sxs-lookup"><span data-stu-id="fc3be-110">The presentation clock freezes.</span></span>                                                            |
| <span data-ttu-id="fc3be-111">Reproducir-> detener</span><span class="sxs-lookup"><span data-stu-id="fc3be-111">Play -> Stop</span></span>  | <span data-ttu-id="fc3be-112">El reloj de la presentación se restablece.</span><span class="sxs-lookup"><span data-stu-id="fc3be-112">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="fc3be-113">Pausar-> reproducir</span><span class="sxs-lookup"><span data-stu-id="fc3be-113">Pause -> Play</span></span> | <span data-ttu-id="fc3be-114">El reloj de la presentación se reanuda desde el tiempo que se inmovilizó durante la transición de reproducción a pausa.</span><span class="sxs-lookup"><span data-stu-id="fc3be-114">The presentation clock resumes from the time it froze during the Play to Pause transition.</span></span> |
| <span data-ttu-id="fc3be-115">Pausar-> detener</span><span class="sxs-lookup"><span data-stu-id="fc3be-115">Pause -> Stop</span></span> | <span data-ttu-id="fc3be-116">El reloj de la presentación se restablece.</span><span class="sxs-lookup"><span data-stu-id="fc3be-116">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="fc3be-117">Detener-> reproducir</span><span class="sxs-lookup"><span data-stu-id="fc3be-117">Stop -> Play</span></span>  | <span data-ttu-id="fc3be-118">El reloj de la presentación comienza desde el principio de la presentación.</span><span class="sxs-lookup"><span data-stu-id="fc3be-118">The presentation clock starts from the beginning of the presentation.</span></span>                      |
| <span data-ttu-id="fc3be-119">Detener-> pausar</span><span class="sxs-lookup"><span data-stu-id="fc3be-119">Stop -> Pause</span></span> | <span data-ttu-id="fc3be-120">No permitido.</span><span class="sxs-lookup"><span data-stu-id="fc3be-120">Not allowed.</span></span>                                                                               |



 

## <a name="to-change-presentation-states"></a><span data-ttu-id="fc3be-121">Para cambiar los Estados de presentación</span><span class="sxs-lookup"><span data-stu-id="fc3be-121">To change presentation states</span></span>

-   <span data-ttu-id="fc3be-122">Llame al método [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) para pausar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="fc3be-122">Call the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method to pause playback.</span></span>

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    <span data-ttu-id="fc3be-123">Antes de llamar a este método, la aplicación debe llamar al método [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) para detectar si el origen de medios admite el estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="fc3be-123">Before calling this method, the application must call the [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) method to discover whether the media source supports the Pause state.</span></span> <span data-ttu-id="fc3be-124">Si lo hace, este método devuelve **MFSESSIONCAP \_ PAUSE** en el parámetro *pdwCaps* .</span><span class="sxs-lookup"><span data-stu-id="fc3be-124">If it does, this method returns **MFSESSIONCAP\_PAUSE** in the *pdwCaps* parameter.</span></span>

    <span data-ttu-id="fc3be-125">Pausar detiene temporalmente la sesión multimedia, el reloj de la presentación y el receptor de la secuencia de la presentación actual.</span><span class="sxs-lookup"><span data-stu-id="fc3be-125">Pause temporarily stops the Media Session, the presentation clock, and the stream sink for the current presentation.</span></span> <span data-ttu-id="fc3be-126">Una vez que la llamada se completa correctamente, la aplicación recibe un evento [MESessionPaused](mesessionpaused.md) .</span><span class="sxs-lookup"><span data-stu-id="fc3be-126">After the call completes successfully, the application receives a [MESessionPaused](mesessionpaused.md) event.</span></span>

-   <span data-ttu-id="fc3be-127">Llame al método [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) para detener la reproducción.</span><span class="sxs-lookup"><span data-stu-id="fc3be-127">Call the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method to stop playback.</span></span>

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    <span data-ttu-id="fc3be-128">Este método detiene la sesión multimedia al detener el origen del medio, los relojes correspondientes y los receptores de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fc3be-128">This method stops the Media Session by stopping the media source, the corresponding clocks, and stream sinks.</span></span> <span data-ttu-id="fc3be-129">Si la sesión multimedia controla el [origen del secuenciador](sequencer-source.md), el origen del secuenciador detiene los orígenes nativos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="fc3be-129">If the Media Session is controlling the [Sequencer Source](sequencer-source.md), the underlying native sources are stopped by the sequencer source.</span></span> <span data-ttu-id="fc3be-130">Una vez detenida la sesión multimedia, la aplicación recibe un evento [MESessionStopped](mesessionstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="fc3be-130">After the Media Session is stopped, the application receives a [MESessionStopped](mesessionstopped.md) event.</span></span>

-   <span data-ttu-id="fc3be-131">Llame al método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar la reproducción o buscar en una nueva posición.</span><span class="sxs-lookup"><span data-stu-id="fc3be-131">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method to start playback or seek to a new position.</span></span>

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    <span data-ttu-id="fc3be-132">Este método inicia la sesión de medios desde los Estados de pausa y detención.</span><span class="sxs-lookup"><span data-stu-id="fc3be-132">This method starts the Media Session from Pause and Stop states.</span></span> <span data-ttu-id="fc3be-133">La sesión multimedia es responsable de configurar el flujo de datos en la canalización.</span><span class="sxs-lookup"><span data-stu-id="fc3be-133">The Media Session is responsible for setting up the data flow in the pipeline.</span></span> <span data-ttu-id="fc3be-134">Este método indica a la sesión de medios que inicie el reloj de la presentación.</span><span class="sxs-lookup"><span data-stu-id="fc3be-134">This method instructs the Media Session to start the presentation clock.</span></span> <span data-ttu-id="fc3be-135">Después de esta llamada, la sesión multimedia envía un evento [MESessionStarted](mesessionstarted.md) a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc3be-135">After this call, Media Session sends a [MESessionStarted](mesessionstarted.md) event to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc3be-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc3be-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc3be-137">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="fc3be-137">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



