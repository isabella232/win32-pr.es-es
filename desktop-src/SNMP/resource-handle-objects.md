---
title: Objetos de identificador de recursos
description: La estructura de un objeto de recurso está restringida a la implementación de Microsoft WinSNMP. Una aplicación WinSNMP puede tener acceso a un objeto de recurso con un identificador.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778595"
---
# <a name="resource-handle-objects"></a><span data-ttu-id="b6421-104">Objetos de identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="b6421-104">Resource Handle Objects</span></span>

<span data-ttu-id="b6421-105">La estructura de un objeto de recurso está restringida a la implementación de Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="b6421-105">The structure of a resource object is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="b6421-106">Una aplicación WinSNMP puede tener acceso a un objeto de recurso con un identificador.</span><span class="sxs-lookup"><span data-stu-id="b6421-106">A WinSNMP application can access a resource object with a handle.</span></span>

<span data-ttu-id="b6421-107">La implementación puede asignar uno de los siguientes tipos de identificadores de recursos para una aplicación WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="b6421-107">The implementation can allocate one of the following types of resource handles for a WinSNMP application.</span></span>

| <span data-ttu-id="b6421-108">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="b6421-108">Handle type</span></span>        | <span data-ttu-id="b6421-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6421-109">Description</span></span>                       |
|--------------------|-----------------------------------|
| <span data-ttu-id="b6421-110">**sesión de HSNMP \_**</span><span class="sxs-lookup"><span data-stu-id="b6421-110">**HSNMP\_SESSION**</span></span> | <span data-ttu-id="b6421-111">Identificador de una sesión WinSNMP</span><span class="sxs-lookup"><span data-stu-id="b6421-111">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="b6421-112">**\_entidad HSNMP**</span><span class="sxs-lookup"><span data-stu-id="b6421-112">**HSNMP\_ENTITY**</span></span>  | <span data-ttu-id="b6421-113">Identificador de una entidad SNMP</span><span class="sxs-lookup"><span data-stu-id="b6421-113">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="b6421-114">**contexto de HSNMP \_**</span><span class="sxs-lookup"><span data-stu-id="b6421-114">**HSNMP\_CONTEXT**</span></span> | <span data-ttu-id="b6421-115">Identificador de un contexto WinSNMP</span><span class="sxs-lookup"><span data-stu-id="b6421-115">Handle to a WinSNMP context</span></span>       |
| <span data-ttu-id="b6421-116">**PDU de HSNMP \_**</span><span class="sxs-lookup"><span data-stu-id="b6421-116">**HSNMP\_PDU**</span></span>     | <span data-ttu-id="b6421-117">Identificador de una unidad de datos de protocolo</span><span class="sxs-lookup"><span data-stu-id="b6421-117">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="b6421-118">**HSNMP \_ VBL**</span><span class="sxs-lookup"><span data-stu-id="b6421-118">**HSNMP\_VBL**</span></span>     | <span data-ttu-id="b6421-119">Identificador de una lista de enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="b6421-119">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="b6421-120">Una aplicación WinSNMP puede solicitar que la implementación cree o elimine identificadores de recursos, pero la implementación realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="b6421-120">A WinSNMP application can request that the implementation create or delete resource handles, but the implementation performs the operation.</span></span> <span data-ttu-id="b6421-121">Para obtener información adicional sobre cómo liberar recursos individuales, vea las funciones [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)y [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .</span><span class="sxs-lookup"><span data-stu-id="b6421-121">For additional information about freeing individual resources, see the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), and [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) functions.</span></span>

 

 




