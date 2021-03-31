---
title: Valores de sintaxis de la aplicación SNMP (SNMP. h)
description: Las aplicaciones de administración que emplean la API de administración de SNMP de Microsoft usan los valores de sintaxis de la aplicación SNMP.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150165"
---
# <a name="snmp-application-syntax-values"></a><span data-ttu-id="d0f81-103">Valores de sintaxis de la aplicación SNMP</span><span class="sxs-lookup"><span data-stu-id="d0f81-103">SNMP Application Syntax Values</span></span>

<span data-ttu-id="d0f81-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d0f81-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d0f81-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="d0f81-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d0f81-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="d0f81-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="d0f81-107">Las aplicaciones de administración que emplean la API de administración de SNMP de Microsoft usan los valores de sintaxis de la aplicación SNMP.</span><span class="sxs-lookup"><span data-stu-id="d0f81-107">The SNMP Application Syntax Values are used by management applications that employ the Microsoft SNMP Management API.</span></span>



| <span data-ttu-id="d0f81-108">Constante</span><span class="sxs-lookup"><span data-stu-id="d0f81-108">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="d0f81-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0f81-109">Description</span></span>                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <span data-ttu-id="d0f81-110"><dt>**\_dirección IP de ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-110"><dt>**ASN\_IPADDRESS**</dt></span></span> </dl>                             | <span data-ttu-id="d0f81-111">Indica una variable de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="d0f81-111">Indicates an IP address variable.</span></span><br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <span data-ttu-id="d0f81-112"><dt>**\_COUNTER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-112"><dt>**ASN\_COUNTER32**</dt></span></span> </dl>                             | <span data-ttu-id="d0f81-113">Indica una variable de contador.</span><span class="sxs-lookup"><span data-stu-id="d0f81-113">Indicates a counter variable.</span></span><br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <span data-ttu-id="d0f81-114"><dt>**\_GAUGE32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-114"><dt>**ASN\_GAUGE32**</dt></span></span> </dl>                                   | <span data-ttu-id="d0f81-115">Indica una variable de medidor.</span><span class="sxs-lookup"><span data-stu-id="d0f81-115">Indicates a gauge variable.</span></span> <span data-ttu-id="d0f81-116">Esta variable describe un tipo Unsigned32 en conformidad con RFC 1902.</span><span class="sxs-lookup"><span data-stu-id="d0f81-116">This variable describes an Unsigned32 type in conformance with RFC 1902.</span></span><br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <span data-ttu-id="d0f81-117"><dt>**\_TIMETICKS ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-117"><dt>**ASN\_TIMETICKS**</dt></span></span> </dl>                             | <span data-ttu-id="d0f81-118">Indica una variable timeticks.</span><span class="sxs-lookup"><span data-stu-id="d0f81-118">Indicates a timeticks variable.</span></span><br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <span data-ttu-id="d0f81-119"><dt>**opaco de ASN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-119"><dt>**ASN\_OPAQUE**</dt></span></span> </dl>                                      | <span data-ttu-id="d0f81-120">Indica una variable opaca.</span><span class="sxs-lookup"><span data-stu-id="d0f81-120">Indicates an opaque variable.</span></span><br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <span data-ttu-id="d0f81-121"><dt>**\_COUNTER64 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-121"><dt>**ASN\_COUNTER64**</dt></span></span> </dl>                             | <span data-ttu-id="d0f81-122">Indica una variable de contador que aumenta hasta que alcanza un valor máximo de (2 ^ 64)-1.</span><span class="sxs-lookup"><span data-stu-id="d0f81-122">Indicates a counter variable that increases until it reaches a maximum value of (2^64) - 1.</span></span><br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <span data-ttu-id="d0f81-123"><dt>**\_UINTEGER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-123"><dt>**ASN\_UINTEGER32**</dt></span></span> </dl>                          | <span data-ttu-id="d0f81-124">Indica una variable de entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="d0f81-124">Indicates a 32-bit unsigned integer variable.</span></span> <span data-ttu-id="d0f81-125">Esta variable describe un tipo UInteger32 en conformidad con RFC 1442.</span><span class="sxs-lookup"><span data-stu-id="d0f81-125">This variable describes a UInteger32 type in conformance with RFC 1442.</span></span><br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <span data-ttu-id="d0f81-126"><dt>**\_UNSIGNED32 RFC2578 \_ ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-126"><dt>**ASN\_RFC2578\_UNSIGNED32**</dt></span></span> </dl> | <span data-ttu-id="d0f81-127">Consulte ASN \_ GAUGE32.</span><span class="sxs-lookup"><span data-stu-id="d0f81-127">See ASN\_GAUGE32.</span></span><br/>                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="d0f81-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0f81-128">Requirements</span></span>



| <span data-ttu-id="d0f81-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0f81-129">Requirement</span></span> | <span data-ttu-id="d0f81-130">Value</span><span class="sxs-lookup"><span data-stu-id="d0f81-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d0f81-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0f81-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f81-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d0f81-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="d0f81-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0f81-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f81-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0f81-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d0f81-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0f81-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0f81-136"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0f81-136"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0f81-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0f81-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f81-138">Introducción al Protocolo simple de administración de redes (SNMP)</span><span class="sxs-lookup"><span data-stu-id="d0f81-138">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="d0f81-139">Referencia de SNMP</span><span class="sxs-lookup"><span data-stu-id="d0f81-139">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="d0f81-140">Constantes de SNMP</span><span class="sxs-lookup"><span data-stu-id="d0f81-140">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

