---
description: Especifica que el codificador MFT admite la recepción de eventos MEEncodingParameter durante el streaming.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: MFT_ENCODER_SUPPORTS_CONFIG_EVENT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659867"
---
# <a name="mft_encoder_supports_config_event-attribute"></a><span data-ttu-id="3a307-103">El \_ codificador MFT \_ admite \_ el \_ atributo de evento de configuración</span><span class="sxs-lookup"><span data-stu-id="3a307-103">MFT\_ENCODER\_SUPPORTS\_CONFIG\_EVENT attribute</span></span>

<span data-ttu-id="3a307-104">Especifica que el codificador MFT admite la recepción de eventos [MEEncodingParameter](meencodingparameters.md) durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="3a307-104">Specifies that the MFT encoder supports receiving [MEEncodingParameter](meencodingparameters.md) events while streaming.</span></span>

## <a name="data-type"></a><span data-ttu-id="3a307-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3a307-105">Data type</span></span>

<span data-ttu-id="3a307-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="3a307-106">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3a307-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a307-107">Remarks</span></span>

<span data-ttu-id="3a307-108">Enviado por el codificador de MFT a través de [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="3a307-108">Sent by the MFT encoder through [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a307-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a307-109">Requirements</span></span>



| <span data-ttu-id="3a307-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a307-110">Requirement</span></span> | <span data-ttu-id="3a307-111">Value</span><span class="sxs-lookup"><span data-stu-id="3a307-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a307-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a307-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3a307-113">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="3a307-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="3a307-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a307-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3a307-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3a307-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="3a307-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a307-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a307-117"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a307-117"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a307-118">IDL</span><span class="sxs-lookup"><span data-stu-id="3a307-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a307-119"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a307-119"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a307-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a307-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a307-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a307-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a307-122">**IMFTransform::P rocessEvent**</span><span class="sxs-lookup"><span data-stu-id="3a307-122">**IMFTransform::ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




