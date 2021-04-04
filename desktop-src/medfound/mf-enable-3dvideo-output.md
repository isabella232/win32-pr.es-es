---
description: Especifica cómo una transformación de Media Foundation (MFT) debe generar una secuencia de vídeo Stereoscopic 3D.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: MF_ENABLE_3DVIDEO_OUTPUT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908461"
---
# <a name="mf_enable_3dvideo_output-attribute"></a><span data-ttu-id="13c54-103">MF \_ habilitar \_ atributo de salida de 3DVIDEO \_</span><span class="sxs-lookup"><span data-stu-id="13c54-103">MF\_ENABLE\_3DVIDEO\_OUTPUT attribute</span></span>

<span data-ttu-id="13c54-104">Especifica cómo una transformación de Media Foundation (MFT) debe generar una secuencia de vídeo Stereoscopic 3D.</span><span class="sxs-lookup"><span data-stu-id="13c54-104">Specifies how a Media Foundation transform (MFT) should output a 3D stereoscopic video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="13c54-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="13c54-105">Data type</span></span>

<span data-ttu-id="13c54-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="13c54-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="13c54-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13c54-107">Remarks</span></span>

<span data-ttu-id="13c54-108">El valor del atributo es un miembro de la enumeración [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .</span><span class="sxs-lookup"><span data-stu-id="13c54-108">The value of the attribute is a member of the [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) enumeration.</span></span>

<span data-ttu-id="13c54-109">Este atributo solo se aplica si MFT devuelve **true** para el [atributo \_ \_ 3DVIDEO de compatibilidad con MFT](mft-support-3dvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="13c54-109">This attribute applies only if the MFT returns **TRUE** for the [MFT\_SUPPORT\_3DVIDEO](mft-support-3dvideo.md) attribute.</span></span>

<span data-ttu-id="13c54-110">Para obtener o establecer este atributo, llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global de MFT.</span><span class="sxs-lookup"><span data-stu-id="13c54-110">To get or set this attribute call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c54-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13c54-111">Requirements</span></span>



| <span data-ttu-id="13c54-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="13c54-112">Requirement</span></span> | <span data-ttu-id="13c54-113">Value</span><span class="sxs-lookup"><span data-stu-id="13c54-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c54-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13c54-114">Minimum supported client</span></span><br/> | <span data-ttu-id="13c54-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="13c54-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="13c54-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13c54-116">Minimum supported server</span></span><br/> | <span data-ttu-id="13c54-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="13c54-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="13c54-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13c54-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="13c54-119"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="13c54-119"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c54-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="13c54-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c54-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13c54-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




