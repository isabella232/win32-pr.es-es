---
description: Especifica el número de fotogramas de vídeo que se omiten porque eran duplicados de fotogramas anteriores.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: Propiedad MFPKEY_ZEROBYTEFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908382"
---
# <a name="mfpkey_zerobyteframes-property"></a><span data-ttu-id="e469a-103">\_Propiedad ZEROBYTEFRAMES de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="e469a-103">MFPKEY\_ZEROBYTEFRAMES Property</span></span>

<span data-ttu-id="e469a-104">Especifica el número de fotogramas de vídeo que se omiten porque eran duplicados de fotogramas anteriores.</span><span class="sxs-lookup"><span data-stu-id="e469a-104">Specifies the number of video frames that are skipped because they were duplicates of previous frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e469a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e469a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e469a-106">g \_ wszWMVCZeroByteFrames</span><span class="sxs-lookup"><span data-stu-id="e469a-106">g\_wszWMVCZeroByteFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="e469a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e469a-107">Data Type</span></span>

<span data-ttu-id="e469a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e469a-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="e469a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e469a-109">Remarks</span></span>

<span data-ttu-id="e469a-110">Este valor no se resta del número total de fotogramas pasados ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) al calcular el número de fotogramas codificados ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="e469a-110">This value is not subtracted from the total number of frames passed ([MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md)) when calculating the number of encoded frames ([MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md)).</span></span>

<span data-ttu-id="e469a-111">Puede impedir que el códec omita fotogramas duplicados estableciendo [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="e469a-111">You can stop the codec from skipping duplicate frames by setting [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to VARIANT\_TRUE.</span></span>

<span data-ttu-id="e469a-112">Puede obtener este valor después de haber terminado de pasar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="e469a-112">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="e469a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e469a-113">Requirements</span></span>



| <span data-ttu-id="e469a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e469a-114">Requirement</span></span> | <span data-ttu-id="e469a-115">Value</span><span class="sxs-lookup"><span data-stu-id="e469a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e469a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e469a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e469a-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e469a-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e469a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e469a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e469a-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e469a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e469a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e469a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e469a-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e469a-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e469a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="e469a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e469a-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e469a-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




