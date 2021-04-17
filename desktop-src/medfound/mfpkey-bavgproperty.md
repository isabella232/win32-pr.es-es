---
description: Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por MFPKEY \_ RAVG).
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: Propiedad MFPKEY_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697144"
---
# <a name="mfpkey_bavg-property"></a><span data-ttu-id="5ecdd-103">\_Propiedad BAVG de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="5ecdd-103">MFPKEY\_BAVG Property</span></span>

<span data-ttu-id="5ecdd-104">Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida con la velocidad de bits media (especificada por [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="5ecdd-104">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by [MFPKEY\_RAVG](mfpkey-ravgproperty.md)).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5ecdd-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5ecdd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5ecdd-106">g \_ wszWMVCBAvg</span><span class="sxs-lookup"><span data-stu-id="5ecdd-106">g\_wszWMVCBAvg</span></span>

## <a name="data-type"></a><span data-ttu-id="5ecdd-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5ecdd-107">Data Type</span></span>

<span data-ttu-id="5ecdd-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5ecdd-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5ecdd-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="5ecdd-109">Default Value</span></span>

<span data-ttu-id="5ecdd-110">No hay ningún valor predeterminado, pero el códec calculará un valor adecuado en función de la configuración de VBR limitada.</span><span class="sxs-lookup"><span data-stu-id="5ecdd-110">No default value, but the codec will compute an appropriate value based on the other constrained VBR settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ecdd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ecdd-111">Remarks</span></span>

<span data-ttu-id="5ecdd-112">El códec calcula este valor después de la fase de codificación final.</span><span class="sxs-lookup"><span data-stu-id="5ecdd-112">This value is computed by the codec after the final encoding pass.</span></span> <span data-ttu-id="5ecdd-113">No debe consultar este valor hasta que se complete la codificación.</span><span class="sxs-lookup"><span data-stu-id="5ecdd-113">You should not query for this value until after encoding is complete.</span></span> <span data-ttu-id="5ecdd-114">El códec interpreta una solicitud de este valor como una señal en la que se encuentra la sesión de codificación. el siguiente ejemplo que se procesa se trata como el principio de una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="5ecdd-114">The codec interprets a request for this value as a signal that the encoding session is over; the next sample that you process is treated as the beginning of a new session.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ecdd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ecdd-115">Requirements</span></span>



| <span data-ttu-id="5ecdd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ecdd-116">Requirement</span></span> | <span data-ttu-id="5ecdd-117">Value</span><span class="sxs-lookup"><span data-stu-id="5ecdd-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ecdd-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ecdd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ecdd-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5ecdd-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5ecdd-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ecdd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ecdd-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ecdd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ecdd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ecdd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ecdd-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ecdd-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ecdd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ecdd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ecdd-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5ecdd-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




