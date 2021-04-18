---
description: 'Más información acerca de: JetStopBackup (función)'
title: JetStopBackup función)
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47a1454e5846fae510a7b91c197d4b180fd14a7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718583"
---
# <a name="jetstopbackup-function"></a><span data-ttu-id="e88be-103">JetStopBackup función)</span><span class="sxs-lookup"><span data-stu-id="e88be-103">JetStopBackup Function</span></span>


<span data-ttu-id="e88be-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e88be-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetstopbackup-function"></a><span data-ttu-id="e88be-105">JetStopBackup función)</span><span class="sxs-lookup"><span data-stu-id="e88be-105">JetStopBackup Function</span></span>

<span data-ttu-id="e88be-106">La función **JetStopBackup** evita que cualquier actividad relacionada con la copia de seguridad de secuencias continúe en una instancia en ejecución específica, con lo que finaliza la copia de seguridad de streaming de forma predecible.</span><span class="sxs-lookup"><span data-stu-id="e88be-106">The **JetStopBackup** function prevents any streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="e88be-107">**Windows XP:**  Esta función se ha introducido en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e88be-107">**Windows XP:**  This function is introduced in Windows XP.</span></span>

<span data-ttu-id="e88be-108">[JetStopService](./jetstopservice-function.md) es la llamada heredada cuando solo se permite una instancia.</span><span class="sxs-lookup"><span data-stu-id="e88be-108">[JetStopService](./jetstopservice-function.md) is the legacy call when only one instance is allowed.</span></span> <span data-ttu-id="e88be-109">En este caso, la única instancia activa es aquella en la que se está preparando la terminación.</span><span class="sxs-lookup"><span data-stu-id="e88be-109">In this case, the only active instance is the one being prepared for termination.</span></span>

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="e88be-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e88be-110">Parameters</span></span>

<span data-ttu-id="e88be-111">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e88be-111">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="e88be-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e88be-112">Return Value</span></span>

<span data-ttu-id="e88be-113">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="e88be-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e88be-114">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e88be-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e88be-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e88be-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="e88be-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e88be-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e88be-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e88be-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e88be-118">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e88be-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e88be-119">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="e88be-119">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="e88be-120">No está claro qué instancia se debe preparar para la finalización cuando se usa <a href="gg269240(v=exchg.10).md">JetStopService</a> con el modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="e88be-120">It is not clear which instance to prepare for termination when using <a href="gg269240(v=exchg.10).md">JetStopService</a> with multiple instance mode.</span></span></p>
<p><span data-ttu-id="e88be-121"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e88be-121"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e88be-122">Si esta función se ejecuta correctamente, la instancia de iniciará la conmutación por error de las nuevas API de copia de seguridad de streaming.</span><span class="sxs-lookup"><span data-stu-id="e88be-122">If this function succeeds, the instance will start failing any new streaming backup APIs.</span></span>

<span data-ttu-id="e88be-123">Si se produce un error en esta función, no se realizará ningún paso para preparar la finalización de la copia de seguridad en la instancia de y no se producirá ningún cambio en el estado de la instancia.</span><span class="sxs-lookup"><span data-stu-id="e88be-123">If this function fails, no steps to prepare for the backup termination on the instance will be taken and no change to the instance state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e88be-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e88be-124">Remarks</span></span>

<span data-ttu-id="e88be-125">La copia de seguridad se desencadena normalmente mediante un evento fuera del mecanismo de proceso y mediante esta API, la propia aplicación ESENT realizará cualquier llamada posterior a las API de copia de seguridad de streaming para producir un error.</span><span class="sxs-lookup"><span data-stu-id="e88be-125">Backup is usually triggered by an event outside the process mechanism and by using this API, the ESENT application itself will make any further calls to the streaming backup APIs to fail.</span></span> <span data-ttu-id="e88be-126">La mayoría de las API de copia de seguridad de streaming comenzarán a generar errores con JET_errBackupAbortByServer.</span><span class="sxs-lookup"><span data-stu-id="e88be-126">The majority of streaming backup APIs will start failing with JET_errBackupAbortByServer.</span></span> <span data-ttu-id="e88be-127">Como tal, cualquier progreso de la copia de seguridad de streaming (como [JetReadFileInstance](./jetreadfileinstance-function.md)) devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="e88be-127">As such, any streaming backup progress (like [JetReadFileInstance](./jetreadfileinstance-function.md)) will return an error.</span></span> <span data-ttu-id="e88be-128">Todavía se permitirán las operaciones de copia de seguridad que forman parte de la finalización de la copia de seguridad (como [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)).</span><span class="sxs-lookup"><span data-stu-id="e88be-128">Backup operations which are part of the backup termination (such as [JetEndExternalBackupInstance](./jetendexternalbackupinstance-function.md)) will still be allowed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e88be-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e88be-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e88be-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e88be-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e88be-131">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e88be-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e88be-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e88be-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e88be-133">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e88be-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e88be-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e88be-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e88be-135">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="e88be-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e88be-136"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="e88be-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e88be-137">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e88be-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e88be-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e88be-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e88be-139">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e88be-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e88be-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e88be-140">See Also</span></span>

[<span data-ttu-id="e88be-141">JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="e88be-141">JetEndExternalBackupInstance</span></span>](./jetendexternalbackupinstance-function.md)  
[<span data-ttu-id="e88be-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e88be-142">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e88be-143">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e88be-143">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e88be-144">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="e88be-144">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="e88be-145">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e88be-145">JetStopService</span></span>](./jetstopservice-function.md)
