---
description: Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por MFPKEY \_ RMAX).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: Propiedad MFPKEY_BMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697699"
---
# <a name="mfpkey_bmax-property"></a><span data-ttu-id="58264-103">\_Propiedad Bmax de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="58264-103">MFPKEY\_BMAX Property</span></span>

<span data-ttu-id="58264-104">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida en la velocidad de bits máxima (especificada por [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="58264-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by [MFPKEY\_RMAX](mfpkey-rmaxproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="58264-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="58264-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="58264-106">g \_ wszWMVCBMax</span><span class="sxs-lookup"><span data-stu-id="58264-106">g\_wszWMVCBMax</span></span>

## <a name="data-type"></a><span data-ttu-id="58264-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="58264-107">Data Type</span></span>

<span data-ttu-id="58264-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="58264-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="58264-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="58264-109">Default Value</span></span>

<span data-ttu-id="58264-110">No hay valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="58264-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="58264-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58264-111">Remarks</span></span>

<span data-ttu-id="58264-112">Debe establecer este valor para la codificación VBR máxima limitada.</span><span class="sxs-lookup"><span data-stu-id="58264-112">You must set this value for peak-constrained VBR encoding.</span></span> <span data-ttu-id="58264-113">Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que termine de codificar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="58264-113">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="58264-114">El códec interpreta una solicitud de este valor como una señal en la que se encuentra la sesión de codificación. el siguiente ejemplo que se procesa se trata como el principio de una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="58264-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="58264-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58264-115">Requirements</span></span>



| <span data-ttu-id="58264-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="58264-116">Requirement</span></span> | <span data-ttu-id="58264-117">Value</span><span class="sxs-lookup"><span data-stu-id="58264-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58264-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58264-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58264-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="58264-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="58264-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58264-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58264-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="58264-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58264-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58264-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="58264-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="58264-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58264-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="58264-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58264-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58264-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




