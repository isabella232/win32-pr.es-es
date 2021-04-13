---
title: Descriptores de WinSNMP
description: En el entorno de programación WinSNMP, un descriptor es una de las dos estructuras siguientes.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356804"
---
# <a name="winsnmp-descriptors"></a><span data-ttu-id="8ba30-103">Descriptores de WinSNMP</span><span class="sxs-lookup"><span data-stu-id="8ba30-103">WinSNMP Descriptors</span></span>

<span data-ttu-id="8ba30-104">En el entorno de programación WinSNMP, un *descriptor* es una de las dos estructuras siguientes:</span><span class="sxs-lookup"><span data-stu-id="8ba30-104">In the WinSNMP programming environment a *descriptor* is one of the following two structures:</span></span>

-   <span data-ttu-id="8ba30-105">Una estructura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) que describe una variable de cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="8ba30-105">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure which describes an octet string variable</span></span>
-   <span data-ttu-id="8ba30-106">Una estructura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) que describe una variable de identificador de objeto SNMP</span><span class="sxs-lookup"><span data-stu-id="8ba30-106">An [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure which describes an SNMP object identifier variable</span></span>

<span data-ttu-id="8ba30-107">Un descriptor WinSNMP es una estructura que tiene dos miembros: un miembro de longitud, **Len** y un miembro de puntero, **ptr**.</span><span class="sxs-lookup"><span data-stu-id="8ba30-107">A WinSNMP descriptor is a structure that has two members: a length member, **len**, and a pointer member, **ptr**.</span></span> <span data-ttu-id="8ba30-108">El miembro **ptr** apunta a la cadena de octeto o al identificador de objeto de interés.</span><span class="sxs-lookup"><span data-stu-id="8ba30-108">The **ptr** member points to the octet string or object identifier of interest.</span></span> <span data-ttu-id="8ba30-109">El miembro **ptr** puede ser el tipo de datos **smiLPBYTE** o **smiLPUINT32** .</span><span class="sxs-lookup"><span data-stu-id="8ba30-109">The **ptr** member can be either the **smiLPBYTE** or **smiLPUINT32** data type.</span></span>

<span data-ttu-id="8ba30-110">Un descriptor de [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o un descriptor [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) puede ser el miembro de **valor** de una estructura **smiVALUE** .</span><span class="sxs-lookup"><span data-stu-id="8ba30-110">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor or an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) descriptor can be the **value** member of an **smiVALUE** structure.</span></span> <span data-ttu-id="8ba30-111">La estructura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) describe el valor asociado a un nombre de variable en una entrada de enlace de variables.</span><span class="sxs-lookup"><span data-stu-id="8ba30-111">The [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure describes the value associated with a variable name in a variable binding entry.</span></span>

<span data-ttu-id="8ba30-112">La implementación de Microsoft WinSNMP asigna y desasigna memoria para todas las estructuras **smiOCTETS** y **smiOID** de salida.</span><span class="sxs-lookup"><span data-stu-id="8ba30-112">The Microsoft WinSNMP implementation allocates and deallocates memory for all output **smiOCTETS** and **smiOID** structures.</span></span> <span data-ttu-id="8ba30-113">Por lo tanto, la aplicación debe llamar a la función [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar la memoria para el miembro **ptr** de estas estructuras.</span><span class="sxs-lookup"><span data-stu-id="8ba30-113">Therefore, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free the memory for the **ptr** member of these structures.</span></span>

<span data-ttu-id="8ba30-114">Los miembros de cadena en los descriptores no requieren un byte de terminación **null** .</span><span class="sxs-lookup"><span data-stu-id="8ba30-114">String members in descriptors do not require a **NULL** terminating byte.</span></span> <span data-ttu-id="8ba30-115">Para obtener información adicional sobre la administración de la memoria asignada para los descriptores, vea [asignar objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8ba30-115">For additional information about managing the memory allocated for descriptors, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




