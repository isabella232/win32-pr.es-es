---
description: El codificador de Windows Media Audio Voice está optimizado para codificar las proporciones de la voz humana a alta compresión. Este es el codificador preferido para las secuencias que se componen principalmente de palabras pronunciadas.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Codificador de Windows Media Audio Voice (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700208"
---
# <a name="windows-media-audio-voice-encoder"></a><span data-ttu-id="07538-104">Codificador de voz Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="07538-104">Windows Media Audio Voice Encoder</span></span>

<span data-ttu-id="07538-105">El codificador de Windows Media Audio Voice está optimizado para codificar las proporciones de la voz humana a alta compresión.</span><span class="sxs-lookup"><span data-stu-id="07538-105">The Windows Media Audio Voice encoder is optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="07538-106">Este es el codificador preferido para las secuencias que se componen principalmente de palabras pronunciadas.</span><span class="sxs-lookup"><span data-stu-id="07538-106">This is the preferred encoder for streams consisting mostly of spoken words.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="07538-107">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="07538-107">Class Identifier</span></span>

<span data-ttu-id="07538-108">El identificador de clase (CLSID) del codificador de Windows Media Audio Voice se representa mediante la constante **\_ CWMSPEncMediaObject2 de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="07538-108">The class identifier (CLSID) for the Windows Media Audio Voice encoder is represented by the constant **CLSID\_CWMSPEncMediaObject2**.</span></span> <span data-ttu-id="07538-109">Puede crear una instancia del codificador de voz llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="07538-109">You can create an instance of the voice encoder by calling **CoCreateInstance**.</span></span>

## <a name="output-formats"></a><span data-ttu-id="07538-110">Formatos de salida</span><span class="sxs-lookup"><span data-stu-id="07538-110">Output Formats</span></span>

<span data-ttu-id="07538-111">Windows Media Audio contenido codificado por voz se identifica mediante la etiqueta de formato 0x00A.</span><span class="sxs-lookup"><span data-stu-id="07538-111">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="07538-112">Propiedades del codificador</span><span class="sxs-lookup"><span data-stu-id="07538-112">Encoder Properties</span></span>

<span data-ttu-id="07538-113">El codificador de Windows Media Audio Voice admite las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="07538-113">The Windows Media Audio Voice encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="07538-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="07538-114">Property</span></span></th>
<th><span data-ttu-id="07538-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="07538-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07538-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span><span class="sxs-lookup"><span data-stu-id="07538-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span></span></td>
<td><span data-ttu-id="07538-117">Especifica la ventana de búfer, en milisegundos, que se usa para el códec de voz.</span><span class="sxs-lookup"><span data-stu-id="07538-117">Specifies the buffer window, in milliseconds, used for the voice codec.</span></span><br/> <dl> <span data-ttu-id="07538-118">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="07538-118">Windows XP and later.</span></span><br />
<span data-ttu-id="07538-119">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="07538-119">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07538-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span><span class="sxs-lookup"><span data-stu-id="07538-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span></span></td>
<td><span data-ttu-id="07538-121">Especifica la latencia del codificador en unidades de paquetes.</span><span class="sxs-lookup"><span data-stu-id="07538-121">Specifies encoder latency in packet units.</span></span><br/> <dl> <span data-ttu-id="07538-122">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="07538-122">Windows XP and later.</span></span><br />
<span data-ttu-id="07538-123">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="07538-123">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07538-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span><span class="sxs-lookup"><span data-stu-id="07538-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span></span></td>
<td><span data-ttu-id="07538-125">Especifica las partes de contenido que el códec de voz debe codificar como música.</span><span class="sxs-lookup"><span data-stu-id="07538-125">Specifies the portions of content to be encoded as music by the voice codec.</span></span><br/> <dl> <span data-ttu-id="07538-126">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="07538-126">Windows XP and later.</span></span><br />
<span data-ttu-id="07538-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="07538-127">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07538-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span><span class="sxs-lookup"><span data-stu-id="07538-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span></span></td>
<td><span data-ttu-id="07538-129">Especifica el modo del códec de voz.</span><span class="sxs-lookup"><span data-stu-id="07538-129">Specifies the mode of the voice codec.</span></span><br/> <dl> <span data-ttu-id="07538-130">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="07538-130">Windows XP and later.</span></span><br />
<span data-ttu-id="07538-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="07538-131">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="07538-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07538-132">Requirements</span></span>



| <span data-ttu-id="07538-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="07538-133">Requirement</span></span> | <span data-ttu-id="07538-134">Value</span><span class="sxs-lookup"><span data-stu-id="07538-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07538-135">Remoto</span><span class="sxs-lookup"><span data-stu-id="07538-135">Client</span></span><br/> | <span data-ttu-id="07538-136">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="07538-136">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="07538-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07538-137">Header</span></span><br/> | <dl> <span data-ttu-id="07538-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="07538-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="07538-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07538-139">DLL</span></span><br/>    | <dl> <span data-ttu-id="07538-140"><dt>Wmspdmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07538-140"><dt>Wmspdmoe.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07538-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="07538-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07538-142">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="07538-142">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="07538-143">Usar el códec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="07538-143">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




