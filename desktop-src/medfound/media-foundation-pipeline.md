---
description: La capa de canalización en Microsoft Media Foundation es el nivel de la arquitectura que genera o procesa directamente los datos multimedia.
ms.assetid: d6396246-ddc4-4e24-9371-35ddbef59b8a
title: Canalización de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f307049d7f88ca6b50479bdb261c75ba20f9b41e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721328"
---
# <a name="media-foundation-pipeline"></a><span data-ttu-id="caa49-103">Canalización de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="caa49-103">Media Foundation Pipeline</span></span>

<span data-ttu-id="caa49-104">La capa de *canalización* en Microsoft Media Foundation es el nivel de la arquitectura que genera o procesa directamente los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="caa49-104">The *pipeline* layer in Microsoft Media Foundation is the layer of the architecture that directly generates or processes media data.</span></span>

<span data-ttu-id="caa49-105">La mayoría de las aplicaciones no llaman a métodos directamente en los componentes de canalización, aunque es posible hacerlo.</span><span class="sxs-lookup"><span data-stu-id="caa49-105">Most applications do not call methods directly on the pipeline components, although it is possible to do so.</span></span> <span data-ttu-id="caa49-106">Lea estos temas si está escribiendo un componente de canalización personalizado.</span><span class="sxs-lookup"><span data-stu-id="caa49-106">Read these topics if you are writing a custom pipeline component.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="caa49-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="caa49-107">In this section</span></span>



| <span data-ttu-id="caa49-108">Tema</span><span class="sxs-lookup"><span data-stu-id="caa49-108">Topic</span></span>                                                                     | <span data-ttu-id="caa49-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="caa49-109">Description</span></span>                                                                                                                           |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="caa49-110">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="caa49-110">Media Sources</span></span>](media-sources.md)<br/>                             | <span data-ttu-id="caa49-111">Los orígenes multimedia generan datos multimedia, normalmente desde un archivo, un dispositivo de captura o un flujo de red.</span><span class="sxs-lookup"><span data-stu-id="caa49-111">Media sources generate media data, typically from a file, capture device, or network stream.</span></span> <br/>                              |
| [<span data-ttu-id="caa49-112">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="caa49-112">Media Foundation Transforms</span></span>](media-foundation-transforms.md)<br/> | <span data-ttu-id="caa49-113">Media Foundation transformaciones (MFTs) procesan datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="caa49-113">Media Foundation transforms (MFTs) process media data.</span></span> <span data-ttu-id="caa49-114">Por ejemplo, los códecs de Media Foundation se implementan como MFTs.</span><span class="sxs-lookup"><span data-stu-id="caa49-114">For example, codecs in Media Foundation are implemented as MFTs.</span></span> <br/>   |
| [<span data-ttu-id="caa49-115">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="caa49-115">Media Sinks</span></span>](media-sinks.md)<br/>                                 | <span data-ttu-id="caa49-116">Los receptores de medios consumen datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="caa49-116">Media sinks consume media data.</span></span> <span data-ttu-id="caa49-117">Por ejemplo, un receptor de medios podría escribir los datos en un archivo o enviar los datos a través de una red.</span><span class="sxs-lookup"><span data-stu-id="caa49-117">For example, a media sink might write the data to a file, or send the data over a network.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="caa49-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="caa49-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caa49-119">Media Foundation y COM</span><span class="sxs-lookup"><span data-stu-id="caa49-119">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="caa49-120">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="caa49-120">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




