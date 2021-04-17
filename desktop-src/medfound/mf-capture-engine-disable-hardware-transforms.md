---
description: Deshabilita el uso de transformaciones de Media Foundation basadas en hardware (MFTs) en el motor de captura.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715653"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a><span data-ttu-id="8c9ac-103">El \_ \_ atributo de \_ \_ transformaciones de hardware deshabilitar el motor de captura MF \_</span><span class="sxs-lookup"><span data-stu-id="8c9ac-103">MF\_CAPTURE\_ENGINE\_DISABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="8c9ac-104">Deshabilita el uso de transformaciones de Media Foundation basadas en hardware (MFTs) en el motor de captura.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-104">Disables the use of hardware-based Media Foundation transforms (MFTs) in the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c9ac-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8c9ac-105">Data type</span></span>

<span data-ttu-id="8c9ac-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8c9ac-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8c9ac-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c9ac-107">Remarks</span></span>

<span data-ttu-id="8c9ac-108">De forma predeterminada, el motor de captura utiliza descodificadores o codificadores de hardware.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-108">By default, the capture engine uses hardware decoders or encoders.</span></span> <span data-ttu-id="8c9ac-109">Para deshabilitar el uso de MFTs de hardware, establezca este atributo en **true** al crear el motor de captura.</span><span class="sxs-lookup"><span data-stu-id="8c9ac-109">To disable the use of hardware MFTs, set this attribute to **TRUE** when you create the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9ac-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c9ac-110">Requirements</span></span>



| <span data-ttu-id="8c9ac-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c9ac-111">Requirement</span></span> | <span data-ttu-id="8c9ac-112">Value</span><span class="sxs-lookup"><span data-stu-id="8c9ac-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9ac-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c9ac-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9ac-114">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c9ac-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8c9ac-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c9ac-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9ac-116">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c9ac-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8c9ac-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c9ac-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c9ac-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c9ac-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c9ac-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c9ac-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c9ac-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c9ac-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c9ac-121">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="8c9ac-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c9ac-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="8c9ac-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




