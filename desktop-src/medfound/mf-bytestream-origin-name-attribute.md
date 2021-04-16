---
description: Especifica la dirección URL original de un flujo de bytes.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: MF_BYTESTREAM_ORIGIN_NAME atributo (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686972"
---
# <a name="mf_bytestream_origin_name-attribute"></a><span data-ttu-id="0ae6e-103">\_Atributo de \_ nombre de origen MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="0ae6e-103">MF\_BYTESTREAM\_ORIGIN\_NAME attribute</span></span>

<span data-ttu-id="0ae6e-104">Especifica la dirección URL original de un flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-104">Specifies the original URL for a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="0ae6e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0ae6e-105">Data type</span></span>

<span data-ttu-id="0ae6e-106">Cadena de caracteres anchos</span><span class="sxs-lookup"><span data-stu-id="0ae6e-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="0ae6e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ae6e-107">Remarks</span></span>

<span data-ttu-id="0ae6e-108">Los flujos de bytes basados en archivos pueden admitir este atributo.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-108">File-based byte streams can support this attribute.</span></span> <span data-ttu-id="0ae6e-109">El valor del atributo se establece cuando se crea el flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-109">The attribute value is set when the byte stream is created.</span></span> <span data-ttu-id="0ae6e-110">Para obtener el valor del atributo, consulte el objeto de flujo de bytes para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="0ae6e-110">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="0ae6e-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ae6e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ae6e-112">Requirements</span></span>



| <span data-ttu-id="0ae6e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ae6e-113">Requirement</span></span> | <span data-ttu-id="0ae6e-114">Value</span><span class="sxs-lookup"><span data-stu-id="0ae6e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae6e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ae6e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0ae6e-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="0ae6e-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="0ae6e-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ae6e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0ae6e-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="0ae6e-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="0ae6e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ae6e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ae6e-120"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ae6e-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ae6e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ae6e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ae6e-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0ae6e-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ae6e-123">Atributos de secuencia de bytes</span><span class="sxs-lookup"><span data-stu-id="0ae6e-123">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ae6e-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="0ae6e-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="0ae6e-125">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="0ae6e-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="0ae6e-126">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="0ae6e-126">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




