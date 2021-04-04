---
description: Contiene un puntero a los atributos de secuencia de la secuencia conectada en una transformación de Media Foundation basada en hardware (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: MFT_CONNECTED_STREAM_ATTRIBUTE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908647"
---
# <a name="mft_connected_stream_attribute-attribute"></a><span data-ttu-id="b58af-103">\_Atributo de \_ atributo de secuencia de MFT conectado \_</span><span class="sxs-lookup"><span data-stu-id="b58af-103">MFT\_CONNECTED\_STREAM\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="b58af-104">Contiene un puntero a los atributos de secuencia de la secuencia conectada en una transformación de Media Foundation basada en hardware (MFT).</span><span class="sxs-lookup"><span data-stu-id="b58af-104">Contains a pointer to the stream attributes of the connected stream on a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="b58af-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b58af-105">Data type</span></span>

<span data-ttu-id="b58af-106">**IMFAttributes \** _ almacenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="b58af-106">**IMFAttributes\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="b58af-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b58af-107">Get/set</span></span>

<span data-ttu-id="b58af-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="b58af-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="b58af-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="b58af-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="b58af-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b58af-110">Remarks</span></span>

<span data-ttu-id="b58af-111">Normalmente, las aplicaciones no usan este atributo.</span><span class="sxs-lookup"><span data-stu-id="b58af-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="b58af-112">Este atributo se usa para MFTs que actúan como servidores proxy en un dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="b58af-112">This attribute is used for MFTs that act as proxies to a hardware device.</span></span> <span data-ttu-id="b58af-113">Para obtener más información, consulte [hardware MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="b58af-113">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>

<span data-ttu-id="b58af-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b58af-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b58af-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b58af-115">Requirements</span></span>



| <span data-ttu-id="b58af-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b58af-116">Requirement</span></span> | <span data-ttu-id="b58af-117">Value</span><span class="sxs-lookup"><span data-stu-id="b58af-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b58af-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b58af-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b58af-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="b58af-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b58af-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b58af-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b58af-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b58af-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b58af-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b58af-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b58af-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b58af-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b58af-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b58af-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58af-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b58af-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b58af-126">MFT \_ conectado \_ al \_ flujo de HW \_</span><span class="sxs-lookup"><span data-stu-id="b58af-126">MFT\_CONNECTED\_TO\_HW\_STREAM</span></span>](mft-connected-to-hw-stream.md)
</dt> <dt>

[<span data-ttu-id="b58af-127">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="b58af-127">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="b58af-128">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="b58af-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




