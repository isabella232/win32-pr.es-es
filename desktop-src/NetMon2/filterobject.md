---
description: Define un único objeto de un filtro de presentación.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Estructura FILTEROBJECT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677296"
---
# <a name="filterobject-structure"></a><span data-ttu-id="85687-103">Estructura FILTEROBJECT</span><span class="sxs-lookup"><span data-stu-id="85687-103">FILTEROBJECT structure</span></span>

<span data-ttu-id="85687-104">La estructura **FILTEROBJECT** define un único objeto de un filtro de presentación.</span><span class="sxs-lookup"><span data-stu-id="85687-104">The **FILTEROBJECT** structure defines a single object of a display filter.</span></span> <span data-ttu-id="85687-105">La función [**FilterAddObject**](filteraddobject.md) usa **FILTEROBJECT** para crear un filtro de presentación.</span><span class="sxs-lookup"><span data-stu-id="85687-105">The [**FilterAddObject**](filteraddobject.md) function uses **FILTEROBJECT** to build a display filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="85687-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85687-106">Syntax</span></span>


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a><span data-ttu-id="85687-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="85687-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="85687-108">**Acción**</span><span class="sxs-lookup"><span data-stu-id="85687-108">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="85687-109">Marca que especifica la acción **FILTEROBJECT** .</span><span class="sxs-lookup"><span data-stu-id="85687-109">Flag that specifies the **FILTEROBJECT** action.</span></span> <span data-ttu-id="85687-110">Una marca puede especificar una propiedad, un valor o un operador.</span><span class="sxs-lookup"><span data-stu-id="85687-110">A flag can specify a property, value, or operator.</span></span>

<span data-ttu-id="85687-111">En la tabla siguiente se enumeran las marcas de propiedades de miembro de acción.</span><span class="sxs-lookup"><span data-stu-id="85687-111">The following table lists Action member property flags.</span></span>



| <span data-ttu-id="85687-112">Value</span><span class="sxs-lookup"><span data-stu-id="85687-112">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="85687-113">Significado</span><span class="sxs-lookup"><span data-stu-id="85687-113">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <span data-ttu-id="85687-114"><dt>**\_propiedad FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-114"><dt>**FILTERACTION\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="85687-115">Contiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="85687-115">Contains this property.</span></span><br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <span data-ttu-id="85687-116"><dt>**FILTERACTION \_ PROPERTYEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-116"><dt>**FILTERACTION\_PROPERTYEXIST**</dt></span></span> </dl> | <span data-ttu-id="85687-117">Indica que ya se ha definido una propiedad de acción de filtrado.</span><span class="sxs-lookup"><span data-stu-id="85687-117">Indicates that a filter action property is already defined.</span></span><br/> |



 

<span data-ttu-id="85687-118">En la tabla siguiente se enumeran las marcas de valor de miembro de acción.</span><span class="sxs-lookup"><span data-stu-id="85687-118">The following table lists Action member value flags.</span></span>



