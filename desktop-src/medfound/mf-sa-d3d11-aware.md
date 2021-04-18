---
description: Especifica si una transformación de Media Foundation (MFT) es compatible con Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: MF_SA_D3D11_AWARE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360434"
---
# <a name="mf_sa_d3d11_aware-attribute"></a><span data-ttu-id="f69e2-103">\_ \_ Atributo compatible con D3D11 de MF SA \_</span><span class="sxs-lookup"><span data-stu-id="f69e2-103">MF\_SA\_D3D11\_AWARE attribute</span></span>

<span data-ttu-id="f69e2-104">Especifica si una transformación de Media Foundation (MFT) es compatible con Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="f69e2-104">Specifies whether a Media Foundation transform (MFT) supports Microsoft Direct3D 11.</span></span>

## <a name="data-type"></a><span data-ttu-id="f69e2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f69e2-105">Data type</span></span>

<span data-ttu-id="f69e2-106">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="f69e2-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f69e2-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f69e2-107">Remarks</span></span>

<span data-ttu-id="f69e2-108">Este atributo solo se aplica a MFTs de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f69e2-108">This attribute applies only to video MFTs.</span></span> <span data-ttu-id="f69e2-109">Para consultar este atributo, llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos de MFT.</span><span class="sxs-lookup"><span data-stu-id="f69e2-109">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT attribute store.</span></span> <span data-ttu-id="f69e2-110">Si **GetAttributes** se realiza correctamente, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f69e2-110">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

-   <span data-ttu-id="f69e2-111">Si el atributo es distinto de cero, el cliente puede dar a la MFT un puntero a la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) antes de que se inicie el streaming.</span><span class="sxs-lookup"><span data-stu-id="f69e2-111">If the attribute is nonzero, the client can give the MFT a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface before streaming starts.</span></span> <span data-ttu-id="f69e2-112">Para ello, el cliente envía el mensaje [**de \_ \_ Administrador de \_ D3D \_ de conjunto de mensajes MFT**](mft-message-set-d3d-manager.md) a la MFT.</span><span class="sxs-lookup"><span data-stu-id="f69e2-112">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="f69e2-113">No es necesario que el cliente envíe este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f69e2-113">The client is not required to send this message.</span></span>
-   <span data-ttu-id="f69e2-114">Si este atributo es cero (**false**), el MFT no es compatible con Direct3D 11 y el cliente no debe enviar el mensaje de [**Administrador de D3D del \_ conjunto de mensajes \_ \_ \_ MFT**](mft-message-set-d3d-manager.md) a la MFT.</span><span class="sxs-lookup"><span data-stu-id="f69e2-114">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 11, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="f69e2-115">El valor predeterminado de este atributo es **false**.</span><span class="sxs-lookup"><span data-stu-id="f69e2-115">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="f69e2-116">Trate este atributo como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f69e2-116">Treat this attribute as read-only.</span></span> <span data-ttu-id="f69e2-117">No cambie el valor; la MFT omitirá cualquier cambio en el valor.</span><span class="sxs-lookup"><span data-stu-id="f69e2-117">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f69e2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f69e2-118">Requirements</span></span>



| <span data-ttu-id="f69e2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f69e2-119">Requirement</span></span> | <span data-ttu-id="f69e2-120">Value</span><span class="sxs-lookup"><span data-stu-id="f69e2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f69e2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f69e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f69e2-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="f69e2-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f69e2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f69e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f69e2-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="f69e2-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f69e2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f69e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f69e2-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f69e2-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f69e2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f69e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f69e2-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f69e2-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f69e2-129">Compatibilidad con la descodificación de vídeo Direct3D 11 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f69e2-129">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




