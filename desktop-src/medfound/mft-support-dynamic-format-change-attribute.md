---
description: Especifica si una transformación de Media Foundation (MFT) admite cambios de formato dinámico.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706125"
---
# <a name="mft_support_dynamic_format_change-attribute"></a><span data-ttu-id="dafa2-103">El \_ \_ atributo de \_ cambio de formato dinámico \_ de MFT es compatible</span><span class="sxs-lookup"><span data-stu-id="dafa2-103">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE attribute</span></span>

<span data-ttu-id="dafa2-104">Especifica si una transformación de Media Foundation (MFT) admite cambios de formato dinámico.</span><span class="sxs-lookup"><span data-stu-id="dafa2-104">Specifies whether a Media Foundation transform (MFT) supports dynamic format changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="dafa2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="dafa2-105">Data type</span></span>

<span data-ttu-id="dafa2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dafa2-106">**UINT32**</span></span>

<span data-ttu-id="dafa2-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="dafa2-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dafa2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dafa2-108">Remarks</span></span>

<span data-ttu-id="dafa2-109">Este atributo puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="dafa2-109">This attribute can have the following values.</span></span>



| <span data-ttu-id="dafa2-110">Value</span><span class="sxs-lookup"><span data-stu-id="dafa2-110">Value</span></span>     | <span data-ttu-id="dafa2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dafa2-111">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="dafa2-112">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="dafa2-112">**TRUE**</span></span>  | <span data-ttu-id="dafa2-113">El cliente puede cambiar el formato de entrada durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="dafa2-113">The client can change the input format during streaming.</span></span>               |
| <span data-ttu-id="dafa2-114">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="dafa2-114">**FALSE**</span></span> | <span data-ttu-id="dafa2-115">La MFT se debe purgar antes de que el cliente pueda cambiar el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="dafa2-115">The MFT must be drained before the client can change the input format.</span></span> |



 

<span data-ttu-id="dafa2-116">Para obtener este atributo, primero llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global para MFT.</span><span class="sxs-lookup"><span data-stu-id="dafa2-116">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store for the MFT.</span></span> <span data-ttu-id="dafa2-117">Después, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obtener el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="dafa2-117">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span>

<span data-ttu-id="dafa2-118">Si se produce un error en [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) o el atributo no está presente, el valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="dafa2-118">If [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) fails or the attribute is not present, the default value if **FALSE**.</span></span>

<span data-ttu-id="dafa2-119">Los [MFTs asincrónicos](asynchronous-mfts.md) deben devolver el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="dafa2-119">[Asynchronous MFTs](asynchronous-mfts.md) must return the value **TRUE**.</span></span>

<span data-ttu-id="dafa2-120">Para obtener más información, consulte [control de los cambios de flujo](handling-stream-changes.md).</span><span class="sxs-lookup"><span data-stu-id="dafa2-120">For more information, see [Handling Stream Changes](handling-stream-changes.md).</span></span>

<span data-ttu-id="dafa2-121">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dafa2-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dafa2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dafa2-122">Requirements</span></span>



| <span data-ttu-id="dafa2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dafa2-123">Requirement</span></span> | <span data-ttu-id="dafa2-124">Value</span><span class="sxs-lookup"><span data-stu-id="dafa2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dafa2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dafa2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dafa2-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="dafa2-126">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dafa2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dafa2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dafa2-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="dafa2-128">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dafa2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dafa2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dafa2-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dafa2-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dafa2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="dafa2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dafa2-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dafa2-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dafa2-133">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="dafa2-133">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="dafa2-134">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="dafa2-134">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="dafa2-135">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dafa2-135">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dafa2-136">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dafa2-136">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dafa2-137">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="dafa2-137">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




