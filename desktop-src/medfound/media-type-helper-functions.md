---
description: Las siguientes funciones pertenecen a los objetos de tipo de medio.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Funciones auxiliares de tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547398"
---
# <a name="media-type-helper-functions"></a><span data-ttu-id="2e906-103">Funciones auxiliares de tipos de medios</span><span class="sxs-lookup"><span data-stu-id="2e906-103">Media Type Helper Functions</span></span>

<span data-ttu-id="2e906-104">Las siguientes funciones pertenecen a los objetos de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2e906-104">The following functions pertain to media type objects.</span></span>



| <span data-ttu-id="2e906-105">Función</span><span class="sxs-lookup"><span data-stu-id="2e906-105">Function</span></span>                                                                     | <span data-ttu-id="2e906-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e906-106">Description</span></span>                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="2e906-107">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="2e906-107">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="2e906-108">Calcula la velocidad de fotogramas a partir de la duración media de un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e906-108">Calculates the frame rate from the average duration of a video frame.</span></span> |
| [<span data-ttu-id="2e906-109">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="2e906-109">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="2e906-110">Recupera el tamaño de la imagen para un formato de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="2e906-110">Retrieves the image size for an uncompressed video format.</span></span>            |
| [<span data-ttu-id="2e906-111">**MFCompareFullToPartialMediaType**</span><span class="sxs-lookup"><span data-stu-id="2e906-111">**MFCompareFullToPartialMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | <span data-ttu-id="2e906-112">Compara un tipo de medio completo con un tipo de medio parcial.</span><span class="sxs-lookup"><span data-stu-id="2e906-112">Compares a full media type to a partial media type.</span></span>                   |
| [<span data-ttu-id="2e906-113">**MFCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="2e906-113">**MFCreateMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | <span data-ttu-id="2e906-114">Crea un tipo de medio vacío.</span><span class="sxs-lookup"><span data-stu-id="2e906-114">Creates an empty media type.</span></span>                                          |
| [<span data-ttu-id="2e906-115">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="2e906-115">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="2e906-116">Convierte una velocidad de fotogramas de vídeo en una duración de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2e906-116">Converts a video frame rate into a frame duration.</span></span>                    |
| [<span data-ttu-id="2e906-117">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="2e906-117">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="2e906-118">Recupera el intervalo mínimo de superficie para un formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e906-118">Retrieves the minimum surface stride for a video format.</span></span>              |
| [<span data-ttu-id="2e906-119">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="2e906-119">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="2e906-120">Consulta si un código FOURCC o un valor **D3DFORMAT** es un formato YUV.</span><span class="sxs-lookup"><span data-stu-id="2e906-120">Queries whether a FOURCC code or **D3DFORMAT** value is a YUV format.</span></span> |
| [<span data-ttu-id="2e906-121">**MFValidateMediaTypeSize**</span><span class="sxs-lookup"><span data-stu-id="2e906-121">**MFValidateMediaTypeSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | <span data-ttu-id="2e906-122">Valida el tamaño de un búfer para un bloque de formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e906-122">Validates the size of a buffer for a video format block.</span></span>              |
| [<span data-ttu-id="2e906-123">**MFWrapMediaType**</span><span class="sxs-lookup"><span data-stu-id="2e906-123">**MFWrapMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | <span data-ttu-id="2e906-124">Crea un tipo de medio que contiene otro tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2e906-124">Creates a media type that wraps another media type.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="2e906-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e906-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e906-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2e906-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2e906-127">Conversiones de tipos de medios</span><span class="sxs-lookup"><span data-stu-id="2e906-127">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="2e906-128">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="2e906-128">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



