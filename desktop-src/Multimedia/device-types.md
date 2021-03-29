---
title: Tipos de dispositivos
description: Tipos de dispositivos
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778504"
---
# <a name="device-types"></a><span data-ttu-id="3a96a-103">Tipos de dispositivos</span><span class="sxs-lookup"><span data-stu-id="3a96a-103">Device Types</span></span>

<span data-ttu-id="3a96a-104">MCI reconoce un conjunto básico de *tipos de dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="3a96a-104">MCI recognizes a basic set of *device types*.</span></span> <span data-ttu-id="3a96a-105">Un tipo de dispositivo es un conjunto de controladores MCI que comparten un conjunto de comandos común y se usan para controlar dispositivos multimedia o archivos de datos similares.</span><span class="sxs-lookup"><span data-stu-id="3a96a-105">A device type is a set of MCI drivers that share a common command set and are used to control similar multimedia devices or data files.</span></span> <span data-ttu-id="3a96a-106">Muchos comandos MCI, como [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)), requieren que especifique un tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a96a-106">Many MCI commands, such as [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)), require you to specify a device type.</span></span>

<span data-ttu-id="3a96a-107">En la tabla siguiente se enumeran los tipos de dispositivos definidos.</span><span class="sxs-lookup"><span data-stu-id="3a96a-107">The following table lists the defined device types.</span></span> <span data-ttu-id="3a96a-108">La implementación actual de MCI incluye conjuntos de comandos para un subconjunto de estos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3a96a-108">The current implementation of MCI includes command sets for a subset of these devices.</span></span>



