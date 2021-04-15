---
title: Valores de tipo de PDU (SNMP. h)
description: Los valores de tipo PDU se usan en el \_ campo de tipo PDU de la PDU para describir su tipo.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492323"
---
# <a name="pdu-type-values"></a><span data-ttu-id="039d8-103">Valores de tipo de PDU</span><span class="sxs-lookup"><span data-stu-id="039d8-103">PDU Type Values</span></span>

<span data-ttu-id="039d8-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="039d8-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="039d8-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="039d8-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="039d8-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="039d8-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="039d8-107">Los valores de tipo PDU se usan en el campo de **\_ tipo PDU** de la PDU para describir su tipo.</span><span class="sxs-lookup"><span data-stu-id="039d8-107">The PDU type values are used in the **pdu\_type** field of the PDU to describe its type.</span></span>



| <span data-ttu-id="039d8-108">Constante</span><span class="sxs-lookup"><span data-stu-id="039d8-108">Constant</span></span>                                                                                                                                                                   | <span data-ttu-id="039d8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="039d8-109">Description</span></span>                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <span data-ttu-id="039d8-110"><dt>**\_obtención de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-110"><dt>**SNMP\_PDU\_GET**</dt></span></span> </dl>                | <span data-ttu-id="039d8-111">Busque y recupere un valor de una variable SNMP especificada.</span><span class="sxs-lookup"><span data-stu-id="039d8-111">Search and retrieve a value from a specified SNMP variable.</span></span><br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <span data-ttu-id="039d8-112"><dt>**\_GETNEXT de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-112"><dt>**SNMP\_PDU\_GETNEXT**</dt></span></span> </dl>    | <span data-ttu-id="039d8-113">Busque y recupere el valor de una variable SNMP sin conocer el nombre exacto de la variable.</span><span class="sxs-lookup"><span data-stu-id="039d8-113">Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.</span></span><br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <span data-ttu-id="039d8-114"><dt>**\_respuesta de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-114"><dt>**SNMP\_PDU\_RESPONSE**</dt></span></span> </dl> | <span data-ttu-id="039d8-115">Responda a una solicitud de PDU de SNMP \_ \_ get o a una \_ solicitud GETNEXT de PDU de SNMP \_ .</span><span class="sxs-lookup"><span data-stu-id="039d8-115">Reply to an SNMP\_PDU\_GET or an SNMP\_PDU\_GETNEXT request.</span></span><br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <span data-ttu-id="039d8-116"><dt>**\_conjunto de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-116"><dt>**SNMP\_PDU\_SET**</dt></span></span> </dl>                | <span data-ttu-id="039d8-117">Almacene un valor en una variable SNMP especificada.</span><span class="sxs-lookup"><span data-stu-id="039d8-117">Store a value in a specified SNMP variable.</span></span><br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <span data-ttu-id="039d8-118"><dt>**\_V1TRAP de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-118"><dt>**SNMP\_PDU\_V1TRAP**</dt></span></span> </dl>       | <span data-ttu-id="039d8-119">Indica que la captura de PDU tiene el formato que se ajusta al estándar SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="039d8-119">Indicates that the PDU trap is formatted to conform with the SNMPv1 standard.</span></span><br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <span data-ttu-id="039d8-120"><dt>**\_GetBulk e inform de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-120"><dt>**SNMP\_PDU\_GETBULK**</dt></span></span> </dl>    | <span data-ttu-id="039d8-121">Busque y recupere varios valores con una única solicitud.</span><span class="sxs-lookup"><span data-stu-id="039d8-121">Search and retrieve multiple values with a single request.</span></span><br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <span data-ttu-id="039d8-122"><dt>**\_Informe de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-122"><dt>**SNMP\_PDU\_INFORM**</dt></span></span> </dl>       | <span data-ttu-id="039d8-123">Indica una PDU de solicitud de informe.</span><span class="sxs-lookup"><span data-stu-id="039d8-123">Indicates an inform request PDU.</span></span><br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <span data-ttu-id="039d8-124"><dt>**\_captura de PDU de SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-124"><dt>**SNMP\_PDU\_TRAP**</dt></span></span> </dl>             | <span data-ttu-id="039d8-125">Avisa al sistema de administración de un evento extraordinario bajo SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="039d8-125">Alerts the management system to an extraordinary event under SNMPv2C.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="039d8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="039d8-126">Requirements</span></span>



| <span data-ttu-id="039d8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="039d8-127">Requirement</span></span> | <span data-ttu-id="039d8-128">Value</span><span class="sxs-lookup"><span data-stu-id="039d8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="039d8-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="039d8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="039d8-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="039d8-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="039d8-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="039d8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="039d8-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="039d8-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="039d8-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="039d8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="039d8-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="039d8-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="039d8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="039d8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039d8-136">Introducción al Protocolo simple de administración de redes (SNMP)</span><span class="sxs-lookup"><span data-stu-id="039d8-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="039d8-137">Referencia de SNMP</span><span class="sxs-lookup"><span data-stu-id="039d8-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="039d8-138">Constantes de SNMP</span><span class="sxs-lookup"><span data-stu-id="039d8-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

