---
description: Especifica la calidad de codificación del receptor de medios de la Alianza de redes digitales (DLNA).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: MF_MP2DLNA_ENCODE_QUALITY atributo (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082732"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a><span data-ttu-id="ce4f2-103">\_Atributo de \_ calidad de codificación MF MP2DLNA \_</span><span class="sxs-lookup"><span data-stu-id="ce4f2-103">MF\_MP2DLNA\_ENCODE\_QUALITY attribute</span></span>

<span data-ttu-id="ce4f2-104">Especifica la calidad de codificación del receptor de medios de la Alianza de redes digitales (DLNA).</span><span class="sxs-lookup"><span data-stu-id="ce4f2-104">Specifies the encoding quality for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce4f2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ce4f2-105">Data type</span></span>

<span data-ttu-id="ce4f2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ce4f2-106">**UINT32**</span></span>

<span data-ttu-id="ce4f2-107">Intervalo: de 0 a 18</span><span class="sxs-lookup"><span data-stu-id="ce4f2-107">Range: 0–18</span></span>

## <a name="getset"></a><span data-ttu-id="ce4f2-108">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="ce4f2-108">Get/set</span></span>

<span data-ttu-id="ce4f2-109">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ce4f2-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ce4f2-110">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ce4f2-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce4f2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce4f2-111">Remarks</span></span>

<span data-ttu-id="ce4f2-112">Los números más altos indican una mejor calidad de codificación.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-112">Higher numbers indicate better encoding quality.</span></span> <span data-ttu-id="ce4f2-113">Los números más bajos indican una codificación más rápida, pero reducen la calidad de la codificación.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-113">Lower numbers indicate faster encoding, but lower encoding quality.</span></span> <span data-ttu-id="ce4f2-114">El valor predeterminado es 9.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-114">The default value is 9.</span></span>

<span data-ttu-id="ce4f2-115">Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="ce4f2-115">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="ce4f2-116">Establezca el atributo antes de que comience la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="ce4f2-116">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4f2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce4f2-117">Requirements</span></span>



| <span data-ttu-id="ce4f2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce4f2-118">Requirement</span></span> | <span data-ttu-id="ce4f2-119">Value</span><span class="sxs-lookup"><span data-stu-id="ce4f2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4f2-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce4f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ce4f2-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce4f2-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ce4f2-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce4f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ce4f2-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce4f2-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ce4f2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce4f2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce4f2-125"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce4f2-125"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce4f2-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce4f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4f2-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce4f2-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




