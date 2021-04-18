---
description: Especifica el perfil de audio y el nivel de una secuencia de codificación de audio avanzada (AAC).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bfc2b41cff3cbd92fc9a60be150ea598e1cc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718970"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a><span data-ttu-id="30d17-103">\_Atributo de \_ \_ indicación de \_ nivel de Perfil de audio MF \_ MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="30d17-103">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION attribute</span></span>

<span data-ttu-id="30d17-104">Especifica el perfil de audio y el nivel de una secuencia de codificación de audio avanzada (AAC).</span><span class="sxs-lookup"><span data-stu-id="30d17-104">Specifies the audio profile and level of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="30d17-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="30d17-105">Data type</span></span>

<span data-ttu-id="30d17-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="30d17-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="30d17-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="30d17-107">Get/set</span></span>

<span data-ttu-id="30d17-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="30d17-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="30d17-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="30d17-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="30d17-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="30d17-110">Applies To</span></span>

[<span data-ttu-id="30d17-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="30d17-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="30d17-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30d17-112">Remarks</span></span>

<span data-ttu-id="30d17-113">Este atributo contiene el valor del campo **audioProfileLevelIndication** , tal y como se define en ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="30d17-113">This attribute contains the value of the **audioProfileLevelIndication** field, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="30d17-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="30d17-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="30d17-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30d17-115">Requirements</span></span>



| <span data-ttu-id="30d17-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="30d17-116">Requirement</span></span> | <span data-ttu-id="30d17-117">Value</span><span class="sxs-lookup"><span data-stu-id="30d17-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30d17-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30d17-118">Header</span></span><br/> | <dl> <span data-ttu-id="30d17-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="30d17-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30d17-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="30d17-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30d17-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="30d17-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="30d17-122">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="30d17-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




