---
description: Especifica si el receptor de medios de la Alianza de redes digitales (DLNA) usa el servicio de programador de clases multimedia (MMCSS).
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: MF_MP2DLNA_USE_MMCSS atributo (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082730"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a><span data-ttu-id="7d11f-103">MF \_ MP2DLNA \_ usar el \_ atributo MMCSS</span><span class="sxs-lookup"><span data-stu-id="7d11f-103">MF\_MP2DLNA\_USE\_MMCSS attribute</span></span>

<span data-ttu-id="7d11f-104">Especifica si el receptor de medios de la Alianza de redes digitales (DLNA) usa el servicio de programador de clases multimedia (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="7d11f-104">Specifies whether the Digital Living Network Alliance (DLNA) media sink uses the Multimedia Class Scheduler Service (MMCSS).</span></span>

## <a name="data-type"></a><span data-ttu-id="7d11f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7d11f-105">Data type</span></span>

<span data-ttu-id="7d11f-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="7d11f-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7d11f-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="7d11f-107">Get/set</span></span>

<span data-ttu-id="7d11f-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7d11f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7d11f-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7d11f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d11f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d11f-110">Remarks</span></span>

<span data-ttu-id="7d11f-111">Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="7d11f-111">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="7d11f-112">Establezca el atributo antes de que comience la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="7d11f-112">Set the attribute before streaming begins.</span></span>

<span data-ttu-id="7d11f-113">Si este atributo es **true**, el receptor de medios DLNA se registra a sí mismo con MMCSS.</span><span class="sxs-lookup"><span data-stu-id="7d11f-113">If this attribute is **TRUE**, the DLNA media sink registers itself with MMCSS.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d11f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d11f-114">Requirements</span></span>



| <span data-ttu-id="7d11f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d11f-115">Requirement</span></span> | <span data-ttu-id="7d11f-116">Value</span><span class="sxs-lookup"><span data-stu-id="7d11f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d11f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d11f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7d11f-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d11f-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7d11f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d11f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7d11f-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d11f-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7d11f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d11f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d11f-122"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d11f-122"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d11f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d11f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d11f-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7d11f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




