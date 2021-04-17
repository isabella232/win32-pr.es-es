---
description: Establece el límite máximo &\# 0034; depósito de fugas&\# 0034; parámetros (vea la sección comentarios) para codificar un archivo de Windows Media. Estos parámetros se usan para la velocidad de bits máxima. Establezca este atributo mediante la interfaz IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET2 atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678107"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a><span data-ttu-id="bb94b-105">\_ \_ Atributo LEAKYBUCKET2 de MF ASFSTREAMCONFIG</span><span class="sxs-lookup"><span data-stu-id="bb94b-105">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2 attribute</span></span>

<span data-ttu-id="bb94b-106">Establece los parámetros de límite máximo de "depósito de fugas" (vea la sección comentarios) para codificar un archivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bb94b-106">Sets the peak "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="bb94b-107">Estos parámetros se usan para la velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="bb94b-107">These parameters are used for the peak bit rate.</span></span> <span data-ttu-id="bb94b-108">Establezca este atributo mediante la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="bb94b-108">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb94b-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bb94b-109">Data type</span></span>

<span data-ttu-id="bb94b-110">Byte array</span><span class="sxs-lookup"><span data-stu-id="bb94b-110">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="bb94b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb94b-111">Remarks</span></span>

<span data-ttu-id="bb94b-112">El valor de este atributo es una matriz de tres **DWORD** s, en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="bb94b-112">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="bb94b-113">Velocidad de bits, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="bb94b-113">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="bb94b-114">Ventana de búfer, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="bb94b-114">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="bb94b-115">Llenado inicial del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="bb94b-115">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="bb94b-116">Para obtener más información sobre el concepto de depósito con fugas, vea el tema [modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md) en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="bb94b-116">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="bb94b-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="bb94b-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb94b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb94b-118">Requirements</span></span>



| <span data-ttu-id="bb94b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb94b-119">Requirement</span></span> | <span data-ttu-id="bb94b-120">Value</span><span class="sxs-lookup"><span data-stu-id="bb94b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb94b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb94b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb94b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb94b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bb94b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb94b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb94b-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb94b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bb94b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb94b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb94b-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb94b-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb94b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb94b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb94b-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb94b-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb94b-129">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="bb94b-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb94b-130">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="bb94b-130">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="bb94b-131">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="bb94b-131">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="bb94b-132">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="bb94b-132">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




