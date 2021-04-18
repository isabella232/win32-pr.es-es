---
description: Contiene los intrínsecos de la cámara pinhole para el ejemplo.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: MFSampleExtension_PinholeCameraIntrinsics atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720491"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="af5e5-103">\_Atributo PinholeCameraIntrinsics de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="af5e5-103">MFSampleExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="af5e5-104">Contiene los intrínsecos de la cámara pinhole para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="af5e5-104">Contains the pinhole camera intrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="af5e5-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="af5e5-105">Data type</span></span>

<span data-ttu-id="af5e5-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="af5e5-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="af5e5-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="af5e5-107">Get/set</span></span>

<span data-ttu-id="af5e5-108">Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="af5e5-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="af5e5-109">Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="af5e5-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="af5e5-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="af5e5-110">Applies to</span></span>

[<span data-ttu-id="af5e5-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="af5e5-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="af5e5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af5e5-112">Remarks</span></span>

<span data-ttu-id="af5e5-113">El valor del atributo es [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span><span class="sxs-lookup"><span data-stu-id="af5e5-113">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

<span data-ttu-id="af5e5-114">Este atributo es opcional para admitir cámaras que no estén calibradas.</span><span class="sxs-lookup"><span data-stu-id="af5e5-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5e5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af5e5-115">Requirements</span></span>



| <span data-ttu-id="af5e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af5e5-116">Requirement</span></span> | <span data-ttu-id="af5e5-117">Value</span><span class="sxs-lookup"><span data-stu-id="af5e5-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af5e5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af5e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af5e5-119">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="af5e5-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af5e5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af5e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af5e5-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="af5e5-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="af5e5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af5e5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af5e5-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="af5e5-123"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




