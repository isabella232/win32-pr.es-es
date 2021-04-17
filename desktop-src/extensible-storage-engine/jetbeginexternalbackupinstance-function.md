---
description: 'Más información acerca de: JetBeginExternalBackupInstance (función)'
title: JetBeginExternalBackupInstance función)
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496936"
---
# <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="e2bd6-103">JetBeginExternalBackupInstance función)</span><span class="sxs-lookup"><span data-stu-id="e2bd6-103">JetBeginExternalBackupInstance Function</span></span>


<span data-ttu-id="e2bd6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e2bd6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackupinstance-function"></a><span data-ttu-id="e2bd6-105">JetBeginExternalBackupInstance función)</span><span class="sxs-lookup"><span data-stu-id="e2bd6-105">JetBeginExternalBackupInstance Function</span></span>

<span data-ttu-id="e2bd6-106">La función **JetBeginExternalBackupInstance** inicia una copia de seguridad externa mientras el motor y la base de datos están en línea y activos.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-106">The **JetBeginExternalBackupInstance** function initiates an external backup while the engine and database are online and active.</span></span>

<span data-ttu-id="e2bd6-107">**Windows XP: JetBeginExternalBackupInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-107">**Windows XP:  JetBeginExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e2bd6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2bd6-108">Parameters</span></span>

<span data-ttu-id="e2bd6-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="e2bd6-109">*instance*</span></span>

<span data-ttu-id="e2bd6-110">Instancia de base de datos que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-110">The database instance to use for this call.</span></span>

<span data-ttu-id="e2bd6-111">En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="e2bd6-112">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="e2bd6-113">En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="e2bd6-114">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="e2bd6-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e2bd6-115">*grbit*</span></span>

<span data-ttu-id="e2bd6-116">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2bd6-117">Value</span><span class="sxs-lookup"><span data-stu-id="e2bd6-117">Value</span></span></p></th>
<th><p><span data-ttu-id="e2bd6-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e2bd6-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2bd6-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="e2bd6-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="e2bd6-120">Esta marca está en desuso.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-120">This flag is deprecated.</span></span> <span data-ttu-id="e2bd6-121">El uso de este bit producirá JET_errInvalidgrbit devuelto.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-121">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2bd6-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="e2bd6-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="e2bd6-123">Crea una copia de seguridad incremental en lugar de una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="e2bd6-124">Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-124">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2bd6-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="e2bd6-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="e2bd6-126">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-126">Reserved for future use.</span></span> <span data-ttu-id="e2bd6-127">Definido para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-127">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e2bd6-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2bd6-128">Return Value</span></span>

<span data-ttu-id="e2bd6-129">El sistema puede generar códigos de éxito o error como resultado de una llamada a esta función.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-129">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="e2bd6-130">Para obtener una lista completa de los errores de esta API, consulte [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e2bd6-130">For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="e2bd6-131">Vea [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="e2bd6-131">See [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

#### <a name="remarks"></a><span data-ttu-id="e2bd6-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2bd6-132">Remarks</span></span>

<span data-ttu-id="e2bd6-133">**JetBeginExternalBackupInstance** es la primera función de una serie de funciones a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-133">**JetBeginExternalBackupInstance** is the first function in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span> <span data-ttu-id="e2bd6-134">Vea también [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) y [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="e2bd6-134">See also [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) and [JetStopBackupInstance](./jetstopbackupinstance-function.md).</span></span>

<span data-ttu-id="e2bd6-135">Se puede utilizar una copia de seguridad externa para implementar copias de seguridad completas, incrementales o diferenciales.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-135">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="e2bd6-136">La copia de seguridad será aproximada, en la que la copia de seguridad será coherente con un único punto en el tiempo en el historial de transacciones, pero no es posible controlar el punto exacto en el tiempo en este momento.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-136">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible at this time.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e2bd6-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2bd6-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2bd6-138"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e2bd6-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e2bd6-139">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2bd6-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e2bd6-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e2bd6-141">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2bd6-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e2bd6-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e2bd6-143">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2bd6-144"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="e2bd6-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e2bd6-145">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2bd6-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e2bd6-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e2bd6-147">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e2bd6-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e2bd6-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e2bd6-148">See Also</span></span>

[<span data-ttu-id="e2bd6-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e2bd6-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e2bd6-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e2bd6-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e2bd6-151">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e2bd6-151">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="e2bd6-152">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="e2bd6-152">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="e2bd6-153">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="e2bd6-153">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="e2bd6-154">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="e2bd6-154">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="e2bd6-155">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="e2bd6-155">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="e2bd6-156">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="e2bd6-156">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="e2bd6-157">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="e2bd6-157">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="e2bd6-158">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="e2bd6-158">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="e2bd6-159">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="e2bd6-159">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="e2bd6-160">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="e2bd6-160">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="e2bd6-161">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="e2bd6-161">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="e2bd6-162">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="e2bd6-162">JetTruncateLog</span></span>](./jettruncatelog-function.md)