| <span data-ttu-id="85687-119">Value</span><span class="sxs-lookup"><span data-stu-id="85687-119">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="85687-120">Significado</span><span class="sxs-lookup"><span data-stu-id="85687-120">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <span data-ttu-id="85687-121"><dt>**valor de FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-121"><dt>**FILTERACTION\_VALUE**</dt></span></span> </dl>                 | <span data-ttu-id="85687-122">Contiene este valor.</span><span class="sxs-lookup"><span data-stu-id="85687-122">Contains this value.</span></span><br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <span data-ttu-id="85687-123"><dt>**cadena de FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-123"><dt>**FILTERACTION\_STRING**</dt></span></span> </dl>              | <span data-ttu-id="85687-124">Contiene esta cadena.</span><span class="sxs-lookup"><span data-stu-id="85687-124">Contains this string.</span></span><br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <span data-ttu-id="85687-125"><dt>**FILTERACTION ( \_ matriz)**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-125"><dt>**FILTERACTION\_ARRAY**</dt></span></span> </dl>                 | <span data-ttu-id="85687-126">Contiene esta matriz.</span><span class="sxs-lookup"><span data-stu-id="85687-126">Contains this array.</span></span><br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <span data-ttu-id="85687-127"><dt>**FILTERACTION \_ CONTAINSNC**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-127"><dt>**FILTERACTION\_CONTAINSNC**</dt></span></span> </dl>  | <span data-ttu-id="85687-128">Indica que una propiedad contiene una subcadena que no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-128">Indicates that a property contains a case-insensitive substring.</span></span><br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <span data-ttu-id="85687-129"><dt>**la FILTERACTION \_ contiene**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-129"><dt>**FILTERACTION\_CONTAINS**</dt></span></span> </dl>        | <span data-ttu-id="85687-130">Indica que una propiedad contiene una subcadena que distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-130">Indicates that a property contains a case sensitive substring.</span></span><br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <span data-ttu-id="85687-131"><dt>**Dirección de la FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-131"><dt>**FILTERACTION\_ADDRESS**</dt></span></span> </dl>           | <span data-ttu-id="85687-132">Contiene la dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="85687-132">Contains the MAC address.</span></span><br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <span data-ttu-id="85687-133"><dt>**FILTERACTION \_ ADDRESSANY**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-133"><dt>**FILTERACTION\_ADDRESSANY**</dt></span></span> </dl>  | <span data-ttu-id="85687-134">Coincide con cualquier dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="85687-134">Matches any MAC address.</span></span><br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <span data-ttu-id="85687-135"><dt>**FILTERACTION \_ desde**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-135"><dt>**FILTERACTION\_FROM**</dt></span></span> </dl>                    | <span data-ttu-id="85687-136">Indica la dirección **Mac de** .</span><span class="sxs-lookup"><span data-stu-id="85687-136">Indicates the **From MAC** address.</span></span><br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <span data-ttu-id="85687-137"><dt>**FILTERACTION \_ en**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-137"><dt>**FILTERACTION\_TO**</dt></span></span> </dl>                          | <span data-ttu-id="85687-138">Indica la dirección **Mac** .</span><span class="sxs-lookup"><span data-stu-id="85687-138">Indicates the **To MAC** address.</span></span><br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <span data-ttu-id="85687-139"><dt>**FILTERACTION \_ fromto**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-139"><dt>**FILTERACTION\_FROMTO**</dt></span></span> </dl>              | <span data-ttu-id="85687-140">Indica una combinación de **/para** emparejar direcciones MAC.</span><span class="sxs-lookup"><span data-stu-id="85687-140">Indicates a **From/To** pairing of MAC addresses.</span></span><br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <span data-ttu-id="85687-141"><dt>**FILTERACTION \_ LARGEINT**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-141"><dt>**FILTERACTION\_LARGEINT**</dt></span></span> </dl>        | <span data-ttu-id="85687-142">Contiene un entero grande.</span><span class="sxs-lookup"><span data-stu-id="85687-142">Contains a large integer.</span></span><br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <span data-ttu-id="85687-143"><dt>**tiempo de la FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-143"><dt>**FILTERACTION\_TIME**</dt></span></span> </dl>                    | <span data-ttu-id="85687-144">Contiene una estructura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="85687-144">Contains a **SYSTEMTIME** structure.</span></span><br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <span data-ttu-id="85687-145"><dt>**Dirección de la FILTERACTION \_ \_ ether**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-145"><dt>**FILTERACTION\_ADDR\_ETHER**</dt></span></span> </dl> | <span data-ttu-id="85687-146">Contiene una dirección MAC de Ethernet.</span><span class="sxs-lookup"><span data-stu-id="85687-146">Contains an Ethernet MAC address.</span></span><br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <span data-ttu-id="85687-147"><dt>**\_token de dirección de la FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-147"><dt>**FILTERACTION\_ADDR\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="85687-148">Contiene una dirección MAC de token ring.</span><span class="sxs-lookup"><span data-stu-id="85687-148">Contains a token ring MAC address.</span></span><br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <span data-ttu-id="85687-149"><dt>**Dirección de filtrado \_ \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-149"><dt>**FILTERACTION\_ADDR\_FDDI**</dt></span></span> </dl>    | <span data-ttu-id="85687-150">Contiene una dirección MAC FDDI.</span><span class="sxs-lookup"><span data-stu-id="85687-150">Contains a FDDI MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <span data-ttu-id="85687-151"><dt>**Dirección de filtrado \_ \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-151"><dt>**FILTERACTION\_ADDR\_IPX**</dt></span></span> </dl>       | <span data-ttu-id="85687-152">Contiene una dirección MAC de IPX.</span><span class="sxs-lookup"><span data-stu-id="85687-152">Contains an IPX MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <span data-ttu-id="85687-153"><dt>**Dirección IP de la dirección de filtrado \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-153"><dt>**FILTERACTION\_ADDR\_IP**</dt></span></span> </dl>          | <span data-ttu-id="85687-154">Contiene una dirección MAC de IP.</span><span class="sxs-lookup"><span data-stu-id="85687-154">Contains an IP MAC address.</span></span><br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <span data-ttu-id="85687-155"><dt>**OID de FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-155"><dt>**FILTERACTION\_OID**</dt></span></span> </dl>                       | <span data-ttu-id="85687-156">Contiene un identificador de objeto (OID).</span><span class="sxs-lookup"><span data-stu-id="85687-156">Contains an Object Identifier (OID).</span></span><br/>                             |



 

