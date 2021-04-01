---
description: Especifica un flujo de entrada en una transformación de Media Foundation (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: MF_EVENT_MFT_INPUT_STREAM_ID atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d3966c33dc563fc9e38ad367cc675ba6616c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275578"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a><span data-ttu-id="99ed0-103">\_Atributo de \_ \_ identificador de flujo de entrada de MFT de \_ evento MF \_</span><span class="sxs-lookup"><span data-stu-id="99ed0-103">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID attribute</span></span>

<span data-ttu-id="99ed0-104">Especifica un flujo de entrada en una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="99ed0-104">Specifies an input stream on a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="99ed0-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="99ed0-105">Data type</span></span>

<span data-ttu-id="99ed0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="99ed0-106">**UINT32**</span></span>

<span data-ttu-id="99ed0-107">El valor es un identificador de flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="99ed0-107">The value is an input stream identifier.</span></span>

## <a name="getset"></a><span data-ttu-id="99ed0-108">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="99ed0-108">Get/set</span></span>

<span data-ttu-id="99ed0-109">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="99ed0-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="99ed0-110">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="99ed0-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="99ed0-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="99ed0-111">Applies to</span></span>

[<span data-ttu-id="99ed0-112">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="99ed0-112">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="99ed0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99ed0-113">Remarks</span></span>

<span data-ttu-id="99ed0-114">Este atributo se utiliza con los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="99ed0-114">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="99ed0-115">METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="99ed0-115">METransformDrainComplete</span></span>](metransformdraincomplete.md)
-   [<span data-ttu-id="99ed0-116">METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="99ed0-116">METransformNeedInput</span></span>](metransformneedinput.md)

<span data-ttu-id="99ed0-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="99ed0-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="99ed0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99ed0-118">Requirements</span></span>



| <span data-ttu-id="99ed0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="99ed0-119">Requirement</span></span> | <span data-ttu-id="99ed0-120">Value</span><span class="sxs-lookup"><span data-stu-id="99ed0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99ed0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99ed0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="99ed0-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="99ed0-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="99ed0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99ed0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="99ed0-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="99ed0-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="99ed0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99ed0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="99ed0-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="99ed0-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99ed0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="99ed0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ed0-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="99ed0-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="99ed0-129">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="99ed0-129">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="99ed0-130">Atributos de eventos</span><span class="sxs-lookup"><span data-stu-id="99ed0-130">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




