---
description: Especifica si una transformación de Media Foundation (MFT) es compatible con la aceleración de vídeo de DirectX (DXVA). Este atributo solo se aplica a MFTs de vídeo.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: MF_SA_D3D_AWARE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706643"
---
# <a name="mf_sa_d3d_aware-attribute"></a><span data-ttu-id="d38d7-104">\_Atributo MF \_ compatible con D3D de SA \_</span><span class="sxs-lookup"><span data-stu-id="d38d7-104">MF\_SA\_D3D\_AWARE attribute</span></span>

<span data-ttu-id="d38d7-105">Especifica si una transformación de Media Foundation (MFT) es compatible con la aceleración de vídeo de DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="d38d7-105">Specifies whether a Media Foundation transform (MFT) supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="d38d7-106">Este atributo solo se aplica a MFTs de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d38d7-106">This attribute applies only to video MFTs.</span></span>

## <a name="data-type"></a><span data-ttu-id="d38d7-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d38d7-107">Data type</span></span>

<span data-ttu-id="d38d7-108">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="d38d7-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d38d7-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d38d7-109">Remarks</span></span>

<span data-ttu-id="d38d7-110">Para consultar este atributo, llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global de MFT.</span><span class="sxs-lookup"><span data-stu-id="d38d7-110">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="d38d7-111">Si **GetAttributes** se realiza correctamente, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d38d7-111">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d38d7-112">Este atributo indica al cliente si el MFT puede usar el vídeo de Direct3D 9:</span><span class="sxs-lookup"><span data-stu-id="d38d7-112">This attribute tells the client whether the MFT can use Direct3D 9 video:</span></span>

-   <span data-ttu-id="d38d7-113">Si el atributo es distinto de cero, el cliente puede dar a la MFT un puntero a la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) antes de que se inicie el streaming.</span><span class="sxs-lookup"><span data-stu-id="d38d7-113">If the attribute is nonzero, the client can give the MFT a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface before streaming starts.</span></span> <span data-ttu-id="d38d7-114">Para ello, el cliente envía el mensaje [**de \_ \_ Administrador de \_ D3D \_ de conjunto de mensajes MFT**](mft-message-set-d3d-manager.md) a la MFT.</span><span class="sxs-lookup"><span data-stu-id="d38d7-114">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="d38d7-115">No es necesario que el cliente envíe este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d38d7-115">The client is not required to send this message.</span></span>
-   <span data-ttu-id="d38d7-116">Si este atributo es cero (**false**), el MFT no es compatible con el vídeo de Direct3D 9 y el cliente no debe enviar el mensaje de [**Administrador de D3D del \_ conjunto de mensajes \_ \_ \_ MFT**](mft-message-set-d3d-manager.md) a la MFT.</span><span class="sxs-lookup"><span data-stu-id="d38d7-116">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 9 video, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="d38d7-117">El valor predeterminado de este atributo es **false**.</span><span class="sxs-lookup"><span data-stu-id="d38d7-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="d38d7-118">Trate este atributo como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d38d7-118">Treat this attribute as read-only.</span></span> <span data-ttu-id="d38d7-119">No cambie el valor; la MFT omitirá cualquier cambio en el valor.</span><span class="sxs-lookup"><span data-stu-id="d38d7-119">Do not change the value; the MFT will ignore any changes to the value.</span></span>

<span data-ttu-id="d38d7-120">Para obtener más información sobre la implementación de este atributo en una MFT personalizada, consulte [MFTs compatible con Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="d38d7-120">For more information about implementing this attribute in a custom MFT, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

<span data-ttu-id="d38d7-121">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d38d7-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="d38d7-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d38d7-122">Examples</span></span>

<span data-ttu-id="d38d7-123">En el código siguiente se comprueba si una MFT es compatible con DXVA.</span><span class="sxs-lookup"><span data-stu-id="d38d7-123">The following code tests whether an MFT supports DXVA.</span></span>


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a><span data-ttu-id="d38d7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d38d7-124">Requirements</span></span>



| <span data-ttu-id="d38d7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d38d7-125">Requirement</span></span> | <span data-ttu-id="d38d7-126">Value</span><span class="sxs-lookup"><span data-stu-id="d38d7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38d7-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d38d7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d38d7-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="d38d7-128">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="d38d7-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d38d7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d38d7-130">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="d38d7-130">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d38d7-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d38d7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d38d7-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="d38d7-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38d7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d38d7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38d7-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d38d7-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d38d7-135">MFTs compatible con Direct3D</span><span class="sxs-lookup"><span data-stu-id="d38d7-135">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="d38d7-136">Compatibilidad con DXVA 2,0 en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d38d7-136">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="d38d7-137">Media Foundation transformaciones</span><span class="sxs-lookup"><span data-stu-id="d38d7-137">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="d38d7-138">Atributos de transformación</span><span class="sxs-lookup"><span data-stu-id="d38d7-138">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="d38d7-139">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d38d7-139">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d38d7-140">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d38d7-140">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d38d7-141">\_ \_ modo DXVA de topología \_ MF</span><span class="sxs-lookup"><span data-stu-id="d38d7-141">MF\_TOPOLOGY\_DXVA\_MODE</span></span>](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




