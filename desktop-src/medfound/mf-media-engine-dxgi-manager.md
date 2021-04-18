---
description: Establece la infraestructura de gráficos de Microsoft DirectX (DXGI) Administrador de dispositivos en el motor multimedia.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: MF_MEDIA_ENGINE_DXGI_MANAGER atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707529"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a><span data-ttu-id="d4382-103">MF \_ ( \_ atributo de administrador de DXGI de motor multimedia) \_ \_</span><span class="sxs-lookup"><span data-stu-id="d4382-103">MF\_MEDIA\_ENGINE\_DXGI\_MANAGER attribute</span></span>

<span data-ttu-id="d4382-104">Establece la infraestructura de gráficos de Microsoft DirectX (DXGI) Administrador de dispositivos en el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="d4382-104">Sets the Microsoft DirectX Graphics Infrastructure (DXGI) Device Manager on the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4382-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d4382-105">Data type</span></span>

<span data-ttu-id="d4382-106">**IMFDXGIDeviceManager \* *_ se almacena como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="d4382-106">**IMFDXGIDeviceManager\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="d4382-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="d4382-107">Get/set</span></span>

<span data-ttu-id="d4382-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="d4382-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="d4382-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="d4382-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4382-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4382-110">Remarks</span></span>

<span data-ttu-id="d4382-111">El valor de este atributo es un puntero a la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="d4382-111">The value of this attribute is a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="d4382-112">En el modo de servidor de tramas, este atributo permite al motor multimedia usar la aceleración de hardware para la descodificación de vídeo y el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d4382-112">In frame-server mode, this attribute enables the Media Engine to use hardware acceleration for video decoding and video processing.</span></span> <span data-ttu-id="d4382-113">Si no se establece el atributo, el motor multimedia utiliza la descodificación y el procesamiento de software.</span><span class="sxs-lookup"><span data-stu-id="d4382-113">If the attribute is not set, the Media Engine uses software decoding and processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4382-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4382-114">Requirements</span></span>



| <span data-ttu-id="d4382-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4382-115">Requirement</span></span> | <span data-ttu-id="d4382-116">Value</span><span class="sxs-lookup"><span data-stu-id="d4382-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4382-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4382-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d4382-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="d4382-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="d4382-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4382-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d4382-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d4382-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="d4382-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4382-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4382-122"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4382-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4382-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4382-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4382-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4382-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d4382-125">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="d4382-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




