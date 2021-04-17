---
description: Media Foundation transformaciones
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Media Foundation transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707565"
---
# <a name="media-foundation-transforms"></a><span data-ttu-id="dc9e5-103">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="dc9e5-103">Media Foundation Transforms</span></span>

<span data-ttu-id="dc9e5-104">Media Foundation transformaciones (MFTs) proporcionan un modelo genérico para procesar los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-104">Media Foundation transforms (MFTs) provide a generic model for processing media data.</span></span> <span data-ttu-id="dc9e5-105">MFTs se usan para descodificadores, codificadores y procesadores de señal digital (DSP).</span><span class="sxs-lookup"><span data-stu-id="dc9e5-105">MFTs are used for decoders, encoders, and digital signal processors (DSPs).</span></span> <span data-ttu-id="dc9e5-106">En Resumen, todo lo que se encuentra en la canalización multimedia entre el origen multimedia y el receptor multimedia es un MFT.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-106">In short, anything that sits in the media pipeline between the media source and the media sink is an MFT.</span></span>

<span data-ttu-id="dc9e5-107">En esta sección se describe el modelo de programación de MFT y cómo implementar una MFT, con recomendaciones para tipos específicos de MFTs, como descodificadores.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-107">This section describes the MFT programming model and how to implement an MFT, with recommendations for specific types of MFTs, such as decoders.</span></span>



| <span data-ttu-id="dc9e5-108">Tema</span><span class="sxs-lookup"><span data-stu-id="dc9e5-108">Topic</span></span>                                                                    | <span data-ttu-id="dc9e5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc9e5-109">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc9e5-110">Acerca de MFTs</span><span class="sxs-lookup"><span data-stu-id="dc9e5-110">About MFTs</span></span>](about-mfts.md)                                             | <span data-ttu-id="dc9e5-111">Proporciona una breve introducción a MFTs</span><span class="sxs-lookup"><span data-stu-id="dc9e5-111">Provides a brief overview of MFTs</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="dc9e5-112">Modelo básico de procesamiento de MFT</span><span class="sxs-lookup"><span data-stu-id="dc9e5-112">Basic MFT Processing Model</span></span>](basic-mft-processing-model.md)             | <span data-ttu-id="dc9e5-113">Describe con más detalle el modelo básico de procesamiento de datos con una MFT.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-113">Describes in more detail the basic model for processing data with an MFT.</span></span>                                                                                                                           |
| [<span data-ttu-id="dc9e5-114">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="dc9e5-114">Asynchronous MFTs</span></span>](asynchronous-mfts.md)                               | <span data-ttu-id="dc9e5-115">Describe un modelo de procesamiento asincrónico que es una alternativa al modelo básico.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-115">Describes an asynchronous processing model that is an alternative to the basic model.</span></span><br/> <span data-ttu-id="dc9e5-116">El procesamiento asincrónico se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-116">Asynchronous processing was introduced in Windows 7.</span></span> <span data-ttu-id="dc9e5-117">No todos los MFT admiten este modelo.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-117">Not every MFT supports this model.</span></span><br/> |
| [<span data-ttu-id="dc9e5-118">Registro y enumeración de MFTs</span><span class="sxs-lookup"><span data-stu-id="dc9e5-118">Registering and Enumerating MFTs</span></span>](registering-and-enumerating-mfts.md) | <span data-ttu-id="dc9e5-119">Cómo registrar una MFT y cómo enumerar MFTs en el registro.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-119">How to register an MFT and how to enumerate MFTs in the registry.</span></span>                                                                                                                                   |
| [<span data-ttu-id="dc9e5-120">Campo de restricciones de uso</span><span class="sxs-lookup"><span data-stu-id="dc9e5-120">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)               | <span data-ttu-id="dc9e5-121">Describe el mecanismo para desbloquear una MFT que tiene restricciones de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-121">Describes the mechanism for unlocking an MFT that has field-of-use restrictions.</span></span>                                                                                                                    |
| [<span data-ttu-id="dc9e5-122">Comparación de MFT y DMO</span><span class="sxs-lookup"><span data-stu-id="dc9e5-122">Comparison of MFTs and DMOs</span></span>](comparison-of-mfts-and-dmos.md)           | <span data-ttu-id="dc9e5-123">Resume las diferencias entre MFTs y DMOs.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-123">Summarizes the differences between MFTs and DMOs.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="dc9e5-124">Escribir una MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="dc9e5-124">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)                         | <span data-ttu-id="dc9e5-125">Instrucciones para escribir un MFT personalizado.</span><span class="sxs-lookup"><span data-stu-id="dc9e5-125">Guidelines for writing a custom MFT.</span></span>                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="dc9e5-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc9e5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc9e5-127">Canalización de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc9e5-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="dc9e5-128">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc9e5-128">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="dc9e5-129">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="dc9e5-129">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




