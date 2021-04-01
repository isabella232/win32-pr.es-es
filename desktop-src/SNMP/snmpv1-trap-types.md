---
title: Tipos de captura de SNMPv1 (SNMP. h)
description: Los tipos de captura de SNMPv1 describen un conjunto predefinido de tipos de captura genéricos con formato para cumplir con el estándar de la PDU de captura de SNMPv1.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905621"
---
# <a name="snmpv1-trap-types"></a><span data-ttu-id="9663e-103">SNMPv1 (tipos de captura)</span><span class="sxs-lookup"><span data-stu-id="9663e-103">SNMPv1 Trap Types</span></span>

<span data-ttu-id="9663e-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="9663e-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9663e-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="9663e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9663e-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="9663e-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="9663e-107">Los tipos de captura de SNMPv1 describen un conjunto predefinido de tipos de captura genéricos con formato para cumplir con el estándar de la PDU de captura de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="9663e-107">The SNMPv1 trap types describe a predefined set of generic trap types that are formatted to comply with the SNMPv1 trap PDU standard.</span></span>



| <span data-ttu-id="9663e-108">Constante</span><span class="sxs-lookup"><span data-stu-id="9663e-108">Constant</span></span>                                                                                                                                                                                                          | <span data-ttu-id="9663e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9663e-109">Description</span></span>                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <span data-ttu-id="9663e-110"><dt>**\_COLDSTART GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="9663e-110"><dt>**SNMP\_GENERICTRAP\_COLDSTART**</dt></span></span> </dl>             | <span data-ttu-id="9663e-111">Indica una captura de inicio en frío.</span><span class="sxs-lookup"><span data-stu-id="9663e-111">Indicates a cold start trap.</span></span> <span data-ttu-id="9663e-112">El agente está inicializando entidades de protocolo en el modo administrado.</span><span class="sxs-lookup"><span data-stu-id="9663e-112">The agent is initializing protocol entities on the managed mode.</span></span> <span data-ttu-id="9663e-113">Puede modificar los objetos en su vista.</span><span class="sxs-lookup"><span data-stu-id="9663e-113">It may alter objects in its view.</span></span><br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <span data-ttu-id="9663e-114"><dt>**\_WARMSTART GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="9663e-114"><dt>**SNMP\_GENERICTRAP\_WARMSTART**</dt></span></span> </dl>             | <span data-ttu-id="9663e-115">Indica una captura de inicio en caliente.</span><span class="sxs-lookup"><span data-stu-id="9663e-115">Indicates a warm start trap.</span></span> <span data-ttu-id="9663e-116">El agente se está reinicializando, pero no modificará los objetos en su vista.</span><span class="sxs-lookup"><span data-stu-id="9663e-116">The agent is reinitializing itself but it will not alter objects in its view.</span></span><br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <span data-ttu-id="9663e-117"><dt>**\_LINKDOWN GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="9663e-117"><dt>**SNMP\_GENERICTRAP\_LINKDOWN**</dt></span></span> </dl>                | <span data-ttu-id="9663e-118">Indica una captura de vínculo.</span><span class="sxs-lookup"><span data-stu-id="9663e-118">Indicates a link-down trap.</span></span> <span data-ttu-id="9663e-119">Una interfaz adjunta ha cambiado del estado up al estado Down.</span><span class="sxs-lookup"><span data-stu-id="9663e-119">An attached interface has changed from the up state to the down state.</span></span> <span data-ttu-id="9663e-120">La primera variable de la lista de enlaces de variables identifica la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9663e-120">The first variable in the variable bindings list identifies the interface.</span></span><br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <span data-ttu-id="9663e-121"><dt>**\_LINKUP GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="9663e-121"><dt>**SNMP\_GENERICTRAP\_LINKUP**</dt></span></span> </dl>                      | <span data-ttu-id="9663e-122">Indica una captura de vínculo.</span><span class="sxs-lookup"><span data-stu-id="9663e-122">Indicates a link-up trap.</span></span> <span data-ttu-id="9663e-123">Una interfaz asociada ha cambiado desde el inicio hacia abajo hasta el estado activo.</span><span class="sxs-lookup"><span data-stu-id="9663e-123">An attached interface has changed from the down start to the up state.</span></span> <span data-ttu-id="9663e-124">La primera variable de la lista de enlaces de variables identifica la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9663e-124">The first variable in the variable bindings list identifies the interface.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <span data-ttu-id="9663e-125"><dt>**\_AUTHFAILURE GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="9663e-125"><dt>**SNMP\_GENERICTRAP\_AUTHFAILURE**</dt></span></span> </dl>       | <span data-ttu-id="9663e-126">Indica una interceptación de errores de autenticación.</span><span class="sxs-lookup"><span data-stu-id="9663e-126">Indicates an authentication failure trap.</span></span> <span data-ttu-id="9663e-127">Una entidad SNMP ha enviado un mensaje SNMP, pero se ha reclamado falsamente que pertenece a una comunidad conocida.</span><span class="sxs-lookup"><span data-stu-id="9663e-127">An SNMP entity has sent an SNMP message, but it has falsely claimed to belong to a known community.</span></span><br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <span data-ttu-id="9663e-128"><dt>**\_EGPNEIGHLOSS GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="9663e-128"><dt>**SNMP\_GENERICTRAP\_EGPNEIGHLOSS**</dt></span></span> </dl>    | <span data-ttu-id="9663e-129">Indica una captura de pérdida del vecino EGP.</span><span class="sxs-lookup"><span data-stu-id="9663e-129">Indicates an EGP neighbor loss trap.</span></span> <span data-ttu-id="9663e-130">Un elemento EGP del mismo nivel ha cambiado al estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="9663e-130">An EGP peer has changed to the down state.</span></span> <span data-ttu-id="9663e-131">La primera variable de la lista de enlaces de variables identifica la dirección IP del homólogo EGP.</span><span class="sxs-lookup"><span data-stu-id="9663e-131">The first variable in the variable bindings list identifies the IP address of the EGP peer.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <span data-ttu-id="9663e-132"><dt>**\_ENTERSPECIFIC GENERICTRAP \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="9663e-132"><dt>**SNMP\_GENERICTRAP\_ENTERSPECIFIC**</dt></span></span> </dl> | <span data-ttu-id="9663e-133">Indica una captura específica de la empresa.</span><span class="sxs-lookup"><span data-stu-id="9663e-133">Indicates an enterprise-specific trap.</span></span> <span data-ttu-id="9663e-134">Se ha producido un evento extraordinario.</span><span class="sxs-lookup"><span data-stu-id="9663e-134">An extraordinary event has occurred.</span></span> <span data-ttu-id="9663e-135">Se identifica en el parámetro *specificTrap* con un valor específico de la empresa.</span><span class="sxs-lookup"><span data-stu-id="9663e-135">It is identified in the *specificTrap* parameter with an enterprise-specific value.</span></span><br/>               |



## <a name="requirements"></a><span data-ttu-id="9663e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9663e-136">Requirements</span></span>



| <span data-ttu-id="9663e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="9663e-137">Requirement</span></span> | <span data-ttu-id="9663e-138">Value</span><span class="sxs-lookup"><span data-stu-id="9663e-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9663e-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9663e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9663e-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9663e-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="9663e-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9663e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9663e-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9663e-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9663e-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9663e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9663e-144"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="9663e-144"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9663e-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="9663e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9663e-146">Introducción al Protocolo simple de administración de redes (SNMP)</span><span class="sxs-lookup"><span data-stu-id="9663e-146">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="9663e-147">Referencia de SNMP</span><span class="sxs-lookup"><span data-stu-id="9663e-147">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="9663e-148">Constantes de SNMP</span><span class="sxs-lookup"><span data-stu-id="9663e-148">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

