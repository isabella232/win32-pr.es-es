---
description: Búferes multimedia
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Búferes multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721354"
---
# <a name="media-buffers"></a><span data-ttu-id="241cc-103">Búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="241cc-103">Media Buffers</span></span>

<span data-ttu-id="241cc-104">Un búfer multimedia es un objeto COM que administra un bloque de memoria, normalmente para contener datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="241cc-104">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="241cc-105">Los búferes de medios se utilizan para trasladar datos de un componente de canalización al siguiente.</span><span class="sxs-lookup"><span data-stu-id="241cc-105">Media buffers are used to move data from one pipeline component to the next.</span></span> <span data-ttu-id="241cc-106">La mayoría de las aplicaciones no usan búferes multimedia directamente, ya que la sesión multimedia controla todo el flujo de datos entre los objetos de canalización.</span><span class="sxs-lookup"><span data-stu-id="241cc-106">Most applications do not use media buffers directly, because the Media Session handles all of the data flow between pipeline objects.</span></span> <span data-ttu-id="241cc-107">Debe usar búferes multimedia si está escribiendo su propio componente de canalización o si usa un componente de canalización directamente sin la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="241cc-107">You must use media buffers if you are writing your own pipeline component, or if you are using a pipeline component directly without the Media Session.</span></span>

<span data-ttu-id="241cc-108">Los búferes multimedia exponen la interfaz [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="241cc-108">Media buffers exposes the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="241cc-109">Esta interfaz está diseñada para leer o escribir cualquier tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="241cc-109">This interface is designed for reading or writing any type of data.</span></span> <span data-ttu-id="241cc-110">Los fotogramas de vídeo sin comprimir requieren un tratamiento especial, ya que pueden almacenarse en superficies de Direct3D ubicadas en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="241cc-110">Uncompressed video frames require special handling, because they might be stored in Direct3D surfaces located in video memory.</span></span>

<span data-ttu-id="241cc-111">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="241cc-111">This section contains the following topics.</span></span>



| <span data-ttu-id="241cc-112">Tema</span><span class="sxs-lookup"><span data-stu-id="241cc-112">Topic</span></span>                                                        | <span data-ttu-id="241cc-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="241cc-113">Description</span></span>                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="241cc-114">Trabajar con búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="241cc-114">Working with Media Buffers</span></span>](working-with-media-buffers.md) | <span data-ttu-id="241cc-115">Describe el comportamiento general de los búferes multimedia para todos los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="241cc-115">Describes the general behavior of media buffers for all media types.</span></span> |
| [<span data-ttu-id="241cc-116">Búferes de vídeo sin comprimir</span><span class="sxs-lookup"><span data-stu-id="241cc-116">Uncompressed Video Buffers</span></span>](uncompressed-video-buffers.md) | <span data-ttu-id="241cc-117">Cómo trabajar con búferes multimedia que contienen fotogramas de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="241cc-117">How work with media buffers that contain uncompressed video frames.</span></span>  |
| [<span data-ttu-id="241cc-118">Búfer de superficie de DirectX</span><span class="sxs-lookup"><span data-stu-id="241cc-118">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)         | <span data-ttu-id="241cc-119">Describe cómo almacenar una superficie de Direct3D en un búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="241cc-119">Describes how to store a Direct3D surface in a media buffer.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="241cc-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="241cc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="241cc-121">Media Foundation primitivas</span><span class="sxs-lookup"><span data-stu-id="241cc-121">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



