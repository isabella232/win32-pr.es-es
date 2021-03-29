---
title: Administrar identificadores de objeto
description: La API WinSNMP proporciona varias funciones de utilidad WinSNMP que simplifican la manipulación de los identificadores de objeto para las aplicaciones WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486983"
---
# <a name="managing-object-identifiers"></a><span data-ttu-id="b7e33-103">Administrar identificadores de objeto</span><span class="sxs-lookup"><span data-stu-id="b7e33-103">Managing Object Identifiers</span></span>

<span data-ttu-id="b7e33-104">La API WinSNMP proporciona varias [funciones de utilidad WinSNMP](winsnmp-functions.md) que simplifican la manipulación de los identificadores de objeto para las aplicaciones WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="b7e33-104">The WinSNMP API provides several [WinSNMP utility functions](winsnmp-functions.md) that simplify the manipulation of object identifiers for WinSNMP applications.</span></span>

<span data-ttu-id="b7e33-105">La función [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) convierte la representación binaria interna de un identificador de objeto en su formato de cadena numérica con puntos.</span><span class="sxs-lookup"><span data-stu-id="b7e33-105">The [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) function converts the internal binary representation of an object identifier to its dotted numeric string format.</span></span> <span data-ttu-id="b7e33-106">Cuando llame a [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), especifique un búfer de cadena de longitud MAXOBJIDSTRSIZE (1408 bytes) para asegurarse de que el búfer de salida es lo suficientemente grande como para contener la cadena convertida.</span><span class="sxs-lookup"><span data-stu-id="b7e33-106">When you call [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specify a string buffer of MAXOBJIDSTRSIZE length (1408 bytes) to ensure that the output buffer is large enough to hold the converted string.</span></span> <span data-ttu-id="b7e33-107">Para convertir un identificador de objeto del formato de cadena numérica con puntos en su representación binaria interna, llame a la función [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .</span><span class="sxs-lookup"><span data-stu-id="b7e33-107">To convert an object identifier from the dotted numeric string format to its internal binary representation, call the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) function.</span></span>

<span data-ttu-id="b7e33-108">Para copiar un identificador de objeto SNMP, llame a la función [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="b7e33-108">To copy an SNMP object identifier call the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) function.</span></span> <span data-ttu-id="b7e33-109">Esta función asigna cualquier memoria necesaria para el nuevo identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="b7e33-109">This function allocates any necessary memory for the new object identifier.</span></span>

<span data-ttu-id="b7e33-110">Una aplicación WinSNMP debe llamar a la función [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar los recursos asignados para el miembro **ptr** de la estructura [**SmiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) especificada por las funciones [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) y [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="b7e33-110">A WinSNMP application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free resources allocated for the **ptr** member of the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure specified by both the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) and the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) functions.</span></span>

<span data-ttu-id="b7e33-111">La función [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) compara dos identificadores de objeto SNMP.</span><span class="sxs-lookup"><span data-stu-id="b7e33-111">The [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) function compares two SNMP object identifiers.</span></span> <span data-ttu-id="b7e33-112">La aplicación WinSNMP puede especificar el número de subidentificadors que se van a comparar.</span><span class="sxs-lookup"><span data-stu-id="b7e33-112">The WinSNMP application can specify the number of subidentifiers to compare.</span></span> <span data-ttu-id="b7e33-113">Llame a **SnmpOidCompare** para determinar si dos identificadores de objeto tienen prefijos comunes.</span><span class="sxs-lookup"><span data-stu-id="b7e33-113">Call **SnmpOidCompare** to determine whether two object identifiers have common prefixes.</span></span>

<span data-ttu-id="b7e33-114">Para obtener información adicional sobre la administración de la memoria asignada para los identificadores de objeto, vea [asignar objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b7e33-114">For additional information about managing the memory allocated for object identifiers, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




