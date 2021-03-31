---
description: 'Más información acerca de: JetIdle (función)'
title: JetIdle función)
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911438"
---
# <a name="jetidle-function"></a><span data-ttu-id="9f8c9-103">JetIdle función)</span><span class="sxs-lookup"><span data-stu-id="9f8c9-103">JetIdle Function</span></span>


<span data-ttu-id="9f8c9-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9f8c9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetidle-function"></a><span data-ttu-id="9f8c9-105">JetIdle función)</span><span class="sxs-lookup"><span data-stu-id="9f8c9-105">JetIdle Function</span></span>

<span data-ttu-id="9f8c9-106">La función **JetIdle** está inactiva y solo debe usarse con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-106">The **JetIdle** function is defunct, and should only be used for testing purposes.</span></span> <span data-ttu-id="9f8c9-107">**JetIdle** se puede usar para realizar tareas de limpieza inactiva o comprobar el estado del almacén de versiones en ese.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-107">**JetIdle** can be used to perform idle cleanup tasks or check the version store status in ESE.</span></span>

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9f8c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f8c9-108">Parameters</span></span>

<span data-ttu-id="9f8c9-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9f8c9-109">*sesid*</span></span>

<span data-ttu-id="9f8c9-110">La sesión que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-110">The session that will be used for this call.</span></span>

<span data-ttu-id="9f8c9-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9f8c9-111">*grbit*</span></span>

<span data-ttu-id="9f8c9-112">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los bits siguientes:</span><span class="sxs-lookup"><span data-stu-id="9f8c9-112">A group of bits that contain the options to be used for this call, which include zero or more of the following bits:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f8c9-113">Value</span><span class="sxs-lookup"><span data-stu-id="9f8c9-113">Value</span></span></p></th>
<th><p><span data-ttu-id="9f8c9-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9f8c9-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f8c9-115">JET_bitIdleCompact</span><span class="sxs-lookup"><span data-stu-id="9f8c9-115">JET_bitIdleCompact</span></span></p></td>
<td><p><span data-ttu-id="9f8c9-116">Desencadena la limpieza del almacén de versiones.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-116">Triggers cleanup of the version store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f8c9-117">JET_bitIdleFlushBuffers</span><span class="sxs-lookup"><span data-stu-id="9f8c9-117">JET_bitIdleFlushBuffers</span></span></p></td>
<td><p><span data-ttu-id="9f8c9-118">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-118">Reserved for future use.</span></span> <span data-ttu-id="9f8c9-119">Si se especifica esta marca, la API devolverá JET_errInvalidgrbit.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-119">If this flag is specified, the API will return JET_errInvalidgrbit.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f8c9-120">JET_bitIdleStatus</span><span class="sxs-lookup"><span data-stu-id="9f8c9-120">JET_bitIdleStatus</span></span></p></td>
<td><p><span data-ttu-id="9f8c9-121">Devuelve JET_wrnIdleFull si el almacén de versiones es más de la mitad de llenado.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-121">Returns JET_wrnIdleFull if version store is more than half full.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9f8c9-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f8c9-122">Return Value</span></span>

<span data-ttu-id="9f8c9-123">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9f8c9-124">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9f8c9-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9f8c9-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9f8c9-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="9f8c9-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f8c9-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f8c9-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9f8c9-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9f8c9-128">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f8c9-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9f8c9-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9f8c9-130">Un parámetro <em>grbit</em> que se proporcionó a la API no era válido.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-130">A <em>grbit</em> parameter that was provided to the API was not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9f8c9-131">Si esta función se ejecuta correctamente, se desencadenará la operación adecuada o un código de error que indique el grado de llenado del almacén de versiones según el valor de *grbit* proporcionado.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-131">If this function succeeds, the appropriate operation will be triggered, or an error code indicating how full the version store is depending on the *grbit* provided.</span></span>

<span data-ttu-id="9f8c9-132">Si se produce un error en esta función, la operación solicitada no se completará correctamente.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-132">If this function fails, the requested operation will not have completed successfully.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9f8c9-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f8c9-133">Remarks</span></span>

<span data-ttu-id="9f8c9-134">El almacén de versiones mantiene el mecanismo de aislamiento de instantáneas de ESE.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-134">The version store maintains ESE's snapshot isolation mechanism.</span></span> <span data-ttu-id="9f8c9-135">Si el almacén de versiones es más de la mitad, el programa podría cerrar las transacciones de ejecución prolongada.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-135">If the version store is more than half full, the program might close long-running transactions.</span></span> <span data-ttu-id="9f8c9-136">Si una transacción de ejecución prolongada agota el almacén de versiones, ESE dejará de permitir operaciones de escritura en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-136">If a long-running transaction exhausts the version store, ESE will stop allowing write operations to the database.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9f8c9-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f8c9-137">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9f8c9-138"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9f8c9-138"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8c9-139">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-139">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f8c9-140"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9f8c9-140"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8c9-141">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-141">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f8c9-142"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9f8c9-142"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8c9-143">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-143">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9f8c9-144"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="9f8c9-144"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8c9-145">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-145">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9f8c9-146"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9f8c9-146"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9f8c9-147">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9f8c9-147">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9f8c9-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f8c9-148">See Also</span></span>

[<span data-ttu-id="9f8c9-149">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9f8c9-149">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9f8c9-150">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9f8c9-150">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9f8c9-151">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9f8c9-151">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9f8c9-152">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="9f8c9-152">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