<span data-ttu-id="85687-157">En la tabla siguiente se enumeran las marcas de operador de miembro de acción.</span><span class="sxs-lookup"><span data-stu-id="85687-157">The following table lists Action member operator flags.</span></span>



| <span data-ttu-id="85687-158">Value</span><span class="sxs-lookup"><span data-stu-id="85687-158">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="85687-159">Significado</span><span class="sxs-lookup"><span data-stu-id="85687-159">Meaning</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <span data-ttu-id="85687-160"><dt>**FILTERACTION \_ no válida**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-160"><dt>**FILTERACTION\_INVALID**</dt></span></span> </dl>                           | <span data-ttu-id="85687-161">Indica una acción de filtro no válida.</span><span class="sxs-lookup"><span data-stu-id="85687-161">Indicates an invalid filter action.</span></span><br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <span data-ttu-id="85687-162"><dt>**FILTERACTION \_ y**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-162"><dt>**FILTERACTION\_AND**</dt></span></span> </dl>                                       | <span data-ttu-id="85687-163">Indica una instrucción **and** lógica.</span><span class="sxs-lookup"><span data-stu-id="85687-163">Indicates a logical **AND** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <span data-ttu-id="85687-164"><dt>**FILTERACTION \_ o**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-164"><dt>**FILTERACTION\_OR**</dt></span></span> </dl>                                          | <span data-ttu-id="85687-165">Indica una instrucción **or** lógica.</span><span class="sxs-lookup"><span data-stu-id="85687-165">Indicates a logical **OR** statement.</span></span><br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <span data-ttu-id="85687-166"><dt>**FILTERACTION \_ XOR**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-166"><dt>**FILTERACTION\_XOR**</dt></span></span> </dl>                                       | <span data-ttu-id="85687-167">Indica una instrucción or **exclusiva lógica** (XOR).</span><span class="sxs-lookup"><span data-stu-id="85687-167">Indicates a logical exclusive **OR** (XOR) statement.</span></span><br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <span data-ttu-id="85687-168"><dt>**FILTERACTION \_ no**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-168"><dt>**FILTERACTION\_NOT**</dt></span></span> </dl>                                       | <span data-ttu-id="85687-169">Indica una instrucción **Not** lógica.</span><span class="sxs-lookup"><span data-stu-id="85687-169">Indicates a logical **NOT** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <span data-ttu-id="85687-170"><dt>**FILTERACTION \_ EQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-170"><dt>**FILTERACTION\_EQUALNC**</dt></span></span> </dl>                           | <span data-ttu-id="85687-171">La acción de filtrado es igual y no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-171">Filter action is equal and case insensitive.</span></span><br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <span data-ttu-id="85687-172"><dt>**FILTERACTION \_ igual**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-172"><dt>**FILTERACTION\_EQUAL**</dt></span></span> </dl>                                 | <span data-ttu-id="85687-173">La acción de filtrado es igual y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-173">Filter action is equal and case sensitive.</span></span><br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <span data-ttu-id="85687-174"><dt>**FILTERACTION \_ NOTEQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-174"><dt>**FILTERACTION\_NOTEQUALNC**</dt></span></span> </dl>                  | <span data-ttu-id="85687-175">La instrucción not lógica es igual y **no** distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-175">Logical **NOT** statement is equal and case insensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <span data-ttu-id="85687-176"><dt>**FILTRADO \_ NOTEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-176"><dt>**FILTERACTION\_NOTEQUAL**</dt></span></span> </dl>                        | <span data-ttu-id="85687-177">La instrucción **Not** lógica es igual y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-177">Logical **NOT** statement is equal and is case sensitive.</span></span><br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <span data-ttu-id="85687-178"><dt>**FILTERACTION \_ GREATERNC**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-178"><dt>**FILTERACTION\_GREATERNC**</dt></span></span> </dl>                     | <span data-ttu-id="85687-179">La acción de filtrado es mayor que (>) y no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-179">Filter action is greater than (>) and case insensitive.</span></span><br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <span data-ttu-id="85687-180"><dt>**la FILTERACTION es \_ mayor**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-180"><dt>**FILTERACTION\_GREATER**</dt></span></span> </dl>                           | <span data-ttu-id="85687-181">La acción de filtrado es mayor que (>) y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-181">Filter action is greater than (>) and case sensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <span data-ttu-id="85687-182"><dt>**FILTERACTION \_ LESSNC**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-182"><dt>**FILTERACTION\_LESSNC**</dt></span></span> </dl>                              | <span data-ttu-id="85687-183">La acción de filtrado es menor que (<) y no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-183">Filter action is less than (<) and case insensitive.</span></span><br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <span data-ttu-id="85687-184"><dt>**FILTERACTION \_ menos**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-184"><dt>**FILTERACTION\_LESS**</dt></span></span> </dl>                                    | <span data-ttu-id="85687-185">La acción de filtrado es menor que (<) y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-185">Filter action is less than (<) and case sensitive.</span></span><br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <span data-ttu-id="85687-186"><dt>**FILTERACTION \_ GREATEREQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-186"><dt>**FILTERACTION\_GREATEREQUALNC**</dt></span></span> </dl>      | <span data-ttu-id="85687-187">La acción de filtrado es mayor o igual que (>=) y no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-187">Filter action is greater than or equal to (>=) and case insensitive.</span></span><br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <span data-ttu-id="85687-188"><dt>**FILTERACTION \_ mayor criticalthreshold**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-188"><dt>**FILTERACTION\_GREATEREQUAL**</dt></span></span> </dl>            | <span data-ttu-id="85687-189">La acción de filtrado es mayor o igual que (>=) y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-189">Filter action is greater than or equal to (>=) and case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <span data-ttu-id="85687-190"><dt>**FILTERACTION \_ LESSEQUALNC**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-190"><dt>**FILTERACTION\_LESSEQUALNC**</dt></span></span> </dl>               | <span data-ttu-id="85687-191">La acción de filtrado es menor o igual que (<=) y no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-191">Filter action is less than or equal to (<=) and case insensitive.</span></span><br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <span data-ttu-id="85687-192"><dt>**FILTERACTION \_ LESSEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-192"><dt>**FILTERACTION\_LESSEQUAL**</dt></span></span> </dl>                     | <span data-ttu-id="85687-193">La acción de filtrado es menor o igual que (<=) y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="85687-193">Filter action is less than or equal to (<=) and is case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <span data-ttu-id="85687-194"><dt>**FILTERACTION \_ Plus**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-194"><dt>**FILTERACTION\_PLUS**</dt></span></span> </dl>                                    | <span data-ttu-id="85687-195">Agregar operador (+).</span><span class="sxs-lookup"><span data-stu-id="85687-195">Add operator (+).</span></span><br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <span data-ttu-id="85687-196"><dt>**FILTERACTION \_ menos**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-196"><dt>**FILTERACTION\_MINUS**</dt></span></span> </dl>                                 | <span data-ttu-id="85687-197">Operador de resta (-).</span><span class="sxs-lookup"><span data-stu-id="85687-197">Subtract operator (-).</span></span><br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <span data-ttu-id="85687-198"><dt>**FILTERACTION \_ AREBITSON**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-198"><dt>**FILTERACTION\_AREBITSON**</dt></span></span> </dl>                     | <span data-ttu-id="85687-199">Indica una operación bit a bit.</span><span class="sxs-lookup"><span data-stu-id="85687-199">Indicates a bitwise operation.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <span data-ttu-id="85687-200"><dt>**FILTERACTION \_ AREBITSOFF**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-200"><dt>**FILTERACTION\_AREBITSOFF**</dt></span></span> </dl>                  | <span data-ttu-id="85687-201">Indica una operación no bit a bit.</span><span class="sxs-lookup"><span data-stu-id="85687-201">Indicates a non-bitwise operation.</span></span><br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <span data-ttu-id="85687-202"><dt>**FILTERACTION \_ PROTOCOLSEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-202"><dt>**FILTERACTION\_PROTOCOLSEXIST**</dt></span></span> </dl>      | <span data-ttu-id="85687-203">Indica que existen los protocolos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="85687-203">Indicates that the selected protocols exist.</span></span><br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <span data-ttu-id="85687-204"><dt>**FILTERACTION \_ PROTOCOLEXIST**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-204"><dt>**FILTERACTION\_PROTOCOLEXIST**</dt></span></span> </dl>         | <span data-ttu-id="85687-205">Indica que el protocolo seleccionado existe.</span><span class="sxs-lookup"><span data-stu-id="85687-205">Indicates that the selected protocol exists.</span></span><br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <span data-ttu-id="85687-206"><dt>**FILTERACTION \_ ARRAYEQUAL**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-206"><dt>**FILTERACTION\_ARRAYEQUAL**</dt></span></span> </dl>                  | <span data-ttu-id="85687-207">Indica que el contenido de la matriz es igual.</span><span class="sxs-lookup"><span data-stu-id="85687-207">Indicates that array contents are equal.</span></span> <span data-ttu-id="85687-208">La marca se debe usar con una estructura de la **\_ matriz de FILTERACTION** .</span><span class="sxs-lookup"><span data-stu-id="85687-208">The flag must be used with a **FILTERACTION\_ARRAY** structure.</span></span><br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <span data-ttu-id="85687-209"><dt>**FILTERACTION \_ DEREFPROPERTY**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-209"><dt>**FILTERACTION\_DEREFPROPERTY**</dt></span></span> </dl>         | <span data-ttu-id="85687-210">Describe una coincidencia de patrones en un desplazamiento (en bytes) del protocolo.</span><span class="sxs-lookup"><span data-stu-id="85687-210">Describes a pattern match at an offset (in bytes), from the protocol.</span></span><br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <span data-ttu-id="85687-211"><dt>**el OID de la FILTERACTION \_ \_ contiene**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-211"><dt>**FILTERACTION\_OID\_CONTAINS**</dt></span></span> </dl>           | <span data-ttu-id="85687-212">Evalúa una subcadena dentro de un identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="85687-212">Evaluates a substring within an object identifier.</span></span> <span data-ttu-id="85687-213">La acción debe usarse con la estructura de la **FILTERACTION del \_ OID** .</span><span class="sxs-lookup"><span data-stu-id="85687-213">The action must be used with the **FILTERACTION\_OID** structure.</span></span><br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <span data-ttu-id="85687-214"><dt>**el \_ OID \_ de FILTERACTION comienza \_ con**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-214"><dt>**FILTERACTION\_OID\_BEGINS\_WITH**</dt></span></span> </dl> | <span data-ttu-id="85687-215">Evalúa una subcadena que comienza un identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="85687-215">Evaluates a substring that begins an object identifier.</span></span> <span data-ttu-id="85687-216">La marca debe usarse con **el \_ OID** de la FILTERACTION.</span><span class="sxs-lookup"><span data-stu-id="85687-216">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <span data-ttu-id="85687-217"><dt>**el \_ OID \_ de la FILTERACTION termina \_ con**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-217"><dt>**FILTERACTION\_OID\_ENDS\_WITH**</dt></span></span> </dl>       | <span data-ttu-id="85687-218">Evalúa una subcadena que finaliza un identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="85687-218">Evaluates a substring that ends an object identifier.</span></span> <span data-ttu-id="85687-219">La marca debe usarse con **el \_ OID** de la FILTERACTION.</span><span class="sxs-lookup"><span data-stu-id="85687-219">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <span data-ttu-id="85687-220"><dt>**Dirección de filtrado- \_ \_ Vines**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-220"><dt>**FILTERACTION\_ADDR\_VINES**</dt></span></span> </dl>                 | <span data-ttu-id="85687-221">Contiene una dirección MAC de Vines.</span><span class="sxs-lookup"><span data-stu-id="85687-221">Contains a Vines MAC address.</span></span><br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <span data-ttu-id="85687-222"><dt>**\_expresión FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-222"><dt>**FILTERACTION\_EXPRESSION**</dt></span></span> </dl>                  | <span data-ttu-id="85687-223">Contiene una expresión de acción.</span><span class="sxs-lookup"><span data-stu-id="85687-223">Contains an action expression.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <span data-ttu-id="85687-224"><dt>**FILTERACTION \_ bool**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-224"><dt>**FILTERACTION\_BOOL**</dt></span></span> </dl>                                    | <span data-ttu-id="85687-225">Contiene un tipo de datos **bool** .</span><span class="sxs-lookup"><span data-stu-id="85687-225">Contains a **BOOL** data type.</span></span><br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <span data-ttu-id="85687-226"><dt>**Dirección del filtro \_ \_ siguiente**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-226"><dt>**FILTER\_DIRECTION\_NEXT**</dt></span></span> </dl>                       | <span data-ttu-id="85687-227">Controla la dirección secuencial (fotograma siguiente) dentro de un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="85687-227">Controls sequential direction (Next frame) within a capture file.</span></span><br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <span data-ttu-id="85687-228"><dt>**Dirección del filtro \_ \_ anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="85687-228"><dt>**FILTER\_DIRECTION\_PREV**</dt></span></span> </dl>                       | <span data-ttu-id="85687-229">Controla la dirección secuencial (fotograma anterior) dentro de un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="85687-229">Controls sequential direction (Previous frame) within a capture file.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="85687-230">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="85687-230">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="85687-231">Identificador de una clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="85687-231">Handle to a property key.</span></span>

