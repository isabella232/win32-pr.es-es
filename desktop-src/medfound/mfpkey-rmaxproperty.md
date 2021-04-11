---
description: Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la reproducción de velocidad de bits variable (VBR) limitada de dos pasos.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: Propiedad MFPKEY_RMAX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3568e0a3ee506640200413a5dc222c7cccec2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276289"
---
# <a name="mfpkey_rmax-property"></a><span data-ttu-id="a2f16-103">\_Propiedad RMAX de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="a2f16-103">MFPKEY\_RMAX Property</span></span>

<span data-ttu-id="a2f16-104">Especifica la velocidad de bits máxima, en bits por segundo, que se usa para la reproducción de velocidad de bits variable (VBR) limitada de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="a2f16-104">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) playback.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a2f16-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a2f16-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a2f16-106">g \_ wszWMVCMaxBitrate</span><span class="sxs-lookup"><span data-stu-id="a2f16-106">g\_wszWMVCMaxBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="a2f16-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a2f16-107">Data Type</span></span>

<span data-ttu-id="a2f16-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a2f16-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a2f16-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a2f16-109">Default Value</span></span>

<span data-ttu-id="a2f16-110">No hay valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a2f16-110">No default.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2f16-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2f16-111">Remarks</span></span>

<span data-ttu-id="a2f16-112">Este valor representa la velocidad de bits máxima para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a2f16-112">This value represents the peak bit rate for playback.</span></span> <span data-ttu-id="a2f16-113">El valor de [MFPKEY \_ Bmax](mfpkey-bmaxproperty.md) se usa para describir el búfer en términos de esta velocidad de bits; de hecho, la VBR restringida es similar a la velocidad de bits constante (CBR) con este valor como la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="a2f16-113">The value of [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is used to describe the buffer in terms of this bit rate; in effect, constrained VBR is similar to constant bit rate (CBR) using this value as the bit rate.</span></span> <span data-ttu-id="a2f16-114">Sin embargo, una secuencia VBR restringida se puede reproducir a una velocidad de bits más baja, siempre y cuando aumente el búfer.</span><span class="sxs-lookup"><span data-stu-id="a2f16-114">However, a constrained VBR stream can be played back at a lower bit rate, as long as the buffer is increased.</span></span>

<span data-ttu-id="a2f16-115">Debe establecer este valor para la codificación VBR de dos pases restringida.</span><span class="sxs-lookup"><span data-stu-id="a2f16-115">You must set this value for peak-constrained two-pass VBR encoding.</span></span> <span data-ttu-id="a2f16-116">Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que termine de codificar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a2f16-116">After you begin processing samples, you must not query for this value until you are finished encoding the stream.</span></span> <span data-ttu-id="a2f16-117">El codificador interpreta una solicitud para este valor como una señal en la que se ha superado la sesión de codificación; el siguiente ejemplo que se procesa se trata como el principio de una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="a2f16-117">The encoder interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

<span data-ttu-id="a2f16-118">Normalmente, este valor es de dos a tres veces mayor que el valor de [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a2f16-118">Typically, this value is two to three times greater than the value of [MFPKEY\_RAVG](mfpkey-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2f16-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2f16-119">Requirements</span></span>



| <span data-ttu-id="a2f16-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2f16-120">Requirement</span></span> | <span data-ttu-id="a2f16-121">Value</span><span class="sxs-lookup"><span data-stu-id="a2f16-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f16-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2f16-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a2f16-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a2f16-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a2f16-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2f16-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a2f16-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2f16-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a2f16-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2f16-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2f16-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2f16-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2f16-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2f16-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f16-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2f16-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




