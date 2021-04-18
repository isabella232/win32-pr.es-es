---
description: Especifica el número de subprocesos que utilizará el codificador.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: Propiedad MFPKEY_NUMTHREADS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544910"
---
# <a name="mfpkey_numthreads-property"></a><span data-ttu-id="2adce-103">\_Propiedad NUMTHREADS de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="2adce-103">MFPKEY\_NUMTHREADS Property</span></span>

<span data-ttu-id="2adce-104">Especifica el número de subprocesos que utilizará el codificador.</span><span class="sxs-lookup"><span data-stu-id="2adce-104">Specifies the number of threads that the encoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2adce-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2adce-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2adce-106">g \_ wszWMVCNumThreads</span><span class="sxs-lookup"><span data-stu-id="2adce-106">g\_wszWMVCNumThreads</span></span>

## <a name="data-type"></a><span data-ttu-id="2adce-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2adce-107">Data Type</span></span>

<span data-ttu-id="2adce-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2adce-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="2adce-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2adce-109">Default Value</span></span>

<span data-ttu-id="2adce-110">1</span><span class="sxs-lookup"><span data-stu-id="2adce-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="2adce-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2adce-111">Remarks</span></span>

<span data-ttu-id="2adce-112">Este valor está pensado para dividir la codificación en varios subprocesos con el fin de aprovechar los equipos con varios procesadores.</span><span class="sxs-lookup"><span data-stu-id="2adce-112">This value is intended to divide encoding into multiple threads to take advantage of computers with multiple processors.</span></span> <span data-ttu-id="2adce-113">Dividir las tareas de codificación en varios subprocesos puede provocar una ligera disminución de la calidad en comparación con un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="2adce-113">Splitting encoding tasks into multiple threads can cause a slight decrease in quality as compared to a single thread.</span></span>

<span data-ttu-id="2adce-114">Para el codificador de vídeo (wmvencod.dll) lanzado con Windows XP y Windows Vista, esta propiedad debe establecerse en 1, 2 o 4.</span><span class="sxs-lookup"><span data-stu-id="2adce-114">For the video encoder (wmvencod.dll) released with Windows XP and Windows Vista, this property should be set to 1, 2, or 4.</span></span> <span data-ttu-id="2adce-115">Otros valores se redondean hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="2adce-115">Other values will be rounded down.</span></span>

<span data-ttu-id="2adce-116">En el caso del codificador de vídeo (wmvencod.dll) lanzado con Windows 7, esta propiedad debe establecerse en 1, 2, 4 u 8.</span><span class="sxs-lookup"><span data-stu-id="2adce-116">For the video encoder (wmvencod.dll) released with Windows 7, this property should be set to 1, 2, 4, or 8.</span></span> <span data-ttu-id="2adce-117">Otros valores se redondean hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="2adce-117">Other values will be rounded down.</span></span>

## <a name="requirements"></a><span data-ttu-id="2adce-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2adce-118">Requirements</span></span>



| <span data-ttu-id="2adce-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2adce-119">Requirement</span></span> | <span data-ttu-id="2adce-120">Value</span><span class="sxs-lookup"><span data-stu-id="2adce-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2adce-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2adce-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2adce-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2adce-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2adce-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2adce-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2adce-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2adce-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2adce-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2adce-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2adce-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2adce-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2adce-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2adce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2adce-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2adce-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




