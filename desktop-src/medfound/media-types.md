---
description: Tipos de medios
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Tipos de medios (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361923"
---
# <a name="media-types-media-foundation"></a><span data-ttu-id="28bbf-103">Tipos de medios (Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="28bbf-103">Media Types (Media Foundation)</span></span>

<span data-ttu-id="28bbf-104">Un *tipo de medio* es una manera de describir el formato de un flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="28bbf-104">A *media type* is a way to describe the format of a media stream.</span></span> <span data-ttu-id="28bbf-105">En Media Foundation, los tipos de medios se representan mediante la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="28bbf-105">In Media Foundation, media types are represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="28bbf-106">Las aplicaciones usan tipos de medios para detectar el formato de un archivo multimedia o un flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="28bbf-106">Applications use media types to discover the format of a media file or media stream.</span></span> <span data-ttu-id="28bbf-107">Los objetos de la canalización Media Foundation utilizan tipos de medios para negociar los formatos que entregarán o recibirán.</span><span class="sxs-lookup"><span data-stu-id="28bbf-107">Objects in the Media Foundation pipeline use media types to negotiate the formats they will deliver or receive.</span></span>

<span data-ttu-id="28bbf-108">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="28bbf-108">This section contains the following topics.</span></span>



| <span data-ttu-id="28bbf-109">Tema</span><span class="sxs-lookup"><span data-stu-id="28bbf-109">Topic</span></span>                                                                    | <span data-ttu-id="28bbf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="28bbf-110">Description</span></span>                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="28bbf-111">Acerca de los tipos de medios</span><span class="sxs-lookup"><span data-stu-id="28bbf-111">About Media Types</span></span>](about-media-types.md)                               | <span data-ttu-id="28bbf-112">Información general de los tipos de medios en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="28bbf-112">General overview of media types in Media Foundation.</span></span>                             |
| [<span data-ttu-id="28bbf-113">GUID de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="28bbf-113">Media Type GUIDs</span></span>](media-type-guids.md)                                 | <span data-ttu-id="28bbf-114">Enumera los GUID definidos para los tipos y subtipos principales.</span><span class="sxs-lookup"><span data-stu-id="28bbf-114">Lists the defined GUIDs for major types and subtypes.</span></span>                            |
| [<span data-ttu-id="28bbf-115">Tipos de medios de audio</span><span class="sxs-lookup"><span data-stu-id="28bbf-115">Audio Media Types</span></span>](audio-media-types.md)                               | <span data-ttu-id="28bbf-116">Cómo crear tipos de medios para formatos de audio.</span><span class="sxs-lookup"><span data-stu-id="28bbf-116">How to create media types for audio formats.</span></span>                                     |
| [<span data-ttu-id="28bbf-117">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="28bbf-117">Video Media Types</span></span>](video-media-types.md)                               | <span data-ttu-id="28bbf-118">Cómo crear tipos de medios para formatos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="28bbf-118">How to create media types for video formats.</span></span>                                     |
| [<span data-ttu-id="28bbf-119">Tipos de medios completos y parciales</span><span class="sxs-lookup"><span data-stu-id="28bbf-119">Complete and Partial Media Types</span></span>](complete-and-partial-media-types.md) | <span data-ttu-id="28bbf-120">Describe la diferencia entre los tipos de medios completos y los tipos de medios parciales.</span><span class="sxs-lookup"><span data-stu-id="28bbf-120">Describes the difference between complete media types and partial media types.</span></span>   |
| [<span data-ttu-id="28bbf-121">Conversiones de tipos de medios</span><span class="sxs-lookup"><span data-stu-id="28bbf-121">Media Type Conversions</span></span>](media-type-conversions.md)                     | <span data-ttu-id="28bbf-122">Cómo convertir entre Media Foundation tipos de medios y estructuras de formato anteriores.</span><span class="sxs-lookup"><span data-stu-id="28bbf-122">How to convert between Media Foundation media types and older format structures.</span></span> |
| [<span data-ttu-id="28bbf-123">Funciones auxiliares de tipos de medios</span><span class="sxs-lookup"><span data-stu-id="28bbf-123">Media Type Helper Functions</span></span>](media-type-helper-functions.md)           | <span data-ttu-id="28bbf-124">Una lista de funciones que manipulan u obtienen información de un tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="28bbf-124">A list of functions that manipulate or get information from a media type.</span></span>        |
| [<span data-ttu-id="28bbf-125">Código de depuración de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="28bbf-125">Media Type Debugging Code</span></span>](media-type-debugging-code.md)               | <span data-ttu-id="28bbf-126">Código de ejemplo que muestra cómo ver un tipo de medio durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="28bbf-126">Example code that shows how to view a media type while debugging.</span></span>                |



 

## <a name="related-topics"></a><span data-ttu-id="28bbf-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="28bbf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28bbf-128">Media Foundation primitivas</span><span class="sxs-lookup"><span data-stu-id="28bbf-128">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> <dt>

[<span data-ttu-id="28bbf-129">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="28bbf-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 



