---
description: El método GetKaraokeChannelAssignment recupera un valor que indica cómo se asignan los canales de karaoke a los altavoces.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Método GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906896"
---
# <a name="getkaraokechannelassignment-method"></a><span data-ttu-id="dab9c-103">Método GetKaraokeChannelAssignment</span><span class="sxs-lookup"><span data-stu-id="dab9c-103">GetKaraokeChannelAssignment Method</span></span>

> [!Note]  
> <span data-ttu-id="dab9c-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dab9c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dab9c-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="dab9c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dab9c-106">El `GetKaraokeChannelAssignment` método recupera un valor que indica cómo se asignan los canales de karaoke a los altavoces.</span><span class="sxs-lookup"><span data-stu-id="dab9c-106">The `GetKaraokeChannelAssignment` method retrieves a value that indicates how the karaoke channels are assigned to the speakers.</span></span>

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a><span data-ttu-id="dab9c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dab9c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab9c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="dab9c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="dab9c-109">Especifica la secuencia de audio como un entero.</span><span class="sxs-lookup"><span data-stu-id="dab9c-109">Specifies the audio stream as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dab9c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dab9c-110">Return Value</span></span>

<span data-ttu-id="dab9c-111">Devuelve un entero que indica la asignación de altavoz para la secuencia especificada.</span><span class="sxs-lookup"><span data-stu-id="dab9c-111">Returns an integer indicating the speaker assignment for the specified stream.</span></span>



| <span data-ttu-id="dab9c-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dab9c-112">Return code</span></span> | <span data-ttu-id="dab9c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab9c-113">Description</span></span>                                                             |
|-------------|-------------------------------------------------------------------------|
| <span data-ttu-id="dab9c-114">2</span><span class="sxs-lookup"><span data-stu-id="dab9c-114">2</span></span>           | <span data-ttu-id="dab9c-115">La secuencia se asigna a los altavoces izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="dab9c-115">The stream is assigned to the left and right speakers.</span></span>                  |
| <span data-ttu-id="dab9c-116">3</span><span class="sxs-lookup"><span data-stu-id="dab9c-116">3</span></span>           | <span data-ttu-id="dab9c-117">La secuencia se asigna a los altavoces izquierdo, derecho y medio.</span><span class="sxs-lookup"><span data-stu-id="dab9c-117">The stream is assigned to the left, right, and middle speakers.</span></span>         |
| <span data-ttu-id="dab9c-118">4</span><span class="sxs-lookup"><span data-stu-id="dab9c-118">4</span></span>           | <span data-ttu-id="dab9c-119">La secuencia se asigna a los altavoces izquierdo, derecho y AUDIO1.</span><span class="sxs-lookup"><span data-stu-id="dab9c-119">The stream is assigned to the left, right, and audio1 speakers.</span></span>         |
| <span data-ttu-id="dab9c-120">5</span><span class="sxs-lookup"><span data-stu-id="dab9c-120">5</span></span>           | <span data-ttu-id="dab9c-121">La secuencia se asigna a los altavoces izquierdo, derecho, medio y AUDIO1.</span><span class="sxs-lookup"><span data-stu-id="dab9c-121">The stream is assigned to the left, right, middle, and audio1 speakers.</span></span> |
| <span data-ttu-id="dab9c-122">6</span><span class="sxs-lookup"><span data-stu-id="dab9c-122">6</span></span>           | <span data-ttu-id="dab9c-123">La secuencia se asigna a los altavoces izquierdo, derecho y Audio2.</span><span class="sxs-lookup"><span data-stu-id="dab9c-123">The stream is assigned to the left, right, and audio2 speakers.</span></span>         |
| <span data-ttu-id="dab9c-124">7</span><span class="sxs-lookup"><span data-stu-id="dab9c-124">7</span></span>           | <span data-ttu-id="dab9c-125">La secuencia se asigna a los altavoces izquierdo, derecho, medio y Audio2.</span><span class="sxs-lookup"><span data-stu-id="dab9c-125">The stream is assigned to the left, right, middle, and audio2 speakers.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="dab9c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="dab9c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab9c-127">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="dab9c-127">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



