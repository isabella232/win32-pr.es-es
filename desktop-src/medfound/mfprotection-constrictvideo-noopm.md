---
description: Este atributo especifica protección adicional ofrecida por una autoridad de confianza de salida de vídeo (OTA) cuando un conector no ofrece protección de la salida.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: MFPROTECTION_CONSTRICTVIDEO_NOOPM atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001455"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a><span data-ttu-id="ec1e3-103">MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM</span><span class="sxs-lookup"><span data-stu-id="ec1e3-103">MFPROTECTION\_CONSTRICTVIDEO\_NOOPM attribute</span></span>

<span data-ttu-id="ec1e3-104">Este atributo especifica protección adicional ofrecida por una autoridad de confianza de salida de vídeo (OTA) cuando un conector no ofrece protección de la salida.</span><span class="sxs-lookup"><span data-stu-id="ec1e3-104">This attribute specifies additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="ec1e3-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ec1e3-105">Data type</span></span>

<span data-ttu-id="ec1e3-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="ec1e3-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="ec1e3-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec1e3-107">Remarks</span></span>

<span data-ttu-id="ec1e3-108">Se trata de una protección adicional que ofrece una autoridad de confianza (OTA) de salida de vídeo cuando un conector no ofrece protección de salida (consulte [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span><span class="sxs-lookup"><span data-stu-id="ec1e3-108">This is an additional protection offered by a video output trust authority(OTA) when a connector does not offer output protection (see [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)).</span></span> <span data-ttu-id="ec1e3-109">En este caso, la OTA puede ofrecer esta protección cuyo efecto es el mismo que el de la protección de [ \_ CONSTRICTVIDEO de MFPROTECTION](mfprotection-constrictvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="ec1e3-109">In this case the OTA may offer this protection whose effect is the same as the [MFPROTECTION\_CONSTRICTVIDEO](mfprotection-constrictvideo.md) protection.</span></span> <span data-ttu-id="ec1e3-110">Esto se define para evitar la confusión con llamadas anteriores a interacciones de [**IMFOutputPolicy:: GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) en las que se usó la presencia de MFPROTECTION \_ CONSTRICTVIDEO Protection para ayudar a identificar el pseudo conector del administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="ec1e3-110">This is defined to avoid confusion with previous calls to [**IMFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interactions where the presence of MFPROTECTION\_CONSTRICTVIDEO protection was used to help identify the desktop window manager pseudo-connector.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec1e3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec1e3-111">Requirements</span></span>



| <span data-ttu-id="ec1e3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec1e3-112">Requirement</span></span> | <span data-ttu-id="ec1e3-113">Value</span><span class="sxs-lookup"><span data-stu-id="ec1e3-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1e3-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec1e3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1e3-115">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="ec1e3-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ec1e3-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec1e3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1e3-117">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec1e3-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ec1e3-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec1e3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec1e3-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec1e3-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec1e3-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec1e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec1e3-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec1e3-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




