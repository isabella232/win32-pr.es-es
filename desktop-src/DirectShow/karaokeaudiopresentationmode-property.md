---
description: La propiedad KaraokeAudioPresentationMode establece o recupera la combinación de altavoces derecha izquierda para los canales de karaoke auxiliares.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Propiedad KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686288"
---
# <a name="karaokeaudiopresentationmode-property"></a><span data-ttu-id="e1bf6-103">Propiedad KaraokeAudioPresentationMode</span><span class="sxs-lookup"><span data-stu-id="e1bf6-103">KaraokeAudioPresentationMode Property</span></span>

> [!Note]  
> <span data-ttu-id="e1bf6-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e1bf6-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e1bf6-106">La `KaraokeAudioPresentationMode` propiedad establece o recupera la combinación de altavoces derecha izquierda para los canales de karaoke auxiliares.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-106">The `KaraokeAudioPresentationMode` property sets or retrieves the right-left speaker mix for the auxiliary karaoke channels.</span></span>

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a><span data-ttu-id="e1bf6-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1bf6-107">Return Value</span></span>

<span data-ttu-id="e1bf6-108">Devuelve un valor entero que contiene un conjunto de marcas de bits que indican cómo se downmixed los canales de karaoke auxiliares a los altavoces izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-108">Returns an integer value containing a set of bit flags indicating how the auxiliary karaoke channels are downmixed to the left and right speakers.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1bf6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1bf6-109">Remarks</span></span>

<span data-ttu-id="e1bf6-110">Esta propiedad es de lectura/escritura y su valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-110">This property is read/write with a default value of zero.</span></span>

<span data-ttu-id="e1bf6-111">Los canales de audio están basados en cero, por lo que los canales 0 y 1 suelen representar los canales de altavoz derecho e izquierdo y los canales 2 a 4 son los tres canales de karaoke auxiliares.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-111">Audio channels are zero-based, so channels 0 and 1 generally represent the right and left speaker channels and channels 2 through 4 are the three auxiliary karaoke channels.</span></span> <span data-ttu-id="e1bf6-112">Cuando el objeto MSWebDVD entra en el modo de karaoke, silencia automáticamente los canales 2 y superiores.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-112">When the MSWebDVD object enters karaoke mode, it automatically mutes channels 2 and higher.</span></span> <span data-ttu-id="e1bf6-113">Use operaciones OR bit a bit para establecer **el bit adecuado** con el fin de enviar un canal auxiliar al altavoz izquierdo, altavoz derecho, ambos altavoces (ambos bits en) o sin altavoces (ambos bits desactivados).</span><span class="sxs-lookup"><span data-stu-id="e1bf6-113">Use bitwise **OR** operations to set the appropriate bit in order to send an auxiliary channel to the left speaker, right speaker, both speakers (both bits on), or to no speakers (both bits off).</span></span> <span data-ttu-id="e1bf6-114">Estos bits están desactivados de forma predeterminada siempre que el navegador de DVD entra en el modo de karaoke.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-114">These bits are all off by default whenever the DVD Navigator enters karaoke mode.</span></span> <span data-ttu-id="e1bf6-115">En la tabla siguiente se proporciona el valor de los bits y su acción correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e1bf6-115">The value of the bits and their corresponding action is given in the following table.</span></span>



| <span data-ttu-id="e1bf6-116">Value</span><span class="sxs-lookup"><span data-stu-id="e1bf6-116">Value</span></span>  | <span data-ttu-id="e1bf6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1bf6-117">Description</span></span>                            |
|--------|----------------------------------------|
| <span data-ttu-id="e1bf6-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="e1bf6-118">0x0004</span></span> | <span data-ttu-id="e1bf6-119">Canal 2 de downmix al altavoz izquierdo</span><span class="sxs-lookup"><span data-stu-id="e1bf6-119">Downmix Channel 2 to the left speaker</span></span>  |
| <span data-ttu-id="e1bf6-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="e1bf6-120">0x0008</span></span> | <span data-ttu-id="e1bf6-121">Downmix Channel 3 al altavoz izquierdo</span><span class="sxs-lookup"><span data-stu-id="e1bf6-121">Downmix Channel 3 to the left speaker</span></span>  |
| <span data-ttu-id="e1bf6-122">0x0010</span><span class="sxs-lookup"><span data-stu-id="e1bf6-122">0x0010</span></span> | <span data-ttu-id="e1bf6-123">Canal 4 de downmix al altavoz izquierdo</span><span class="sxs-lookup"><span data-stu-id="e1bf6-123">Downmix Channel 4 to the left speaker</span></span>  |
| <span data-ttu-id="e1bf6-124">0x0400</span><span class="sxs-lookup"><span data-stu-id="e1bf6-124">0x0400</span></span> | <span data-ttu-id="e1bf6-125">Downmix Channel 2 al altavoz derecho</span><span class="sxs-lookup"><span data-stu-id="e1bf6-125">Downmix Channel 2 to the right speaker</span></span> |
| <span data-ttu-id="e1bf6-126">0x0800</span><span class="sxs-lookup"><span data-stu-id="e1bf6-126">0x0800</span></span> | <span data-ttu-id="e1bf6-127">Downmix Channel 3 al altavoz derecho</span><span class="sxs-lookup"><span data-stu-id="e1bf6-127">Downmix Channel 3 to the right speaker</span></span> |
| <span data-ttu-id="e1bf6-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="e1bf6-128">0x1000</span></span> | <span data-ttu-id="e1bf6-129">Downmix Channel 4 al altavoz derecho</span><span class="sxs-lookup"><span data-stu-id="e1bf6-129">Downmix Channel 4 to the right speaker</span></span> |



 

 

 



