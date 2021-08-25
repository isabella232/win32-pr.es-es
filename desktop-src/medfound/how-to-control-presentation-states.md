---
description: Cómo controlar los estados de presentación
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Cómo controlar los estados de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2148410527ecf966b10e605bbe4d6beb0ac3d515acd6895e4fc03e73564a72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942425"
---
# <a name="how-to-control-presentation-states"></a>Cómo controlar los estados de presentación

La sesión multimedia proporciona control de transporte, como cambiar los estados de presentación (Reproducir, Pausar y Detener en un escenario de reproducción de estilo de lista de reproducción). En este tema se describen los métodos de sesión multimedia a los que debe llamar una aplicación para cambiar el estado de reproducción.

En la tabla siguiente se muestran las transiciones de estado de presentación válidas.



| Transición de estado | Descripción                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| Reproducir -> pausa | El reloj de presentación se bloquea.                                                            |
| Play -> Stop  | Se restablece el reloj de presentación.                                                           |
| Pausar -> Play | El reloj de presentación se reanuda desde el momento en que se congeló durante la transición reproducir a pausar. |
| Pausar -> Detener | Se restablece el reloj de presentación.                                                           |
| Detener -> Play  | El reloj de presentación comienza desde el principio de la presentación.                      |
| Detener -> pausa | No permitido.                                                                               |



 

## <a name="to-change-presentation-states"></a>Para cambiar los estados de presentación

-   Llame al [**método IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) para pausar la reproducción.

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    Antes de llamar a este método, la aplicación debe llamar al método [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) para detectar si el origen multimedia admite el estado Pause. Si es así, este método devuelve **MFSESSIONCAP \_ PAUSE en** el *parámetro pdwCaps.*

    Pausar detiene temporalmente la sesión multimedia, el reloj de presentación y el receptor de secuencias de la presentación actual. Una vez completada correctamente la llamada, la aplicación recibe un [evento MESessionPaused.](mesessionpaused.md)

-   Llame al [**método IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) para detener la reproducción.

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    Este método detiene la sesión multimedia al detener el origen multimedia, los relojes correspondientes y los receptores de flujo. Si la sesión multimedia controla el origen [del secuenciador](sequencer-source.md), el origen del secuenciador detiene los orígenes nativos subyacentes. Una vez detenida la sesión multimedia, la aplicación recibe un [evento MESessionStopped.](mesessionstopped.md)

-   Llame al [**método IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar la reproducción o buscar en una nueva posición.

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    Este método inicia la sesión multimedia desde los estados Pausar y Detener. La sesión multimedia es responsable de configurar el flujo de datos en la canalización. Este método indica a la sesión multimedia que inicie el reloj de presentación. Después de esta llamada, Media Session envía un [evento MESessionStarted](mesessionstarted.md) a la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> </dl>

 

 



