---
title: Identificadores de objeto (SNMP)
description: Un identificador de objeto SNMP asigna un nombre único a un objeto e identifica su ubicación dentro de una estructura de árbol de la base de datos de información de administración (MIB).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800649"
---
# <a name="object-identifiers-snmp"></a><span data-ttu-id="94761-103">Identificadores de objeto (SNMP)</span><span class="sxs-lookup"><span data-stu-id="94761-103">Object Identifiers (SNMP)</span></span>

<span data-ttu-id="94761-104">Un identificador de objeto SNMP asigna un nombre único a un objeto e identifica su ubicación dentro de una estructura de árbol de la base de datos de información de administración (MIB).</span><span class="sxs-lookup"><span data-stu-id="94761-104">An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure.</span></span> <span data-ttu-id="94761-105">Los identificadores de objeto son tipos de datos de notación de sintaxis abstracta (ASN. 1) independientes de la aplicación que se componen de una secuencia de enteros no negativos o de subidentificadors.</span><span class="sxs-lookup"><span data-stu-id="94761-105">Object identifiers are application-independent Abstract Syntax Notation One (ASN.1) data types that consist of a sequence of non-negative integers, or subidentifiers.</span></span> <span data-ttu-id="94761-106">Los identificadores de objeto deben tener un mínimo de dos subidentificadors y no deben superar los 128 subidentificadors.</span><span class="sxs-lookup"><span data-stu-id="94761-106">Object identifiers must have a minimum of two subidentifiers and they must not exceed 128 subidentifiers.</span></span>

<span data-ttu-id="94761-107">El entorno de programación WinSNMP utiliza la estructura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) para administrar los identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="94761-107">The WinSNMP programming environment uses the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure to manage object identifiers.</span></span> <span data-ttu-id="94761-108">El formato de la matriz de identificadores de objeto en una estructura **smiOID** es un subidentificador por elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="94761-108">The format of the object identifier array in an **smiOID** structure is one subidentifier per array element.</span></span>

<span data-ttu-id="94761-109">La representación de cadena numérica con puntos de un identificador de objeto separa sus subidentificadors con puntos; por ejemplo, "1.2.3.4.5.6".</span><span class="sxs-lookup"><span data-stu-id="94761-109">The dotted numeric string representation of an object identifier separates its subidentifiers with periods; for example, "1.2.3.4.5.6".</span></span>

<span data-ttu-id="94761-110">Para obtener más información, consulte [la base de datos de información de administración (MIB) de SNMP](the-snmp-management-information-base-mib-.md) y las RFC pertinentes.</span><span class="sxs-lookup"><span data-stu-id="94761-110">For more information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) and the relevant RFCs.</span></span>

 

 




