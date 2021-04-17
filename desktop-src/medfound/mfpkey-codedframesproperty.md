---
description: Especifica el número de fotogramas de vídeo codificados por el códec.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: Propiedad MFPKEY_CODEDFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667713"
---
# <a name="mfpkey_codedframes-property"></a><span data-ttu-id="ebfb4-103">\_Propiedad CODEDFRAMES de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="ebfb4-103">MFPKEY\_CODEDFRAMES Property</span></span>

<span data-ttu-id="ebfb4-104">Especifica el número de fotogramas de vídeo codificados por el códec.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-104">Specifies the number of video frames encoded by the codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ebfb4-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ebfb4-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ebfb4-106">g \_ wszWMVCCodedFrames</span><span class="sxs-lookup"><span data-stu-id="ebfb4-106">g\_wszWMVCCodedFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="ebfb4-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ebfb4-107">Data Type</span></span>

<span data-ttu-id="ebfb4-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ebfb4-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="ebfb4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebfb4-109">Remarks</span></span>

<span data-ttu-id="ebfb4-110">Este valor es igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos cualquier fotograma que se haya quitado debido a restricciones de velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-110">This value is equal to [MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) minus any frames that were dropped due to bit-rate constraints.</span></span> <span data-ttu-id="ebfb4-111">Puede obtener este valor después de haber terminado de pasar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-111">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebfb4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebfb4-112">Requirements</span></span>



| <span data-ttu-id="ebfb4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebfb4-113">Requirement</span></span> | <span data-ttu-id="ebfb4-114">Value</span><span class="sxs-lookup"><span data-stu-id="ebfb4-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfb4-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebfb4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ebfb4-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ebfb4-116">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ebfb4-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebfb4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ebfb4-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ebfb4-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ebfb4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebfb4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebfb4-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebfb4-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebfb4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebfb4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfb4-122">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ebfb4-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




