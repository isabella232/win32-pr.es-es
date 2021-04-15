---
description: El método GetKaraokeChannelContent recupera un valor que indica el tipo de contenido del canal de karaoke especificado en la secuencia especificada.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Método GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677121"
---
# <a name="getkaraokechannelcontent-method"></a><span data-ttu-id="d5e18-103">Método GetKaraokeChannelContent</span><span class="sxs-lookup"><span data-stu-id="d5e18-103">GetKaraokeChannelContent Method</span></span>

> [!Note]  
> <span data-ttu-id="d5e18-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d5e18-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d5e18-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="d5e18-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d5e18-106">El `GetKaraokeChannelContent` método recupera un valor que indica el tipo de contenido del canal de karaoke especificado en la secuencia especificada.</span><span class="sxs-lookup"><span data-stu-id="d5e18-106">The `GetKaraokeChannelContent` method retrieves a value that indicates the type of content in the specified karaoke channel in the specified stream.</span></span>

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a><span data-ttu-id="d5e18-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5e18-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5e18-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="d5e18-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="d5e18-109">Especifica la secuencia de audio como un entero.</span><span class="sxs-lookup"><span data-stu-id="d5e18-109">Specifies the audio stream as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="d5e18-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span><span class="sxs-lookup"><span data-stu-id="d5e18-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span></span>
</dt> <dd>

<span data-ttu-id="d5e18-111">Especifica el canal como un entero.</span><span class="sxs-lookup"><span data-stu-id="d5e18-111">Specifies the channel as an Integer.</span></span> <span data-ttu-id="d5e18-112">Los valores posibles para cada canal son:</span><span class="sxs-lookup"><span data-stu-id="d5e18-112">The possible values for each channel are:</span></span>



| <span data-ttu-id="d5e18-113">Value</span><span class="sxs-lookup"><span data-stu-id="d5e18-113">Value</span></span>  | <span data-ttu-id="d5e18-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5e18-114">Description</span></span>    |
|--------|----------------|
| <span data-ttu-id="d5e18-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="d5e18-115">0x0001</span></span> | <span data-ttu-id="d5e18-116">Guía de vocal 1</span><span class="sxs-lookup"><span data-stu-id="d5e18-116">Guide Vocal 1</span></span>  |
| <span data-ttu-id="d5e18-117">0x0002</span><span class="sxs-lookup"><span data-stu-id="d5e18-117">0x0002</span></span> | <span data-ttu-id="d5e18-118">Guía vocal 2</span><span class="sxs-lookup"><span data-stu-id="d5e18-118">Guide Vocal 2</span></span>  |
| <span data-ttu-id="d5e18-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="d5e18-119">0x0004</span></span> | <span data-ttu-id="d5e18-120">Guía Melody 1</span><span class="sxs-lookup"><span data-stu-id="d5e18-120">Guide Melody 1</span></span> |
| <span data-ttu-id="d5e18-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="d5e18-121">0x0008</span></span> | <span data-ttu-id="d5e18-122">Guía Melody 2</span><span class="sxs-lookup"><span data-stu-id="d5e18-122">Guide Melody 2</span></span> |
| <span data-ttu-id="d5e18-123">0x0010</span><span class="sxs-lookup"><span data-stu-id="d5e18-123">0x0010</span></span> | <span data-ttu-id="d5e18-124">Guía Melody A</span><span class="sxs-lookup"><span data-stu-id="d5e18-124">Guide Melody A</span></span> |
| <span data-ttu-id="d5e18-125">0x0020</span><span class="sxs-lookup"><span data-stu-id="d5e18-125">0x0020</span></span> | <span data-ttu-id="d5e18-126">Guía Melody B</span><span class="sxs-lookup"><span data-stu-id="d5e18-126">Guide Melody B</span></span> |
| <span data-ttu-id="d5e18-127">0x0040</span><span class="sxs-lookup"><span data-stu-id="d5e18-127">0x0040</span></span> | <span data-ttu-id="d5e18-128">Efecto de sonido A</span><span class="sxs-lookup"><span data-stu-id="d5e18-128">Sound Effect A</span></span> |
| <span data-ttu-id="d5e18-129">0x0080</span><span class="sxs-lookup"><span data-stu-id="d5e18-129">0x0080</span></span> | <span data-ttu-id="d5e18-130">Efecto de sonido B</span><span class="sxs-lookup"><span data-stu-id="d5e18-130">Sound Effect B</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5e18-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5e18-131">Return Value</span></span>

<span data-ttu-id="d5e18-132">Devuelve un valor entero cuyos bits individuales especifican el contenido del canal de karaoke.</span><span class="sxs-lookup"><span data-stu-id="d5e18-132">Returns an integer value whose individual bits specify the contents of the karaoke channel.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e18-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5e18-133">Remarks</span></span>

<span data-ttu-id="d5e18-134">La numeración de canales de audio de DVD se basa en cero, por lo que los canales 2, 3 y 4 son los canales de karaoke auxiliares.</span><span class="sxs-lookup"><span data-stu-id="d5e18-134">DVD audio channel numbering is zero-based, so channels 2, 3, and 4 are the auxiliary karaoke channels.</span></span> <span data-ttu-id="d5e18-135">Después de que el método vuelva, realice una operación and bit a bit en *iContent* para determinar el contenido de cada canal.</span><span class="sxs-lookup"><span data-stu-id="d5e18-135">After the method returns, perform a bitwise AND operation on *iContent* to determine the contents of each channel.</span></span> <span data-ttu-id="d5e18-136">Dado que un único canal puede tener más de un tipo de contenido registrado, debe comprobar todos los valores posibles incluso después de encontrar una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="d5e18-136">Because a single channel might have more than one type of content recorded on it, you should test for all the possible values even after a match is found.</span></span>

<span data-ttu-id="d5e18-137">Una vez que el usuario conoce el contenido de cada canal, debe ser capaz de ajustar el volumen o activar o desactivar los canales individuales según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d5e18-137">After the user knows the contents of each channel, he or she must be able to adjust the volume or turn the individual channels on or off as needed.</span></span> <span data-ttu-id="d5e18-138">Implemente esta funcionalidad en la aplicación mediante la propiedad [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d5e18-138">Implement this functionality in your application by using the [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="d5e18-139">Para reproducir discos Karaoke, el descodificador de audio en el sistema del usuario debe ser compatible con la implementación de Karaoke de DirectShow 8.</span><span class="sxs-lookup"><span data-stu-id="d5e18-139">To play karaoke discs, the audio decoder on the user's system must be compatible with the DirectShow 8 karaoke implementation.</span></span>

 

 

 



