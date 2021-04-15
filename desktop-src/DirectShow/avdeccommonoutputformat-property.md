---
description: Especifica el formato de salida para el descodificador.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propiedad AVDecCommonOutputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538013"
---
# <a name="avdeccommonoutputformat-property"></a><span data-ttu-id="b5a32-103">Propiedad AVDecCommonOutputFormat</span><span class="sxs-lookup"><span data-stu-id="b5a32-103">AVDecCommonOutputFormat property</span></span>

<span data-ttu-id="b5a32-104">Especifica el formato de salida para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="b5a32-104">Specifies the output format for the decoder.</span></span>

<span data-ttu-id="b5a32-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b5a32-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5a32-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b5a32-106">Data type</span></span>

<span data-ttu-id="b5a32-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="b5a32-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b5a32-108">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="b5a32-108">Property GUID</span></span>

<span data-ttu-id="b5a32-109">**CODECAPI \_ AVDecCommonOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="b5a32-109">**CODECAPI\_AVDecCommonOutputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="b5a32-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b5a32-110">Property value</span></span>



| <span data-ttu-id="b5a32-111">GUID</span><span class="sxs-lookup"><span data-stu-id="b5a32-111">GUID</span></span>                                                               | <span data-ttu-id="b5a32-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5a32-112">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a32-113">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM</span><span class="sxs-lookup"><span data-stu-id="b5a32-113">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM</span></span>                        | <span data-ttu-id="b5a32-114">Audio PCM, con cualquier número de canales</span><span class="sxs-lookup"><span data-stu-id="b5a32-114">PCM audio, using any number of channels</span></span>                                                                                                                                                                             |
| <span data-ttu-id="b5a32-115">\_Auriculares CODECAPI GUID \_ AVDecAudioOutputFormat \_ PCM \_</span><span class="sxs-lookup"><span data-stu-id="b5a32-115">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Headphones</span></span>            | <span data-ttu-id="b5a32-116">Audio PCM estéreo, con el downmix de solo izquierda/solo hacia la derecha (lo/ro)</span><span class="sxs-lookup"><span data-stu-id="b5a32-116">Stereo PCM audio, using left-only/right-only (Lo/Ro) downmix</span></span>                                                                                                                                                        |
| <span data-ttu-id="b5a32-117">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ estéreo \_ auto</span><span class="sxs-lookup"><span data-stu-id="b5a32-117">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_Auto</span></span>          | <span data-ttu-id="b5a32-118">Audio PCM estéreo mediante la selección automática del modo downmix estéreo (lo/ro o LT/RT).</span><span class="sxs-lookup"><span data-stu-id="b5a32-118">Stereo PCM audio, using automatic selection of the stereo downmix mode (Lo/Ro or Lt/Rt).</span></span> <span data-ttu-id="b5a32-119">Puede usar este valor para los formatos de audio en los que el flujo de entrada define el modo de downmix preferido, como Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="b5a32-119">You can use this value for audio formats in which the input stream defines the preferred downmix mode, such as Dolby AC-3.</span></span> |
| <span data-ttu-id="b5a32-120">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ estéreo \_ MatrixEncoded</span><span class="sxs-lookup"><span data-stu-id="b5a32-120">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_MatrixEncoded</span></span> | <span data-ttu-id="b5a32-121">Audio PCM estéreo con codificación de matriz codificada downmix (LT/RT)</span><span class="sxs-lookup"><span data-stu-id="b5a32-121">Stereo PCM audio, using matrix-encoded stereo downmix (Lt/Rt)</span></span>                                                                                                                                                       |
| <span data-ttu-id="b5a32-122">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ fragmentada</span><span class="sxs-lookup"><span data-stu-id="b5a32-122">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_Bitstream</span></span>           | <span data-ttu-id="b5a32-123">S/PDIF (formato de interfaz digital de Sony/Philips) comprimido fragmentada, tal como se define en IEC-60958</span><span class="sxs-lookup"><span data-stu-id="b5a32-123">S/PDIF (Sony/Philips Digital Interface Format) compressed bitstream, as defined by IEC-60958</span></span>                                                                                                                        |
| <span data-ttu-id="b5a32-124">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ \_ PCM SPDIF</span><span class="sxs-lookup"><span data-stu-id="b5a32-124">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="b5a32-125">Estéreo S/PDIF PCM, tal como se define en IEC-60958</span><span class="sxs-lookup"><span data-stu-id="b5a32-125">S/PDIF PCM stereo, as defined by IEC-60958</span></span>                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="b5a32-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a32-126">Requirements</span></span>



| <span data-ttu-id="b5a32-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a32-127">Requirement</span></span> | <span data-ttu-id="b5a32-128">Value</span><span class="sxs-lookup"><span data-stu-id="b5a32-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a32-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5a32-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a32-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="b5a32-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b5a32-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5a32-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a32-132">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="b5a32-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b5a32-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5a32-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5a32-134"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5a32-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a32-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5a32-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a32-136">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="b5a32-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b5a32-137">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b5a32-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




