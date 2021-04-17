---
description: En esta sección se describe el diseño general de Microsoft Media Foundation. Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea Guía de programación de Media Foundation.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Arquitectura de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721349"
---
# <a name="media-foundation-architecture"></a><span data-ttu-id="8b2b9-104">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b2b9-104">Media Foundation Architecture</span></span>

<span data-ttu-id="8b2b9-105">En esta sección se describe el diseño general de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-105">This section describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="8b2b9-106">Para obtener información sobre el uso de Media Foundation para tareas de programación específicas, vea [Guía de programación de Media Foundation](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="8b2b9-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8b2b9-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8b2b9-107">In this section</span></span>



| <span data-ttu-id="8b2b9-108">Tema</span><span class="sxs-lookup"><span data-stu-id="8b2b9-108">Topic</span></span>                                                                                                         | <span data-ttu-id="8b2b9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b2b9-109">Description</span></span>                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b2b9-110">Información general de la arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b2b9-110">Overview of the Media Foundation Architecture</span></span>](overview-of-the-media-foundation-architecture.md)<br/> | <span data-ttu-id="8b2b9-111">Proporciona información general de alto nivel sobre la arquitectura de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-111">Gives a high-level overview of the Media Foundation architecture.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="8b2b9-112">Media Foundation primitivas</span><span class="sxs-lookup"><span data-stu-id="8b2b9-112">Media Foundation Primitives</span></span>](media-foundation-primitives.md)<br/>                                     | <span data-ttu-id="8b2b9-113">Describe algunas interfaces básicas que se usan en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-113">Describes some basic interfaces that are used throughout Media Foundation.</span></span><br/> <span data-ttu-id="8b2b9-114">Casi todas las aplicaciones Media Foundation usarán estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-114">Almost all Media Foundation applications will use these interfaces.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="8b2b9-115">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="8b2b9-115">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)<br/>                               | <span data-ttu-id="8b2b9-116">Describe las funciones básicas de Media Foundation, como las devoluciones de llamada asincrónicas y las colas de trabajos.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-116">Describes core Media Foundation functions, such as asynchronous callbacks and work queues.</span></span><br/> <span data-ttu-id="8b2b9-117">Algunas aplicaciones pueden usar interfaces de nivel de plataforma.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-117">Some applications might use platform-level interfaces.</span></span> <span data-ttu-id="8b2b9-118">Además, los complementos personalizados, como los orígenes multimedia y MFTs, usan estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-118">Also, custom plug-ins, such as media sources and MFTs, use these interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="8b2b9-119">Canalización de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b2b9-119">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)<br/>                                         | <span data-ttu-id="8b2b9-120">La capa de canalización Media Foundation se compone de orígenes de medios, MFTs y receptores de medios.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-120">The Media Foundation pipeline layer consists of media sources, MFTs, and media sinks.</span></span> <span data-ttu-id="8b2b9-121">La mayoría de las aplicaciones no llaman a métodos directamente en la capa de canalización.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-121">Most applications do not call methods directly on the pipeline layer.</span></span> <span data-ttu-id="8b2b9-122">En su lugar, las aplicaciones usan uno de los niveles superiores, como la sesión multimedia o el lector de origen y el escritor del receptor.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-122">Instead, applications use one of the higher layers, such as the Media Session or the Source Reader and Sink Writer.</span></span><br/> |
| [<span data-ttu-id="8b2b9-123">Sesión de medios</span><span class="sxs-lookup"><span data-stu-id="8b2b9-123">Media Session</span></span>](media-session.md)<br/>                                                                 | <span data-ttu-id="8b2b9-124">La sesión multimedia administra el flujo de datos en la canalización de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-124">The Media Session manages data flow in the Media Foundation pipeline.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="8b2b9-125">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="8b2b9-125">Source Reader</span></span>](source-reader.md)<br/>                                                                 | <span data-ttu-id="8b2b9-126">El lector de origen permite a una aplicación obtener datos de un origen multimedia, sin necesidad de realizar llamadas directamente a las API de origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-126">The Source Reader enables an application to get data from a media source, without the applicating needing to call the media source APIs directly.</span></span> <span data-ttu-id="8b2b9-127">El lector de origen también puede realizar la descodificación de secuencias comprimidas.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-127">The Source Reader can also perform decoding of compressed streams.</span></span><br/>                                                            |
| [<span data-ttu-id="8b2b9-128">Ruta de acceso a medios protegidos</span><span class="sxs-lookup"><span data-stu-id="8b2b9-128">Protected Media Path</span></span>](protected-media-path.md)<br/>                                                   | <span data-ttu-id="8b2b9-129">La ruta de acceso a medios protegidos (PMP) proporciona un entorno protegido para reproducir contenido de vídeo Premium.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-129">The protected media path (PMP) provides a protected environment for playing premium video content.</span></span> <span data-ttu-id="8b2b9-130">No es necesario usar el PMP al escribir una aplicación Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b2b9-130">It is not necessary to use the PMP when writing a Media Foundation application.</span></span> <br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="8b2b9-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b2b9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b2b9-132">Acerca de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b2b9-132">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="8b2b9-133">Media Foundation: conceptos esenciales</span><span class="sxs-lookup"><span data-stu-id="8b2b9-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="8b2b9-134">Media Foundation y COM</span><span class="sxs-lookup"><span data-stu-id="8b2b9-134">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="8b2b9-135">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b2b9-135">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




