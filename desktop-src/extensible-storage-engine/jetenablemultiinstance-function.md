---
description: 'Más información acerca de: JetEnableMultiInstance (función)'
title: JetEnableMultiInstance función)
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697873"
---
# <a name="jetenablemultiinstance-function"></a><span data-ttu-id="70617-103">JetEnableMultiInstance función)</span><span class="sxs-lookup"><span data-stu-id="70617-103">JetEnableMultiInstance Function</span></span>


<span data-ttu-id="70617-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="70617-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetenablemultiinstance-function"></a><span data-ttu-id="70617-105">JetEnableMultiInstance función)</span><span class="sxs-lookup"><span data-stu-id="70617-105">JetEnableMultiInstance Function</span></span>

<span data-ttu-id="70617-106">La función **JetEnableMultiInstance** configura el motor de base de datos para su uso con varias instancias en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="70617-106">The **JetEnableMultiInstance** function configures the database engine for use with multiple instances in the same process.</span></span> <span data-ttu-id="70617-107">Una matriz opcional de parámetros globales del sistema está disponible para el primer llamador, lo que permite el cambio en el modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="70617-107">An optional array of global system parameters is available to the first caller allowing for the change to multi-instance mode.</span></span>

<span data-ttu-id="70617-108">**Windows XP: JetEnableMultiInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70617-108">**Windows XP:  JetEnableMultiInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a><span data-ttu-id="70617-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70617-109">Parameters</span></span>

<span data-ttu-id="70617-110">*psetsysparam*</span><span class="sxs-lookup"><span data-stu-id="70617-110">*psetsysparam*</span></span>

<span data-ttu-id="70617-111">Una matriz de parámetros globales del sistema para establecer si y solo si el motor entra en modo de varias instancias como resultado de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="70617-111">An array of global system parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="70617-112">Si *csetsysparam* es cero, *psetsysparam* se omite.</span><span class="sxs-lookup"><span data-stu-id="70617-112">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="70617-113">*csetsysparam*</span><span class="sxs-lookup"><span data-stu-id="70617-113">*csetsysparam*</span></span>

<span data-ttu-id="70617-114">Recuento de elementos de la matriz de parámetros globales que se van a establecer si y solo si el motor entra en modo de varias instancias como resultado de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="70617-114">The count of elements for the array of global parameters to set if and only if the engine enters multi-instance mode as a result of this call.</span></span> <span data-ttu-id="70617-115">Si *csetsysparam* es cero, *psetsysparam* se omite.</span><span class="sxs-lookup"><span data-stu-id="70617-115">If *csetsysparam* is zero then *psetsysparam* is ignored.</span></span>

<span data-ttu-id="70617-116">*pcsetsucceed*</span><span class="sxs-lookup"><span data-stu-id="70617-116">*pcsetsucceed*</span></span>

<span data-ttu-id="70617-117">Puntero al recuento de parámetros del sistema globales que se configuraron correctamente como resultado de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="70617-117">A pointer to the count of global system parameters that were successfully configured as a result of this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="70617-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70617-118">Return Value</span></span>

