---
description: 'Más información acerca de: JetSetTableSequential (función)'
title: JetSetTableSequential función)
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b633b348b712e446535054c5a39d2768236b7705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715026"
---
# <a name="jetsettablesequential-function"></a><span data-ttu-id="493b2-103">JetSetTableSequential función)</span><span class="sxs-lookup"><span data-stu-id="493b2-103">JetSetTableSequential Function</span></span>


<span data-ttu-id="493b2-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="493b2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsettablesequential-function"></a><span data-ttu-id="493b2-105">JetSetTableSequential función)</span><span class="sxs-lookup"><span data-stu-id="493b2-105">JetSetTableSequential Function</span></span>

<span data-ttu-id="493b2-106">La función **JetSetTableSequential** notifica al motor de base de datos que la aplicación está examinando todo el índice actual que contiene un cursor determinado.</span><span class="sxs-lookup"><span data-stu-id="493b2-106">The **JetSetTableSequential** function notifies the database engine that the application is scanning the entire current index that contains a given cursor.</span></span> <span data-ttu-id="493b2-107">Por lo tanto, los métodos que se usan para tener acceso a los datos del índice se optimizarán para que este escenario sea lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="493b2-107">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span>

<span data-ttu-id="493b2-108">**Windows XP:**  **JetSetTableSequential** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="493b2-108">**Windows XP:**  **JetSetTableSequential** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="493b2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="493b2-109">Parameters</span></span>

<span data-ttu-id="493b2-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="493b2-110">*sesid*</span></span>

<span data-ttu-id="493b2-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="493b2-111">The session to use for this call.</span></span>

<span data-ttu-id="493b2-112">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="493b2-112">*tableid*</span></span>

<span data-ttu-id="493b2-113">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="493b2-113">The cursor to use for this call.</span></span>

<span data-ttu-id="493b2-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="493b2-114">*grbit*</span></span>

<span data-ttu-id="493b2-115">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="493b2-115">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="493b2-116">Value</span><span class="sxs-lookup"><span data-stu-id="493b2-116">Value</span></span></p></th>
<th><p><span data-ttu-id="493b2-117">Significado</span><span class="sxs-lookup"><span data-stu-id="493b2-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="493b2-118">JET_bitPrereadForward</span><span class="sxs-lookup"><span data-stu-id="493b2-118">JET_bitPrereadForward</span></span></p></td>
<td><p><span data-ttu-id="493b2-119">Esta opción se utiliza para indizar en la dirección de avance.</span><span class="sxs-lookup"><span data-stu-id="493b2-119">This option is used to index in the forward direction.</span></span></p>
<p><span data-ttu-id="493b2-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> se introduce en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="493b2-120"><strong>Windows 7:</strong>  <strong>JET_bitPrereadForward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="493b2-121">JET_bitPrereadBackward</span><span class="sxs-lookup"><span data-stu-id="493b2-121">JET_bitPrereadBackward</span></span></p></td>
<td><p><span data-ttu-id="493b2-122">Esta opción se usa para indexar en dirección hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="493b2-122">This option is used to index in the backward direction.</span></span></p>
<p><span data-ttu-id="493b2-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> se introduce en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="493b2-123"><strong>Windows 7:</strong>  <strong>JET_bitPrereadBackward</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="493b2-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="493b2-124">Return Value</span></span>

<span data-ttu-id="493b2-125">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="493b2-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="493b2-126">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="493b2-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="493b2-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="493b2-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="493b2-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="493b2-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="493b2-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="493b2-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="493b2-130">No se puede completar la operación porque toda la actividad en la instancia asociada a la sesión se ha detenido como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="493b2-130">The operation cannot complete because all activity on the instance that is associated with the session has been quiesced as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="493b2-131">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="493b2-131">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="493b2-132">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="493b2-132">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="493b2-133"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="493b2-133"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="493b2-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="493b2-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="493b2-135">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="493b2-135">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="493b2-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="493b2-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="493b2-137">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="493b2-137">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="493b2-138">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="493b2-138">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="493b2-139">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="493b2-139">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="493b2-140">Si esta función se ejecuta correctamente, el índice actual del cursor se optimiza para un examen secuencial de todo el índice.</span><span class="sxs-lookup"><span data-stu-id="493b2-140">If this function succeeds, the current index of the cursor is optimized for a sequential scan of the entire index.</span></span> <span data-ttu-id="493b2-141">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="493b2-141">No change to the database state will occur.</span></span>