</dd> <dt>

<span data-ttu-id="85687-232">**Valor**</span><span class="sxs-lookup"><span data-stu-id="85687-232">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="85687-233">Valor de un objeto.</span><span class="sxs-lookup"><span data-stu-id="85687-233">Value of an object.</span></span>

</dd> <dt>

<span data-ttu-id="85687-234">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="85687-234">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="85687-235">Identificador para mostrar el protocolo de filtro.</span><span class="sxs-lookup"><span data-stu-id="85687-235">Handle to display filter protocol.</span></span>

</dd> <dt>

<span data-ttu-id="85687-236">**lpArray**</span><span class="sxs-lookup"><span data-stu-id="85687-236">**lpArray**</span></span>
</dt> <dd>

<span data-ttu-id="85687-237">Puntero a una matriz.</span><span class="sxs-lookup"><span data-stu-id="85687-237">Pointer to an array.</span></span>

</dd> <dt>

<span data-ttu-id="85687-238">**lpProtocolTable**</span><span class="sxs-lookup"><span data-stu-id="85687-238">**lpProtocolTable**</span></span>
</dt> <dd>

<span data-ttu-id="85687-239">Puntero a una lista de protocolos diseñada para probar la existencia de un protocolo en un marco.</span><span class="sxs-lookup"><span data-stu-id="85687-239">Pointer to a protocol list designed to test the existence of protocol in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="85687-240">**lpAddress**</span><span class="sxs-lookup"><span data-stu-id="85687-240">**lpAddress**</span></span>
</dt> <dd>

