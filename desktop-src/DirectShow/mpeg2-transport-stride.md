---
description: La estructura MPEG2 TRANSPORT STRIDE describe el formato de los paquetes de flujo de transporte \_ \_ MPEG-2 (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE estructura (Bdatypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908493"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="6497f-103">Estructura MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="6497f-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="6497f-104">La estructura describe el formato de los paquetes de flujo de transporte `MPEG2_TRANSPORT_STRIDE` MPEG-2 (TS).</span><span class="sxs-lookup"><span data-stu-id="6497f-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="6497f-105">Esta estructura permite los flujos de transporte en los que los paquetes de transporte de 188 bytes no son contiguos.</span><span class="sxs-lookup"><span data-stu-id="6497f-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="6497f-106">Para esta documentación, estos paquetes se conocen como *paquetes de paso* a paso.</span><span class="sxs-lookup"><span data-stu-id="6497f-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="6497f-107">Los paquetes stride se identifican mediante el siguiente tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="6497f-107">Stride packets are identified by the following media type:</span></span>



| <span data-ttu-id="6497f-108">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="6497f-108">Label</span></span> | <span data-ttu-id="6497f-109">Value</span><span class="sxs-lookup"><span data-stu-id="6497f-109">Value</span></span> |
|-------------|----------------------------------------|
| <span data-ttu-id="6497f-110">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="6497f-110">Major Type</span></span>  | <span data-ttu-id="6497f-111">Secuencia \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="6497f-111">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="6497f-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="6497f-112">Subtype</span></span>     | <span data-ttu-id="6497f-113">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="6497f-113">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="6497f-114">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="6497f-114">Format Type</span></span> | <span data-ttu-id="6497f-115">FORMAT \_ None</span><span class="sxs-lookup"><span data-stu-id="6497f-115">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="6497f-116">El bloque de formato (**pbFormat**) es opcional.</span><span class="sxs-lookup"><span data-stu-id="6497f-116">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="6497f-117">Si se incluye el bloque de formato, debe comenzar con una **estructura MPEG2 \_ TRANSPORT \_ STRIDE.**</span><span class="sxs-lookup"><span data-stu-id="6497f-117">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="6497f-118">Esta estructura define el diseño del paquete de transporte dentro del paquete stride.</span><span class="sxs-lookup"><span data-stu-id="6497f-118">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="6497f-119">Si el bloque de formato **es NULL,** se supone que los paquetes usan un conjunto de valores predeterminados; consulte la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6497f-119">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="6497f-120">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6497f-120">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="6497f-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="6497f-121">Members</span></span>

<dl> <dt>

<span data-ttu-id="6497f-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="6497f-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="6497f-123">Especifica el desplazamiento, en bytes, desde el principio del paquete hasta el primer byte del paquete de transporte incrustado.</span><span class="sxs-lookup"><span data-stu-id="6497f-123">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="6497f-124">El valor debe oscilar entre cero y `(dwStride - dwPacketLength)` , ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="6497f-124">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="6497f-125">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="6497f-125">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="6497f-126">Especifica la longitud del paquete de transporte incrustado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6497f-126">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="6497f-127">Para los paquetes de transporte MPEG-2 estándar, el valor debe ser de 188 bytes.</span><span class="sxs-lookup"><span data-stu-id="6497f-127">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6497f-128">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="6497f-128">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="6497f-129">Especifica la longitud del paquete stride completo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6497f-129">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="6497f-130">El valor debe ser al menos `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="6497f-130">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6497f-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6497f-131">Remarks</span></span>

<span data-ttu-id="6497f-132">En el diagrama siguiente se muestran las relaciones entre los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="6497f-132">The following diagram illustrates the relations between the structure members.</span></span>

![paquete de paso mpeg-2](images/mpeg2-stride-packet.png)

<span data-ttu-id="6497f-134">Los búferes de entrada que contienen paquetes de paso multiplexado tienen algunas restricciones:</span><span class="sxs-lookup"><span data-stu-id="6497f-134">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="6497f-135">Los paquetes stride deben empaquetarse de forma contigua dentro del búfer.</span><span class="sxs-lookup"><span data-stu-id="6497f-135">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="6497f-136">Ningún bytes puede preceder al primer paquete de paso o seguir el último paquete de paso.</span><span class="sxs-lookup"><span data-stu-id="6497f-136">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="6497f-137">Un número entero de paquetes de paso debe caber en el búfer; es decir, la longitud del búfer % dwStride es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="6497f-137">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="6497f-138">No hay ninguna restricción en el número de paquetes de paso por búfer.</span><span class="sxs-lookup"><span data-stu-id="6497f-138">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="6497f-139">Si el tipo de medio no contiene un bloque de formato **(pbFormat** es **NULL),** se usan los siguientes valores predeterminados:</span><span class="sxs-lookup"><span data-stu-id="6497f-139">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="6497f-140">**dwOffset:** 0</span><span class="sxs-lookup"><span data-stu-id="6497f-140">**dwOffset**: 0</span></span>
-   <span data-ttu-id="6497f-141">**dwPacketLength:** 188</span><span class="sxs-lookup"><span data-stu-id="6497f-141">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="6497f-142">**dwStride:** 188</span><span class="sxs-lookup"><span data-stu-id="6497f-142">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="6497f-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6497f-143">Requirements</span></span>



| <span data-ttu-id="6497f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6497f-144">Requirement</span></span> | <span data-ttu-id="6497f-145">Value</span><span class="sxs-lookup"><span data-stu-id="6497f-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6497f-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6497f-146">Header</span></span><br/> | <dl> <span data-ttu-id="6497f-147"><dt>Bdatypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="6497f-147"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6497f-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6497f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6497f-149">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="6497f-149">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="6497f-150">Tipos de medios MPEG-2</span><span class="sxs-lookup"><span data-stu-id="6497f-150">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




