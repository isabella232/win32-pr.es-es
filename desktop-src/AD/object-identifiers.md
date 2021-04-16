---
title: Identificadores de objeto (AD DS)
description: Los identificadores de objeto (OID) son valores numéricos únicos emitidos por varias autoridades emisoras para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificadores de objeto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "105656305"
---
# <a name="object-identifiers-ad-ds"></a><span data-ttu-id="013f3-104">Identificadores de objeto (AD DS)</span><span class="sxs-lookup"><span data-stu-id="013f3-104">Object Identifiers (AD DS)</span></span>

<span data-ttu-id="013f3-105">Los identificadores de objeto (OID) son valores numéricos únicos emitidos por varias autoridades emisoras para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas.</span><span class="sxs-lookup"><span data-stu-id="013f3-105">Object Identifiers (OIDs) are unique numeric values issued by various issuing authorities to uniquely identify data elements, syntaxes, and other parts of distributed applications.</span></span> <span data-ttu-id="013f3-106">Los OID se encuentran en aplicaciones OSI, directorios X. 500, SNMP y otras aplicaciones en las que la unicidad es importante.</span><span class="sxs-lookup"><span data-stu-id="013f3-106">OIDs are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="013f3-107">Los OID se basan en una estructura de árbol, en la que una entidad de emisión superior, como la ISO, asigna una rama del árbol a un subautoridad, que a su vez puede asignar subramas.</span><span class="sxs-lookup"><span data-stu-id="013f3-107">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a subauthority, who in turn can allocate subbranches.</span></span>

<span data-ttu-id="013f3-108">El protocolo LDAP (RFC 2251) requiere un servicio de directorio para identificar las clases de objetos, atributos y sintaxis con OID.</span><span class="sxs-lookup"><span data-stu-id="013f3-108">The LDAP protocol (RFC 2251) requires a directory service to identify object classes, attributes, and syntaxes with OIDs.</span></span> <span data-ttu-id="013f3-109">Esto forma parte de las versiones anteriores de LDAP X. 500.</span><span class="sxs-lookup"><span data-stu-id="013f3-109">This is part of the LDAP X.500 legacy.</span></span>

<span data-ttu-id="013f3-110">Los OID de Active Directory Domain Services incluyen algunos emitidos por la ISO para las clases y atributos X. 500 y otros emitidos por Microsoft y otras entidades emisoras.</span><span class="sxs-lookup"><span data-stu-id="013f3-110">OIDs in Active Directory Domain Services include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft and other issuing authorities.</span></span> <span data-ttu-id="013f3-111">La notación OID es una cadena de números con puntos, por ejemplo "1.2.840.113556.1.5.9", que se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="013f3-111">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.9", which is described in the following table.</span></span>



| <span data-ttu-id="013f3-112">Value</span><span class="sxs-lookup"><span data-stu-id="013f3-112">Value</span></span>  | <span data-ttu-id="013f3-113">Significado</span><span class="sxs-lookup"><span data-stu-id="013f3-113">Meaning</span></span>          | <span data-ttu-id="013f3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="013f3-114">Description</span></span>                                              |
|--------|------------------|----------------------------------------------------------|
| <span data-ttu-id="013f3-115">1</span><span class="sxs-lookup"><span data-stu-id="013f3-115">1</span></span>      | <span data-ttu-id="013f3-116">ISO</span><span class="sxs-lookup"><span data-stu-id="013f3-116">ISO</span></span>              | <span data-ttu-id="013f3-117">Identifica la entidad de certificación raíz.</span><span class="sxs-lookup"><span data-stu-id="013f3-117">Identifies the root authority.</span></span>                           |
| <span data-ttu-id="013f3-118">2</span><span class="sxs-lookup"><span data-stu-id="013f3-118">2</span></span>      | <span data-ttu-id="013f3-119">ANSI</span><span class="sxs-lookup"><span data-stu-id="013f3-119">ANSI</span></span>             | <span data-ttu-id="013f3-120">Designación de grupo asignada por ISO.</span><span class="sxs-lookup"><span data-stu-id="013f3-120">Group designation assigned by ISO.</span></span>                       |
| <span data-ttu-id="013f3-121">840</span><span class="sxs-lookup"><span data-stu-id="013f3-121">840</span></span>    | <span data-ttu-id="013f3-122">EE. UU.</span><span class="sxs-lookup"><span data-stu-id="013f3-122">USA</span></span>              | <span data-ttu-id="013f3-123">Designación de país o región asignada por el grupo.</span><span class="sxs-lookup"><span data-stu-id="013f3-123">Country/region designation assigned by the group.</span></span>        |
| <span data-ttu-id="013f3-124">113556</span><span class="sxs-lookup"><span data-stu-id="013f3-124">113556</span></span> | <span data-ttu-id="013f3-125">Microsoft</span><span class="sxs-lookup"><span data-stu-id="013f3-125">Microsoft</span></span>        | <span data-ttu-id="013f3-126">Designación de la organización asignada por el país o la región.</span><span class="sxs-lookup"><span data-stu-id="013f3-126">Organization designation assigned by the country/region.</span></span> |
| <span data-ttu-id="013f3-127">1</span><span class="sxs-lookup"><span data-stu-id="013f3-127">1</span></span>      | <span data-ttu-id="013f3-128">Active Directory</span><span class="sxs-lookup"><span data-stu-id="013f3-128">Active Directory</span></span> | <span data-ttu-id="013f3-129">Asignado por la organización.</span><span class="sxs-lookup"><span data-stu-id="013f3-129">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="013f3-130">5</span><span class="sxs-lookup"><span data-stu-id="013f3-130">5</span></span>      | <span data-ttu-id="013f3-131">Clases</span><span class="sxs-lookup"><span data-stu-id="013f3-131">Classes</span></span>          | <span data-ttu-id="013f3-132">Asignado por la organización.</span><span class="sxs-lookup"><span data-stu-id="013f3-132">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="013f3-133">9</span><span class="sxs-lookup"><span data-stu-id="013f3-133">9</span></span>      | <span data-ttu-id="013f3-134">clase de **usuario**</span><span class="sxs-lookup"><span data-stu-id="013f3-134">**user** class</span></span>   | <span data-ttu-id="013f3-135">Asignado por la organización.</span><span class="sxs-lookup"><span data-stu-id="013f3-135">Assigned by the organization.</span></span>                            |



 

<span data-ttu-id="013f3-136">Para obtener más información y una explicación de los dos procedimientos utilizados para obtener OID válidos para su uso en la extensión del esquema de Active Directory, vea [obtener un identificador de objeto](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="013f3-136">For more information, and a discussion of two procedures used to obtain valid OIDs for use in extending the Active Directory schema, see [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>

 

 




