---
description: Contiene el nombre para mostrar de una transformación de Media Foundation basada en hardware (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: MFT_FRIENDLY_NAME_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33417fd30f4d856ce7306fbbbd492fa29575f7ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648295"
---
# <a name="mft_friendly_name_attribute-attribute"></a><span data-ttu-id="d2edc-103">Atributo \_ de \_ atributo de nombre descriptivo de MFT \_</span><span class="sxs-lookup"><span data-stu-id="d2edc-103">MFT\_FRIENDLY\_NAME\_Attribute attribute</span></span>

<span data-ttu-id="d2edc-104">Contiene el nombre para mostrar de una transformación de Media Foundation basada en hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="d2edc-104">Contains the display name for a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="d2edc-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d2edc-105">Data type</span></span>

<span data-ttu-id="d2edc-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d2edc-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="d2edc-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="d2edc-107">Get/set</span></span>

<span data-ttu-id="d2edc-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="d2edc-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="d2edc-109">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="d2edc-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="d2edc-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2edc-110">Remarks</span></span>

<span data-ttu-id="d2edc-111">Este atributo es compatible con MFTs basados en hardware.</span><span class="sxs-lookup"><span data-stu-id="d2edc-111">This attribute is supported by hardware-based MFTs.</span></span> <span data-ttu-id="d2edc-112">También se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) asignados por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , cuando esos punteros representan MFTs basados en hardware.</span><span class="sxs-lookup"><span data-stu-id="d2edc-112">It is also set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers allocated by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function, when those pointers represent hardware-based MFTs.</span></span>

<span data-ttu-id="d2edc-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d2edc-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2edc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2edc-114">Requirements</span></span>



| <span data-ttu-id="d2edc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2edc-115">Requirement</span></span> | <span data-ttu-id="d2edc-116">Value</span><span class="sxs-lookup"><span data-stu-id="d2edc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2edc-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2edc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d2edc-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="d2edc-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d2edc-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2edc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d2edc-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d2edc-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d2edc-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2edc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2edc-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2edc-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2edc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2edc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2edc-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2edc-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2edc-125">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="d2edc-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




