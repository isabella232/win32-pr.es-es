---
description: Obtiene la dirección URL efectiva de una secuencia de bytes.
ms.assetid: 0A83CFC0-7EAA-464B-BA39-50DF220AF683
title: MF_BYTESTREAM_EFFECTIVE_URL atributo (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95e01238f04c30f72d55f940b3f3105863247ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686973"
---
# <a name="mf_bytestream_effective_url-attribute"></a><span data-ttu-id="9a472-103">\_BYTESTREAM \_ atributo de \_ dirección URL efectiva de MF</span><span class="sxs-lookup"><span data-stu-id="9a472-103">MF\_BYTESTREAM\_EFFECTIVE\_URL attribute</span></span>

<span data-ttu-id="9a472-104">Obtiene la dirección URL efectiva de una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="9a472-104">Gets the effective URL of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="9a472-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9a472-105">Data type</span></span>

## <a name="getset"></a><span data-ttu-id="9a472-106">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="9a472-106">Get/set</span></span>

<span data-ttu-id="9a472-107">Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="9a472-107">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="9a472-108">Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="9a472-108">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9a472-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="9a472-109">Applies to</span></span>

[<span data-ttu-id="9a472-110">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="9a472-110">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="9a472-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a472-111">Remarks</span></span>

<span data-ttu-id="9a472-112">La dirección URL efectiva puede diferir de la dirección URL original si la dirección URL original contiene cualquier información adicional, como cadenas de búsqueda o delimitadores, o si se redirigió la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a472-112">The effective URL can differ from the original URL if the original URL contains any extra information, such as search strings or anchors, or if the request was redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a472-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a472-113">Requirements</span></span>



| <span data-ttu-id="9a472-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a472-114">Requirement</span></span> | <span data-ttu-id="9a472-115">Value</span><span class="sxs-lookup"><span data-stu-id="9a472-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a472-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a472-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a472-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="9a472-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                      |
| <span data-ttu-id="9a472-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a472-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a472-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="9a472-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                            |
| <span data-ttu-id="9a472-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a472-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a472-121"><dt>Mfobjects. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a472-121"><dt>Mfobjects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a472-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a472-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a472-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9a472-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a472-124">Atributos de secuencia de bytes</span><span class="sxs-lookup"><span data-stu-id="9a472-124">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a472-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="9a472-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