<span data-ttu-id="85687-241">Puntero a la dirección del tipo de kernel.</span><span class="sxs-lookup"><span data-stu-id="85687-241">Pointer to the kernel type address.</span></span> <span data-ttu-id="85687-242">Por ejemplo, MAC o IP.</span><span class="sxs-lookup"><span data-stu-id="85687-242">For example, MAC or IP.</span></span>

</dd> <dt>

<span data-ttu-id="85687-243">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="85687-243">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="85687-244">Doble **DWORD** usado en una aplicación Windows NT o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="85687-244">Double **DWORD** used in a Windows NT or Windows 2000 application.</span></span>

</dd> <dt>

<span data-ttu-id="85687-245">**lpTime**</span><span class="sxs-lookup"><span data-stu-id="85687-245">**lpTime**</span></span>
</dt> <dd>

<span data-ttu-id="85687-246">Puntero a una estructura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="85687-246">A pointer to a **SYSTEMTIME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="85687-247">**lpOID**</span><span class="sxs-lookup"><span data-stu-id="85687-247">**lpOID**</span></span>
</dt> <dd>

<span data-ttu-id="85687-248">Puntero a la estructura **de \_ identificador de objeto** (OID).</span><span class="sxs-lookup"><span data-stu-id="85687-248">A pointer to the **OBJECT\_IDENTIFIER** (OID) structure.</span></span>

