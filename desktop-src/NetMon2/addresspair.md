---
description: La estructura ADDRESSPAIR crea un filtro de captura.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Estructura ADDRESSPAIR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667744"
---
# <a name="addresspair-structure"></a><span data-ttu-id="de9a2-103">Estructura ADDRESSPAIR</span><span class="sxs-lookup"><span data-stu-id="de9a2-103">ADDRESSPAIR structure</span></span>

<span data-ttu-id="de9a2-104">La estructura **ADDRESSPAIR** crea un filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="de9a2-104">The **ADDRESSPAIR** structure constructs a capture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de9a2-105">Syntax</span></span>


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a><span data-ttu-id="de9a2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="de9a2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="de9a2-107">**AddressFlags**</span><span class="sxs-lookup"><span data-stu-id="de9a2-107">**AddressFlags**</span></span>
</dt> <dd>

<span data-ttu-id="de9a2-108">Marcas que describen las direcciones utilizadas por un filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="de9a2-108">Flags that describe the addresses used by a capture filter.</span></span> <span data-ttu-id="de9a2-109">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="de9a2-109">See Remarks for more information.</span></span>



| <span data-ttu-id="de9a2-110">Value</span><span class="sxs-lookup"><span data-stu-id="de9a2-110">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="de9a2-111">Significado</span><span class="sxs-lookup"><span data-stu-id="de9a2-111">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <span data-ttu-id="de9a2-112"><dt>**marcas de dirección \_ \_ Match \_ DST**</dt></span><span class="sxs-lookup"><span data-stu-id="de9a2-112"><dt>**ADDRESS\_FLAGS\_MATCH\_DST**</dt></span></span> </dl>                 | <span data-ttu-id="de9a2-113">Coincide con la dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="de9a2-113">Matches the destination address.</span></span><br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <span data-ttu-id="de9a2-114"><dt>**coincidencia de marcas de dirección \_ \_ \_ src**</dt></span><span class="sxs-lookup"><span data-stu-id="de9a2-114"><dt>**ADDRESS\_FLAGS\_MATCH\_SRC**</dt></span></span> </dl>                 | <span data-ttu-id="de9a2-115">Coincide con la dirección de origen.</span><span class="sxs-lookup"><span data-stu-id="de9a2-115">Matches the source address.</span></span><br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <span data-ttu-id="de9a2-116"><dt>**marcas de dirección \_ \_ excluidas**</dt></span><span class="sxs-lookup"><span data-stu-id="de9a2-116"><dt>**ADDRESS\_FLAGS\_EXCLUDED**</dt></span></span> </dl>                     | <span data-ttu-id="de9a2-117">Excluye el marco si se encuentra esta dirección.</span><span class="sxs-lookup"><span data-stu-id="de9a2-117">Excludes the frame if this address is found.</span></span><br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <span data-ttu-id="de9a2-118"><dt>**marcas de dirección \_ \_ grupo de DST \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de9a2-118"><dt>**ADDRESS\_FLAGS\_DST\_GROUP\_ADDR**</dt></span></span> </dl> | <span data-ttu-id="de9a2-119">Coincide solo con el bit de grupo.</span><span class="sxs-lookup"><span data-stu-id="de9a2-119">Matches group bit only.</span></span> <span data-ttu-id="de9a2-120">Utilice esto para los mensajes de tipo difusión.</span><span class="sxs-lookup"><span data-stu-id="de9a2-120">Use this for broadcast-type messages.</span></span><br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <span data-ttu-id="de9a2-121"><dt>**las \_ marcas de dirección \_ coinciden con \_ ambas**</dt></span><span class="sxs-lookup"><span data-stu-id="de9a2-121"><dt>**ADDRESS\_FLAGS\_MATCH\_BOTH**</dt></span></span> </dl>              | <span data-ttu-id="de9a2-122">Coincide con las direcciones de destino y de origen.</span><span class="sxs-lookup"><span data-stu-id="de9a2-122">Matches destination and source addresses.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="de9a2-123">**NalReserved**</span><span class="sxs-lookup"><span data-stu-id="de9a2-123">**NalReserved**</span></span>
</dt> <dd>

<span data-ttu-id="de9a2-124">Está reservada.</span><span class="sxs-lookup"><span data-stu-id="de9a2-124">This is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="de9a2-125">**DstAddress**</span><span class="sxs-lookup"><span data-stu-id="de9a2-125">**DstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="de9a2-126">Dirección de destino del elemento de par de direcciones.</span><span class="sxs-lookup"><span data-stu-id="de9a2-126">Destination address of the address pair element.</span></span>

</dd> <dt>

<span data-ttu-id="de9a2-127">**SrcAddress**</span><span class="sxs-lookup"><span data-stu-id="de9a2-127">**SrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="de9a2-128">Dirección de origen del elemento de par de direcciones.</span><span class="sxs-lookup"><span data-stu-id="de9a2-128">Source address of the address pair element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de9a2-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de9a2-129">Remarks</span></span>

<span data-ttu-id="de9a2-130">Las marcas del miembro **AddressFlags** se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="de9a2-130">The flags of the **AddressFlags** member can be combined.</span></span> <span data-ttu-id="de9a2-131">Por ejemplo, la siguiente configuración excluye el marco si se detecta la dirección de origen especificada.</span><span class="sxs-lookup"><span data-stu-id="de9a2-131">For example the following setting excludes the frame if the specified source address is detected.</span></span>

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

<span data-ttu-id="de9a2-132">Para obtener más información sobre la implementación de esta estructura, vea [Capture filters](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="de9a2-132">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de9a2-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de9a2-133">Requirements</span></span>



| <span data-ttu-id="de9a2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="de9a2-134">Requirement</span></span> | <span data-ttu-id="de9a2-135">Value</span><span class="sxs-lookup"><span data-stu-id="de9a2-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="de9a2-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de9a2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="de9a2-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="de9a2-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="de9a2-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de9a2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="de9a2-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="de9a2-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="de9a2-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de9a2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="de9a2-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="de9a2-141"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9a2-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="de9a2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9a2-143">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="de9a2-143">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