| <span data-ttu-id="3a96a-109">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="3a96a-109">Device type</span></span>      | <span data-ttu-id="3a96a-110">Constante</span><span class="sxs-lookup"><span data-stu-id="3a96a-110">Constant</span></span>                      | <span data-ttu-id="3a96a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a96a-111">Description</span></span>                                      |
|------------------|-------------------------------|--------------------------------------------------|
| <span data-ttu-id="3a96a-112">**cdaudio**</span><span class="sxs-lookup"><span data-stu-id="3a96a-112">**cdaudio**</span></span>      | <span data-ttu-id="3a96a-113">AUDIO de CD de MCI \_ DEVTYPE \_ \_</span><span class="sxs-lookup"><span data-stu-id="3a96a-113">MCI\_DEVTYPE\_CD\_AUDIO</span></span>       | <span data-ttu-id="3a96a-114">Reproductor de audio de CD</span><span class="sxs-lookup"><span data-stu-id="3a96a-114">CD audio player</span></span>                                  |
| <span data-ttu-id="3a96a-115">**incrementa**</span><span class="sxs-lookup"><span data-stu-id="3a96a-115">**dat**</span></span>          | <span data-ttu-id="3a96a-116">\_ \_ archivos DAT de MCI DEVTYPE</span><span class="sxs-lookup"><span data-stu-id="3a96a-116">MCI\_DEVTYPE\_DAT</span></span>             | <span data-ttu-id="3a96a-117">Reproductor de cintas de audio digital</span><span class="sxs-lookup"><span data-stu-id="3a96a-117">Digital-audio tape player</span></span>                        |
| <span data-ttu-id="3a96a-118">**digitalvideo**</span><span class="sxs-lookup"><span data-stu-id="3a96a-118">**digitalvideo**</span></span> | <span data-ttu-id="3a96a-119">\_ \_ vídeo digital de MCI DEVTYPE \_</span><span class="sxs-lookup"><span data-stu-id="3a96a-119">MCI\_DEVTYPE\_DIGITAL\_VIDEO</span></span>  | <span data-ttu-id="3a96a-120">Vídeo digital en una ventana (no basada en GDI)</span><span class="sxs-lookup"><span data-stu-id="3a96a-120">Digital video in a window (not GDI-based)</span></span>        |
| <span data-ttu-id="3a96a-121">**distinta**</span><span class="sxs-lookup"><span data-stu-id="3a96a-121">**other**</span></span>        | <span data-ttu-id="3a96a-122">MCI \_ DEVTYPE \_ otro</span><span class="sxs-lookup"><span data-stu-id="3a96a-122">MCI\_DEVTYPE\_OTHER</span></span>           | <span data-ttu-id="3a96a-123">Dispositivo MCI sin definir</span><span class="sxs-lookup"><span data-stu-id="3a96a-123">Undefined MCI device</span></span>                             |
| <span data-ttu-id="3a96a-124">**cubrimiento**</span><span class="sxs-lookup"><span data-stu-id="3a96a-124">**overlay**</span></span>      | <span data-ttu-id="3a96a-125">superposición de MCI \_ DEVTYPE \_</span><span class="sxs-lookup"><span data-stu-id="3a96a-125">MCI\_DEVTYPE\_OVERLAY</span></span>         | <span data-ttu-id="3a96a-126">Dispositivo superpuesto (vídeo analógico en una ventana)</span><span class="sxs-lookup"><span data-stu-id="3a96a-126">Overlay device (analog video in a window)</span></span>        |
| <span data-ttu-id="3a96a-127">**scanner**</span><span class="sxs-lookup"><span data-stu-id="3a96a-127">**scanner**</span></span>      | <span data-ttu-id="3a96a-128">\_escáner MCI DEVTYPE \_</span><span class="sxs-lookup"><span data-stu-id="3a96a-128">MCI\_DEVTYPE\_SCANNER</span></span>         | <span data-ttu-id="3a96a-129">Escáner de imágenes</span><span class="sxs-lookup"><span data-stu-id="3a96a-129">Image scanner</span></span>                                    |
| <span data-ttu-id="3a96a-130">**sequencer**</span><span class="sxs-lookup"><span data-stu-id="3a96a-130">**sequencer**</span></span>    | <span data-ttu-id="3a96a-131">\_ \_ secuenciador MCI DEVTYPE</span><span class="sxs-lookup"><span data-stu-id="3a96a-131">MCI\_DEVTYPE\_SEQUENCER</span></span>       | <span data-ttu-id="3a96a-132">Secuenciador MIDI</span><span class="sxs-lookup"><span data-stu-id="3a96a-132">MIDI sequencer</span></span>                                   |
| <span data-ttu-id="3a96a-133">**vídeos**</span><span class="sxs-lookup"><span data-stu-id="3a96a-133">**vcr**</span></span>          | <span data-ttu-id="3a96a-134">\_VCR DEVTYPE de MCI \_</span><span class="sxs-lookup"><span data-stu-id="3a96a-134">MCI\_DEVTYPE\_VCR</span></span>             | <span data-ttu-id="3a96a-135">Grabadora o reproductor de casete de vídeo</span><span class="sxs-lookup"><span data-stu-id="3a96a-135">Video-cassette recorder or player</span></span>                |
| <span data-ttu-id="3a96a-136">**videodisco**</span><span class="sxs-lookup"><span data-stu-id="3a96a-136">**videodisc**</span></span>    | <span data-ttu-id="3a96a-137">videodisco de MCI \_ DEVTYPE \_</span><span class="sxs-lookup"><span data-stu-id="3a96a-137">MCI\_DEVTYPE\_VIDEODISC</span></span>       | <span data-ttu-id="3a96a-138">Reproductor de videodisco</span><span class="sxs-lookup"><span data-stu-id="3a96a-138">Videodisc player</span></span>                                 |
| <span data-ttu-id="3a96a-139">**waveaudio**</span><span class="sxs-lookup"><span data-stu-id="3a96a-139">**waveaudio**</span></span>    | <span data-ttu-id="3a96a-140">\_audio de \_ onda \_ DEVTYPE de MCI</span><span class="sxs-lookup"><span data-stu-id="3a96a-140">MCI\_DEVTYPE\_WAVEFORM\_AUDIO</span></span> | <span data-ttu-id="3a96a-141">Dispositivo de audio que reproduce archivos de onda digitalizados</span><span class="sxs-lookup"><span data-stu-id="3a96a-141">Audio device that plays digitized waveform files</span></span> |



 

<span data-ttu-id="3a96a-142">En este documento, los nombres de los tipos de dispositivo aparecen en negrita.</span><span class="sxs-lookup"><span data-stu-id="3a96a-142">In this document, the names of device types are bold.</span></span> <span data-ttu-id="3a96a-143">Los nombres de tipo de dispositivo se usan con la interfaz de cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="3a96a-143">Device-type names are used with the command-string interface.</span></span> <span data-ttu-id="3a96a-144">Las constantes de tipo de dispositivo se usan con la interfaz de mensajes de comandos.</span><span class="sxs-lookup"><span data-stu-id="3a96a-144">Device-type constants are used with the command-message interface.</span></span>

 

 




