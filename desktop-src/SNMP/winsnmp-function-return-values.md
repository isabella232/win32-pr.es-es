---
title: Valores devueltos de la función WinSNMP
description: El valor devuelto de una llamada de función WinSNMP puede ser un identificador de un recurso que la implementación de Microsoft WinSNMP asigna a la aplicación WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078246"
---
# <a name="winsnmp-function-return-values"></a><span data-ttu-id="9d70d-103">Valores devueltos de la función WinSNMP</span><span class="sxs-lookup"><span data-stu-id="9d70d-103">WinSNMP Function Return Values</span></span>

<span data-ttu-id="9d70d-104">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="9d70d-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9d70d-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="9d70d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9d70d-106">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="9d70d-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="9d70d-107">El valor devuelto de una llamada de función WinSNMP puede ser un identificador de un recurso que la implementación de Microsoft WinSNMP asigna a la aplicación WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="9d70d-107">The return value from a WinSNMP function call can be a handle to a resource that the Microsoft WinSNMP implementation allocates for the WinSNMP application.</span></span>

<span data-ttu-id="9d70d-108">En la tabla siguiente se enumeran los cinco tipos de identificadores de recursos que asigna la implementación.</span><span class="sxs-lookup"><span data-stu-id="9d70d-108">The following table lists the five types of resource handles that the implementation allocates.</span></span>



| <span data-ttu-id="9d70d-109">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="9d70d-109">Handle type</span></span>    | <span data-ttu-id="9d70d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d70d-110">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="9d70d-111">sesión de HSNMP \_</span><span class="sxs-lookup"><span data-stu-id="9d70d-111">HSNMP\_SESSION</span></span> | <span data-ttu-id="9d70d-112">Identificador de una sesión WinSNMP</span><span class="sxs-lookup"><span data-stu-id="9d70d-112">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="9d70d-113">\_entidad HSNMP</span><span class="sxs-lookup"><span data-stu-id="9d70d-113">HSNMP\_ENTITY</span></span>  | <span data-ttu-id="9d70d-114">Identificador de una entidad SNMP</span><span class="sxs-lookup"><span data-stu-id="9d70d-114">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="9d70d-115">contexto de HSNMP \_</span><span class="sxs-lookup"><span data-stu-id="9d70d-115">HSNMP\_CONTEXT</span></span> | <span data-ttu-id="9d70d-116">Identificador de un contexto SNMP</span><span class="sxs-lookup"><span data-stu-id="9d70d-116">Handle to an SNMP context</span></span>         |
| <span data-ttu-id="9d70d-117">PDU de HSNMP \_</span><span class="sxs-lookup"><span data-stu-id="9d70d-117">HSNMP\_PDU</span></span>     | <span data-ttu-id="9d70d-118">Identificador de una unidad de datos de protocolo</span><span class="sxs-lookup"><span data-stu-id="9d70d-118">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="9d70d-119">HSNMP \_ VBL</span><span class="sxs-lookup"><span data-stu-id="9d70d-119">HSNMP\_VBL</span></span>     | <span data-ttu-id="9d70d-120">Identificador de una lista de enlaces de variables</span><span class="sxs-lookup"><span data-stu-id="9d70d-120">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="9d70d-121">Para obtener más información, vea [objetos de identificador de recursos](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9d70d-121">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="9d70d-122">El valor devuelto también puede ser un valor entero largo sin signo del tipo **smiUINT32** que representa un \_ valor de estado snmpapi.</span><span class="sxs-lookup"><span data-stu-id="9d70d-122">The return value can also be an unsigned long integer value of the **smiUINT32** type that represents an SNMPAPI\_STATUS value.</span></span>

<span data-ttu-id="9d70d-123">En la tabla siguiente se enumeran los valores de estado de WinSNMP y su significado.</span><span class="sxs-lookup"><span data-stu-id="9d70d-123">The following table lists the WinSNMP status values and their meaning.</span></span>



| <span data-ttu-id="9d70d-124">Status</span><span class="sxs-lookup"><span data-stu-id="9d70d-124">Status</span></span>           | <span data-ttu-id="9d70d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d70d-125">Description</span></span>                                                                      |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9d70d-126">error de SNMPAPI \_</span><span class="sxs-lookup"><span data-stu-id="9d70d-126">SNMPAPI\_FAILURE</span></span> | <span data-ttu-id="9d70d-127">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="9d70d-127">Indicates an error.</span></span> <span data-ttu-id="9d70d-128">Equivale a 0 o **null**.</span><span class="sxs-lookup"><span data-stu-id="9d70d-128">Equates to 0 or **NULL**.</span></span>                                    |
| <span data-ttu-id="9d70d-129">SNMPAPI \_ correcto</span><span class="sxs-lookup"><span data-stu-id="9d70d-129">SNMPAPI\_SUCCESS</span></span> | <span data-ttu-id="9d70d-130">Indica que la función se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d70d-130">Indicates the function completed successfully.</span></span> <span data-ttu-id="9d70d-131">Equivale a 1 o a un recuento positivo.</span><span class="sxs-lookup"><span data-stu-id="9d70d-131">Equates to 1 or a positive count.</span></span> |



 

 

 