---
description: Especifica cuándo se modificó por última vez una secuencia de bytes.
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: MF_BYTESTREAM_LAST_MODIFIED_TIME atributo (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a5069f8c3f826db9f2ec031d5674013839d97f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811863"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a><span data-ttu-id="d0a1a-103">\_Atributo de \_ hora de última \_ modificación \_ de MF BYTESTREAM</span><span class="sxs-lookup"><span data-stu-id="d0a1a-103">MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="d0a1a-104">Especifica cuándo se modificó por última vez una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-104">Specifies when a byte stream was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="d0a1a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d0a1a-105">Data type</span></span>

<span data-ttu-id="d0a1a-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="d0a1a-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a1a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0a1a-107">Remarks</span></span>

<span data-ttu-id="d0a1a-108">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-108">This attribute is optional.</span></span> <span data-ttu-id="d0a1a-109">El valor del atributo es una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="d0a1a-109">The value of the attribute is a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

<span data-ttu-id="d0a1a-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a1a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0a1a-111">Requirements</span></span>



| <span data-ttu-id="d0a1a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0a1a-112">Requirement</span></span> | <span data-ttu-id="d0a1a-113">Value</span><span class="sxs-lookup"><span data-stu-id="d0a1a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a1a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0a1a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a1a-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="d0a1a-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="d0a1a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0a1a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a1a-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="d0a1a-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="d0a1a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0a1a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a1a-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0a1a-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a1a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0a1a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a1a-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0a1a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0a1a-122">Atributos de secuencia de bytes</span><span class="sxs-lookup"><span data-stu-id="d0a1a-122">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0a1a-123">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="d0a1a-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="d0a1a-124">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="d0a1a-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="d0a1a-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="d0a1a-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
