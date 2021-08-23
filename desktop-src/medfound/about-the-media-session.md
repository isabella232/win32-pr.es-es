---
description: Acerca de la sesión multimedia
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Acerca de la sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68816f4c9b9468de2e687a7d00087c5232cc5d24509c9166c5f04c7c0370f6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035643"
---
# <a name="about-the-media-session"></a>Acerca de la sesión multimedia

La sesión multimedia expone la [**interfaz IMFMediaSession.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) Hay dos maneras de crear la sesión multimedia, en función de si la aplicación admitirá contenido protegido:

-   Si la aplicación no admite contenido protegido, puede crear la sesión multimedia llamando a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession). Esta función crea la sesión multimedia dentro del proceso de aplicación.
-   Para admitir contenido protegido, cree la sesión multimedia mediante una llamada [**a MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Esta función crea la sesión multimedia dentro del proceso de ruta de acceso multimedia protegida (PMP). La aplicación recibe un puntero a un objeto proxy que serializa las llamadas de método a través del límite del proceso. Tenga en cuenta que la sesión multimedia de PMP se puede usar para reproducir contenido claro, así como contenido protegido.

Cualquier aplicación que use la sesión multimedia seguirá estos pasos generales:

1.  Cree una topología.
2.  Poner en cola la topología en la sesión multimedia llamando [**a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).
3.  Para controlar el flujo de datos, llame a [**IMFMediaSession::Start,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) [**IMFMediaSession::P ause o**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) [**ASEMEDIASESSION::Stop.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)
4.  Antes de que se cierre la aplicación, llame [**a IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la sesión multimedia.
5.  Apague los orígenes de medios creados por la aplicación mediante una llamada [**a IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
6.  Apague la sesión de medios mediante una llamada [**a IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

Cuando se usa la sesión multimedia, la aplicación no debe iniciar, pausar ni detener directamente el origen multimedia. Todos los cambios de estado deben iniciarse mediante una llamada a [**los métodos DE LANMEDIASESSION.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) La sesión multimedia controla los cambios de estado en el origen de medios.

Muchos otros detalles dependerán de la funcionalidad específica de la aplicación.

## <a name="protected-content"></a>Contenido protegido

Para reproducir contenido protegido, debe crear la sesión multimedia dentro de la ruta de acceso multimedia protegida (PMP), llamando a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Esta función crea una instancia de la sesión multimedia dentro del PMP y devuelve un puntero a un objeto proxy que serializa las interfaces a través del límite del proceso.

En la mayoría de los aspectos, el uso de la sesión multimedia dentro del PMP es transparente para la aplicación. Sin embargo, es posible que la aplicación tenga que invocar determinadas acciones que permiten al usuario reproducir el contenido. Por ejemplo, es posible que el usuario tenga que obtener una licencia DRM. Media Foundation define un mecanismo genérico para estas acciones mediante la [**interfaz IMFContentEnabler.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)

Para obtener más información, vea los temas siguientes:

-   [Ruta de acceso de medios protegidos](protected-media-path.md)
-   [Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>Reloj de presentación

La sesión multimedia administra todos los aspectos del reloj de presentación:

-   Crear el reloj de presentación.

-   Seleccionar el origen de la hora.

-   Notificación a los receptores de medios sobre el reloj

-   Iniciar, detener y pausar el reloj según sea necesario.

-   Apagar el reloj.

Para obtener un puntero al reloj de presentación, llame [**a IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) en la sesión multimedia. El reloj de presentación no devuelve una hora válida hasta que la sesión multimedia envía el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con la marca MF \_ TOPOSTATUS \_ READY. Hasta entonces, **GetClock devuelve** MF \_ E CLOCK NO TIME \_ \_ \_ \_ SOURCE.

Una aplicación que usa la sesión multimedia nunca debe iniciar, detener ni pausar el reloj de presentación; cambiar la velocidad del reloj; o apagar el reloj.

Cuando la aplicación llama a [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), la sesión multimedia inicia el reloj de presentación con una hora de inicio igual a la posición inicial especificada en el **método Start.** Para obtener más información sobre la sesión multimedia, vea [Sesión multimedia](media-session.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> </dl>

 

 



