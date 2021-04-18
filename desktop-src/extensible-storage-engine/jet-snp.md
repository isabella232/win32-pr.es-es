---
description: 'Más información acerca de: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666257"
---
# <a name="jet_snp"></a><span data-ttu-id="83942-103">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="83942-103">JET_SNP</span></span>


<span data-ttu-id="83942-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="83942-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snp"></a><span data-ttu-id="83942-105">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="83942-105">JET_SNP</span></span>

<span data-ttu-id="83942-106">El **JET_SNP** grupo de constantes describe el tipo de la operación para la que se va a obtener información de progreso.</span><span class="sxs-lookup"><span data-stu-id="83942-106">The **JET_SNP** group of constants describe the type of the operation for which progress information is to be obtained.</span></span> <span data-ttu-id="83942-107">Estas constantes se utilizan como el parámetro *SNP* de la función de devolución de llamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="83942-107">These constants are used as the *snp* parameter of the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83942-108">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="83942-108">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="83942-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="83942-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83942-110">JET_snpRepair</span><span class="sxs-lookup"><span data-stu-id="83942-110">JET_snpRepair</span></span><br />
<span data-ttu-id="83942-111">2</span><span class="sxs-lookup"><span data-stu-id="83942-111">2</span></span></p></td>
<td><p><span data-ttu-id="83942-112">La devolución de llamada es para una operación de reparación.</span><span class="sxs-lookup"><span data-stu-id="83942-112">The callback is for a repair operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83942-113">JET_snpCompact</span><span class="sxs-lookup"><span data-stu-id="83942-113">JET_snpCompact</span></span><br />
<span data-ttu-id="83942-114">4</span><span class="sxs-lookup"><span data-stu-id="83942-114">4</span></span></p></td>
<td><p><span data-ttu-id="83942-115">La devolución de llamada es para desfragmentación de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="83942-115">The callback is for database defragmentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83942-116">JET_snpRestore</span><span class="sxs-lookup"><span data-stu-id="83942-116">JET_snpRestore</span></span><br />
<span data-ttu-id="83942-117">8</span><span class="sxs-lookup"><span data-stu-id="83942-117">8</span></span></p></td>
<td><p><span data-ttu-id="83942-118">La devolución de llamada es para una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="83942-118">The callback is for a restore operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83942-119">JET_snpBackup</span><span class="sxs-lookup"><span data-stu-id="83942-119">JET_snpBackup</span></span><br />
<span data-ttu-id="83942-120">9</span><span class="sxs-lookup"><span data-stu-id="83942-120">9</span></span></p></td>
<td><p><span data-ttu-id="83942-121">La devolución de llamada es para una operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="83942-121">The callback is for a backup operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83942-122">JET_snpUpgrade</span><span class="sxs-lookup"><span data-stu-id="83942-122">JET_snpUpgrade</span></span><br />
<span data-ttu-id="83942-123">10</span><span class="sxs-lookup"><span data-stu-id="83942-123">10</span></span></p></td>
<td><p><span data-ttu-id="83942-124">No se admite.</span><span class="sxs-lookup"><span data-stu-id="83942-124">Not supported.</span></span></p>
<p><span data-ttu-id="83942-125"><strong>Windows 2000:</strong>  La devolución de llamada es para la operación de actualización del formato de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="83942-125"><strong>Windows 2000:</strong>  The callback is for the database format upgrade operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83942-126">JET_snpScrub</span><span class="sxs-lookup"><span data-stu-id="83942-126">JET_snpScrub</span></span><br />
<span data-ttu-id="83942-127">11</span><span class="sxs-lookup"><span data-stu-id="83942-127">11</span></span></p></td>
<td><p><span data-ttu-id="83942-128">La devolución de llamada es para una operación de ceros de base de datos (es decir, limpieza).</span><span class="sxs-lookup"><span data-stu-id="83942-128">The callback is for a database zeroing (that is, scrubbing) operation.</span></span></p>
<p><span data-ttu-id="83942-129"><strong>Windows server 2003 y windows 2000 Server:</strong>  No compatible.</span><span class="sxs-lookup"><span data-stu-id="83942-129"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83942-130">JET_snpUpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="83942-130">JET_snpUpgradeRecordFormat</span></span><br />
<span data-ttu-id="83942-131">12</span><span class="sxs-lookup"><span data-stu-id="83942-131">12</span></span></p></td>
<td><p><span data-ttu-id="83942-132">La devolución de llamada es para el proceso de actualización del formato de registro de todas las páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="83942-132">The callback is for the process of upgrading the record format of all database pages.</span></span></p>
<p><span data-ttu-id="83942-133"><strong>Windows server 2003 y windows 2000 Server:</strong>  No compatible.</span><span class="sxs-lookup"><span data-stu-id="83942-133"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="83942-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83942-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83942-135"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="83942-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="83942-136">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="83942-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83942-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="83942-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="83942-138">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="83942-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83942-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="83942-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="83942-140">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="83942-140">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="83942-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="83942-141">See Also</span></span>

[<span data-ttu-id="83942-142">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="83942-142">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="83942-143">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="83942-143">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="83942-144">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="83942-144">JET_SNT</span></span>](./jet-snt.md)
