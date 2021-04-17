---
description: En el caso de los tipos de medios YUV, define la matriz de conversión a partir del espacio de colores YCbCr en el espacio de colores RGB.
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: MF_MT_YUV_MATRIX atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c6976e4652c69b3bddc910dcc536a3d07bf39a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653019"
---
# <a name="mf_mt_yuv_matrix-attribute"></a><span data-ttu-id="452a0-103">\_Atributo de matriz MF MT \_ YUV \_</span><span class="sxs-lookup"><span data-stu-id="452a0-103">MF\_MT\_YUV\_MATRIX attribute</span></span>

<span data-ttu-id="452a0-104">En el caso de los tipos de medios YUV, define la matriz de conversión del espacio de colores de Y'Cb'Cr al espacio de colores R'G'B.</span><span class="sxs-lookup"><span data-stu-id="452a0-104">For YUV media types, defines the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space.</span></span>

## <a name="data-type"></a><span data-ttu-id="452a0-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="452a0-105">Data type</span></span>

<span data-ttu-id="452a0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="452a0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="452a0-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="452a0-107">Remarks</span></span>

<span data-ttu-id="452a0-108">El valor de este atributo es un miembro de la enumeración [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) .</span><span class="sxs-lookup"><span data-stu-id="452a0-108">The value of this attribute is a member of the [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) enumeration.</span></span>

<span data-ttu-id="452a0-109">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="452a0-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="452a0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="452a0-110">Requirements</span></span>



| <span data-ttu-id="452a0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="452a0-111">Requirement</span></span> | <span data-ttu-id="452a0-112">Value</span><span class="sxs-lookup"><span data-stu-id="452a0-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="452a0-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="452a0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="452a0-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="452a0-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="452a0-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="452a0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="452a0-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="452a0-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="452a0-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="452a0-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="452a0-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="452a0-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452a0-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="452a0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452a0-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="452a0-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="452a0-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="452a0-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="452a0-122">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="452a0-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="452a0-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="452a0-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="452a0-124">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="452a0-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="452a0-125">Información de color ampliada</span><span class="sxs-lookup"><span data-stu-id="452a0-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




