---
description: Establece un puntero al Administrador de dispositivos de DXGI en el motor de captura.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: MF_CAPTURE_ENGINE_D3D_MANAGER atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154645"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a><span data-ttu-id="a04f4-103">\_Atributo de \_ Administrador de D3D del motor de captura MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="a04f4-103">MF\_CAPTURE\_ENGINE\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="a04f4-104">Establece un puntero al Administrador de dispositivos de DXGI en el motor de captura.</span><span class="sxs-lookup"><span data-stu-id="a04f4-104">Sets a pointer to the DXGI Device Manager on the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="a04f4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a04f4-105">Data type</span></span>

<span data-ttu-id="a04f4-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="a04f4-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="a04f4-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a04f4-107">Remarks</span></span>

<span data-ttu-id="a04f4-108">El valor de este atributo es un puntero a la interfaz [_ *IMFDXGIDeviceManager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="a04f4-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span> <span data-ttu-id="a04f4-109">Este atributo permite al motor de captura asignar fotogramas de vídeo mediante superficies de DXGI y usar la aceleración de hardware para la descodificación y el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a04f4-109">This attribute enables the capture engine to allocate video frames using DXGI surfaces, and to use hardware acceleration for decoding and video processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="a04f4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a04f4-110">Requirements</span></span>



| <span data-ttu-id="a04f4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a04f4-111">Requirement</span></span> | <span data-ttu-id="a04f4-112">Value</span><span class="sxs-lookup"><span data-stu-id="a04f4-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a04f4-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a04f4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a04f4-114">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a04f4-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a04f4-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a04f4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a04f4-116">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a04f4-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a04f4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a04f4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a04f4-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04f4-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04f4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="a04f4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04f4-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a04f4-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a04f4-121">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="a04f4-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="a04f4-122">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="a04f4-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




