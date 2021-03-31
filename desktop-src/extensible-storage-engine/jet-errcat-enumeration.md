---
description: 'Más información acerca de: enumeración JET_ERRCAT'
title: Enumeración JET_ERRCAT (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e08ec4ce308003dc30edaa32a07000e244dc9f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277114"
---
# <a name="jet_errcat-enumeration"></a><span data-ttu-id="0effa-103">Enumeración JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="0effa-103">JET_ERRCAT enumeration</span></span>

<span data-ttu-id="0effa-104">La categoría de error.</span><span class="sxs-lookup"><span data-stu-id="0effa-104">The error category.</span></span> <span data-ttu-id="0effa-105">La jerarquía es la siguiente: JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//problemas de e/s incorrectos, pueden o no ser transitorios.</span><span class="sxs-lookup"><span data-stu-id="0effa-105">The hierarchy is as follows: JET_errcatError | |-- JET_errcatOperation | |-- JET_errcatFatal | |-- JET_errcatIO // bad IO issues, may or may not be transient.</span></span> <span data-ttu-id="0effa-106">| |--JET_errcatResource | |--JET_errcatMemory//sin memoria (todas las variantes) | |--JET_errcatQuota | |--JET_errcatDisk//espacio insuficiente en disco (todas las variantes) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//suele deberse a un mal control del usuario | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete</span><span class="sxs-lookup"><span data-stu-id="0effa-106">| |-- JET_errcatResource | |-- JET_errcatMemory // out of memory (all variants) | |-- JET_errcatQuota | |-- JET_errcatDisk // out of disk space (all variants) |-- JET_errcatData | |-- JET_errcatCorruption | |-- JET_errcatInconsistent // typically caused by user Mishandling | |-- JET_errcatFragmentation |-- JET_errcatApi |-- JET_errcatUsage |-- JET_errcatState |-- JET_errcatObsolete</span></span>

<span data-ttu-id="0effa-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0effa-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="0effa-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0effa-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0effa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0effa-109">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a><span data-ttu-id="0effa-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="0effa-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0effa-111">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="0effa-111">Member name</span></span></th>
<th><span data-ttu-id="0effa-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0effa-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-113">Unknown</span><span class="sxs-lookup"><span data-stu-id="0effa-113">Unknown</span></span></td>
<td><span data-ttu-id="0effa-114">Categoría desconocida.</span><span class="sxs-lookup"><span data-stu-id="0effa-114">Unknown category.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-115">Error</span><span class="sxs-lookup"><span data-stu-id="0effa-115">Error</span></span></td>
<td><span data-ttu-id="0effa-116">Una categoría genérica.</span><span class="sxs-lookup"><span data-stu-id="0effa-116">A generic category.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-117">Operación</span><span class="sxs-lookup"><span data-stu-id="0effa-117">Operation</span></span></td>
<td><span data-ttu-id="0effa-118">Errores que normalmente se pueden producir en cualquier momento debido a condiciones no controlables.</span><span class="sxs-lookup"><span data-stu-id="0effa-118">Errors that can usually happen any time due to uncontrollable conditions.</span></span> <span data-ttu-id="0effa-119">Con frecuencia temporal, pero no siempre.</span><span class="sxs-lookup"><span data-stu-id="0effa-119">Frequently temporary, but not always.</span></span> <span data-ttu-id="0effa-120">Recuperación: probablemente inténtelo de nuevo o informará al operador.</span><span class="sxs-lookup"><span data-stu-id="0effa-120">Recovery: Probably retry, or eventually inform the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-121">Crítico</span><span class="sxs-lookup"><span data-stu-id="0effa-121">Fatal</span></span></td>
<td><span data-ttu-id="0effa-122">Este error de ordenación se produce solo cuando ESE encuentra una condición de error tan grave, que no se puede continuar en un modo seguro (a menudo transaccional) y no en los datos dañados que se producen errores de esta categoría.</span><span class="sxs-lookup"><span data-stu-id="0effa-122">This sort error happens only when ESE encounters an error condition so grave, that we can not continue on in a safe (often transactional) way, and rather than corrupt data we throw errors of this category.</span></span> <span data-ttu-id="0effa-123">Recuperación: reinicie la instancia o el proceso.</span><span class="sxs-lookup"><span data-stu-id="0effa-123">Recovery: Restart the instance or process.</span></span> <span data-ttu-id="0effa-124">Si el problema persiste, informe al operador.</span><span class="sxs-lookup"><span data-stu-id="0effa-124">If the problem persists inform the operator.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-125">IO</span><span class="sxs-lookup"><span data-stu-id="0effa-125">IO</span></span></td>
<td><span data-ttu-id="0effa-126">O los errores provienen del sistema operativo y están fuera del control de ESE, es posible que este tipo de error sea temporal, posiblemente no.</span><span class="sxs-lookup"><span data-stu-id="0effa-126">O errors come from the OS, and are out of ESE's control, this sort of error is possibly temporary, possibly not.</span></span> <span data-ttu-id="0effa-127">Recuperación: Reintentar.</span><span class="sxs-lookup"><span data-stu-id="0effa-127">Recovery: Retry.</span></span> <span data-ttu-id="0effa-128">Si no se resuelve, preguntar al operador sobre el problema del disco.</span><span class="sxs-lookup"><span data-stu-id="0effa-128">If not resolved, ask operator about disk issue.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-129">Recurso</span><span class="sxs-lookup"><span data-stu-id="0effa-129">Resource</span></span></td>
<td><span data-ttu-id="0effa-130">Esta es una categoría que indica una de las numerosas condiciones de recursos insuficientes.</span><span class="sxs-lookup"><span data-stu-id="0effa-130">This is a category that indicates one of many potential out-of-resource conditions.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-131">Memory</span><span class="sxs-lookup"><span data-stu-id="0effa-131">Memory</span></span></td>
<td><span data-ttu-id="0effa-132">Estado de memoria insuficiente clásico.</span><span class="sxs-lookup"><span data-stu-id="0effa-132">Classic out of memory condition.</span></span> <span data-ttu-id="0effa-133">Recuperación: Espere un poco y vuelva a intentarlo, libere memoria o salga.</span><span class="sxs-lookup"><span data-stu-id="0effa-133">Recovery: Wait a while and retry, free up memory, or quit.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-134">Quota</span><span class="sxs-lookup"><span data-stu-id="0effa-134">Quota</span></span></td>
<td><span data-ttu-id="0effa-135">Determinados &quot; &quot; recursos especializados se encuentran en grupos de cierto tamaño, lo que facilita la detección de pérdidas de estos recursos.</span><span class="sxs-lookup"><span data-stu-id="0effa-135">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span> <span data-ttu-id="0effa-136">Recuperación: podría requerir algunos cambios de código secundarios.</span><span class="sxs-lookup"><span data-stu-id="0effa-136">Recovery: Might require some minor code changes.</span></span> <span data-ttu-id="0effa-137">La aplicación debe tener una acción de solo depuración, como una aserción, en estas condiciones para detectarlas durante el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="0effa-137">Your application should have a debug only action, such as an Assert, on these conditions in order to detect them during development.</span></span> <span data-ttu-id="0effa-138">En el caso de código comercial, se recomienda que trate este error como el error de categoría de memoria y que vuelva a intentarlo, libere memoria o salga de la operación.</span><span class="sxs-lookup"><span data-stu-id="0effa-138">For retail code, we recommend that you treat this error like the Memory category error and either retry, free up memory, or quit the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-139">Disco</span><span class="sxs-lookup"><span data-stu-id="0effa-139">Disk</span></span></td>
<td><span data-ttu-id="0effa-140">Condiciones de disco insuficiente.</span><span class="sxs-lookup"><span data-stu-id="0effa-140">Out of disk conditions.</span></span> <span data-ttu-id="0effa-141">Recuperación: puede volver a intentarlo más tarde con la esperanza de que haya más espacio disponible o pedir al operador que libere espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="0effa-141">Recovery: Can retry later in the hope more space is available, or ask the operator to free some disk space.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-142">Datos</span><span class="sxs-lookup"><span data-stu-id="0effa-142">Data</span></span></td>
<td><span data-ttu-id="0effa-143">Un error relacionado con datos.</span><span class="sxs-lookup"><span data-stu-id="0effa-143">A data-related error.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-144">Ocasiona</span><span class="sxs-lookup"><span data-stu-id="0effa-144">Corruption</span></span></td>
<td><span data-ttu-id="0effa-145">Mi unidad de disco duro comió mis deberes.</span><span class="sxs-lookup"><span data-stu-id="0effa-145">My hard drive ate my homework.</span></span> <span data-ttu-id="0effa-146">Problemas de daños clásicos, permanentes con frecuencia sin acción correctiva.</span><span class="sxs-lookup"><span data-stu-id="0effa-146">Classic corruption issues, frequently permanent without corrective action.</span></span> <span data-ttu-id="0effa-147">Recuperación: restaure desde una copia de seguridad, quizás la operación de reparación de utilidades de ese (que solo recupera los datos que se han dejado y se pierden). Además, en el caso de la recuperación (JetInit), quizás se pueda realizar una recuperación al permitir la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="0effa-147">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy) .Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-148">Incoherente</span><span class="sxs-lookup"><span data-stu-id="0effa-148">Inconsistent</span></span></td>
<td><span data-ttu-id="0effa-149">Esto es similar a los daños en que los archivos de base de datos o de registro se encuentran en un estado incoherente y no se pueden reconciliar entre sí.</span><span class="sxs-lookup"><span data-stu-id="0effa-149">This is similar to Corruption in that the database and/or log files are in a state that is inconsistent and unreconcilable with each other.</span></span> <span data-ttu-id="0effa-150">A menudo, esto se debe a un mal control del administrador o la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0effa-150">Often this is caused by application/administrator mishandling.</span></span> <span data-ttu-id="0effa-151">Recuperación: restaure desde una copia de seguridad, quizás la operación de reparación de utilidades de ese (que solo recupera los datos que se han dejado y se pierden).</span><span class="sxs-lookup"><span data-stu-id="0effa-151">Recovery: Restore from backup, perhaps the ese utilities repair operation (which only salvages what data is left / lossy).</span></span> <span data-ttu-id="0effa-152">Además, en el caso de la recuperación (JetInit), quizás se pueda realizar una recuperación al permitir la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="0effa-152">Also in the case of recovery(JetInit) perhaps recovery can be performed by allowing data loss.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-153">Fragmentación</span><span class="sxs-lookup"><span data-stu-id="0effa-153">Fragmentation</span></span></td>
<td><span data-ttu-id="0effa-154">Se trata de una clase de errores en los que se ha agotado algún recurso interno persistente. Recuperación: en el caso de los errores de base de datos, la desfragmentación sin conexión rectificará el problema. en _primer lugar_ , los archivos de registro recuperan todas las bases de datos asociadas a un cierre correcto y, a continuación, eliminan todos los archivos de registro y el punto de control</span><span class="sxs-lookup"><span data-stu-id="0effa-154">This is a class of errors where some persisted internal resource ran out. Recovery: For database errors, offline defragmentation will rectify the problem, for the log files _first_ recover all attached databases to a clean shutdown, and then delete all the log files and checkpoint.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-155">API</span><span class="sxs-lookup"><span data-stu-id="0effa-155">Api</span></span></td>
<td><span data-ttu-id="0effa-156">Un contenedor para el uso y el estado.</span><span class="sxs-lookup"><span data-stu-id="0effa-156">A container for Usage and State.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-157">Uso</span><span class="sxs-lookup"><span data-stu-id="0effa-157">Usage</span></span></td>
<td><span data-ttu-id="0effa-158">Error de uso clásico, esto significa que el código de cliente no ha pasado los argumentos correctos a la API de JET.</span><span class="sxs-lookup"><span data-stu-id="0effa-158">Classic usage error, this means the client code did not pass correct arguments to the JET API.</span></span> <span data-ttu-id="0effa-159">Este error probablemente no desaparecerá con el reintento.</span><span class="sxs-lookup"><span data-stu-id="0effa-159">This error will likely not go away with retry.</span></span> <span data-ttu-id="0effa-160">Recuperación: en general, el código de cliente debe imponer () no se devuelve esta clase de errores, por lo que se pueden detectar problemas durante el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="0effa-160">Recovery: Generally speaking client code should Assert() this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="0effa-161">En el comercio minorista, es probable que la aplicación tenga poca opción pero devolver el problema al operador.</span><span class="sxs-lookup"><span data-stu-id="0effa-161">In retail, the app will probably have little option but to return the issue up to the operator.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-162">Estado</span><span class="sxs-lookup"><span data-stu-id="0effa-162">State</span></span></td>
<td><span data-ttu-id="0effa-163">Esta es la clasificación para las diferentes señales que la API podría devolver describe el estado de la base de datos, un caso clásico es JET_errRecordNotFound que puede ser devuelto por JetSeek () cuando no se encuentra el registro que solicitó.</span><span class="sxs-lookup"><span data-stu-id="0effa-163">This is the classification for different signals the API could return describe the state of the database, a classic case is JET_errRecordNotFound which can be returned by JetSeek() when the record you asked for was not found.</span></span> <span data-ttu-id="0effa-164">Recuperación: no es realmente relevante, depende en gran medida de la API.</span><span class="sxs-lookup"><span data-stu-id="0effa-164">Recovery: Not really relevant, depends greatly on the API.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0effa-165">Obsoletos</span><span class="sxs-lookup"><span data-stu-id="0effa-165">Obsolete</span></span></td>
<td><span data-ttu-id="0effa-166">El error se reconoce como un error válido, pero no se espera que sea devuelto por esta versión de la API.</span><span class="sxs-lookup"><span data-stu-id="0effa-166">The error is recognized as a valid error, but is not expected to be returned by this version of the API.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0effa-167">Máx.</span><span class="sxs-lookup"><span data-stu-id="0effa-167">Max</span></span></td>
<td><span data-ttu-id="0effa-168">Valor máximo de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="0effa-168">The maximum value for the enum.</span></span> <span data-ttu-id="0effa-169">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="0effa-169">This should not be used.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0effa-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="0effa-170">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0effa-171">Referencia</span><span class="sxs-lookup"><span data-stu-id="0effa-171">Reference</span></span>

[<span data-ttu-id="0effa-172">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="0effa-172">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
