---
description: Especifica la duración de una secuencia de bytes, en unidades de 100-nanosegundos.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: MF_BYTESTREAM_DURATION atributo (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360516"
---
# <a name="mf_bytestream_duration-attribute"></a><span data-ttu-id="52591-103">\_Atributo de \_ duración MF BYTESTREAM</span><span class="sxs-lookup"><span data-stu-id="52591-103">MF\_BYTESTREAM\_DURATION attribute</span></span>

<span data-ttu-id="52591-104">Especifica la duración de una secuencia de bytes, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="52591-104">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="52591-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="52591-105">Data type</span></span>

<span data-ttu-id="52591-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="52591-106">**UINT64**</span></span>

<span data-ttu-id="52591-107">Trata como un valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="52591-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52591-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52591-108">Remarks</span></span>

<span data-ttu-id="52591-109">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="52591-109">This attribute is optional.</span></span> <span data-ttu-id="52591-110">Si el objeto que crea el flujo de bytes puede determinar la duración, puede establecer este atributo.</span><span class="sxs-lookup"><span data-stu-id="52591-110">If the object that creates the byte stream can determine the duration, it can set this attribute.</span></span> <span data-ttu-id="52591-111">(Por ejemplo, en un flujo de red, la duración puede ser parte de la descripción de la sesión).</span><span class="sxs-lookup"><span data-stu-id="52591-111">(For example, in a network stream, the duration might be part of the session description.)</span></span>

<span data-ttu-id="52591-112">Para obtener el valor del atributo, llame a **QueryInterface** en el flujo de bytes para obtener un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="52591-112">To get the attribute value, call **QueryInterface** on the byte stream to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="52591-113">Este atributo es un valor con signo, aunque se almacena como **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="52591-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="52591-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="52591-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="52591-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52591-115">Requirements</span></span>



| <span data-ttu-id="52591-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="52591-116">Requirement</span></span> | <span data-ttu-id="52591-117">Value</span><span class="sxs-lookup"><span data-stu-id="52591-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52591-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52591-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52591-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="52591-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="52591-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52591-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52591-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="52591-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="52591-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52591-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="52591-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52591-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52591-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="52591-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52591-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52591-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="52591-126">Atributos de secuencia de bytes</span><span class="sxs-lookup"><span data-stu-id="52591-126">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="52591-127">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="52591-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="52591-128">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="52591-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="52591-129">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="52591-129">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




