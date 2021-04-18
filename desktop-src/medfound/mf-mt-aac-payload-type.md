---
description: Especifica el tipo de carga de una secuencia de codificación de audio avanzada (AAC).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: MF_MT_AAC_PAYLOAD_TYPE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721579"
---
# <a name="mf_mt_aac_payload_type-attribute"></a><span data-ttu-id="59998-103">\_Atributo de \_ \_ tipo de carga de módulo MF MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="59998-103">MF\_MT\_AAC\_PAYLOAD\_TYPE attribute</span></span>

<span data-ttu-id="59998-104">Especifica el tipo de carga de una secuencia de codificación de audio avanzada (AAC).</span><span class="sxs-lookup"><span data-stu-id="59998-104">Specifies the payload type of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="59998-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="59998-105">Data type</span></span>

<span data-ttu-id="59998-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="59998-106">**UINT32**</span></span>

<span data-ttu-id="59998-107">Los valores siguientes son posibles.</span><span class="sxs-lookup"><span data-stu-id="59998-107">The following values are possible.</span></span>



| <span data-ttu-id="59998-108">Value</span><span class="sxs-lookup"><span data-stu-id="59998-108">Value</span></span>                                                                        | <span data-ttu-id="59998-109">Significado</span><span class="sxs-lookup"><span data-stu-id="59998-109">Meaning</span></span>                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59998-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59998-110"><dt>0</dt></span></span> </dl> | <span data-ttu-id="59998-111">El flujo solo contiene \_ elementos de bloque de datos sin procesar \_ .</span><span class="sxs-lookup"><span data-stu-id="59998-111">The stream contains raw\_data\_block elements only.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="59998-112"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="59998-112"><dt>1</dt></span></span> </dl> | <span data-ttu-id="59998-113">Secuencia de transporte de datos de audio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="59998-113">Audio Data Transport Stream (ADTS).</span></span> <span data-ttu-id="59998-114">La secuencia contiene una \_ secuencia ADTS, tal y como se define en MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="59998-114">The stream contains an adts\_sequence, as defined by MPEG-2.</span></span><br/>                       |
| <dl> <span data-ttu-id="59998-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="59998-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="59998-116">Formato de intercambio de datos de audio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="59998-116">Audio Data Interchange Format (ADIF).</span></span> <span data-ttu-id="59998-117">La secuencia contiene una \_ secuencia Adif, tal y como se define en MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="59998-117">The stream contains an adif\_sequence, as defined by MPEG-2.</span></span><br/>                     |
| <dl> <span data-ttu-id="59998-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="59998-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="59998-119">La secuencia contiene una secuencia de transporte de audio MPEG-4 con una capa de sincronización (Loa) y una capa de multiplexación (LATM).</span><span class="sxs-lookup"><span data-stu-id="59998-119">The stream contains an MPEG-4 audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="59998-120">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="59998-120">Get/set</span></span>

<span data-ttu-id="59998-121">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="59998-121">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="59998-122">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="59998-122">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="59998-123">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="59998-123">Applies To</span></span>

[<span data-ttu-id="59998-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="59998-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="59998-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59998-125">Remarks</span></span>

<span data-ttu-id="59998-126">El \_ \_ tipo de carga AAC MT AAC \_ \_ es opcional.</span><span class="sxs-lookup"><span data-stu-id="59998-126">MF\_MT\_AAC\_PAYLOAD\_TYPE is optional.</span></span> <span data-ttu-id="59998-127">Si no se especifica este atributo, se usa el valor predeterminado 0, que especifica que la secuencia contiene \_ solo elementos de bloque de datos sin procesar \_ .</span><span class="sxs-lookup"><span data-stu-id="59998-127">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw\_data\_block elements only.</span></span>

<span data-ttu-id="59998-128">Solo se aplica a **MFAudioFormat \_ AAC**.</span><span class="sxs-lookup"><span data-stu-id="59998-128">Applies only to **MFAudioFormat\_AAC**.</span></span>

<span data-ttu-id="59998-129">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="59998-129">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="59998-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59998-130">Requirements</span></span>



| <span data-ttu-id="59998-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="59998-131">Requirement</span></span> | <span data-ttu-id="59998-132">Value</span><span class="sxs-lookup"><span data-stu-id="59998-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59998-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59998-133">Header</span></span><br/> | <dl> <span data-ttu-id="59998-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="59998-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59998-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="59998-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59998-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59998-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="59998-137">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="59998-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




