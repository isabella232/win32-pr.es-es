---
description: Especifica si una transformación de Media Foundation basado en hardware (MFT) está conectada a otro MFT basado en hardware.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: MFT_CONNECTED_TO_HW_STREAM atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659833"
---
# <a name="mft_connected_to_hw_stream-attribute"></a><span data-ttu-id="37834-103">MFT \_ conectado \_ al \_ atributo de flujo de HW \_</span><span class="sxs-lookup"><span data-stu-id="37834-103">MFT\_CONNECTED\_TO\_HW\_STREAM attribute</span></span>

<span data-ttu-id="37834-104">Especifica si una transformación de Media Foundation basado en hardware (MFT) está conectada a otro MFT basado en hardware.</span><span class="sxs-lookup"><span data-stu-id="37834-104">Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.</span></span>

## <a name="data-type"></a><span data-ttu-id="37834-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="37834-105">Data type</span></span>

<span data-ttu-id="37834-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="37834-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="37834-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="37834-107">Get/set</span></span>

<span data-ttu-id="37834-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="37834-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="37834-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="37834-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="37834-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37834-110">Remarks</span></span>

<span data-ttu-id="37834-111">Normalmente, las aplicaciones no usan este atributo.</span><span class="sxs-lookup"><span data-stu-id="37834-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="37834-112">Este atributo se usa con MFTs basados en hardware.</span><span class="sxs-lookup"><span data-stu-id="37834-112">This attribute is used with hardware-based MFTs.</span></span> <span data-ttu-id="37834-113">Cuando dos MFTs de hardware están conectados en una topología, el cargador de topología establece este atributo en **true** en los objetos siguientes:</span><span class="sxs-lookup"><span data-stu-id="37834-113">When two hardware MFTs are connected within a topology, the topology loader sets this attribute to **TRUE** on the following objects:</span></span>

-   <span data-ttu-id="37834-114">El flujo de salida del MFT ascendente</span><span class="sxs-lookup"><span data-stu-id="37834-114">The output stream of the upstream MFT</span></span>
-   <span data-ttu-id="37834-115">El flujo de entrada del MFT de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="37834-115">The input stream of the downstream MFT</span></span>

<span data-ttu-id="37834-116">Para obtener el almacén de atributos para el flujo de salida, el cargador de topología llama a [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) en el MFT ascendente.</span><span class="sxs-lookup"><span data-stu-id="37834-116">To get the attribute store for the output stream, the topology loader calls [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) on the upstream MFT.</span></span> <span data-ttu-id="37834-117">Para obtener el almacén de atributos para el flujo de entrada, el cargador de topología llama a [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) en el MFT de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="37834-117">To get the attribute store for the input stream, the topology loader calls [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) on the downstream MFT.</span></span>

<span data-ttu-id="37834-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="37834-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="37834-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37834-119">Requirements</span></span>



| <span data-ttu-id="37834-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="37834-120">Requirement</span></span> | <span data-ttu-id="37834-121">Value</span><span class="sxs-lookup"><span data-stu-id="37834-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="37834-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37834-122">Minimum supported client</span></span><br/> | <span data-ttu-id="37834-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="37834-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="37834-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37834-124">Minimum supported server</span></span><br/> | <span data-ttu-id="37834-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="37834-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="37834-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37834-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="37834-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="37834-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37834-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="37834-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37834-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37834-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="37834-130">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="37834-130">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="37834-131">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="37834-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




