---
title: Asignación de objetos de memoria WinSNMP
description: Los descriptores, los identificadores de recursos y las cadenas de estilo C son tres tipos de objetos de memoria en el entorno de programación WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075048"
---
# <a name="allocating-winsnmp-memory-objects"></a><span data-ttu-id="81fa1-103">Asignación de objetos de memoria WinSNMP</span><span class="sxs-lookup"><span data-stu-id="81fa1-103">Allocating WinSNMP Memory Objects</span></span>

<span data-ttu-id="81fa1-104">Los descriptores, los identificadores de recursos y las cadenas de estilo C son tres tipos de objetos de memoria en el entorno de programación WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="81fa1-104">Descriptors, resource handles and C-style strings are the three types of memory objects in the WinSNMP programming environment.</span></span>

<span data-ttu-id="81fa1-105">El tipo de objeto determina si la implementación de Microsoft WinSNMP o la aplicación WinSNMP asigna y desasigna la memoria para el objeto.</span><span class="sxs-lookup"><span data-stu-id="81fa1-105">The type of object determines whether the Microsoft WinSNMP implementation or the WinSNMP application allocates and deallocates the memory for the object.</span></span> <span data-ttu-id="81fa1-106">Esto reduce la asignación innecesaria de espacio en búfer temporal y la copia innecesaria de búferes.</span><span class="sxs-lookup"><span data-stu-id="81fa1-106">This reduces unnecessary allocation of temporary buffer space and unnecessary copying of buffers.</span></span>

<span data-ttu-id="81fa1-107">En la tabla siguiente se resume la asignación y desasignación de recursos para los objetos de memoria WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="81fa1-107">The following table summarizes the allocation and deallocation of resources for WinSNMP memory objects.</span></span>



| <span data-ttu-id="81fa1-108">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="81fa1-108">Object type</span></span>                                                                   | <span data-ttu-id="81fa1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="81fa1-109">Description</span></span>                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fa1-110">descriptor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)</span><span class="sxs-lookup"><span data-stu-id="81fa1-110">[**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor</span></span> | <span data-ttu-id="81fa1-111">Si la aplicación WinSNMP asigna la memoria, debe desasignar la memoria con una llamada a una función adecuada.</span><span class="sxs-lookup"><span data-stu-id="81fa1-111">If the WinSNMP application allocates the memory, it must deallocate the memory with a call to an appropriate function.</span></span> <span data-ttu-id="81fa1-112">Si la implementación asigna la memoria, la aplicación debe llamar a la función [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para desasignar la memoria.</span><span class="sxs-lookup"><span data-stu-id="81fa1-112">If the implementation allocates the memory, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to deallocate the memory.</span></span> |
| <span data-ttu-id="81fa1-113">estructura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)</span><span class="sxs-lookup"><span data-stu-id="81fa1-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure</span></span>                                    | <span data-ttu-id="81fa1-114">Si el miembro de **valor** es un descriptor de [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , la aplicación debe continuar como se indicó anteriormente para los descriptores.</span><span class="sxs-lookup"><span data-stu-id="81fa1-114">If the **value** member is an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor, the application must proceed as indicated above for descriptors.</span></span>                                                                                                     |
| <span data-ttu-id="81fa1-115">Identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="81fa1-115">Resource handle</span></span>                                                               | <span data-ttu-id="81fa1-116">La implementación asigna, administra y libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="81fa1-116">The implementation allocates, manages, and frees the memory.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="81fa1-117">Cadena de estilo C</span><span class="sxs-lookup"><span data-stu-id="81fa1-117">C-style string</span></span>                                                                | <span data-ttu-id="81fa1-118">La aplicación WinSNMP debe administrar y liberar la memoria que asigna.</span><span class="sxs-lookup"><span data-stu-id="81fa1-118">The WinSNMP application must manage and free the memory it allocates.</span></span>                                                                                                                                                                                                                |



 

<span data-ttu-id="81fa1-119">Para obtener más información, consulte [liberación de descriptores WinSNMP](freeing-winsnmp-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="81fa1-119">For more information, see [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).</span></span>

 

 