<span data-ttu-id="493b2-142">Si se produce un error en esta función, no se producirá ningún cambio en la configuración del cursor.</span><span class="sxs-lookup"><span data-stu-id="493b2-142">If this function fails, no change to the configuration of the cursor will occur.</span></span> <span data-ttu-id="493b2-143">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="493b2-143">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="493b2-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="493b2-144">Remarks</span></span>

<span data-ttu-id="493b2-145">Si la aplicación necesita examinar de forma eficaz un subconjunto conocido de un índice, también se realiza una optimización similar siempre que se establece un intervalo de índice mediante [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="493b2-145">If the application needs to efficiently scan a known subset of an index, a similar optimization is also performed whenever an index range is established by using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span> <span data-ttu-id="493b2-146">Esta optimización solo está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="493b2-146">This optimization is only available on Windows XP and later releases.</span></span>

<span data-ttu-id="493b2-147">Si la aplicación necesita examinar de forma eficaz un subconjunto desconocido de un índice, no se debe realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="493b2-147">If the application needs to efficiently scan an unknown subset of an index, no action should be taken.</span></span> <span data-ttu-id="493b2-148">El motor puede detectar automáticamente el comportamiento de exploración y capturará los datos con anterioridad.</span><span class="sxs-lookup"><span data-stu-id="493b2-148">The engine can automatically detect scanning behavior and will fetch data ahead of time.</span></span> <span data-ttu-id="493b2-149">Sin embargo, este comportamiento no es tan agresivo.</span><span class="sxs-lookup"><span data-stu-id="493b2-149">This behavior is not as aggressive, however.</span></span>

<span data-ttu-id="493b2-150">Esta optimización hará que el índice principal sea eficaz y hará que el análisis de los datos de entrada de índice en un índice secundario sea eficaz.</span><span class="sxs-lookup"><span data-stu-id="493b2-150">This optimization will make scanning the primary index efficient and will make scanning just the index entry data in a secondary index efficient.</span></span> <span data-ttu-id="493b2-151">No realizará un examen de un índice secundario mientras se recuperan los datos de registro.</span><span class="sxs-lookup"><span data-stu-id="493b2-151">It will not make scanning a secondary index while retrieving record data efficient.</span></span> <span data-ttu-id="493b2-152">Esto se debe a que el motor no realiza una lectura previa en los datos del registro.</span><span class="sxs-lookup"><span data-stu-id="493b2-152">This is because the engine does not perform a read-ahead on the record data.</span></span>

#### <a name="requirements"></a><span data-ttu-id="493b2-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="493b2-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="493b2-154"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="493b2-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="493b2-155">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="493b2-155">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="493b2-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="493b2-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="493b2-157">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="493b2-157">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="493b2-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="493b2-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="493b2-159">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="493b2-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="493b2-160"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="493b2-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="493b2-161">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="493b2-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="493b2-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="493b2-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="493b2-163">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="493b2-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="493b2-164">Consulte también</span><span class="sxs-lookup"><span data-stu-id="493b2-164">See Also</span></span>

[<span data-ttu-id="493b2-165">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="493b2-165">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="493b2-166">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="493b2-166">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="493b2-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="493b2-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="493b2-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="493b2-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="493b2-169">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="493b2-169">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="493b2-170">JetStopService</span><span class="sxs-lookup"><span data-stu-id="493b2-170">JetStopService</span></span>](./jetstopservice-function.md)
