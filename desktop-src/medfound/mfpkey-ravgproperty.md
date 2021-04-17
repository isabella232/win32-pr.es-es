---
description: Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de dos pasos, de velocidad de bits variable (VBR).
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: Propiedad MFPKEY_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad15d2445dc2acea1e91f4d01fad6e7bd83edb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706209"
---
# <a name="mfpkey_ravg-property"></a><span data-ttu-id="34c22-103">\_Propiedad RAVG de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="34c22-103">MFPKEY\_RAVG Property</span></span>

<span data-ttu-id="34c22-104">Especifica la velocidad de bits media, en bits por segundo, que se usa para la codificación de dos pasos, de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="34c22-104">Specifies the average bit rate, in bits per second, used for 2-pass, variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="34c22-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="34c22-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="34c22-106">g \_ wszWMVCAvgBitrate</span><span class="sxs-lookup"><span data-stu-id="34c22-106">g\_wszWMVCAvgBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="34c22-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="34c22-107">Data Type</span></span>

<span data-ttu-id="34c22-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="34c22-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="34c22-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34c22-109">Remarks</span></span>

<span data-ttu-id="34c22-110">En VBR restringida y sin restricciones, este valor es la velocidad de bits promedio a lo largo de la duración del contenido.</span><span class="sxs-lookup"><span data-stu-id="34c22-110">In both constrained and unconstrained VBR, this value is the average bit rate across the duration of the content.</span></span>

<span data-ttu-id="34c22-111">Debe establecer este valor para ambos modos de codificación VBR de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="34c22-111">You must set this value for both modes of two-pass VBR encoding.</span></span> <span data-ttu-id="34c22-112">Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que termine de codificar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="34c22-112">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="34c22-113">El codificador interpreta una solicitud para este valor como una señal en la que se ha superado la sesión de codificación; el siguiente ejemplo que se procesa se trata como el principio de una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="34c22-113">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="34c22-114">Esta propiedad también se puede leer al final de una sesión de codificación VBR de 1 paso.</span><span class="sxs-lookup"><span data-stu-id="34c22-114">This property can also be read at the end of a 1-pass VBR encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="34c22-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34c22-115">Requirements</span></span>



| <span data-ttu-id="34c22-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="34c22-116">Requirement</span></span> | <span data-ttu-id="34c22-117">Value</span><span class="sxs-lookup"><span data-stu-id="34c22-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34c22-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34c22-118">Minimum supported client</span></span><br/> | <span data-ttu-id="34c22-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="34c22-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="34c22-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34c22-120">Minimum supported server</span></span><br/> | <span data-ttu-id="34c22-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="34c22-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34c22-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34c22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="34c22-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34c22-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34c22-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="34c22-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c22-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34c22-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




