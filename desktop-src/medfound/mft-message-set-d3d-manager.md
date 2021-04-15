---
description: Establece o borra el Administrador de dispositivos de Direct3D para DirectX video Accereration (DXVA).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715789"
---
# <a name="mft_message_set_d3d_manager"></a><span data-ttu-id="a6c3c-103">\_ \_ Administrador D3D de conjunto de mensajes de \_ MFT \_</span><span class="sxs-lookup"><span data-stu-id="a6c3c-103">MFT\_MESSAGE\_SET\_D3D\_MANAGER</span></span>

<span data-ttu-id="a6c3c-104">Establece o borra el [Administrador de dispositivos de Direct3D](direct3d-device-manager.md) para DirectX video ACCERERATION (DXVA).</span><span class="sxs-lookup"><span data-stu-id="a6c3c-104">Sets or clears the [Direct3D Device Manager](direct3d-device-manager.md) for DirectX Video Accereration (DXVA).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="a6c3c-105">Parámetro de mensaje</span><span class="sxs-lookup"><span data-stu-id="a6c3c-105">Message Parameter</span></span>

<span data-ttu-id="a6c3c-106">Cuando se inicia el streaming, el parámetro *ulParam* contiene un puntero **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="a6c3c-106">When streaming begins, the *ulParam* parameter contains an **IUnknown** pointer.</span></span> <span data-ttu-id="a6c3c-107">La MFT consultará este puntero para la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) para Direct3D 9 y la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) para Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="a6c3c-107">The MFT will query this pointer for the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface for Direct3D 9 and the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface for Direct3D 11.</span></span> <span data-ttu-id="a6c3c-108">Cuando se detiene el streaming, *ulParameter* contiene el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="a6c3c-108">When streaming stops, the *ulParameter* contains the value **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6c3c-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6c3c-109">Remarks</span></span>

<span data-ttu-id="a6c3c-110">Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="a6c3c-110">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="a6c3c-111">Este mensaje se aplica solo a las transformaciones de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a6c3c-111">This message applies only to video transforms.</span></span> <span data-ttu-id="a6c3c-112">El cliente no debe enviar este mensaje a menos que la MFT devuelva el **valor true** para el atributo [**MF \_ SA \_ \_ compatible**](mf-sa-d3d-aware-attribute.md) con el D3D ([MF \_ SA \_ D3D11 \_ compatible](mf-sa-d3d11-aware.md) con Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="a6c3c-112">The client should not send this message unless the MFT returns **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute ([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span>

<span data-ttu-id="a6c3c-113">No envíe este mensaje a una MFT con varios genera.</span><span class="sxs-lookup"><span data-stu-id="a6c3c-113">Do not send this message to an MFT with multiple ouputs.</span></span>

### <a name="implementation"></a><span data-ttu-id="a6c3c-114">Implementación</span><span class="sxs-lookup"><span data-stu-id="a6c3c-114">Implementation</span></span>

<span data-ttu-id="a6c3c-115">Un MFT solo debe admitir este mensaje si MFT usa la aceleración de vídeo de DirectX para el procesamiento o la descodificación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a6c3c-115">An MFT should support this message only if the MFT uses DirectX Video Acceleration for video processing or decoding.</span></span>

<span data-ttu-id="a6c3c-116">Si un MFT es compatible con este mensaje, también debe implementar el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) y devolver el valor **true** para el atributo MF de ([MF \_ SA \_ D3D11 \_](mf-sa-d3d11-aware.md) para Direct3D 11). [**\_ \_ \_**](mf-sa-d3d-aware-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="a6c3c-116">If an MFT supports this message, it should also implement the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method and return the value **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute (([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span> <span data-ttu-id="a6c3c-117">Este atributo informa al cliente de que el cliente debe enviar el mensaje **de \_ \_ Administrador de \_ D3D \_ del conjunto de mensajes de MFT** a la MFT antes de comenzar la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="a6c3c-117">This attribute informs the client that the client should send the **MFT\_MESSAGE\_SET\_D3D\_MANAGER** message to the MFT before streaming begins.</span></span>

<span data-ttu-id="a6c3c-118">Si una MFT no admite este mensaje, debe devolver **E \_ NOTIMPL** desde [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="a6c3c-118">If an MFT does not support this message, it should return **E\_NOTIMPL** from [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span> <span data-ttu-id="a6c3c-119">Esta es una excepción a la regla general de que una MFT puede devolver **S \_ correcto** desde cualquier mensaje que omita.</span><span class="sxs-lookup"><span data-stu-id="a6c3c-119">This is an exception to the general rule that an MFT can return **S\_OK** from any message it ignores.</span></span>

<span data-ttu-id="a6c3c-120">Para obtener más información, consulte [MFTs compatible con Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="a6c3c-120">For more information, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6c3c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6c3c-121">Requirements</span></span>



| <span data-ttu-id="a6c3c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6c3c-122">Requirement</span></span> | <span data-ttu-id="a6c3c-123">Value</span><span class="sxs-lookup"><span data-stu-id="a6c3c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6c3c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6c3c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a6c3c-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6c3c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6c3c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6c3c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a6c3c-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6c3c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6c3c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6c3c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6c3c-129"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6c3c-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6c3c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6c3c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6c3c-131">MFTs compatible con Direct3D</span><span class="sxs-lookup"><span data-stu-id="a6c3c-131">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="a6c3c-132">Compatibilidad con DXVA 2,0 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6c3c-132">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a6c3c-133">Compatibilidad con la descodificación de vídeo Direct3D 11 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a6c3c-133">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a6c3c-134">**\_tipo de mensaje de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="a6c3c-134">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




