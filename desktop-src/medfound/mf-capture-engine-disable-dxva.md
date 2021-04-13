---
description: Especifica si el motor de captura utiliza la aceleración de vídeo DirectX (DXVA) para la descodificación de vídeo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360386"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a><span data-ttu-id="4ed38-103">\_Módulo de captura MF \_ \_ deshabilitar el \_ atributo DXVA</span><span class="sxs-lookup"><span data-stu-id="4ed38-103">MF\_CAPTURE\_ENGINE\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="4ed38-104">Especifica si el motor de captura utiliza la aceleración de vídeo DirectX (DXVA) para la descodificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4ed38-104">Specifies whether the capture engine uses DirectX Video Acceleration (DXVA) for video decoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="4ed38-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4ed38-105">Data type</span></span>

<span data-ttu-id="4ed38-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4ed38-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed38-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ed38-107">Remarks</span></span>

<span data-ttu-id="4ed38-108">Este atributo se aplica si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="4ed38-108">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="4ed38-109">El motor de captura descodifica una secuencia de vídeo comprimida desde el dispositivo de captura (por ejemplo, si el dispositivo de captura emite el vídeo H. 264).</span><span class="sxs-lookup"><span data-stu-id="4ed38-109">The capture engine decodes a compressed video stream from the capture device (for example, if the capture device outputs H.264 video).</span></span>
-   <span data-ttu-id="4ed38-110">El descodificador de vídeo admite la descodificación acelerada por hardware mediante DXVA.</span><span class="sxs-lookup"><span data-stu-id="4ed38-110">The video decoder supports hardware-accelerated decoding using DXVA.</span></span>
-   <span data-ttu-id="4ed38-111">La aplicación utiliza el atributo de [Administrador de D3D del \_ motor de captura \_ \_ \_ MF](mf-capture-engine-d3d-manager.md) para establecer la administrador de dispositivos de DXGI en el motor de captura.</span><span class="sxs-lookup"><span data-stu-id="4ed38-111">The application uses the [MF\_CAPTURE\_ENGINE\_D3D\_MANAGER](mf-capture-engine-d3d-manager.md) attribute to set the DXGI Device Manager on the capture engine.</span></span>

<span data-ttu-id="4ed38-112">De lo contrario, se omite este atributo.</span><span class="sxs-lookup"><span data-stu-id="4ed38-112">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="4ed38-113">Este atributo permite a la aplicación deshabilitar DXVA mientras se está descodificando en superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4ed38-113">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="4ed38-114">El valor predeterminado de este atributo es **false**, lo que significa que la descodificación de DXVA está habilitada cuando está disponible.</span><span class="sxs-lookup"><span data-stu-id="4ed38-114">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed38-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ed38-115">Requirements</span></span>



| <span data-ttu-id="4ed38-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ed38-116">Requirement</span></span> | <span data-ttu-id="4ed38-117">Value</span><span class="sxs-lookup"><span data-stu-id="4ed38-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed38-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ed38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed38-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ed38-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="4ed38-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ed38-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed38-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4ed38-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4ed38-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ed38-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed38-123"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ed38-123"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed38-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ed38-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed38-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ed38-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ed38-126">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="4ed38-126">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ed38-127">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="4ed38-127">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