</dd> <dt>

<span data-ttu-id="85687-249">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="85687-249">**ByteCount**</span></span>
</dt> <dd>

<span data-ttu-id="85687-250">Número, en bytes, del marco.</span><span class="sxs-lookup"><span data-stu-id="85687-250">The number, in bytes, in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="85687-251">**Byteoffset (**</span><span class="sxs-lookup"><span data-stu-id="85687-251">**ByteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="85687-252">El valor de byte de desplazamiento de la estructura FILTEROBJECT utilizada para comparar las matrices.</span><span class="sxs-lookup"><span data-stu-id="85687-252">The offset byte value of the FILTEROBJECT structure used to compare arrays.</span></span>

</dd> <dt>

<span data-ttu-id="85687-253">**pNext**</span><span class="sxs-lookup"><span data-stu-id="85687-253">**pNext**</span></span>
</dt> <dd>

<span data-ttu-id="85687-254">Reservado.</span><span class="sxs-lookup"><span data-stu-id="85687-254">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85687-255">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85687-255">Requirements</span></span>



| <span data-ttu-id="85687-256">Requisito</span><span class="sxs-lookup"><span data-stu-id="85687-256">Requirement</span></span> | <span data-ttu-id="85687-257">Value</span><span class="sxs-lookup"><span data-stu-id="85687-257">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="85687-258">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85687-258">Minimum supported client</span></span><br/> | <span data-ttu-id="85687-259">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="85687-259">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="85687-260">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85687-260">Minimum supported server</span></span><br/> | <span data-ttu-id="85687-261">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85687-261">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="85687-262">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85687-262">Header</span></span><br/>                   | <dl> <span data-ttu-id="85687-263"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="85687-263"><dt>Netmon.h</dt></span></span> </dl> |



 

 




