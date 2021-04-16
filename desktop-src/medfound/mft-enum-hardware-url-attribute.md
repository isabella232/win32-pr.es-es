---
description: Contiene el vínculo simbólico para una transformación de Media Foundation basada en hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: MFT_ENUM_HARDWARE_URL_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276223"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a><span data-ttu-id="aae6a-103">\_Atributo de \_ \_ atributo de dirección URL de hardware enum de MFT \_</span><span class="sxs-lookup"><span data-stu-id="aae6a-103">MFT\_ENUM\_HARDWARE\_URL\_Attribute attribute</span></span>

<span data-ttu-id="aae6a-104">Contiene el vínculo simbólico para una transformación de Media Foundation basada en hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="aae6a-104">Contains the symbolic link for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="aae6a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="aae6a-105">Data type</span></span>

<span data-ttu-id="aae6a-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="aae6a-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="aae6a-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="aae6a-107">Get/set</span></span>

<span data-ttu-id="aae6a-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="aae6a-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="aae6a-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="aae6a-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="aae6a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aae6a-110">Remarks</span></span>

<span data-ttu-id="aae6a-111">Este atributo es compatible con MFTs basados en hardware.</span><span class="sxs-lookup"><span data-stu-id="aae6a-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="aae6a-112">El valor del atributo es el vínculo simbólico del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aae6a-112">The value of the attribute is the symbolic link for the device driver.</span></span> <span data-ttu-id="aae6a-113">Este atributo también se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) asignados por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , cuando esos punteros representan MFTs basados en hardware.</span><span class="sxs-lookup"><span data-stu-id="aae6a-113">This attribute is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="aae6a-114">El vínculo simbólico debe considerarse una cadena opaca.</span><span class="sxs-lookup"><span data-stu-id="aae6a-114">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="aae6a-115">Para obtener el nombre para mostrar de un dispositivo, consulte el atributo [ \_ \_ nombre descriptivo de MFT](mft-friendly-name-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="aae6a-115">To get the display name for a device, query the [MFT\_FRIENDLY\_NAME](mft-friendly-name-attribute.md) attribute.</span></span>

<span data-ttu-id="aae6a-116">El software MFTs no debe tener establecido este atributo.</span><span class="sxs-lookup"><span data-stu-id="aae6a-116">Software MFTs should not have this attribute set.</span></span>

<span data-ttu-id="aae6a-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="aae6a-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae6a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aae6a-118">Requirements</span></span>



| <span data-ttu-id="aae6a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aae6a-119">Requirement</span></span> | <span data-ttu-id="aae6a-120">Value</span><span class="sxs-lookup"><span data-stu-id="aae6a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aae6a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aae6a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aae6a-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="aae6a-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="aae6a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aae6a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aae6a-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="aae6a-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aae6a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aae6a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae6a-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae6a-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae6a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="aae6a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae6a-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aae6a-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aae6a-129">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="aae6a-129">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="aae6a-130">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="aae6a-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




