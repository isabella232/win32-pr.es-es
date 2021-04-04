---
description: 'Más información acerca de: miembros de Server2003Grbits'
title: Miembros de Server2003Grbits (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910230"
---
# <a name="server2003grbits-members"></a><span data-ttu-id="2cb19-103">Miembros de Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="2cb19-103">Server2003Grbits members</span></span>

<span data-ttu-id="2cb19-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="2cb19-104">Include protected members</span></span>  
<span data-ttu-id="2cb19-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="2cb19-105">Include inherited members</span></span>  

<span data-ttu-id="2cb19-106">Grbits que se han agregado a la versión 2003 de Windows Server de ESENT.</span><span class="sxs-lookup"><span data-stu-id="2cb19-106">Grbits that have been added to the Windows Server 2003 version of ESENT.</span></span>

<span data-ttu-id="2cb19-107">El tipo [Server2003Grbits](./server2003grbits-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="2cb19-107">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="2cb19-108">Campos</span><span class="sxs-lookup"><span data-stu-id="2cb19-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2cb19-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="2cb19-109">Name</span></span></th>
<th><span data-ttu-id="2cb19-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cb19-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="2cb19-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="2cb19-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="2cb19-114">Si una columna determinada no está presente en el registro y tiene un valor predeterminado definido por el usuario, no se devolverá ningún valor de columna.</span><span class="sxs-lookup"><span data-stu-id="2cb19-114">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="2cb19-115">Esta opción impedirá que se llame a la devolución de llamada que calcula el valor predeterminado definido por el usuario para la columna al enumerar los valores de esa columna.</span><span class="sxs-lookup"><span data-stu-id="2cb19-115">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="2cb19-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="2cb19-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="2cb19-119">Esta opción solicita que la tabla temporal se cree solo si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta.</span><span class="sxs-lookup"><span data-stu-id="2cb19-119">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="2cb19-120">Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="2cb19-120">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="2cb19-121">Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="2cb19-121">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="2cb19-122">Consulte <a href="hh558517(v=exchg.10).md">Unique</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2cb19-122">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="2cb19-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="2cb19-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="2cb19-126">Todas las transacciones confirmadas previamente por cualquier sesión que todavía no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="2cb19-126">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="2cb19-127">Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2cb19-127">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="2cb19-128">Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="2cb19-128">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="2cb19-129">Esta opción no se puede usar en combinación con ninguna otra opción.</span><span class="sxs-lookup"><span data-stu-id="2cb19-129">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2cb19-130">Superior</span><span class="sxs-lookup"><span data-stu-id="2cb19-130">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2cb19-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cb19-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2cb19-132">Referencia</span><span class="sxs-lookup"><span data-stu-id="2cb19-132">Reference</span></span>

[<span data-ttu-id="2cb19-133">Clase Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="2cb19-133">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="2cb19-134">Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="2cb19-134">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
