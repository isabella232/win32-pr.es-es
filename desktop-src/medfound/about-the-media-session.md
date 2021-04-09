---
description: Acerca de la sesión multimedia
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Acerca de la sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003308"
---
# <a name="about-the-media-session"></a>Acerca de la sesión multimedia

La sesión multimedia expone la interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) . Hay dos maneras de crear la sesión multimedia, en función de si la aplicación va a admitir contenido protegido:

-   Si la aplicación no admite contenido protegido, puede crear la sesión multimedia llamando a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession). Esta función crea la sesión multimedia dentro del proceso de la aplicación.
-   Para admitir contenido protegido, cree la sesión multimedia mediante una llamada a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Esta función crea la sesión multimedia dentro del proceso de la ruta de acceso a medios protegidos (PMP). La aplicación recibe un puntero a un objeto proxy que calcula las referencias de las llamadas al método a través del límite del proceso. Tenga en cuenta que la sesión de medios de PMP se puede usar para reproducir contenido no cifrado, así como contenido protegido.

Cualquier aplicación que use la sesión multimedia seguirá estos pasos generales:

1.  Cree una topología.
2.  Poner en cola la topología en la sesión multimedia mediante una llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).
3.  Controle el flujo de datos mediante una llamada a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)o [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
4.  Antes de que se cierre la aplicación, llame a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la sesión multimedia.
5.  Cierre los orígenes multimedia que creó la aplicación mediante una llamada a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
6.  Cierre la sesión multimedia mediante una llamada a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

Al utilizar la sesión multimedia, la aplicación no debe iniciar, pausar o detener el origen de medios directamente. Todos los cambios de estado deben iniciarse llamando a métodos [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) . La sesión de medios administra los cambios de estado en el origen de medios.

Muchos otros detalles dependerán de la funcionalidad específica de la aplicación.

## <a name="protected-content"></a>Contenido protegido

Para reproducir contenido protegido, debe crear la sesión multimedia dentro de la ruta de acceso a medios protegidos (PMP) llamando a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Esta función crea una instancia de la sesión multimedia dentro de la PMP y devuelve un puntero a un objeto proxy que calcula las referencias de las interfaces en el límite del proceso.

En la mayoría de los aspectos, el uso de la sesión multimedia dentro de la PMP es transparente para la aplicación. Sin embargo, es posible que la aplicación necesite invocar determinadas acciones que permiten al usuario reproducir el contenido. Por ejemplo, el usuario podría necesitar obtener una licencia DRM. Media Foundation define un mecanismo genérico para estas acciones mediante la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .

Para obtener más información, vea los temas siguientes:

-   [Ruta de acceso a medios protegidos](protected-media-path.md)
-   [Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>Reloj de presentación

La sesión multimedia administra todos los aspectos del reloj de la presentación:

-   Crear el reloj de la presentación.

-   Seleccionar el origen de la hora.

-   Notificar a los receptores de medios sobre el reloj

-   Iniciar, detener y pausar el reloj según sea necesario.

-   Cerrando el reloj.

Para obtener un puntero al reloj de la presentación, llame a [**IMFMediaSession:: GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) en la sesión multimedia. El reloj de la presentación no devuelve una hora válida hasta que la sesión multimedia envía el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con la \_ marca MF TOPOSTATUS \_ Ready. Hasta entonces, **GetClock** devuelve \_ \_ \_ \_ el \_ origen de la hora de MF E.

Una aplicación que utiliza la sesión multimedia nunca debe iniciar, detener o pausar el reloj de la presentación; cambiar la velocidad de reloj; o apague el reloj.

Cuando la aplicación llama a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), la sesión multimedia inicia el reloj de la presentación con una hora de inicio igual a la posición inicial especificada en el método **Start** . Para obtener más información acerca de la sesión multimedia, consulte [sesión de medios](media-session.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> </dl>

 

 