<span data-ttu-id="70617-119">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="70617-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="70617-120">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="70617-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70617-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="70617-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="70617-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="70617-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70617-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="70617-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="70617-124">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="70617-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70617-125">JET_errIndexTuplesInvalidLimits</span><span class="sxs-lookup"><span data-stu-id="70617-125">JET_errIndexTuplesInvalidLimits</span></span></p></td>
<td><p><span data-ttu-id="70617-126">No se permiten los parámetros de índice de tupla especificados.</span><span class="sxs-lookup"><span data-stu-id="70617-126">The specified tuple index parameters were not allowed.</span></span> <span data-ttu-id="70617-127">Este error puede ser devuelto por <strong>JetEnableMultiInstance</strong> solo cuando se establece <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>o <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> en un valor no válido.</span><span class="sxs-lookup"><span data-stu-id="70617-127">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>, or <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> to an illegal value.</span></span></p>
<p><span data-ttu-id="70617-128"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70617-128"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70617-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="70617-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="70617-130">La ruta de acceso del sistema de archivos especificada no era válida.</span><span class="sxs-lookup"><span data-stu-id="70617-130">The specified file system path was invalid.</span></span> <span data-ttu-id="70617-131">Este error puede ser devuelto por <strong>JetEnableMultiInstance</strong> solo cuando se establecen parámetros del sistema que representan rutas de acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="70617-131">This error can be returned by <strong>JetEnableMultiInstance</strong> only when setting system parameters that represent file system paths.</span></span> <span data-ttu-id="70617-132">Por ejemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> puede devolver este error.</span><span class="sxs-lookup"><span data-stu-id="70617-132">For example, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> can return this error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70617-133">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="70617-133">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="70617-134">No se pudo realizar la operación porque no es válida cuando el motor de base de datos está funcionando en modo de instancia única (modo de compatibilidad de Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="70617-134">The operation failed because it is illegal when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70617-135">JET_errSystemParamsAlreadySet</span><span class="sxs-lookup"><span data-stu-id="70617-135">JET_errSystemParamsAlreadySet</span></span></p></td>
<td><p><span data-ttu-id="70617-136">Error de <strong>JetEnableMultiInstance</strong> porque el motor ya está en modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="70617-136"><strong>JetEnableMultiInstance</strong> failed because the engine is already in multi-instance mode.</span></span></p>
<p><span data-ttu-id="70617-137"><strong>Nota:  </strong> Esto ocurrirá aunque no se especifiquen parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="70617-137"><strong>Note  </strong>This will happen even if no system parameters are specified.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70617-138">Si esta función se ejecuta correctamente, el motor de base de datos se configurará para ejecutarse en modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="70617-138">If this function succeeds, the database engine will be configured to run in multi-instance mode.</span></span> <span data-ttu-id="70617-139">El motor también se configuró correctamente con la lista opcional de parámetros del sistema globales.</span><span class="sxs-lookup"><span data-stu-id="70617-139">The engine was also successfully configured with the optional list of global system parameters.</span></span>

<span data-ttu-id="70617-140">Si se produce un error en esta función, el motor de base de datos permanecerá en el modo actual.</span><span class="sxs-lookup"><span data-stu-id="70617-140">If this function fails, the database engine will remain in the current mode.</span></span> <span data-ttu-id="70617-141">Si *pcsetsucceed* es distinto de cero, ese número de parámetros del sistema permanecerá establecido.</span><span class="sxs-lookup"><span data-stu-id="70617-141">If *pcsetsucceed* is non-zero, that number of system parameters will remain set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="70617-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70617-142">Remarks</span></span>

<span data-ttu-id="70617-143">Esta función solo se debe usar si la aplicación debe configurar un conjunto determinado de parámetros del sistema de forma atómica al configurar el motor de base de datos para su uso en un escenario de varios usuarios en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="70617-143">This function should only be used if the application must configure a given set of system parameters atomically when setting up the database engine for use in a multi-user scenario in the same process.</span></span> <span data-ttu-id="70617-144">Si hay otro método de sincronización disponible, es preferible llamar a [JetCreateInstance](./jetcreateinstance-function.md) y [JetSetSystemParameter](./jetsetsystemparameter-function.md) por separado.</span><span class="sxs-lookup"><span data-stu-id="70617-144">If another method of synchronization is available, it is preferable to call [JetCreateInstance](./jetcreateinstance-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) separately.</span></span>

#### <a name="requirements"></a><span data-ttu-id="70617-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70617-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70617-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="70617-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="70617-147">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70617-147">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70617-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="70617-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="70617-149">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="70617-149">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70617-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="70617-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="70617-151">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="70617-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70617-152"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="70617-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="70617-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="70617-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70617-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="70617-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="70617-155">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="70617-155">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70617-156"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="70617-156"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="70617-157">Se implementa como <strong>JetEnableMultiInstanceW</strong> (Unicode) y <strong>JetEnableMultiInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="70617-157">Implemented as <strong>JetEnableMultiInstanceW</strong> (Unicode) and <strong>JetEnableMultiInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="70617-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="70617-158">See Also</span></span>

[<span data-ttu-id="70617-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="70617-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="70617-160">JET_SETSYSPARAM</span><span class="sxs-lookup"><span data-stu-id="70617-160">JET_SETSYSPARAM</span></span>](./jet-setsysparam-structure.md)  
[<span data-ttu-id="70617-161">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="70617-161">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="70617-162">JetInit</span><span class="sxs-lookup"><span data-stu-id="70617-162">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="70617-163">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="70617-163">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
