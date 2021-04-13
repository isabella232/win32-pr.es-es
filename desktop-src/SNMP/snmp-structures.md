---
title: Estructuras SNMP
description: En la tabla siguiente se enumeran las estructuras que se utilizan con SNMP.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP de estructuras SNMP
- Estructuras SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421288"
---
# <a name="snmp-structures"></a><span data-ttu-id="6793d-105">Estructuras SNMP</span><span class="sxs-lookup"><span data-stu-id="6793d-105">SNMP Structures</span></span>

<span data-ttu-id="6793d-106">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6793d-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6793d-107">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="6793d-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6793d-108">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="6793d-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="6793d-109">En la tabla siguiente se enumeran las estructuras que se utilizan con SNMP.</span><span class="sxs-lookup"><span data-stu-id="6793d-109">The following table lists structures that are used with SNMP.</span></span>



| <span data-ttu-id="6793d-110">Estructura SNMP</span><span class="sxs-lookup"><span data-stu-id="6793d-110">SNMP Structure</span></span>                                         | <span data-ttu-id="6793d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6793d-111">Description</span></span>                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6793d-112">**AsnAny**</span><span class="sxs-lookup"><span data-stu-id="6793d-112">**AsnAny**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | <span data-ttu-id="6793d-113">Describe el tipo y el valor de una variable de SNMP especificada.</span><span class="sxs-lookup"><span data-stu-id="6793d-113">Describes the type and value of a specified SNMP variable.</span></span>                                              |
| <span data-ttu-id="6793d-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6793d-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span></span>               | <span data-ttu-id="6793d-115">Contiene un contador de 64 bits especificado por dos valores que describen sus bits de orden inferior y de orden superior.</span><span class="sxs-lookup"><span data-stu-id="6793d-115">Contains a 64-bit counter that is specified by two values describing its low-order and high-order bits.</span></span> |
| [<span data-ttu-id="6793d-116">**AsnObjectIdentifier**</span><span class="sxs-lookup"><span data-stu-id="6793d-116">**AsnObjectIdentifier**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | <span data-ttu-id="6793d-117">Describe un identificador de objeto (OID).</span><span class="sxs-lookup"><span data-stu-id="6793d-117">Describes an object identifier (OID).</span></span>                                                                   |
| [<span data-ttu-id="6793d-118">**AsnOctetString**</span><span class="sxs-lookup"><span data-stu-id="6793d-118">**AsnOctetString**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | <span data-ttu-id="6793d-119">Representa una cadena de octetos, normalmente en valores de bytes.</span><span class="sxs-lookup"><span data-stu-id="6793d-119">Represents a string of octets, usually in byte values.</span></span>                                                  |
| [<span data-ttu-id="6793d-120">**SnmpVarBind**</span><span class="sxs-lookup"><span data-stu-id="6793d-120">**SnmpVarBind**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | <span data-ttu-id="6793d-121">Describe un enlace de variable SNMP.</span><span class="sxs-lookup"><span data-stu-id="6793d-121">Describes an SNMP variable binding.</span></span>                                                                     |
| [<span data-ttu-id="6793d-122">**SnmpVarBindList**</span><span class="sxs-lookup"><span data-stu-id="6793d-122">**SnmpVarBindList**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | <span data-ttu-id="6793d-123">Contiene una lista de enlaces de variables SNMP.</span><span class="sxs-lookup"><span data-stu-id="6793d-123">Contains a list of SNMP variable bindings.</span></span>                                                              |



 

 

 