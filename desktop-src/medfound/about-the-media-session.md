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
# <a name="about-the-media-session"></a><span data-ttu-id="dcc5c-103">Acerca de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="dcc5c-103">About the Media Session</span></span>

<span data-ttu-id="dcc5c-104">La sesión multimedia expone la interfaz [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="dcc5c-104">The Media Session exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface.</span></span> <span data-ttu-id="dcc5c-105">Hay dos maneras de crear la sesión multimedia, en función de si la aplicación va a admitir contenido protegido:</span><span class="sxs-lookup"><span data-stu-id="dcc5c-105">There are two ways to create the Media Session, depending on whether your application will support protected content:</span></span>

-   <span data-ttu-id="dcc5c-106">Si la aplicación no admite contenido protegido, puede crear la sesión multimedia llamando a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-106">If your application does not support protected content, you can create the Media Session by calling the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span></span> <span data-ttu-id="dcc5c-107">Esta función crea la sesión multimedia dentro del proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-107">This function creates the Media Session inside the application process.</span></span>
-   <span data-ttu-id="dcc5c-108">Para admitir contenido protegido, cree la sesión multimedia mediante una llamada a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-108">To support protected content, create the Media Session by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="dcc5c-109">Esta función crea la sesión multimedia dentro del proceso de la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-109">This function creates the Media Session inside the Protected Media Path (PMP) process.</span></span> <span data-ttu-id="dcc5c-110">La aplicación recibe un puntero a un objeto proxy que calcula las referencias de las llamadas al método a través del límite del proceso.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-110">The application receives a pointer to a proxy object that marshals method calls across the process boundary.</span></span> <span data-ttu-id="dcc5c-111">Tenga en cuenta que la sesión de medios de PMP se puede usar para reproducir contenido no cifrado, así como contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-111">Note that the PMP Media Session can be used to play clear content, as well as protected content.</span></span>

<span data-ttu-id="dcc5c-112">Cualquier aplicación que use la sesión multimedia seguirá estos pasos generales:</span><span class="sxs-lookup"><span data-stu-id="dcc5c-112">Any application that uses the Media Session will follow these general steps:</span></span>

1.  <span data-ttu-id="dcc5c-113">Cree una topología.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-113">Create a topology.</span></span>
2.  <span data-ttu-id="dcc5c-114">Poner en cola la topología en la sesión multimedia mediante una llamada a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-114">Queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>
3.  <span data-ttu-id="dcc5c-115">Controle el flujo de datos mediante una llamada a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)o [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-115">Control the flow of data by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
4.  <span data-ttu-id="dcc5c-116">Antes de que se cierre la aplicación, llame a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-116">Before the application exits, call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
5.  <span data-ttu-id="dcc5c-117">Cierre los orígenes multimedia que creó la aplicación mediante una llamada a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-117">Shut down any media sources that the application created, by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
6.  <span data-ttu-id="dcc5c-118">Cierre la sesión multimedia mediante una llamada a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-118">Shut down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="dcc5c-119">Al utilizar la sesión multimedia, la aplicación no debe iniciar, pausar o detener el origen de medios directamente.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-119">When using the Media Session, the application should not directly start, pause, or stop the media source.</span></span> <span data-ttu-id="dcc5c-120">Todos los cambios de estado deben iniciarse llamando a métodos [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="dcc5c-120">All state changes must be initiated by calling [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods.</span></span> <span data-ttu-id="dcc5c-121">La sesión de medios administra los cambios de estado en el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-121">State changes in the media source are handled by the Media Session.</span></span>

<span data-ttu-id="dcc5c-122">Muchos otros detalles dependerán de la funcionalidad específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-122">Many other details will depend on the specific functionality of your application.</span></span>

## <a name="protected-content"></a><span data-ttu-id="dcc5c-123">Contenido protegido</span><span class="sxs-lookup"><span data-stu-id="dcc5c-123">Protected Content</span></span>

<span data-ttu-id="dcc5c-124">Para reproducir contenido protegido, debe crear la sesión multimedia dentro de la ruta de acceso a medios protegidos (PMP) llamando a [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-124">To play protected content, you must create the Media Session inside the protected media path (PMP), by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="dcc5c-125">Esta función crea una instancia de la sesión multimedia dentro de la PMP y devuelve un puntero a un objeto proxy que calcula las referencias de las interfaces en el límite del proceso.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-125">This function creates an instance of the Media Session inside the PMP and returns a pointer to a proxy object that marshals interfaces across the process boundary.</span></span>

<span data-ttu-id="dcc5c-126">En la mayoría de los aspectos, el uso de la sesión multimedia dentro de la PMP es transparente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-126">In most respects, using the Media Session inside the PMP is transparent to the application.</span></span> <span data-ttu-id="dcc5c-127">Sin embargo, es posible que la aplicación necesite invocar determinadas acciones que permiten al usuario reproducir el contenido.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-127">However, the application might need to invoke certain actions that enable the user to play the content.</span></span> <span data-ttu-id="dcc5c-128">Por ejemplo, el usuario podría necesitar obtener una licencia DRM.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-128">For example, the user might need to obtain a DRM license.</span></span> <span data-ttu-id="dcc5c-129">Media Foundation define un mecanismo genérico para estas acciones mediante la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="dcc5c-129">Media Foundation defines a generic mechanism for these actions using the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span>

<span data-ttu-id="dcc5c-130">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="dcc5c-130">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="dcc5c-131">Ruta de acceso a medios protegidos</span><span class="sxs-lookup"><span data-stu-id="dcc5c-131">Protected Media Path</span></span>](protected-media-path.md)
-   [<span data-ttu-id="dcc5c-132">Cómo reproducir archivos multimedia protegidos</span><span class="sxs-lookup"><span data-stu-id="dcc5c-132">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a><span data-ttu-id="dcc5c-133">Reloj de presentación</span><span class="sxs-lookup"><span data-stu-id="dcc5c-133">Presentation Clock</span></span>

<span data-ttu-id="dcc5c-134">La sesión multimedia administra todos los aspectos del reloj de la presentación:</span><span class="sxs-lookup"><span data-stu-id="dcc5c-134">The Media Session manages all aspects of the presentation clock:</span></span>

-   <span data-ttu-id="dcc5c-135">Crear el reloj de la presentación.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-135">Creating the presentation clock.</span></span>

-   <span data-ttu-id="dcc5c-136">Seleccionar el origen de la hora.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-136">Selecting the time source.</span></span>

-   <span data-ttu-id="dcc5c-137">Notificar a los receptores de medios sobre el reloj</span><span class="sxs-lookup"><span data-stu-id="dcc5c-137">Notifying the media sinks about the clock</span></span>

-   <span data-ttu-id="dcc5c-138">Iniciar, detener y pausar el reloj según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-138">Starting, stopping, and pausing the clock as necessary.</span></span>

-   <span data-ttu-id="dcc5c-139">Cerrando el reloj.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-139">Shutting down the clock.</span></span>

<span data-ttu-id="dcc5c-140">Para obtener un puntero al reloj de la presentación, llame a [**IMFMediaSession:: GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-140">To get a pointer to the presentation clock, call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) on the Media Session.</span></span> <span data-ttu-id="dcc5c-141">El reloj de la presentación no devuelve una hora válida hasta que la sesión multimedia envía el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con la \_ marca MF TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-141">The presentation clock does not return a valid time until the Media Session sends the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span> <span data-ttu-id="dcc5c-142">Hasta entonces, **GetClock** devuelve \_ \_ \_ \_ el \_ origen de la hora de MF E.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-142">Until then, **GetClock** returns MF\_E\_CLOCK\_NO\_TIME\_SOURCE.</span></span>

<span data-ttu-id="dcc5c-143">Una aplicación que utiliza la sesión multimedia nunca debe iniciar, detener o pausar el reloj de la presentación; cambiar la velocidad de reloj; o apague el reloj.</span><span class="sxs-lookup"><span data-stu-id="dcc5c-143">An application that uses the Media Session should never start, stop, or pause the presentation clock; change the clock rate; or shut down the clock.</span></span>

<span data-ttu-id="dcc5c-144">Cuando la aplicación llama a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), la sesión multimedia inicia el reloj de la presentación con una hora de inicio igual a la posición inicial especificada en el método **Start** .</span><span class="sxs-lookup"><span data-stu-id="dcc5c-144">When the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), the Media Session starts the presentation clock with a starting time equal to the starting position specified in the **Start** method.</span></span> <span data-ttu-id="dcc5c-145">Para obtener más información acerca de la sesión multimedia, consulte [sesión de medios](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="dcc5c-145">For more information about the Media Session, see [Media Session](media-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcc5c-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dcc5c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcc5c-147">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="dcc5c-147">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



