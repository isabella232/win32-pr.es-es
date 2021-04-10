---
description: Establece el modo de procesamiento del Video Stabilization MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: MF_VIDEODSP_MODE atributo (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154973"
---
# <a name="mf_videodsp_mode-attribute"></a><span data-ttu-id="99ea8-103">\_Atributo de \_ modo MF VIDEODSP</span><span class="sxs-lookup"><span data-stu-id="99ea8-103">MF\_VIDEODSP\_MODE attribute</span></span>

<span data-ttu-id="99ea8-104">Establece el modo de procesamiento del [**video stabilization MFT**](video-stabilization-mft.md).</span><span class="sxs-lookup"><span data-stu-id="99ea8-104">Sets the processing mode of the [**Video Stabilization MFT**](video-stabilization-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="99ea8-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="99ea8-105">Data type</span></span>

<span data-ttu-id="99ea8-106">**MFVideoDSPMode** almacenado como **UIINT32**</span><span class="sxs-lookup"><span data-stu-id="99ea8-106">**MFVideoDSPMode** stored as **UIINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="99ea8-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99ea8-107">Remarks</span></span>

<span data-ttu-id="99ea8-108">El valor de este atributo es un valor de enumeración [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="99ea8-108">The value of this attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="99ea8-109">Este atributo se puede usar para habilitar o deshabilitar la estabilización de la imagen y se puede actualizar para cada ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="99ea8-109">This attribute can be used to enable or disable the image stabilization, and can be updated for each output sample.</span></span>

<span data-ttu-id="99ea8-110">Para establecer este atributo:</span><span class="sxs-lookup"><span data-stu-id="99ea8-110">To set this attribute:</span></span>

1.  <span data-ttu-id="99ea8-111">Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el MFT de estabilización de vídeo para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="99ea8-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video stabilization MFT to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="99ea8-112">Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para establecer el atributo.</span><span class="sxs-lookup"><span data-stu-id="99ea8-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="99ea8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99ea8-113">Requirements</span></span>



| <span data-ttu-id="99ea8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="99ea8-114">Requirement</span></span> | <span data-ttu-id="99ea8-115">Value</span><span class="sxs-lookup"><span data-stu-id="99ea8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99ea8-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99ea8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99ea8-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="99ea8-117">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="99ea8-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99ea8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99ea8-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="99ea8-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99ea8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99ea8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99ea8-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="99ea8-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99ea8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="99ea8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ea8-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="99ea8-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="99ea8-124">**Video Stabilization MFT**</span><span class="sxs-lookup"><span data-stu-id="99ea8-124">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




