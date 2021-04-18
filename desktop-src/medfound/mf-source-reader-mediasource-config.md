---
description: Contiene las propiedades de configuración del lector de origen.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: MF_SOURCE_READER_MEDIASOURCE_CONFIG atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707569"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a><span data-ttu-id="bd7fb-103">\_Atributo de \_ configuración de MEDIASOURCE de lector de origen MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="bd7fb-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CONFIG attribute</span></span>

<span data-ttu-id="bd7fb-104">Contiene las propiedades de configuración del [lector de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="bd7fb-104">Contains configuration properties for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="bd7fb-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="bd7fb-105">Data type</span></span>

<span data-ttu-id="bd7fb-106">**IPropertyStore \* *_ se almacena como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="bd7fb-106">**IPropertyStore\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="bd7fb-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="bd7fb-107">Get/set</span></span>

<span data-ttu-id="bd7fb-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="bd7fb-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="bd7fb-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="bd7fb-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd7fb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd7fb-110">Remarks</span></span>

<span data-ttu-id="bd7fb-111">El valor de este atributo es un puntero a la interfaz **IPropertyStore** de un almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-111">The value of this attribute is a pointer to the **IPropertyStore** interface of a property store.</span></span> <span data-ttu-id="bd7fb-112">Puede usar este atributo para pasar propiedades de configuración al origen de medios.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-112">You can use this attribute to pass configuration properties to the media source.</span></span>

<span data-ttu-id="bd7fb-113">Utilice este atributo con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="bd7fb-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="bd7fb-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="bd7fb-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="bd7fb-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="bd7fb-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="bd7fb-116">Internamente, el lector de origen pasa el puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-116">Internally, the source reader passes the **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="bd7fb-117">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="bd7fb-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd7fb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd7fb-118">Requirements</span></span>



| <span data-ttu-id="bd7fb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd7fb-119">Requirement</span></span> | <span data-ttu-id="bd7fb-120">Value</span><span class="sxs-lookup"><span data-stu-id="bd7fb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd7fb-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd7fb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd7fb-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="bd7fb-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="bd7fb-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd7fb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd7fb-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="bd7fb-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bd7fb-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd7fb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd7fb-126"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd7fb-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd7fb-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd7fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd7fb-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd7fb-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bd7fb-129">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="bd7fb-129">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="bd7fb-130">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="bd7fb-130">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




