---
description: Cada definición de objeto MIB contiene una cláusula ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) que define los derechos de acceso al objeto.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Cláusulas Access y MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697424"
---
# <a name="access-and-max-access-clauses"></a><span data-ttu-id="897b9-103">Cláusulas Access y MAX-ACCESS</span><span class="sxs-lookup"><span data-stu-id="897b9-103">ACCESS and MAX-ACCESS Clauses</span></span>

<span data-ttu-id="897b9-104">Cada definición de objeto MIB contiene una cláusula ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) que define los derechos de acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="897b9-104">Each MIB object definition contains either an ACCESS (SNMPv1) or MAX-ACCESS (SNMPv2C) clause that defines the access rights to the object.</span></span>

> [!Note]  
> <span data-ttu-id="897b9-105">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="897b9-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="897b9-106">En la tabla siguiente se muestra la asignación de la cláusula de acceso SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="897b9-106">The following table lists the mapping of the SNMPv1 ACCESS clause.</span></span>



| <span data-ttu-id="897b9-107">Cláusula de acceso MIB</span><span class="sxs-lookup"><span data-stu-id="897b9-107">MIB ACCESS clause</span></span> | <span data-ttu-id="897b9-108">Calificador de CIM</span><span class="sxs-lookup"><span data-stu-id="897b9-108">CIM qualifier</span></span>       |
|-------------------|---------------------|
| <span data-ttu-id="897b9-109">solo lectura</span><span class="sxs-lookup"><span data-stu-id="897b9-109">read-only</span></span>         | <span data-ttu-id="897b9-110">**Lectura**</span><span class="sxs-lookup"><span data-stu-id="897b9-110">**Read**</span></span>            |
| <span data-ttu-id="897b9-111">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="897b9-111">read-write</span></span>        | <span data-ttu-id="897b9-112">**Lectura**, **escritura**</span><span class="sxs-lookup"><span data-stu-id="897b9-112">**Read**, **Write**</span></span> |
| <span data-ttu-id="897b9-113">de solo escritura</span><span class="sxs-lookup"><span data-stu-id="897b9-113">write-only</span></span>        | <span data-ttu-id="897b9-114">**Escritura**</span><span class="sxs-lookup"><span data-stu-id="897b9-114">**Write**</span></span>           |
| <span data-ttu-id="897b9-115">no accesible</span><span class="sxs-lookup"><span data-stu-id="897b9-115">not-accessible</span></span>    | <span data-ttu-id="897b9-116">**No \_ accesible**</span><span class="sxs-lookup"><span data-stu-id="897b9-116">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="897b9-117">En la tabla siguiente se muestra la asignación de la cláusula de acceso MAX de SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="897b9-117">The following table lists the mapping of the SNMPv2C MAX-ACCESS clause.</span></span>



| <span data-ttu-id="897b9-118">MIB: cláusula de acceso</span><span class="sxs-lookup"><span data-stu-id="897b9-118">MIB-ACCESS clause</span></span>     | <span data-ttu-id="897b9-119">Calificador de CIM</span><span class="sxs-lookup"><span data-stu-id="897b9-119">CIM qualifier</span></span>       |
|-----------------------|---------------------|
| <span data-ttu-id="897b9-120">solo lectura</span><span class="sxs-lookup"><span data-stu-id="897b9-120">read-only</span></span>             | <span data-ttu-id="897b9-121">**Lectura**</span><span class="sxs-lookup"><span data-stu-id="897b9-121">**Read**</span></span>            |
| <span data-ttu-id="897b9-122">lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="897b9-122">read-write</span></span>            | <span data-ttu-id="897b9-123">**Lectura**, **escritura**</span><span class="sxs-lookup"><span data-stu-id="897b9-123">**Read**, **Write**</span></span> |
| <span data-ttu-id="897b9-124">lectura y creación</span><span class="sxs-lookup"><span data-stu-id="897b9-124">read-create</span></span>           | <span data-ttu-id="897b9-125">**Lectura**</span><span class="sxs-lookup"><span data-stu-id="897b9-125">**Read**</span></span>            |
| <span data-ttu-id="897b9-126">accesible para notificaciones</span><span class="sxs-lookup"><span data-stu-id="897b9-126">accessible-for-notify</span></span> | <span data-ttu-id="897b9-127">**No \_ accesible**</span><span class="sxs-lookup"><span data-stu-id="897b9-127">**Not\_Accessible**</span></span> |
| <span data-ttu-id="897b9-128">no accesible</span><span class="sxs-lookup"><span data-stu-id="897b9-128">not-accessible</span></span>        | <span data-ttu-id="897b9-129">**No \_ accesible**</span><span class="sxs-lookup"><span data-stu-id="897b9-129">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="897b9-130">Cuando un objeto MIB se asigna a no accesible y no es una propiedad con clave de la clase, no hay ninguna asignación del propio objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="897b9-130">When a MIB object maps to not-accessible and is not a keyed property of the class, there is no mapping of the MIB object itself.</span></span>

 

 



