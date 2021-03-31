---
title: Tipos de variables de SNMP y tipos PDU de solicitud
description: Las definiciones de algunos tipos de variables de SNMP y tipos PDU de solicitud han cambiado. El archivo SNMP. h asigna los tipos antiguos a los nuevos tipos correspondientes.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792867"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a><span data-ttu-id="7d067-104">Tipos de variables de SNMP y tipos PDU de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d067-104">SNMP Variable Types and Request PDU Types</span></span>

<span data-ttu-id="7d067-105">\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7d067-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d067-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="7d067-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7d067-107">En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]</span><span class="sxs-lookup"><span data-stu-id="7d067-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="7d067-108">Las definiciones de algunos tipos de variables de SNMP y tipos PDU de solicitud han cambiado.</span><span class="sxs-lookup"><span data-stu-id="7d067-108">The definitions for some SNMP variable types and request PDU types have changed.</span></span> <span data-ttu-id="7d067-109">El archivo SNMP. h asigna los tipos antiguos a los nuevos tipos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="7d067-109">The Snmp.h file maps old types to the corresponding new types.</span></span>

## <a name="modified-snmp-variable-types"></a><span data-ttu-id="7d067-110">Tipos de variables SNMP modificados</span><span class="sxs-lookup"><span data-stu-id="7d067-110">Modified SNMP Variable Types</span></span>

<span data-ttu-id="7d067-111">Debe usar los nuevos tipos de variables SNMP que se enumeran en la tabla siguiente al desarrollar aplicaciones de administrador que utilizan la API de administración de SNMP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d067-111">You should use the new SNMP variable types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="7d067-112">En la tabla se enumeran los tipos de variables SNMP anteriores con los nuevos tipos de variables correspondientes.</span><span class="sxs-lookup"><span data-stu-id="7d067-112">The table lists the old SNMP variable types with the corresponding new variable types.</span></span>

| <span data-ttu-id="7d067-113">Tipo de variable anterior</span><span class="sxs-lookup"><span data-stu-id="7d067-113">Old variable type</span></span>        | <span data-ttu-id="7d067-114">Nuevo tipo de variable</span><span class="sxs-lookup"><span data-stu-id="7d067-114">New variable type</span></span> |
|--------------------------|-------------------|
| <span data-ttu-id="7d067-115">\_ \_ Dirección IP de ASN RFC1155</span><span class="sxs-lookup"><span data-stu-id="7d067-115">ASN\_RFC1155\_IPADDRESS</span></span>  | <span data-ttu-id="7d067-116">\_dirección IP de ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-116">ASN\_IPADDRESS</span></span>    |
| <span data-ttu-id="7d067-117">\_Contador RFC1155 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-117">ASN\_RFC1155\_COUNTER</span></span>    | <span data-ttu-id="7d067-118">\_COUNTER32 ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-118">ASN\_COUNTER32</span></span>    |
| <span data-ttu-id="7d067-119">\_Medidor de RFC1155 ASN \_</span><span class="sxs-lookup"><span data-stu-id="7d067-119">ASN\_RFC1155\_GAUGE</span></span>      | <span data-ttu-id="7d067-120">\_GAUGE32 ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-120">ASN\_GAUGE32</span></span>      |
| <span data-ttu-id="7d067-121">\_TIMETICKS RFC1155 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-121">ASN\_RFC1155\_TIMETICKS</span></span>  | <span data-ttu-id="7d067-122">\_TIMETICKS ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-122">ASN\_TIMETICKS</span></span>    |
| <span data-ttu-id="7d067-123">ASN \_ RFC1155 \_ opaco</span><span class="sxs-lookup"><span data-stu-id="7d067-123">ASN\_RFC1155\_OPAQUE</span></span>     | <span data-ttu-id="7d067-124">opaco de ASN \_</span><span class="sxs-lookup"><span data-stu-id="7d067-124">ASN\_OPAQUE</span></span>       |
| <span data-ttu-id="7d067-125">\_DISPSTRING RFC1213 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-125">ASN\_RFC1213\_DISPSTRING</span></span> | <span data-ttu-id="7d067-126">\_OCTETSTRING ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-126">ASN\_OCTETSTRING</span></span>  |



 

## <a name="modified-snmp-pdu-request-types"></a><span data-ttu-id="7d067-127">Tipos de solicitud de PDU de SNMP modificados</span><span class="sxs-lookup"><span data-stu-id="7d067-127">Modified SNMP PDU Request Types</span></span>

<span data-ttu-id="7d067-128">Debe usar los nuevos tipos de PDU de SNMP que se enumeran en la tabla siguiente al desarrollar aplicaciones de administrador que utilizan la API de administración de SNMP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d067-128">You should use the new SNMP PDU types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="7d067-129">En la tabla se enumeran los tipos de PDU de SNMP antiguos con los nuevos tipos PDU correspondientes.</span><span class="sxs-lookup"><span data-stu-id="7d067-129">The table lists the old SNMP PDU types with the corresponding new PDU types.</span></span>

| <span data-ttu-id="7d067-130">Tipo de PDU anterior</span><span class="sxs-lookup"><span data-stu-id="7d067-130">Old PDU type</span></span>                 | <span data-ttu-id="7d067-131">Nuevo tipo de PDU</span><span class="sxs-lookup"><span data-stu-id="7d067-131">New PDU type</span></span>        |
|------------------------------|---------------------|
| <span data-ttu-id="7d067-132">\_GETREQUEST RFC1157 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-132">ASN\_RFC1157\_GETREQUEST</span></span>     | <span data-ttu-id="7d067-133">\_obtención de PDU de SNMP \_</span><span class="sxs-lookup"><span data-stu-id="7d067-133">SNMP\_PDU\_GET</span></span>      |
| <span data-ttu-id="7d067-134">\_GETNEXTREQUEST RFC1157 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-134">ASN\_RFC1157\_GETNEXTREQUEST</span></span> | <span data-ttu-id="7d067-135">\_GETNEXT de PDU de SNMP \_</span><span class="sxs-lookup"><span data-stu-id="7d067-135">SNMP\_PDU\_GETNEXT</span></span>  |
| <span data-ttu-id="7d067-136">ASN \_ RFC1157 \_ GETRESPONSE</span><span class="sxs-lookup"><span data-stu-id="7d067-136">ASN\_RFC1157\_GETRESPONSE</span></span>    | <span data-ttu-id="7d067-137">\_respuesta de PDU de SNMP \_</span><span class="sxs-lookup"><span data-stu-id="7d067-137">SNMP\_PDU\_RESPONSE</span></span> |
| <span data-ttu-id="7d067-138">\_SETREQUEST RFC1157 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="7d067-138">ASN\_RFC1157\_SETREQUEST</span></span>     | <span data-ttu-id="7d067-139">\_conjunto de PDU de SNMP \_</span><span class="sxs-lookup"><span data-stu-id="7d067-139">SNMP\_PDU\_SET</span></span>      |
| <span data-ttu-id="7d067-140">\_Captura de RFC1157 ASN \_</span><span class="sxs-lookup"><span data-stu-id="7d067-140">ASN\_RFC1157\_TRAP</span></span>           | <span data-ttu-id="7d067-141">\_V1TRAP de PDU de SNMP \_</span><span class="sxs-lookup"><span data-stu-id="7d067-141">SNMP\_PDU\_V1TRAP</span></span>   |



 

 

 