---
description: Contiene la cámara extrinsics para el ejemplo.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: MFSampleExtension_CameraExtrinsics atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666779"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a><span data-ttu-id="399ea-103">\_Atributo CameraExtrinsics de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="399ea-103">MFSampleExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="399ea-104">Contiene la cámara extrinsics para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="399ea-104">Contains the camera extrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="399ea-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="399ea-105">Data type</span></span>

<span data-ttu-id="399ea-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="399ea-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="399ea-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="399ea-107">Get/set</span></span>

<span data-ttu-id="399ea-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="399ea-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="399ea-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="399ea-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="399ea-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="399ea-110">Applies to</span></span>

[<span data-ttu-id="399ea-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="399ea-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="399ea-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="399ea-112">Remarks</span></span>

<span data-ttu-id="399ea-113">El valor del atributo es [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="399ea-113">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

<span data-ttu-id="399ea-114">Este atributo es opcional para admitir cámaras que no estén calibradas.</span><span class="sxs-lookup"><span data-stu-id="399ea-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="399ea-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="399ea-115">Requirements</span></span>



| <span data-ttu-id="399ea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="399ea-116">Requirement</span></span> | <span data-ttu-id="399ea-117">Value</span><span class="sxs-lookup"><span data-stu-id="399ea-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="399ea-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="399ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="399ea-119">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="399ea-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="399ea-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="399ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="399ea-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="399ea-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="399ea-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="399ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="399ea-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="399ea-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="399ea-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="399ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="399ea-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="399ea-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




