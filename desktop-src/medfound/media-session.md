---
description: La sesión multimedia es un objeto que administra el flujo de datos en la canalización. Se puede usar para reproducir y codificar archivos.
ms.assetid: dac99908-be90-415d-8837-2f97d573feb5
title: Sesión de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3df4597e5461788f990f620875bce946570ab97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717387"
---
# <a name="media-session"></a><span data-ttu-id="1982e-104">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="1982e-104">Media Session</span></span>

<span data-ttu-id="1982e-105">La sesión multimedia es un objeto que administra el flujo de datos en la canalización.</span><span class="sxs-lookup"><span data-stu-id="1982e-105">The Media Session is an object that manages data flow in the pipeline.</span></span> <span data-ttu-id="1982e-106">Se puede usar para reproducir y codificar archivos.</span><span class="sxs-lookup"><span data-stu-id="1982e-106">It can be used for both playing and encoding files.</span></span>

<span data-ttu-id="1982e-107">En esta sección se describe la sesión multimedia desde un punto de vista de la arquitectura.</span><span class="sxs-lookup"><span data-stu-id="1982e-107">This section describes the Media Session from an architectural standpoint.</span></span> <span data-ttu-id="1982e-108">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="1982e-108">It contains the following sections:</span></span>



| <span data-ttu-id="1982e-109">Tema</span><span class="sxs-lookup"><span data-stu-id="1982e-109">Topic</span></span>                                                                                        | <span data-ttu-id="1982e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1982e-110">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1982e-111">Acerca de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="1982e-111">About the Media Session</span></span>](about-the-media-session.md)                                       | <span data-ttu-id="1982e-112">Proporciona información general sobre la sesión multimedia, cómo una aplicación puede crear la sesión multimedia y cómo la sesión multimedia administra el tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="1982e-112">Provides an overview of the Media Session, how an application can create the Media Session, and how the Media Session manages presentation time.</span></span> |
| [<span data-ttu-id="1982e-113">Topologías</span><span class="sxs-lookup"><span data-stu-id="1982e-113">Topologies</span></span>](topologies.md)                                                                 | <span data-ttu-id="1982e-114">Una topología es un objeto que representa el flujo de datos de la canalización.</span><span class="sxs-lookup"><span data-stu-id="1982e-114">A topology is an object that represents the flow of data in the pipeline.</span></span>                                                                        |
| [<span data-ttu-id="1982e-115">Eventos de sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="1982e-115">Media Session Events</span></span>](media-session-events.md)                                             | <span data-ttu-id="1982e-116">Describe los eventos que una aplicación podría recibir de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="1982e-116">Describes the events that an application might receive from the Media Session.</span></span>                                                                   |
| [<span data-ttu-id="1982e-117">Cómo controlar los Estados de la presentación</span><span class="sxs-lookup"><span data-stu-id="1982e-117">How to Control Presentation States</span></span>](how-to-control-presentation-states.md)                 | <span data-ttu-id="1982e-118">Describe los controles de transporte de la sesión multimedia: reproducir, pausar y detener.</span><span class="sxs-lookup"><span data-stu-id="1982e-118">Describes the Media Session transport controls: Play, Pause, and Stop.</span></span>                                                                           |
| [<span data-ttu-id="1982e-119">Uso de orígenes multimedia con la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="1982e-119">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md) | <span data-ttu-id="1982e-120">Cómo usar orígenes multimedia con la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="1982e-120">How to use media sources with the Media Session.</span></span>                                                                                                 |
| [<span data-ttu-id="1982e-121">Control de tasa</span><span class="sxs-lookup"><span data-stu-id="1982e-121">Rate Control</span></span>](rate-control.md)                                                             | <span data-ttu-id="1982e-122">Describe cómo controlar la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="1982e-122">Describes how to control playback rate.</span></span>                                                                                                          |
| [<span data-ttu-id="1982e-123">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="1982e-123">Video Quality Management</span></span>](video-quality-management.md)                                     | <span data-ttu-id="1982e-124">Describe las mejoras de la canalización de vídeo en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1982e-124">Describes improvements to the video pipeline in Windows 7.</span></span>                                                                                       |
| [<span data-ttu-id="1982e-125">Sesión de medios de PMP</span><span class="sxs-lookup"><span data-stu-id="1982e-125">PMP Media Session</span></span>](pmp-media-session.md)                                                   | <span data-ttu-id="1982e-126">Describe cómo crear la sesión multimedia dentro de un proceso de la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="1982e-126">Describes how to create the Media Session inside a Protected Media Path (PMP) process.</span></span>                                                           |



 

<span data-ttu-id="1982e-127">En los temas siguientes se describe cómo usar la sesión multimedia en escenarios de aplicación específicos:</span><span class="sxs-lookup"><span data-stu-id="1982e-127">The following topics describe how to use the Media Session in specific application scenarios:</span></span>

-   [<span data-ttu-id="1982e-128">Reproducción de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="1982e-128">Audio/Video Playback</span></span>](audio-video-playback.md)
-   [<span data-ttu-id="1982e-129">Codificación y creación de archivos</span><span class="sxs-lookup"><span data-stu-id="1982e-129">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)

## <a name="related-topics"></a><span data-ttu-id="1982e-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1982e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1982e-131">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1982e-131">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="1982e-132">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="1982e-132">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> </dl>

 

 



