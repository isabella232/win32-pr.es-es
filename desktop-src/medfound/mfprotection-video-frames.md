---
description: Especifica si se permite a una aplicación el acceso a fotogramas de vídeo sin comprimir.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: MFPROTECTION_VIDEO_FRAMES atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706129"
---
# <a name="mfprotection_video_frames-attribute"></a><span data-ttu-id="befc4-103">MFPROTECTION \_ \_ atributo de fotogramas de vídeo</span><span class="sxs-lookup"><span data-stu-id="befc4-103">MFPROTECTION\_VIDEO\_FRAMES attribute</span></span>

<span data-ttu-id="befc4-104">Especifica si se permite a una aplicación el acceso a fotogramas de vídeo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="befc4-104">Specifies if an application is allowed access to uncompressed video frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="befc4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="befc4-105">Data type</span></span>

<span data-ttu-id="befc4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="befc4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="befc4-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="befc4-107">Remarks</span></span>

<span data-ttu-id="befc4-108">Un valor de 0 indica que se permite el acceso a la aplicación a los marcos.</span><span class="sxs-lookup"><span data-stu-id="befc4-108">A value of 0 indicates that the application is allowed access to the frames.</span></span> <span data-ttu-id="befc4-109">Esto puede determinarse como resultado de un acuerdo privado entre la aplicación y el sistema de protección de contenido determinado en uso.</span><span class="sxs-lookup"><span data-stu-id="befc4-109">This might be determined as a result of a private agreement between the application and the particular content protection system in use.</span></span>

<span data-ttu-id="befc4-110">Un valor de 1 indica que se permite el acceso de la aplicación a los marcos si la aplicación proporciona un certificado de aplicación válido (vea [**IMFMediaEngineProtectedContent:: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span><span class="sxs-lookup"><span data-stu-id="befc4-110">A value of 1 indicates that the application is allowed access to frames if a valid application certificate is provided by the application (see [**IMFMediaEngineProtectedContent::SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span></span>

<span data-ttu-id="befc4-111">Un valor de 0xFFFFFFFF, que es el valor predeterminado, indica que no se permite el acceso a las aplicaciones a los marcos sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="befc4-111">A value of 0xFFFFFFFF, which is the default value, indicates no applications are allowed access to uncompressed frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="befc4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="befc4-112">Requirements</span></span>



| <span data-ttu-id="befc4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="befc4-113">Requirement</span></span> | <span data-ttu-id="befc4-114">Value</span><span class="sxs-lookup"><span data-stu-id="befc4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="befc4-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="befc4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="befc4-116">\[Solo aplicaciones para UWP de Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="befc4-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="befc4-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="befc4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="befc4-118">\[Solo aplicaciones para UWP de Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="befc4-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="befc4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="befc4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="befc4-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="befc4-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="befc4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="befc4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befc4-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="befc4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="befc4-123">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="befc4-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




