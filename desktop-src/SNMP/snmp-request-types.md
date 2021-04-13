---
title: Tipos de solicitud SNMP (SNMP. h)
description: Los tipos de solicitud SNMP se utilizan para describir la operación que el servicio SNMP solicita al agente de extensión que realice.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492322"
---
# <a name="snmp-request-types"></a><span data-ttu-id="d89d0-103">Tipos de solicitudes SNMP</span><span class="sxs-lookup"><span data-stu-id="d89d0-103">SNMP Request Types</span></span>

<span data-ttu-id="d89d0-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d89d0-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d89d0-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="d89d0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="d89d0-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="d89d0-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="d89d0-107">Los tipos de solicitud SNMP se utilizan para describir la operación que el servicio SNMP solicita al agente de extensión que realice.</span><span class="sxs-lookup"><span data-stu-id="d89d0-107">The SNMP Request Types are used to describe the operation that the SNMP service is requesting the extension agent to perform.</span></span>



| <span data-ttu-id="d89d0-108">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="d89d0-108">Constant/value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="d89d0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d89d0-109">Description</span></span>                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <span data-ttu-id="d89d0-110"><dt>**SNMP \_ EXTENSIÓN \_ Get**</dt> <dt>SNMP \_ PDU \_ Get</dt></span><span class="sxs-lookup"><span data-stu-id="d89d0-110"><dt>**SNMP\_EXTENSION\_GET**</dt> <dt>SNMP\_PDU\_GET</dt></span></span> </dl>                       | <span data-ttu-id="d89d0-111">Recupera el valor de los valores de las variables especificadas.</span><span class="sxs-lookup"><span data-stu-id="d89d0-111">Retrieve the value of values of the specified variables.</span></span><br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <span data-ttu-id="d89d0-112"><dt>**SNMP \_ EXTENSIÓN \_ obtener \_ siguiente**</dt> <dt> \_ \_ GETNEXT de PDU de SNMP</dt></span><span class="sxs-lookup"><span data-stu-id="d89d0-112"><dt>**SNMP\_EXTENSION\_GET\_NEXT**</dt> <dt>SNMP\_PDU\_GETNEXT</dt></span></span> </dl>   | <span data-ttu-id="d89d0-113">Recupere el valor o los valores del sucesor lexicográfico de las variables especificadas.</span><span class="sxs-lookup"><span data-stu-id="d89d0-113">Retrieve the value or values of the lexicographic successor of the specified variables.</span></span><br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <span data-ttu-id="d89d0-114"><dt>**SNMP \_ EXTENSIÓN \_ Get \_ bulk**</dt> <dt>SNMP \_ PDU \_ GetBulk e inform</dt></span><span class="sxs-lookup"><span data-stu-id="d89d0-114"><dt>**SNMP\_EXTENSION\_GET\_BULK**</dt> <dt>SNMP\_PDU\_GETBULK</dt></span></span> </dl>   | <span data-ttu-id="d89d0-115">Busque y recupere varios valores con una única solicitud.</span><span class="sxs-lookup"><span data-stu-id="d89d0-115">Search and retrieve multiple values with a single request.</span></span><br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <span data-ttu-id="d89d0-116"><dt>**\_prueba de \_ conjunto de extensiones SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d89d0-116"><dt>**SNMP\_EXTENSION\_SET\_TEST**</dt></span></span> </dl>                                                                           | <span data-ttu-id="d89d0-117">Valide los valores de las variables especificadas.</span><span class="sxs-lookup"><span data-stu-id="d89d0-117">Validate the values of the specified variables.</span></span> <span data-ttu-id="d89d0-118">Esta operación maximiza la probabilidad de una operación de escritura correcta durante la solicitud de confirmación.</span><span class="sxs-lookup"><span data-stu-id="d89d0-118">This operation maximizes the probability of a successful write operation during the COMMIT request.</span></span> <span data-ttu-id="d89d0-119">Para obtener más información, vea la función [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .</span><span class="sxs-lookup"><span data-stu-id="d89d0-119">For more information, see the [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) function.</span></span><br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <span data-ttu-id="d89d0-120"><dt>**SNMP \_ \_ \_**</dt> conjunto de la <dt> \_ PDU \_</dt> de confirmación del conjunto de extensiones</span><span class="sxs-lookup"><span data-stu-id="d89d0-120"><dt>**SNMP\_EXTENSION\_SET\_COMMIT**</dt> <dt>SNMP\_PDU\_SET</dt></span></span> </dl> | <span data-ttu-id="d89d0-121">Escriba los nuevos valores en las variables especificadas.</span><span class="sxs-lookup"><span data-stu-id="d89d0-121">Write the new values to the specified variables.</span></span><br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <span data-ttu-id="d89d0-122"><dt>**\_Deshacer conjunto de extensiones SNMP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d89d0-122"><dt>**SNMP\_EXTENSION\_SET\_UNDO**</dt></span></span> </dl>                                                                           | <span data-ttu-id="d89d0-123">Restablezca los valores de las variables especificadas a sus valores antes de la solicitud de confirmación.</span><span class="sxs-lookup"><span data-stu-id="d89d0-123">Reset the values of the specified variables to their values before the COMMIT request.</span></span><br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <span data-ttu-id="d89d0-124"><dt>**\_limpieza del \_ conjunto de extensiones SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d89d0-124"><dt>**SNMP\_EXTENSION\_SET\_CLEANUP**</dt></span></span> </dl>                                                                  | <span data-ttu-id="d89d0-125">Libera los recursos asignados en las solicitudes y operaciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d89d0-125">Release the resources allocated in previous requests and operations.</span></span><br/>                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="d89d0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d89d0-126">Requirements</span></span>



| <span data-ttu-id="d89d0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d89d0-127">Requirement</span></span> | <span data-ttu-id="d89d0-128">Value</span><span class="sxs-lookup"><span data-stu-id="d89d0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d89d0-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d89d0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d89d0-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d89d0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="d89d0-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d89d0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d89d0-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d89d0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d89d0-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d89d0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d89d0-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="d89d0-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d89d0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d89d0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89d0-136">Introducción al Protocolo simple de administración de redes (SNMP)</span><span class="sxs-lookup"><span data-stu-id="d89d0-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="d89d0-137">Referencia de SNMP</span><span class="sxs-lookup"><span data-stu-id="d89d0-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="d89d0-138">Constantes de SNMP</span><span class="sxs-lookup"><span data-stu-id="d89d0-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

