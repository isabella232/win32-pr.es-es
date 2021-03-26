---
description: Esta clase es la clase de tipo de evento para los eventos de error de TCP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: TcpIp_Fail (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: a89d882509ea766e62c8b78e6c2a5fa769fbcca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984795"
---
# <a name="tcpip_fail-class"></a><span data-ttu-id="1ba1f-104">TcpIp \_ FAIL (clase)</span><span class="sxs-lookup"><span data-stu-id="1ba1f-104">TcpIp\_Fail class</span></span>

<span data-ttu-id="1ba1f-105">Esta clase es la clase de tipo de evento para los eventos de error de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1ba1f-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="1ba1f-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="1ba1f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba1f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ba1f-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="1ba1f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1ba1f-108">Members</span></span>

<span data-ttu-id="1ba1f-109">La clase de **\_ error de TCPIP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1ba1f-109">The **TcpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="1ba1f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1ba1f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ba1f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1ba1f-111">Properties</span></span>

<span data-ttu-id="1ba1f-112">La clase de **\_ error de TCPIP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1ba1f-112">The **TcpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ba1f-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="1ba1f-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba1f-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba1f-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba1f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1ba1f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba1f-116">Motivo del error.</span><span class="sxs-lookup"><span data-stu-id="1ba1f-116">Reason for the failure.</span></span> <span data-ttu-id="1ba1f-117">Puede ser uno de los siguientes códigos:</span><span class="sxs-lookup"><span data-stu-id="1ba1f-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="1ba1f-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Error \_ de \_Recursos INsuficientes** (1)</span><span class="sxs-lookup"><span data-stu-id="1ba1f-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ba1f-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Error \_ de DEMASIADAs \_ \_ direcciones** (2)</span><span class="sxs-lookup"><span data-stu-id="1ba1f-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ba1f-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Error \_ de \_Existe la dirección** (3)</span><span class="sxs-lookup"><span data-stu-id="1ba1f-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ba1f-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Error \_ de \_Dirección no válida** (4)</span><span class="sxs-lookup"><span data-stu-id="1ba1f-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ba1f-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**Error \_ de OTROS** (5)</span><span class="sxs-lookup"><span data-stu-id="1ba1f-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ba1f-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Error \_ de \_ \_ Existe la dirección TIMEWAIT** (6)</span><span class="sxs-lookup"><span data-stu-id="1ba1f-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1ba1f-124">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="1ba1f-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ba1f-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1ba1f-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1ba1f-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1ba1f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1ba1f-127">Identifica el protocolo.</span><span class="sxs-lookup"><span data-stu-id="1ba1f-127">Identifies the protocol.</span></span> <span data-ttu-id="1ba1f-128">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="1ba1f-128">Can be one of the following values:</span></span>



| <span data-ttu-id="1ba1f-129">Value</span><span class="sxs-lookup"><span data-stu-id="1ba1f-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="1ba1f-130">Significado</span><span class="sxs-lookup"><span data-stu-id="1ba1f-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="1ba1f-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1ba1f-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="1ba1f-132">Familia de direcciones del Protocolo de Internet versión 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="1ba1f-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="1ba1f-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="1ba1f-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="1ba1f-134">Familia de direcciones del Protocolo de Internet versión 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="1ba1f-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ba1f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ba1f-135">Requirements</span></span>



| <span data-ttu-id="1ba1f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ba1f-136">Requirement</span></span> | <span data-ttu-id="1ba1f-137">Value</span><span class="sxs-lookup"><span data-stu-id="1ba1f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ba1f-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ba1f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1ba1f-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ba1f-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1ba1f-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ba1f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1ba1f-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ba1f-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ba1f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ba1f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba1f-143">**Luego**</span><span class="sxs-lookup"><span data-stu-id="1ba1f-143">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




