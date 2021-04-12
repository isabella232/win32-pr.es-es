---
description: Trabajar con tipos de medios de MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Trabajar con tipos de medios de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279784"
---
# <a name="working-with-mft-media-types"></a><span data-ttu-id="d0744-103">Trabajar con tipos de medios de MFT</span><span class="sxs-lookup"><span data-stu-id="d0744-103">Working with MFT Media Types</span></span>

<span data-ttu-id="d0744-104">Un tipo de medio es una manera de describir el formato de un flujo multimedia.</span><span class="sxs-lookup"><span data-stu-id="d0744-104">A media type is a way to describe the format of a media stream.</span></span> <span data-ttu-id="d0744-105">En Media Foundation, los tipos de medios se representan mediante la interfaz **IMFMediaType** .</span><span class="sxs-lookup"><span data-stu-id="d0744-105">In Media Foundation, media types are represented by the **IMFMediaType** interface.</span></span> <span data-ttu-id="d0744-106">Esta interfaz hereda la interfaz **IMFAttributes** .</span><span class="sxs-lookup"><span data-stu-id="d0744-106">This interface inherits the **IMFAttributes** interface.</span></span> <span data-ttu-id="d0744-107">Los detalles de un tipo de medio se especifican como atributos.</span><span class="sxs-lookup"><span data-stu-id="d0744-107">The details of a media type are specified as attributes.</span></span>

<span data-ttu-id="d0744-108">Para crear un nuevo tipo de archivo multimedia, llame a la función **MFCreateMediaType** .</span><span class="sxs-lookup"><span data-stu-id="d0744-108">To create a new media type, call the **MFCreateMediaType** function.</span></span> <span data-ttu-id="d0744-109">Esta función devuelve un puntero a la interfaz **IMFMediaType** .</span><span class="sxs-lookup"><span data-stu-id="d0744-109">This function returns a pointer to the **IMFMediaType** interface.</span></span> <span data-ttu-id="d0744-110">El tipo de medio no tiene inicialmente ningún atributo.</span><span class="sxs-lookup"><span data-stu-id="d0744-110">The media type initially has no attributes.</span></span>

<span data-ttu-id="d0744-111">El SDK de Media Foundation proporciona varias funciones auxiliares para inicializar los tipos de medios desde las estructuras de formato.</span><span class="sxs-lookup"><span data-stu-id="d0744-111">The Media Foundation SDK provides several helper functions for initializing Media Types from format structures.</span></span> <span data-ttu-id="d0744-112">Por ejemplo, la función **MFInitMediaTypeFromVideoInfoHeader** Inicializa un tipo de vídeo a partir de una estructura **VIDEOINFOHEADER** , y la función **MFInitMediaTypeFromWaveFormatEx** Inicializa un tipo de vídeo a partir de una estructura **WAVEFORMATEX** o **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="d0744-112">For example the function **MFInitMediaTypeFromVideoInfoHeader** initializes a video type from a **VIDEOINFOHEADER** structure, and the function **MFInitMediaTypeFromWaveFormatEx** initializes a video type from a **WAVEFORMATEX** or **WAVEFORMATEXTENSIBLE** structure.</span></span>

<span data-ttu-id="d0744-113">Los tipos de formato que usan los códecs generalmente se limitan a los descritos por las estructuras **VIDEOINFOHEADER** y **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="d0744-113">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span>

<span data-ttu-id="d0744-114">Puede encontrar más información sobre cómo crear y obtener acceso a los tipos de medios Media Foundation en la documentación del SDK de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d0744-114">More information on creating and accessing Media Foundation media types is available in the Media Foundation SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0744-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0744-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0744-116">Trabajar con códec MFTs</span><span class="sxs-lookup"><span data-stu-id="d0744-116">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



