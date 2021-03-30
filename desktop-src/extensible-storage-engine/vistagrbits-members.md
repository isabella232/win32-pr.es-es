---
description: 'Más información acerca de: miembros de VistaGrbits'
title: Miembros de VistaGrbits (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 56145954b504f086ff36fbe84ea26768b8e3636a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552294"
---
# <a name="vistagrbits-members"></a><span data-ttu-id="124e1-103">Miembros de VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="124e1-103">VistaGrbits members</span></span>

<span data-ttu-id="124e1-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="124e1-104">Include protected members</span></span>  
<span data-ttu-id="124e1-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="124e1-105">Include inherited members</span></span>  

<span data-ttu-id="124e1-106">Grbits que se han agregado a la versión de vista de ESENT.</span><span class="sxs-lookup"><span data-stu-id="124e1-106">Grbits that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="124e1-107">El tipo [VistaGrbits](./vistagrbits-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="124e1-107">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="124e1-108">Campos</span><span class="sxs-lookup"><span data-stu-id="124e1-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="124e1-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="124e1-109">Name</span></span></th>
<th><span data-ttu-id="124e1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="124e1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span><span class="sxs-lookup"><span data-stu-id="124e1-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="124e1-114">La sesión de instantáneas continúa después de JetOSSnapshotThaw y requerirá una llamada a la función JetOSSnapshotEnd.</span><span class="sxs-lookup"><span data-stu-id="124e1-114">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span><span class="sxs-lookup"><span data-stu-id="124e1-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="124e1-118">Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna con varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave.</span><span class="sxs-lookup"><span data-stu-id="124e1-118">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="124e1-119">De lo contrario, el índice solo tendrá una entrada para cada valor múltiple de la columna de clave más importante que sea una columna con varios valores y cada una de esas entradas de índice usaría el primer valor entre las demás columnas de clave que son columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="124e1-119">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="124e1-120">Por ejemplo, si especificó esta marca para un índice en la columna A que tiene los valores &quot; rojo &quot; y &quot; azul &quot; y sobre la columna B que tiene los valores &quot; 1 &quot; y &quot; 2 &quot; , se crearán las siguientes entradas de índice: &quot; rojo &quot; , &quot; 1 &quot; ; &quot; rojo &quot; , &quot; 2 &quot; ; &quot; azul &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="124e1-120">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="124e1-121">De lo contrario, se crearán las siguientes entradas de índice: &quot; rojo &quot; , &quot; 1 &quot; ; &quot; azul &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="124e1-121">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span><span class="sxs-lookup"><span data-stu-id="124e1-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="124e1-125">Si se especifica este marcador, se producirá un error en cualquier actualización del índice que dé lugar a una clave truncada con <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span><span class="sxs-lookup"><span data-stu-id="124e1-125">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="124e1-126">De lo contrario, las claves se truncarán de forma silenciosa.</span><span class="sxs-lookup"><span data-stu-id="124e1-126">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span><span class="sxs-lookup"><span data-stu-id="124e1-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="124e1-130">Índice de varias columnas con varios valores, pero solo con valores de la misma itagSequence.</span><span class="sxs-lookup"><span data-stu-id="124e1-130">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span><span class="sxs-lookup"><span data-stu-id="124e1-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="124e1-134">Los registros de transacciones deben existir en el directorio del archivo de registro (es decir, no se puede iniciar automáticamente una nueva secuencia).</span><span class="sxs-lookup"><span data-stu-id="124e1-134">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span><span class="sxs-lookup"><span data-stu-id="124e1-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="124e1-138">Realiza la recuperación, pero se detiene en la fase de deshacer.</span><span class="sxs-lookup"><span data-stu-id="124e1-138">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="124e1-139">Permite que los registros estén presentes para que se reproduzcan y, posteriormente, se pueden copiar y reproducir registros adicionales.</span><span class="sxs-lookup"><span data-stu-id="124e1-139">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span><span class="sxs-lookup"><span data-stu-id="124e1-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="124e1-143">Falta la entrada de asignación de base de datos predeterminada en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="124e1-143">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span><span class="sxs-lookup"><span data-stu-id="124e1-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="124e1-147">El motor puede marcar los encabezados de la base de datos según corresponda (por ejemplo, una copia de seguridad completa completada), aunque no se haya completado la llamada a TRUNCATE.</span><span class="sxs-lookup"><span data-stu-id="124e1-147">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><span data-ttu-id="124e1-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span><span class="sxs-lookup"><span data-stu-id="124e1-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="124e1-151">En la recuperación de software correcta, trunque los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="124e1-151">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="124e1-152">Superior</span><span class="sxs-lookup"><span data-stu-id="124e1-152">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="124e1-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="124e1-153">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="124e1-154">Referencia</span><span class="sxs-lookup"><span data-stu-id="124e1-154">Reference</span></span>

[<span data-ttu-id="124e1-155">Clase VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="124e1-155">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="124e1-156">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="124e1-156">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
