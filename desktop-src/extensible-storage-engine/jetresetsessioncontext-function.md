---
description: 'Más información acerca de: JetResetSessionContext (función)'
title: JetResetSessionContext función)
TOCTitle: JetResetSessionContext Function
ms:assetid: 537a4753-b804-457a-9a13-53e8d1056eab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269250(v=EXCHG.10)
ms:contentKeyID: 32765552
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetResetSessionContext
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ee02050a9583aa67f50fbe53d710c352c196048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277100"
---
# <a name="jetresetsessioncontext-function"></a><span data-ttu-id="eca0c-103">JetResetSessionContext función)</span><span class="sxs-lookup"><span data-stu-id="eca0c-103">JetResetSessionContext Function</span></span>


<span data-ttu-id="eca0c-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="eca0c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetresetsessioncontext-function"></a><span data-ttu-id="eca0c-105">JetResetSessionContext función)</span><span class="sxs-lookup"><span data-stu-id="eca0c-105">JetResetSessionContext Function</span></span>

<span data-ttu-id="eca0c-106">La función **JetResetSessionContext** desasocia una sesión del subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="eca0c-106">The **JetResetSessionContext** function disassociates a session from the current thread.</span></span>

```cpp
    JET_ERR JET_API JetResetSessionContext(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="eca0c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eca0c-107">Parameters</span></span>

<span data-ttu-id="eca0c-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="eca0c-108">*sesid*</span></span>

<span data-ttu-id="eca0c-109">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="eca0c-109">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="eca0c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eca0c-110">Return Value</span></span>

<span data-ttu-id="eca0c-111">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="eca0c-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="eca0c-112">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eca0c-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eca0c-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="eca0c-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="eca0c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="eca0c-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eca0c-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="eca0c-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="eca0c-116">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="eca0c-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eca0c-117">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="eca0c-117">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="eca0c-118">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="eca0c-118">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="eca0c-119">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="eca0c-119">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eca0c-120">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="eca0c-120">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="eca0c-121">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="eca0c-121">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eca0c-122">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="eca0c-122">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="eca0c-123">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="eca0c-123">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eca0c-124">JET_errSessionContextNotSetByThisThread</span><span class="sxs-lookup"><span data-stu-id="eca0c-124">JET_errSessionContextNotSetByThisThread</span></span></p></td>
<td><p><span data-ttu-id="eca0c-125">No se pudo desasociar la sesión del subproceso actual porque está asociada a un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="eca0c-125">The session could not be disassociated from the current thread because it is associated with a different thread.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eca0c-126">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="eca0c-126">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="eca0c-127">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="eca0c-127">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="eca0c-128">Si se ejecuta correctamente, la sesión se desasociará del subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="eca0c-128">On success, the session will be disassociated from the current thread.</span></span> <span data-ttu-id="eca0c-129">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="eca0c-129">No change to the database state will occur.</span></span>

<span data-ttu-id="eca0c-130">En caso de error, el estado de la sesión permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="eca0c-130">On failure, the session state will remain unchanged.</span></span> <span data-ttu-id="eca0c-131">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="eca0c-131">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="eca0c-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eca0c-132">Remarks</span></span>

<span data-ttu-id="eca0c-133">Se debe llamar a **JetResetSessionContext** en el mismo subproceso que llamó a [JetSetSessionContext](./jetsetsessioncontext-function.md) para una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="eca0c-133">**JetResetSessionContext** must be called on the same thread that called [JetSetSessionContext](./jetsetsessioncontext-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="eca0c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eca0c-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eca0c-135"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="eca0c-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="eca0c-136">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="eca0c-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eca0c-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="eca0c-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="eca0c-138">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="eca0c-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eca0c-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="eca0c-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="eca0c-140">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="eca0c-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eca0c-141"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="eca0c-141"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="eca0c-142">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="eca0c-142">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eca0c-143"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="eca0c-143"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="eca0c-144">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="eca0c-144">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="eca0c-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="eca0c-145">See Also</span></span>

[<span data-ttu-id="eca0c-146">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="eca0c-146">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="eca0c-147">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="eca0c-147">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="eca0c-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="eca0c-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="eca0c-149">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="eca0c-149">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)
