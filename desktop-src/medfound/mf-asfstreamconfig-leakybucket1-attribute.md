---
description: Establece el promedio &\# 0034; depósito de fugas&\# 0034; parámetros (vea la sección comentarios) para codificar un archivo de Windows Media. Establezca este atributo mediante la interfaz IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: MF_ASFSTREAMCONFIG_LEAKYBUCKET1 atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696764"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a><span data-ttu-id="90156-104">\_ \_ Atributo LEAKYBUCKET1 de MF ASFSTREAMCONFIG</span><span class="sxs-lookup"><span data-stu-id="90156-104">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1 attribute</span></span>

<span data-ttu-id="90156-105">Establece el promedio de parámetros de "depósito de fugas" (vea la sección comentarios) para codificar un archivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="90156-105">Sets the average "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="90156-106">Establezca este atributo mediante la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="90156-106">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="90156-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="90156-107">Data type</span></span>

<span data-ttu-id="90156-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="90156-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="90156-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90156-109">Remarks</span></span>

<span data-ttu-id="90156-110">El valor de este atributo es una matriz de tres **DWORD** s, en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="90156-110">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="90156-111">Velocidad de bits, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="90156-111">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="90156-112">Ventana de búfer, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="90156-112">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="90156-113">Llenado inicial del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="90156-113">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="90156-114">Para obtener más información sobre el concepto de depósito con fugas, vea el tema [modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md) en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="90156-114">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="90156-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="90156-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="90156-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90156-116">Requirements</span></span>



| <span data-ttu-id="90156-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="90156-117">Requirement</span></span> | <span data-ttu-id="90156-118">Value</span><span class="sxs-lookup"><span data-stu-id="90156-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90156-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90156-119">Minimum supported client</span></span><br/> | <span data-ttu-id="90156-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="90156-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="90156-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90156-121">Minimum supported server</span></span><br/> | <span data-ttu-id="90156-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="90156-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="90156-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90156-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="90156-124"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="90156-124"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90156-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="90156-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90156-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90156-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="90156-127">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="90156-127">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="90156-128">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="90156-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="90156-129">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="90156-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="90156-130">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="90156-130">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




