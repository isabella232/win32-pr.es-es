---
description: Arquitectura de DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Arquitectura de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105651438"
---
# <a name="dmo-architecture"></a><span data-ttu-id="d1d59-103">Arquitectura de DMO</span><span class="sxs-lookup"><span data-stu-id="d1d59-103">DMO Architecture</span></span>

<span data-ttu-id="d1d59-104">En esta sección se describe la arquitectura general de un DMO.</span><span class="sxs-lookup"><span data-stu-id="d1d59-104">This section describes the overall architecture of a DMO.</span></span>

<span data-ttu-id="d1d59-105">**Secuencias**</span><span class="sxs-lookup"><span data-stu-id="d1d59-105">**Streams**</span></span>

<span data-ttu-id="d1d59-106">Un DMO es un objeto que toma *m* entradas y genera *n* salidas.</span><span class="sxs-lookup"><span data-stu-id="d1d59-106">A DMO is an object that takes *m* inputs and produces *n* outputs.</span></span> <span data-ttu-id="d1d59-107">Las entradas y salidas se denominan *secuencias*.</span><span class="sxs-lookup"><span data-stu-id="d1d59-107">The inputs and outputs are called *streams*.</span></span> <span data-ttu-id="d1d59-108">Cada DMO tiene al menos un flujo.</span><span class="sxs-lookup"><span data-stu-id="d1d59-108">Every DMO has at least one stream.</span></span> <span data-ttu-id="d1d59-109">Las secuencias no son objetos; simplemente se hace referencia a ellos en la DMO según el número de índice.</span><span class="sxs-lookup"><span data-stu-id="d1d59-109">Streams are not objects; they are simply referenced on the DMO by index number.</span></span> <span data-ttu-id="d1d59-110">El número de flujos se fija en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="d1d59-110">The number of streams is fixed at design time.</span></span>

<span data-ttu-id="d1d59-111">**Tipos de medios**</span><span class="sxs-lookup"><span data-stu-id="d1d59-111">**Media Types**</span></span>

<span data-ttu-id="d1d59-112">Todos los datos se escriben utilizando un *tipo de medio*, que define cómo interpretar el contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="d1d59-112">All data is typed using a *media type*, which defines how to interpret the contents of the data.</span></span> <span data-ttu-id="d1d59-113">Por ejemplo, el vídeo RGB de 320 x 240 24 bits es un tipo; 44,1-kilohercios (kHz) audio PCM estéreo de 16 bits es otro tipo.</span><span class="sxs-lookup"><span data-stu-id="d1d59-113">For example, 320 x 240 24-bit RGB video is one type; 44.1-kilohertz (kHz) 16-bit stereo PCM audio is another type.</span></span> <span data-ttu-id="d1d59-114">Los tipos de medios se describen mediante la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="d1d59-114">Media types are described using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="d1d59-115">Para que el cliente pueda procesar los datos, debe establecer el tipo de medio para cada flujo de DMO.</span><span class="sxs-lookup"><span data-stu-id="d1d59-115">Before the client can process any data, it must set the media type for each stream on the DMO.</span></span>

<span data-ttu-id="d1d59-116">Normalmente, un flujo puede aceptar un intervalo de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="d1d59-116">Typically, a stream can accept a range of media types.</span></span> <span data-ttu-id="d1d59-117">Algunos DMOs admiten una gama más amplia de tipos que otros.</span><span class="sxs-lookup"><span data-stu-id="d1d59-117">Some DMOs support a wider range of types than others.</span></span> <span data-ttu-id="d1d59-118">Las interfaces de DMO definen métodos para que el cliente detecte los tipos admitidos.</span><span class="sxs-lookup"><span data-stu-id="d1d59-118">The DMO interfaces define methods for the client to discover the supported types.</span></span> <span data-ttu-id="d1d59-119">Por ejemplo, un DMO podría admitir el vídeo RGB en cualquier profundidad de bits, mientras que otro podría admitir solo RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="d1d59-119">For example, one DMO might support RGB video at any bit depth, while another might support only 24-bit RGB.</span></span> <span data-ttu-id="d1d59-120">Además, una DMO podría estar limitada a determinadas combinaciones de entradas y salidas.</span><span class="sxs-lookup"><span data-stu-id="d1d59-120">Also, a DMO might be limited to certain combinations of inputs and outputs.</span></span> <span data-ttu-id="d1d59-121">Por ejemplo, si el tipo de entrada es un vídeo de 16 bits, el flujo de salida podría requerir la misma profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="d1d59-121">For example, if the input type is 16-bit video, the output stream might require the same bit depth.</span></span> <span data-ttu-id="d1d59-122">El cliente puede enumerar los tipos preferidos de cada flujo y probar combinaciones específicas.</span><span class="sxs-lookup"><span data-stu-id="d1d59-122">The client can enumerate each stream's preferred types and then test specific combinations.</span></span>

<span data-ttu-id="d1d59-123">**Búferes**</span><span class="sxs-lookup"><span data-stu-id="d1d59-123">**Buffers**</span></span>

<span data-ttu-id="d1d59-124">En el modelo DMO predeterminado, el cliente asigna búferes de entrada y búferes de salida independientes.</span><span class="sxs-lookup"><span data-stu-id="d1d59-124">In the default DMO model, the client allocates separate input buffers and output buffers.</span></span> <span data-ttu-id="d1d59-125">Rellena los búferes de entrada con datos y los entrega a DMO, y el DMO escribe datos nuevos en los búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="d1d59-125">It fills the input buffers with data and delivers them to the DMO, and the DMO writes new data into the output buffers.</span></span>

<span data-ttu-id="d1d59-126">Opcionalmente, un DMO puede admitir el procesamiento "en contexto".</span><span class="sxs-lookup"><span data-stu-id="d1d59-126">Optionally, a DMO can support "in-place" processing.</span></span> <span data-ttu-id="d1d59-127">Con el procesamiento en contexto, DMO escribe la salida directamente en el búfer de entrada, en los datos originales.</span><span class="sxs-lookup"><span data-stu-id="d1d59-127">With in-place processing, the DMO writes the output directly into the input buffer, over the original data.</span></span> <span data-ttu-id="d1d59-128">El procesamiento en contexto elimina la necesidad de búferes independientes.</span><span class="sxs-lookup"><span data-stu-id="d1d59-128">In-place processing eliminates the need for separate buffers.</span></span> <span data-ttu-id="d1d59-129">Por otro lado, modifica los datos originales, que puede que no sean aceptables para algunas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d1d59-129">On the other hand, it alters the original data, which may not be acceptable for some applications.</span></span>

<span data-ttu-id="d1d59-130">El modelo de almacenamiento en búfer predeterminado (no en contexto) se admite a través de la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="d1d59-130">The default (non-in-place) buffering model is supported through the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="d1d59-131">Todos los DMOs deben implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="d1d59-131">All DMOs must implement this interface.</span></span> <span data-ttu-id="d1d59-132">Si un DMO admite el procesamiento en contexto, también expone la interfaz [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="d1d59-132">If a DMO supports in-place processing, it also exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="d1d59-133">El cliente es responsable de la asignación de todos los búferes, tanto de entrada como de salida.</span><span class="sxs-lookup"><span data-stu-id="d1d59-133">The client is responsible for allocating all buffers, both input and output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1d59-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1d59-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1d59-135">Acerca de DMOs</span><span class="sxs-lookup"><span data-stu-id="d1d59-135">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



