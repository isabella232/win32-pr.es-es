---
description: Contiene un puntero al Administrador de dispositivos de Microsoft Direct3D para el lector de origen.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: MF_SOURCE_READER_D3D_MANAGER atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910197"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a><span data-ttu-id="00167-103">\_Atributo de \_ Administrador de D3D de lector de origen MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="00167-103">MF\_SOURCE\_READER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="00167-104">Contiene un puntero al Administrador de dispositivos de Microsoft [Direct3D](direct3d-device-manager.md) para el [lector de origen](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="00167-104">Contains a pointer to the Microsoft [Direct3D Device Manager](direct3d-device-manager.md) for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="00167-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="00167-105">Data type</span></span>

<span data-ttu-id="00167-106">**IDirect3DDeviceManager9 \* o IMFDXGIDeviceManager \*** almacenado como \**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="00167-106">**IDirect3DDeviceManager9\* or IMFDXGIDeviceManager\*** stored as \**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="00167-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="00167-107">Get/set</span></span>

<span data-ttu-id="00167-108">Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="00167-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="00167-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="00167-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="00167-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00167-110">Remarks</span></span>

<span data-ttu-id="00167-111">El valor de este atributo puede ser un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) o a un [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span><span class="sxs-lookup"><span data-stu-id="00167-111">The value of this attribute can be a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface or a [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span></span>

<span data-ttu-id="00167-112">Use este atributo para proporcionar un dispositivo Direct3D para cualquier descodificador de vídeo cargado por el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="00167-112">Use this attribute to provide a Direct3D device for any video decoders loaded by the source reader.</span></span> <span data-ttu-id="00167-113">Si establece este atributo y el descodificador es compatible con Microsoft DirectX video Acceleration (DXVA), el lector de origen usa el dispositivo Direct3D para asignar búferes de vídeo.</span><span class="sxs-lookup"><span data-stu-id="00167-113">If you set this attribute and the decoder supports Microsoft DirectX Video Acceleration (DXVA), the source reader uses the Direct3D device to allocate video buffers.</span></span> <span data-ttu-id="00167-114">Estos búferes son compatibles con el procesador de vídeo DXVA 2.</span><span class="sxs-lookup"><span data-stu-id="00167-114">These buffers are compatible with the DXVA 2 video processor.</span></span> <span data-ttu-id="00167-115">(Consulte el [procesamiento de vídeo de DXVA](dxva-video-processing.md)).</span><span class="sxs-lookup"><span data-stu-id="00167-115">(See [DXVA Video Processing](dxva-video-processing.md).)</span></span>

<span data-ttu-id="00167-116">Utilice este atributo con las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="00167-116">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="00167-117">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="00167-117">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="00167-118">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="00167-118">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="00167-119">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="00167-119">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="00167-120">Normalmente se establece este atributo si se usa el lector de origen para obtener fotogramas de vídeo descodificados y usar Direct3D para mostrar los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="00167-120">Typically you would set this attribute if you are using the source reader to get decoded video frames and using Direct3D to display the frames.</span></span> <span data-ttu-id="00167-121">Al establecer este atributo, el descodificador podrá usar DXVA.</span><span class="sxs-lookup"><span data-stu-id="00167-121">Setting this attribute enables the decoder to use DXVA.</span></span>

<span data-ttu-id="00167-122">No establecería este atributo si:</span><span class="sxs-lookup"><span data-stu-id="00167-122">You would not set this attribute if:</span></span>

-   <span data-ttu-id="00167-123">Está usando el lector de origen para procesar solo audio y no vídeo.</span><span class="sxs-lookup"><span data-stu-id="00167-123">You are using the source reader to process audio only and not video.</span></span>
-   <span data-ttu-id="00167-124">Está obteniendo vídeo comprimido del lector de origen.</span><span class="sxs-lookup"><span data-stu-id="00167-124">You are getting compressed video from the source reader.</span></span> <span data-ttu-id="00167-125">En ese caso, el lector de origen no crea un descodificador.</span><span class="sxs-lookup"><span data-stu-id="00167-125">In that case, the source reader does not create a decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="00167-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00167-126">Requirements</span></span>



| <span data-ttu-id="00167-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="00167-127">Requirement</span></span> | <span data-ttu-id="00167-128">Value</span><span class="sxs-lookup"><span data-stu-id="00167-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00167-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00167-129">Minimum supported client</span></span><br/> | <span data-ttu-id="00167-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="00167-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="00167-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00167-131">Minimum supported server</span></span><br/> | <span data-ttu-id="00167-132">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="00167-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="00167-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00167-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="00167-134"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="00167-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00167-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="00167-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00167-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00167-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00167-137">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="00167-137">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="00167-138">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="00167-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




