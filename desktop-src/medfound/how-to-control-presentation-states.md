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
# <a name="how-to-control-presentation-states"></a>Cómo controlar los Estados de la presentación

La sesión multimedia proporciona control de transporte, como cambiar los Estados de presentación (reproducir, pausar y detener en un escenario de reproducción de estilo de lista de reproducción). En este tema se describen los métodos de sesión multimedia a los que una aplicación debe llamar para cambiar el estado de reproducción.

En la tabla siguiente se muestran las transiciones de estado de presentación válidas.



| Transición de estado | Descripción                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| Reproducir-> pausar | El reloj de la presentación se inmoviliza.                                                            |
| Reproducir-> detener  | El reloj de la presentación se restablece.                                                           |
| Pausar-> reproducir | El reloj de la presentación se reanuda desde el tiempo que se inmovilizó durante la transición de reproducción a pausa. |
| Pausar-> detener | El reloj de la presentación se restablece.                                                           |
| Detener-> reproducir  | El reloj de la presentación comienza desde el principio de la presentación.                      |
| Detener-> pausar | No permitido.                                                                               |



 

## <a name="to-change-presentation-states"></a>Para cambiar los Estados de presentación

-   Llame al método [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) para pausar la reproducción.

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    Antes de llamar a este método, la aplicación debe llamar al método [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) para detectar si el origen de medios admite el estado de pausa. Si lo hace, este método devuelve **MFSESSIONCAP \_ PAUSE** en el parámetro *pdwCaps* .

    Pausar detiene temporalmente la sesión multimedia, el reloj de la presentación y el receptor de la secuencia de la presentación actual. Una vez que la llamada se completa correctamente, la aplicación recibe un evento [MESessionPaused](mesessionpaused.md) .

-   Llame al método [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) para detener la reproducción.

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    Este método detiene la sesión multimedia al detener el origen del medio, los relojes correspondientes y los receptores de la secuencia. Si la sesión multimedia controla el [origen del secuenciador](sequencer-source.md), el origen del secuenciador detiene los orígenes nativos subyacentes. Una vez detenida la sesión multimedia, la aplicación recibe un evento [MESessionStopped](mesessionstopped.md) .

-   Llame al método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar la reproducción o buscar en una nueva posición.

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    Este método inicia la sesión de medios desde los Estados de pausa y detención. La sesión multimedia es responsable de configurar el flujo de datos en la canalización. Este método indica a la sesión de medios que inicie el reloj de la presentación. Después de esta llamada, la sesión multimedia envía un evento [MESessionStarted](mesessionstarted.md) a la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> </dl>

 

 



