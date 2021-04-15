---
description: La \_ \_ estructura de intervalo de transporte de MPEG2 describe el formato de los paquetes de secuencias de transporte MPEG-2 (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE estructura (Bdatypes. h)
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
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690073"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="a0d53-103">Estructura de intervalo de \_ transporte de MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="a0d53-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="a0d53-104">La `MPEG2_TRANSPORT_STRIDE` estructura describe el formato de los paquetes de secuencias de transporte MPEG-2 (TS).</span><span class="sxs-lookup"><span data-stu-id="a0d53-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="a0d53-105">Esta estructura permite transportes de flujos en los que los paquetes de transporte de 188 bytes no son contiguos.</span><span class="sxs-lookup"><span data-stu-id="a0d53-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="a0d53-106">En esta documentación, se hace referencia a estos paquetes como *paquetes STRIDE*.</span><span class="sxs-lookup"><span data-stu-id="a0d53-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="a0d53-107">Los paquetes STRIDE se identifican con el siguiente tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="a0d53-107">Stride packets are identified by the following media type:</span></span>



|             |                                        |
|-------------|----------------------------------------|
| <span data-ttu-id="a0d53-108">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="a0d53-108">Major Type</span></span>  | <span data-ttu-id="a0d53-109">\_Secuencia MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="a0d53-109">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="a0d53-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="a0d53-110">Subtype</span></span>     | <span data-ttu-id="a0d53-111">\_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="a0d53-111">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="a0d53-112">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="a0d53-112">Format Type</span></span> | <span data-ttu-id="a0d53-113">FORMATO \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="a0d53-113">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="a0d53-114">El bloque de formato (**pbFormat**) es opcional.</span><span class="sxs-lookup"><span data-stu-id="a0d53-114">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="a0d53-115">Si se incluye el bloque de formato, debe comenzar con una estructura de **\_ \_ intervalo de transporte de MPEG2** .</span><span class="sxs-lookup"><span data-stu-id="a0d53-115">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="a0d53-116">Esta estructura define el diseño del paquete de transporte en el paquete STRIDE.</span><span class="sxs-lookup"><span data-stu-id="a0d53-116">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="a0d53-117">Si el bloque de formato es **null**, se supone que los paquetes usan un conjunto de valores predeterminados. Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a0d53-117">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d53-118">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0d53-118">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="a0d53-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0d53-119">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0d53-120">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="a0d53-120">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="a0d53-121">Especifica el desplazamiento, en bytes, desde el principio del paquete hasta el primer byte del paquete de transporte incrustado.</span><span class="sxs-lookup"><span data-stu-id="a0d53-121">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="a0d53-122">El valor debe estar comprendido entre cero y `(dwStride - dwPacketLength)` , ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="a0d53-122">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="a0d53-123">**dwPacketLength**</span><span class="sxs-lookup"><span data-stu-id="a0d53-123">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="a0d53-124">Especifica la longitud del paquete de transporte incrustado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a0d53-124">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="a0d53-125">En el caso de los paquetes de transporte MPEG-2 estándar, el valor debe ser 188 bytes.</span><span class="sxs-lookup"><span data-stu-id="a0d53-125">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a0d53-126">**dwStride**</span><span class="sxs-lookup"><span data-stu-id="a0d53-126">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="a0d53-127">Especifica la longitud de todo el paquete STRIDE, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a0d53-127">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="a0d53-128">El valor debe ser al menos `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="a0d53-128">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0d53-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0d53-129">Remarks</span></span>

<span data-ttu-id="a0d53-130">En el siguiente diagrama se ilustran las relaciones entre los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="a0d53-130">The following diagram illustrates the relations between the structure members.</span></span>

![paquete de paso MPEG-2](images/mpeg2-stride-packet.png)

<span data-ttu-id="a0d53-132">Los búferes de entrada que contienen paquetes de intervalo multiplexado tienen algunas restricciones:</span><span class="sxs-lookup"><span data-stu-id="a0d53-132">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="a0d53-133">Los paquetes STRIDE deben empaquetarse de forma contigua en el búfer.</span><span class="sxs-lookup"><span data-stu-id="a0d53-133">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="a0d53-134">Ningún byte puede preceder al primer paquete STRIDE o seguir el último paquete STRIDE.</span><span class="sxs-lookup"><span data-stu-id="a0d53-134">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="a0d53-135">Un número entero de paquetes STRIDE debe caber en el búfer; es decir, la longitud del búfer% dwStride es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="a0d53-135">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="a0d53-136">No hay ninguna restricción en el número de paquetes STRIDE por búfer.</span><span class="sxs-lookup"><span data-stu-id="a0d53-136">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="a0d53-137">Si el tipo de medio no contiene un bloque de formato (**pbFormat** es **null**), se usan los siguientes valores predeterminados:</span><span class="sxs-lookup"><span data-stu-id="a0d53-137">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="a0d53-138">**dwOffset**: 0</span><span class="sxs-lookup"><span data-stu-id="a0d53-138">**dwOffset**: 0</span></span>
-   <span data-ttu-id="a0d53-139">**dwPacketLength**: 188</span><span class="sxs-lookup"><span data-stu-id="a0d53-139">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="a0d53-140">**dwStride**: 188</span><span class="sxs-lookup"><span data-stu-id="a0d53-140">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="a0d53-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0d53-141">Requirements</span></span>



| <span data-ttu-id="a0d53-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0d53-142">Requirement</span></span> | <span data-ttu-id="a0d53-143">Value</span><span class="sxs-lookup"><span data-stu-id="a0d53-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d53-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0d53-144">Header</span></span><br/> | <dl> <span data-ttu-id="a0d53-145"><dt>Bdatypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0d53-145"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0d53-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0d53-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d53-147">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0d53-147">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="a0d53-148">Tipos de medios MPEG-2</span><span class="sxs-lookup"><span data-stu-id="a0d53-148">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




