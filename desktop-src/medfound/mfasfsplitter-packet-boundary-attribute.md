---
description: Especifica si un búfer contiene el inicio de un paquete de formato de sistema avanzado (ASF).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: MFASFSPLITTER_PACKET_BOUNDARY atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648226"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a><span data-ttu-id="0cb8b-103">Atributo de límite de \_ paquetes de MFASFSPLITTER \_</span><span class="sxs-lookup"><span data-stu-id="0cb8b-103">MFASFSPLITTER\_PACKET\_BOUNDARY attribute</span></span>

<span data-ttu-id="0cb8b-104">Especifica si un búfer contiene el inicio de un paquete de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="0cb8b-104">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="0cb8b-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0cb8b-105">Data type</span></span>

<span data-ttu-id="0cb8b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0cb8b-106">**UINT32**</span></span>

<span data-ttu-id="0cb8b-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb8b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cb8b-108">Remarks</span></span>

<span data-ttu-id="0cb8b-109">Si un búfer multimedia expone la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a través de **QueryInterface** y el valor de este atributo es distinto de cero, el divisor de ASF trata el búfer como el inicio de un nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-109">If a media buffer exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface through **QueryInterface**, and the value of this attribute is nonzero, the ASF splitter treats the buffer as the start of a new packet.</span></span>

<span data-ttu-id="0cb8b-110">Este atributo se aplica si usa el divisor de ASF para analizar los datos ASF.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-110">This attribute applies if you are using the ASF splitter to parse ASF data.</span></span> <span data-ttu-id="0cb8b-111">Si los datos ASF tienen longitudes de paquetes variables, debe establecer este atributo en los búferes multimedia que pase al método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="0cb8b-111">If your ASF data has variable packet lengths, you must set this attribute on the media buffers that you pass to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="0cb8b-112">Establezca el atributo en **true** si el búfer contiene el inicio de un nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-112">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="0cb8b-113">Si el búfer contiene una continuación del paquete anterior, establezca el atributo en **false**.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-113">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="0cb8b-114">Los búferes no pueden abarcar varios paquetes.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-114">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="0cb8b-115">En el caso de los datos ASF con tamaños de paquete fijos, este atributo no es necesario y un búfer puede abarcar varios paquetes.</span><span class="sxs-lookup"><span data-stu-id="0cb8b-115">For ASF data with fixed packet sizes, this attribute is not required, and a buffer can can span multiple packets.</span></span>

<span data-ttu-id="0cb8b-116">Tenga en cuenta que las implementaciones estándar de los [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) proporcionados por Media Foundation no exponen [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="0cb8b-116">Note that the standard implementations of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) provided by Media Foundation do not expose [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="0cb8b-117">Para usar este atributo, debe proporcionar su propia implementación de **IMFMediaBuffer**; por ejemplo, ajustando los búferes devueltos por [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span><span class="sxs-lookup"><span data-stu-id="0cb8b-117">To use this attribute, you must provide your own implementation of **IMFMediaBuffer**; for example, by wrapping the buffers returned by [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb8b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb8b-118">Requirements</span></span>



| <span data-ttu-id="0cb8b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb8b-119">Requirement</span></span> | <span data-ttu-id="0cb8b-120">Value</span><span class="sxs-lookup"><span data-stu-id="0cb8b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb8b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cb8b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb8b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0cb8b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0cb8b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cb8b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb8b-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0cb8b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0cb8b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cb8b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb8b-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb8b-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb8b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cb8b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb8b-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0cb8b-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0cb8b-129">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="0cb8b-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="0cb8b-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0cb8b-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0cb8b-131">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0cb8b-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0cb8b-132">**IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="0cb8b-132">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




