---
description: Orígenes multimedia
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Orígenes multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279786"
---
# <a name="media-sources"></a><span data-ttu-id="fc7ef-103">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="fc7ef-103">Media Sources</span></span>

<span data-ttu-id="fc7ef-104">Los *orígenes multimedia* son objetos que generan datos multimedia en la canalización Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-104">*Media sources* are objects that generate media data in the Media Foundation pipeline.</span></span> <span data-ttu-id="fc7ef-105">En esta sección se describen los detalles de las API de origen de medios.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-105">This section describes the media source APIs in detail.</span></span> <span data-ttu-id="fc7ef-106">Lea esta sección si va a implementar un origen multimedia personalizado o a través de un origen multimedia fuera de la canalización Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-106">Read this section if you are implementing a custom media source, or using a media source outside of the Media Foundation pipeline.</span></span>

<span data-ttu-id="fc7ef-107">Si la aplicación usa la capa de control, solo necesita usar un subconjunto limitado de las API de origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-107">If your application uses the control layer, it needs to use only a limited subset of the media source APIs.</span></span> <span data-ttu-id="fc7ef-108">Para obtener más información, consulte el tema [uso de orígenes multimedia con la sesión multimedia](using-media-sources-with-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="fc7ef-108">For information, see the topic [Using Media Sources with the Media Session](using-media-sources-with-the-media-session.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fc7ef-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fc7ef-109">In this section</span></span>



| <span data-ttu-id="fc7ef-110">Tema</span><span class="sxs-lookup"><span data-stu-id="fc7ef-110">Topic</span></span>                                                                                                 | <span data-ttu-id="fc7ef-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc7ef-111">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc7ef-112">Modelo de objetos de origen de medios</span><span class="sxs-lookup"><span data-stu-id="fc7ef-112">Media Source Object Model</span></span>](media-source-object-model.md)<br/>                                 | <span data-ttu-id="fc7ef-113">En este tema se describe el modelo de objetos para orígenes multimedia en Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fc7ef-113">This topic describes the object model for media sources in Microsoft Media Foundation</span></span><br/>                     |
| [<span data-ttu-id="fc7ef-114">Descriptores de presentación</span><span class="sxs-lookup"><span data-stu-id="fc7ef-114">Presentation Descriptors</span></span>](presentation-descriptors.md)<br/>                                   | <span data-ttu-id="fc7ef-115">Un *descriptor de presentación* es un objeto que contiene la descripción de una presentación determinada.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-115">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span><br/>      |
| [<span data-ttu-id="fc7ef-116">Eventos de origen de medios</span><span class="sxs-lookup"><span data-stu-id="fc7ef-116">Media Source Events</span></span>](media-source-events.md)<br/>                                             | <span data-ttu-id="fc7ef-117">En este tema se enumeran los eventos enviados por los orígenes multimedia y los flujos multimedia.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-117">This topic lists the events that are sent by media sources and media streams.</span></span><br/>                             |
| [<span data-ttu-id="fc7ef-118">Escritura de un origen de medios personalizado</span><span class="sxs-lookup"><span data-stu-id="fc7ef-118">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)<br/>                         | <span data-ttu-id="fc7ef-119">En este tema se describe cómo implementar un origen multimedia personalizado en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-119">This topic describes how to implement a custom media source in Media Foundation.</span></span><br/>                          |
| [<span data-ttu-id="fc7ef-120">Caso práctico: origen de medios MPEG-1</span><span class="sxs-lookup"><span data-stu-id="fc7ef-120">Case Study: MPEG-1 Media Source</span></span>](tutorial--writing-a-custom-media-source.md)<br/>             | <span data-ttu-id="fc7ef-121">En este tema se analiza en profundidad el ejemplo de SDK de [origen de medios MPEG-1](mpeg1source-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="fc7ef-121">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span><br/>        |
| [<span data-ttu-id="fc7ef-122">Proveedores de metadatos personalizados para archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="fc7ef-122">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)<br/> | <span data-ttu-id="fc7ef-123">En este tema se describe cómo escribir un controlador de propiedades de Shell personalizado para un Media Foundation origen de medios.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-123">This topic describes how to write a custom Shell property handler for a Media Foundation media source.</span></span><br/>    |
| [<span data-ttu-id="fc7ef-124">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="fc7ef-124">Source Resolver</span></span>](source-resolver.md)<br/>                                                     | <span data-ttu-id="fc7ef-125">La resolución del origen usa una URL o una secuencia de bytes y crea el origen multimedia adecuado para el contenido en cuestión.</span><span class="sxs-lookup"><span data-stu-id="fc7ef-125">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="fc7ef-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc7ef-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc7ef-127">Canalización de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fc7ef-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="fc7ef-128">Proveedores de metadatos personalizados para archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="fc7ef-128">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[<span data-ttu-id="fc7ef-129">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fc7ef-129">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




