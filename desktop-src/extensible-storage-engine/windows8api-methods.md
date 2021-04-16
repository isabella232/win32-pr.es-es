---
description: 'Más información sobre: métodos Windows8Api'
title: Métodos Windows8Api (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: Windows8Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_methods(v=EXCHG.10)
ms:contentKeyID: 55104457
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d8eb8b822affcbf41c375f7ef23b6a71d03afc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564127"
---
# <a name="windows8api-methods"></a><span data-ttu-id="c1f27-103">Métodos Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c1f27-103">Windows8Api methods</span></span>

<span data-ttu-id="c1f27-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="c1f27-104">Include protected members</span></span>  
<span data-ttu-id="c1f27-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="c1f27-105">Include inherited members</span></span>  

<span data-ttu-id="c1f27-106">El tipo [Windows8Api](./windows8api-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="c1f27-106">The [Windows8Api](./windows8api-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="c1f27-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1f27-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="c1f27-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="c1f27-108">Name</span></span></th>
<th><span data-ttu-id="c1f27-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1f27-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-112"><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></span></span></td>
<td><span data-ttu-id="c1f27-113">Hace que una sesión escriba una transacción o cree un nuevo punto de retorno en una transacción existente.</span><span class="sxs-lookup"><span data-stu-id="c1f27-113">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-116"><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></span></span></td>
<td><span data-ttu-id="c1f27-117">Confirma los cambios realizados en el estado de la base de datos durante el punto de almacenamiento actual y los migra al punto de almacenamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="c1f27-117">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="c1f27-118">Si se confirma el punto de almacenamiento más externo, los cambios realizados durante ese punto de almacenamiento se confirmarán en el estado de la base de datos y la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="c1f27-118">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-121"><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></span></span></td>
<td><span data-ttu-id="c1f27-122">Crea índices sobre los datos de una base de datos ESE.</span><span class="sxs-lookup"><span data-stu-id="c1f27-122">Creates indexes over data in an ESE database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-125"><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></span></span></td>
<td><span data-ttu-id="c1f27-126">Crea una tabla, agrega columnas e índices en esa tabla.</span><span class="sxs-lookup"><span data-stu-id="c1f27-126">Creates a table, adds columns, and indices on that table.</span></span> <span data-ttu-id="c1f27-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-127"><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</a></span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-130"><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></span></span></td>
<td><span data-ttu-id="c1f27-131">Obtiene información extendida sobre un error.</span><span class="sxs-lookup"><span data-stu-id="c1f27-131">Gets extended information about an error.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-134"><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></span></span></td>
<td><span data-ttu-id="c1f27-135">Crea una tabla temporal con un índice único.</span><span class="sxs-lookup"><span data-stu-id="c1f27-135">Creates a temporary table with a single index.</span></span> <span data-ttu-id="c1f27-136">Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="c1f27-136">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="c1f27-137">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="c1f27-137">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="c1f27-138">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="c1f27-138">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="c1f27-139">Vea también <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot; API. JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span><span class="sxs-lookup"><span data-stu-id="c1f27-139">Also see <a href="dn292231(v=exchg.10).md">JetOpenTempTable(JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot;Api.JetOpenTempTable2&quot;, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3(JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</span></span> <span data-ttu-id="c1f27-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span><span class="sxs-lookup"><span data-stu-id="c1f27-140"><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-143"><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="c1f27-144">Si los registros con los intervalos de claves especificados no están en la caché del búfer, inicie las lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c1f27-144">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-147"><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></span></span></td>
<td><span data-ttu-id="c1f27-148">Cambia el tamaño de una base de datos abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="c1f27-148">Resizes a currently open database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-151"><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></span></span></td>
<td><span data-ttu-id="c1f27-152">Establezca una matriz de filtros simples para <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="c1f27-152">Set an array of simple filters for <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-155"><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></span></span></td>
<td><span data-ttu-id="c1f27-156">Establece un parámetro en el estado de sesión proporcionado, que se usa para la duración de esta sesión o hasta que se restablezca.</span><span class="sxs-lookup"><span data-stu-id="c1f27-156">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-159"><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></span></span></td>
<td><span data-ttu-id="c1f27-160">Prepara una instancia para la terminación.</span><span class="sxs-lookup"><span data-stu-id="c1f27-160">Prepares an instance for termination.</span></span> <span data-ttu-id="c1f27-161">También se puede usar para reanudar una inactividad anterior.</span><span class="sxs-lookup"><span data-stu-id="c1f27-161">Can also be used to resume a previous quiescing.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-164"><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></span></span></td>
<td><span data-ttu-id="c1f27-165">Si los registros con los intervalos de claves especificados no están en la caché del búfer, inicie las lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c1f27-165">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="c1f27-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span><span class="sxs-lookup"><span data-stu-id="c1f27-168"><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></span></span></td>
<td><span data-ttu-id="c1f27-169">Si los registros con los intervalos de claves especificados no están en la caché del búfer, inicie las lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c1f27-169">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c1f27-170">Superior</span><span class="sxs-lookup"><span data-stu-id="c1f27-170">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="c1f27-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1f27-171">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c1f27-172">Referencia</span><span class="sxs-lookup"><span data-stu-id="c1f27-172">Reference</span></span>

[<span data-ttu-id="c1f27-173">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c1f27-173">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="c1f27-174">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="c1f27-174">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
