---
description: Especifica los miembros de la estructura NMCOLUMNVARIANT.
ms.assetid: 29363341-f4d3-43c3-a523-45402174cb74
title: Enumeración NMCOLUMNTYPE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNTYPE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3c88d001ce3ccf1ebfe1e28855ae9df9fca5d327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818523"
---
# <a name="nmcolumntype-enumeration"></a><span data-ttu-id="ce7dd-103">Enumeración NMCOLUMNTYPE</span><span class="sxs-lookup"><span data-stu-id="ce7dd-103">NMCOLUMNTYPE enumeration</span></span>

<span data-ttu-id="ce7dd-104">La enumeración **NMCOLUMNTYPE** especifica los miembros de la estructura [**NMCOLUMNVARIANT**](nmcolumnvariant.md) .</span><span class="sxs-lookup"><span data-stu-id="ce7dd-104">The **NMCOLUMNTYPE** enumeration specifies the members of the [**NMCOLUMNVARIANT**](nmcolumnvariant.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce7dd-105">Syntax</span></span>


```C++
typedef enum  { 
  NMCOLUMNTYPE_UINT8      = 0,
  NMCOLUMNTYPE_SINT8,
  NMCOLUMNTYPE_UINT16,
  NMCOLUMNTYPE_SINT16,
  NMCOLUMNTYPE_UINT32,
  NMCOLUMNTYPE_SINT32,
  NMCOLUMNTYPE_FLOAT64,
  NMCOLUMNTYPE_FRAME,
  NMCOLUMNTYPE_YESNO,
  NMCOLUMNTYPE_ONOFF,
  NMCOLUMNTYPE_TRUEFALSE,
  NMCOLUMNTYPE_MACADDR,
  NMCOLUMNTYPE_IPXADDR,
  NMCOLUMNTYPE_IPADDR,
  NMCOLUMNTYPE_VARTIME,
  NMCOLUMNTYPE_STRING
} NMCOLUMNTYPE;
```



## <a name="constants"></a><span data-ttu-id="ce7dd-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ce7dd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ce7dd-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE \_ UINT8**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-107"><span id="NMCOLUMNTYPE_UINT8"></span><span id="nmcolumntype_uint8"></span>**NMCOLUMNTYPE\_UINT8**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-108">entero de 8 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-108">8-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE \_ SINT8**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-109"><span id="NMCOLUMNTYPE_SINT8"></span><span id="nmcolumntype_sint8"></span>**NMCOLUMNTYPE\_SINT8**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-110">entero de 8 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-110">8-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE \_ UINT16**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-111"><span id="NMCOLUMNTYPE_UINT16"></span><span id="nmcolumntype_uint16"></span>**NMCOLUMNTYPE\_UINT16**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-112">entero de 16 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-112">16-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE \_ SINT16**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-113"><span id="NMCOLUMNTYPE_SINT16"></span><span id="nmcolumntype_sint16"></span>**NMCOLUMNTYPE\_SINT16**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-114">entero de 16 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-114">16-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**\_UINT32 NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-115"><span id="NMCOLUMNTYPE_UINT32"></span><span id="nmcolumntype_uint32"></span>**NMCOLUMNTYPE\_UINT32**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-116">entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-116">32-bit unsigned integer.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-117"><span id="NMCOLUMNTYPE_SINT32"></span><span id="nmcolumntype_sint32"></span>**NMCOLUMNTYPE\_SINT32**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-118">Entero con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-118">32-bit signed integer.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE \_ FLOAT64**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-119"><span id="NMCOLUMNTYPE_FLOAT64"></span><span id="nmcolumntype_float64"></span>**NMCOLUMNTYPE\_FLOAT64**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-120">valor Float de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-120">64-bit float.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**fotograma NMCOLUMNTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-121"><span id="NMCOLUMNTYPE_FRAME"></span><span id="nmcolumntype_frame"></span>**NMCOLUMNTYPE\_FRAME**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-122">Número de marco.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-122">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE \_ síno**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-123"><span id="NMCOLUMNTYPE_YESNO"></span><span id="nmcolumntype_yesno"></span>**NMCOLUMNTYPE\_YESNO**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-124">"Sí" o "no".</span><span class="sxs-lookup"><span data-stu-id="ce7dd-124">"Yes" or "No".</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE \_ OnOff**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-125"><span id="NMCOLUMNTYPE_ONOFF"></span><span id="nmcolumntype_onoff"></span>**NMCOLUMNTYPE\_ONOFF**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-126">"ON" u "OFF"</span><span class="sxs-lookup"><span data-stu-id="ce7dd-126">"On" or "Off"</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE \_ TRUEFALSE**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-127"><span id="NMCOLUMNTYPE_TRUEFALSE"></span><span id="nmcolumntype_truefalse"></span>**NMCOLUMNTYPE\_TRUEFALSE**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-128">"True" o "false".</span><span class="sxs-lookup"><span data-stu-id="ce7dd-128">"True" or "False".</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE \_ MACADDR**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-129"><span id="NMCOLUMNTYPE_MACADDR"></span><span id="nmcolumntype_macaddr"></span>**NMCOLUMNTYPE\_MACADDR**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-130">Dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-130">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE \_ IPXADDR**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-131"><span id="NMCOLUMNTYPE_IPXADDR"></span><span id="nmcolumntype_ipxaddr"></span>**NMCOLUMNTYPE\_IPXADDR**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-132">Dirección IPX.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-132">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE \_ DirIP**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-133"><span id="NMCOLUMNTYPE_IPADDR"></span><span id="nmcolumntype_ipaddr"></span>**NMCOLUMNTYPE\_IPADDR**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-134">Dirección IP.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-134">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE \_ VARTIME**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-135"><span id="NMCOLUMNTYPE_VARTIME"></span><span id="nmcolumntype_vartime"></span>**NMCOLUMNTYPE\_VARTIME**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-136">Hora de la variante.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-136">Variant time.</span></span>

</dd> <dt>

<span data-ttu-id="ce7dd-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**\_cadena NMCOLUMNTYPE**</span><span class="sxs-lookup"><span data-stu-id="ce7dd-137"><span id="NMCOLUMNTYPE_STRING"></span><span id="nmcolumntype_string"></span>**NMCOLUMNTYPE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="ce7dd-138">Puntero a una cadena.</span><span class="sxs-lookup"><span data-stu-id="ce7dd-138">Pointer to a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce7dd-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce7dd-139">Requirements</span></span>



| <span data-ttu-id="ce7dd-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce7dd-140">Requirement</span></span> | <span data-ttu-id="ce7dd-141">Value</span><span class="sxs-lookup"><span data-stu-id="ce7dd-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7dd-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce7dd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ce7dd-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ce7dd-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ce7dd-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce7dd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ce7dd-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce7dd-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ce7dd-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce7dd-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce7dd-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce7dd-147"><dt>Netmon.h</dt></span></span> </dl> |



 

 




