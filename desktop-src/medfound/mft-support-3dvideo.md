---
description: Especifica si una transformación de Media Foundation (MFT) admite vídeo Stereoscopic 3D.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: MFT_SUPPORT_3DVIDEO atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705897"
---
# <a name="mft_support_3dvideo-attribute"></a><span data-ttu-id="f0256-103">\_Atributo 3DVIDEO de compatibilidad con MFT \_</span><span class="sxs-lookup"><span data-stu-id="f0256-103">MFT\_SUPPORT\_3DVIDEO attribute</span></span>

<span data-ttu-id="f0256-104">Especifica si una transformación de Media Foundation (MFT) admite vídeo Stereoscopic 3D.</span><span class="sxs-lookup"><span data-stu-id="f0256-104">Specifies whether a Media Foundation transform (MFT) supports 3D stereoscopic video.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0256-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f0256-105">Data type</span></span>

<span data-ttu-id="f0256-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="f0256-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f0256-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0256-107">Remarks</span></span>

<span data-ttu-id="f0256-108">Para consultar este atributo, llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global de MFT.</span><span class="sxs-lookup"><span data-stu-id="f0256-108">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="f0256-109">Si **GetAttributes** se realiza correctamente, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f0256-109">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f0256-110">El valor predeterminado de este atributo es **false**.</span><span class="sxs-lookup"><span data-stu-id="f0256-110">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="f0256-111">Trate este atributo como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f0256-111">Treat this attribute as read-only.</span></span> <span data-ttu-id="f0256-112">No cambie el valor; la MFT omitirá cualquier cambio en el valor.</span><span class="sxs-lookup"><span data-stu-id="f0256-112">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0256-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0256-113">Requirements</span></span>



| <span data-ttu-id="f0256-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0256-114">Requirement</span></span> | <span data-ttu-id="f0256-115">Value</span><span class="sxs-lookup"><span data-stu-id="f0256-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0256-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0256-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f0256-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="f0256-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f0256-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0256-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f0256-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="f0256-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f0256-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0256-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0256-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0256-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0256-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0256-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0256-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0256-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




