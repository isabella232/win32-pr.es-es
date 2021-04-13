---
description: 'Más información acerca de: campos Server2003Grbits'
title: Campos Server2003Grbits (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ed7a99118674d955fc6a882ac08407e45837af77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560745"
---
# <a name="server2003grbits-fields"></a><span data-ttu-id="2bc8f-103">Campos de Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="2bc8f-103">Server2003Grbits fields</span></span>

<span data-ttu-id="2bc8f-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="2bc8f-104">Include protected members</span></span>  
<span data-ttu-id="2bc8f-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="2bc8f-105">Include inherited members</span></span>  

<span data-ttu-id="2bc8f-106">El tipo [Server2003Grbits](./server2003grbits-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-106">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="2bc8f-107">Campos</span><span class="sxs-lookup"><span data-stu-id="2bc8f-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2bc8f-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="2bc8f-108">Name</span></span></th>
<th><span data-ttu-id="2bc8f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bc8f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="2bc8f-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="2bc8f-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="2bc8f-113">Si una columna determinada no está presente en el registro y tiene un valor predeterminado definido por el usuario, no se devolverá ningún valor de columna.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-113">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="2bc8f-114">Esta opción impedirá que se llame a la devolución de llamada que calcula el valor predeterminado definido por el usuario para la columna al enumerar los valores de esa columna.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-114">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="2bc8f-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="2bc8f-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="2bc8f-118">Esta opción solicita que la tabla temporal se cree solo si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-118">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="2bc8f-119">Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-119">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="2bc8f-120">Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-120">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="2bc8f-121">Consulte <a href="hh558517(v=exchg.10).md">Unique</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-121">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="2bc8f-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="2bc8f-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="2bc8f-125">Todas las transacciones confirmadas previamente por cualquier sesión que todavía no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-125">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="2bc8f-126">Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-126">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="2bc8f-127">Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-127">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="2bc8f-128">Esta opción no se puede usar en combinación con ninguna otra opción.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-128">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2bc8f-129">Superior</span><span class="sxs-lookup"><span data-stu-id="2bc8f-129">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2bc8f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bc8f-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2bc8f-131">Referencia</span><span class="sxs-lookup"><span data-stu-id="2bc8f-131">Reference</span></span>

[<span data-ttu-id="2bc8f-132">Clase Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="2bc8f-132">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="2bc8f-133">Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="2bc8f-133">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
