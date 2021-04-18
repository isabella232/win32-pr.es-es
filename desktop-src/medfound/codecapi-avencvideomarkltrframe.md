---
description: Marca el marco actual como un marco LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: Propiedad CODECAPI_AVEncVideoMarkLTRFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539622"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a><span data-ttu-id="14d24-103">\_Propiedad AVEncVideoMarkLTRFrame de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="14d24-103">CODECAPI\_AVEncVideoMarkLTRFrame property</span></span>

<span data-ttu-id="14d24-104">Marca el marco actual como un marco LTR.</span><span class="sxs-lookup"><span data-stu-id="14d24-104">Marks the current frame as a LTR frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="14d24-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="14d24-105">Data type</span></span>

<span data-ttu-id="14d24-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="14d24-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="14d24-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="14d24-107">Property GUID</span></span>

<span data-ttu-id="14d24-108">**CODECAPI \_ AVEncVideoMarkLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="14d24-108">**CODECAPI\_AVEncVideoMarkLTRFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="14d24-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14d24-109">Remarks</span></span>

<span data-ttu-id="14d24-110">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="14d24-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="14d24-111">El valor de este control es el valor de la sintaxis H. 264 *LongTermFramIdx* asociada al marco actual.</span><span class="sxs-lookup"><span data-stu-id="14d24-111">The value of this control is the value of H.264 syntax *LongTermFramIdx* associated with the current frame.</span></span> <span data-ttu-id="14d24-112">Si el marco actual no está en el nivel base, por ejemplo, el *\_ identificador temporal* del elemento de sintaxis no es igual a 0, esta propiedad se aplica al siguiente marco de capa base en el orden de codificación.</span><span class="sxs-lookup"><span data-stu-id="14d24-112">If the current frame is not in the base layer, for example syntax element *temporal\_id* is not equal to 0, this property applies to the next base layer frame in encoding order.</span></span>

<span data-ttu-id="14d24-113">No se debe llamar a esta propiedad si se ha emitido una llamada pendiente para marcar un marco LTR mediante la \_ propiedad CODECAPI AVEncVideoMarkLTRFrame y el codificador aún no ha marcado un fotograma como LTR.</span><span class="sxs-lookup"><span data-stu-id="14d24-113">This property should not be called if a pending call to mark an LTR frame has been issued using the CODECAPI\_AVEncVideoMarkLTRFrame property and the encoder has not yet marked a frame as LTR.</span></span> <span data-ttu-id="14d24-114">En otras palabras, el codificador no debe poner en cola \_ las solicitudes de CODECAPI AVEncVideoMarkLTRFrame.</span><span class="sxs-lookup"><span data-stu-id="14d24-114">In other words, the encoder should not queue up CODECAPI\_AVEncVideoMarkLTRFrame requests.</span></span> <span data-ttu-id="14d24-115">Si \_ se envía una solicitud de AVEncVideoMarkLTRFrame de CODECAPI mientras otra solicitud de CODECAPI \_ AVEncVideoMarkLTRFrame todavía está pendiente, se debe quitar la solicitud anterior.</span><span class="sxs-lookup"><span data-stu-id="14d24-115">If a CODECAPI\_AVEncVideoMarkLTRFrame request is submitted while another CODECAPI\_AVEncVideoMarkLTRFrame request is still pending, the older request should be dropped.</span></span>

<span data-ttu-id="14d24-116">La \_ propiedad CODECAPI AVEncVideoMarkLTRFrame es dinámica y se puede establecer durante la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="14d24-116">The CODECAPI\_AVEncVideoMarkLTRFrame property is dynamic and can be set during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d24-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14d24-117">Requirements</span></span>



| <span data-ttu-id="14d24-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d24-118">Requirement</span></span> | <span data-ttu-id="14d24-119">Value</span><span class="sxs-lookup"><span data-stu-id="14d24-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14d24-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14d24-121">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="14d24-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="14d24-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14d24-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="14d24-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="14d24-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14d24-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="14d24-125"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="14d24-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14d24-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="14d24-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d24-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14d24-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




