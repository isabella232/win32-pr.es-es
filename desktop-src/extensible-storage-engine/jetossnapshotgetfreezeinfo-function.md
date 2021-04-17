---
description: 'Más información acerca de: JetOSSnapshotGetFreezeInfo (función)'
title: JetOSSnapshotGetFreezeInfo función)
TOCTitle: JetOSSnapshotGetFreezeInfo Function
ms:assetid: b94eaf91-7407-4c62-ab1e-3249ad076c1a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294070(v=EXCHG.10)
ms:contentKeyID: 32765685
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotGetFreezeInfo
- JetOSSnapshotGetFreezeInfoA
- JetOSSnapshotGetFreezeInfoW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2fbfd3fb31567ea73b8266b5aeba506d62be7714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716601"
---
# <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="a405e-103">JetOSSnapshotGetFreezeInfo función)</span><span class="sxs-lookup"><span data-stu-id="a405e-103">JetOSSnapshotGetFreezeInfo Function</span></span>


<span data-ttu-id="a405e-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a405e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotgetfreezeinfo-function"></a><span data-ttu-id="a405e-105">JetOSSnapshotGetFreezeInfo función)</span><span class="sxs-lookup"><span data-stu-id="a405e-105">JetOSSnapshotGetFreezeInfo Function</span></span>

<span data-ttu-id="a405e-106">La función **JetOSSnapshotGetFreezeInfo** recupera la lista de instancias y bases de datos que forman parte de la sesión de instantáneas en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="a405e-106">The **JetOSSnapshotGetFreezeInfo** function retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="a405e-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a405e-107">**Windows Vista:**  **JetOSSnapshotGetFreezeInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotGetFreezeInfo(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="a405e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a405e-108">Parameters</span></span>

<span data-ttu-id="a405e-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="a405e-109">*snapId*</span></span>

<span data-ttu-id="a405e-110">Identificador de la sesión de instantáneas que se va a iniciar.</span><span class="sxs-lookup"><span data-stu-id="a405e-110">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="a405e-111">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="a405e-111">*pcInstanceInfo*</span></span>

<span data-ttu-id="a405e-112">El número de instancias que se están ejecutando actualmente y que forman parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="a405e-112">The number of instances currently running that are part of the snapshot session.</span></span>

<span data-ttu-id="a405e-113">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="a405e-113">*paInstanceInfo*</span></span>

<span data-ttu-id="a405e-114">Una matriz de estructuras, una para cada instancia en ejecución, que describe la instancia y las bases de datos que forman parte de ella.</span><span class="sxs-lookup"><span data-stu-id="a405e-114">An array of structures, one for each running instance, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="a405e-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a405e-115">*grbit*</span></span>

<span data-ttu-id="a405e-116">Opciones de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a405e-116">The options for this call.</span></span> <span data-ttu-id="a405e-117">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a405e-117">This parameter is reserved for future use.</span></span> <span data-ttu-id="a405e-118">El único valor válido es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="a405e-118">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="a405e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a405e-119">Return Value</span></span>

<span data-ttu-id="a405e-120">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="a405e-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a405e-121">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a405e-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a405e-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a405e-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="a405e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a405e-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a405e-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a405e-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a405e-125">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a405e-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a405e-126">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a405e-126">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a405e-127">Error de la función debido a una condición de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="a405e-127">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a405e-128">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a405e-128">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a405e-129"><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="a405e-129"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a405e-130">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="a405e-130">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="a405e-131">El identificador de la sesión de instantáneas no es válido.</span><span class="sxs-lookup"><span data-stu-id="a405e-131">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a405e-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="a405e-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="a405e-133">Una sesión de instantáneas no está en curso.</span><span class="sxs-lookup"><span data-stu-id="a405e-133">A snapshot session is not in progress.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a405e-134">Si esta función se ejecuta correctamente, la información de la instancia se rellena correctamente y se debe liberar más adelante llamando a [JetFreeBuffer](./jetfreebuffer-function.md) con el puntero a la matriz de información de instancia que se devolvió.</span><span class="sxs-lookup"><span data-stu-id="a405e-134">If this function succeeds, the instance information is properly filled and it must be freed later by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="a405e-135">Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.</span><span class="sxs-lookup"><span data-stu-id="a405e-135">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a405e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a405e-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a405e-137"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a405e-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a405e-138">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a405e-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a405e-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a405e-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a405e-140">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a405e-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a405e-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a405e-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a405e-142">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a405e-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a405e-143"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="a405e-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a405e-144">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a405e-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a405e-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a405e-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a405e-146">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a405e-146">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a405e-147"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a405e-147"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a405e-148">Se implementa como <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) y <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a405e-148">Implemented as <strong>JetOSSnapshotGetFreezeInfoW</strong> (Unicode) and <strong>JetOSSnapshotGetFreezeInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a405e-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a405e-149">See Also</span></span>

[<span data-ttu-id="a405e-150">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="a405e-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="a405e-151">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="a405e-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="a405e-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a405e-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a405e-153">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a405e-153">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)  
[<span data-ttu-id="a405e-154">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="a405e-154">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="a405e-155">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="a405e-155">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="a405e-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="a405e-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
