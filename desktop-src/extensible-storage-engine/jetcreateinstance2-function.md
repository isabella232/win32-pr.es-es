---
description: 'Más información acerca de: JetCreateInstance2 (función)'
title: Función JetCreateInstance2
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af31e7e66d92cf7ebbc238ac54a9b331e6dc5362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720637"
---
# <a name="jetcreateinstance2-function"></a><span data-ttu-id="308bb-103">Función JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="308bb-103">JetCreateInstance2 Function</span></span>


<span data-ttu-id="308bb-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="308bb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance2-function"></a><span data-ttu-id="308bb-105">Función JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="308bb-105">JetCreateInstance2 Function</span></span>

<span data-ttu-id="308bb-106">La función **JetCreateInstance2** se usa para asignar una nueva instancia del motor de base de datos para su uso en un único proceso, con un nombre para mostrar especificado.</span><span class="sxs-lookup"><span data-stu-id="308bb-106">The **JetCreateInstance2** function is used to allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="308bb-107">**Windows XP:**  **JetCreateInstance2** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="308bb-107">**Windows XP:**  **JetCreateInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="308bb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="308bb-108">Parameters</span></span>

<span data-ttu-id="308bb-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="308bb-109">*pinstance*</span></span>

<span data-ttu-id="308bb-110">Búfer de salida que recibirá la instancia que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="308bb-110">The output buffer that will receive the newly created instance.</span></span>

<span data-ttu-id="308bb-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="308bb-111">*szInstanceName*</span></span>

<span data-ttu-id="308bb-112">Especifica un identificador de cadena único para la instancia que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="308bb-112">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="308bb-113">Esta cadena debe ser única dentro de un proceso determinado que hospede el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="308bb-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="308bb-114">**Nota:** Un valor NULL se trata como un identificador de cadena válido para una instancia de.</span><span class="sxs-lookup"><span data-stu-id="308bb-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="308bb-115">Solo una instancia puede tener un identificador de cadena NULL.</span><span class="sxs-lookup"><span data-stu-id="308bb-115">Only one instance may have a NULL string identifier.</span></span>

<span data-ttu-id="308bb-116">*szDisplayName*</span><span class="sxs-lookup"><span data-stu-id="308bb-116">*szDisplayName*</span></span>

<span data-ttu-id="308bb-117">Nombre para mostrar de la instancia de que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="308bb-117">A display name for the instance to be created.</span></span> <span data-ttu-id="308bb-118">Cuando este parámetro no está presente, se supone que su valor es NULL.</span><span class="sxs-lookup"><span data-stu-id="308bb-118">When this parameter is not present, its value is presumed to be NULL.</span></span>

<span data-ttu-id="308bb-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="308bb-119">*grbit*</span></span>

<span data-ttu-id="308bb-120">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="308bb-120">Reserved for future use.</span></span> <span data-ttu-id="308bb-121">Cuando este parámetro no está presente, se supone que su valor es cero.</span><span class="sxs-lookup"><span data-stu-id="308bb-121">When this parameter is not present, its value is presumed to be zero.</span></span>

### <a name="return-value"></a><span data-ttu-id="308bb-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="308bb-122">Return Value</span></span>

<span data-ttu-id="308bb-123">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="308bb-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="308bb-124">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="308bb-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="308bb-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="308bb-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="308bb-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="308bb-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="308bb-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="308bb-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="308bb-128">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="308bb-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308bb-129">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="308bb-129">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="308bb-130">El nombre de instancia especificado ya está en uso para este proceso.</span><span class="sxs-lookup"><span data-stu-id="308bb-130">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="308bb-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="308bb-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="308bb-132">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="308bb-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="308bb-133">Esto puede ocurrir para <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> cuando <em>pinstance</em> es NULL.</span><span class="sxs-lookup"><span data-stu-id="308bb-133">This can happen for <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> when <em>pinstance</em> is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308bb-134">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="308bb-134">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="308bb-135">No se pudo realizar la operación porque no se puede usar cuando el motor de base de datos está funcionando en modo de instancia única (modo de compatibilidad de Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="308bb-135">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="308bb-136">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="308bb-136">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="308bb-137">No se pudo crear una nueva instancia porque se ha alcanzado el número máximo de instancias.</span><span class="sxs-lookup"><span data-stu-id="308bb-137">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="308bb-138">El número máximo de instancias admitidas se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="308bb-138">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="308bb-139">Si se ejecuta correctamente, se asignará una nueva instancia de y se devolverá el identificador de la misma.</span><span class="sxs-lookup"><span data-stu-id="308bb-139">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="308bb-140">En este momento, todos los parámetros del sistema para la instancia de tendrán los valores de los parámetros globales del sistema predeterminados.</span><span class="sxs-lookup"><span data-stu-id="308bb-140">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="308bb-141">Una vez que se asigna una instancia, debe terminarse o liberarse más adelante.</span><span class="sxs-lookup"><span data-stu-id="308bb-141">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="308bb-142">En caso de error, se devolverá un error que representa la causa del error y no se asignará ninguna instancia.</span><span class="sxs-lookup"><span data-stu-id="308bb-142">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="308bb-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="308bb-143">Remarks</span></span>

<span data-ttu-id="308bb-144">Una instancia de se debe inicializar con una llamada a [JetInit](./jetinit-function.md) para que pueda ser utilizada por cualquier cosa que no sea [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="308bb-144">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="308bb-145">Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó con [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="308bb-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="308bb-146">El número máximo de instancias que se pueden crear en un momento determinado se controla mediante *JET_paramMaxInstances*, que se puede configurar mediante una llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="308bb-146">The maximum number of instances that may be created at any one time is controlled by *JET_paramMaxInstances*, which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="308bb-147">Una instancia es la unidad de capacidad de recuperación del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="308bb-147">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="308bb-148">Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="308bb-148">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="308bb-149">Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="308bb-149">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="308bb-150">Si la función se ejecuta correctamente, el motor de base de datos se cambiará automáticamente al modo de varias instancias como un efecto secundario de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="308bb-150">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="308bb-151">Si la aplicación desea permitir solo una instancia en el proceso, se debe utilizar [JetInit](./jetinit-function.md) para iniciar el motor de base de datos en el modo de compatibilidad de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="308bb-151">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="308bb-152">Si está presente, el parámetro *szDisplayName* se usará para identificar la instancia en lugares como el registro de eventos o en otros llamadores como aplicaciones de copia de seguridad (a través de funciones como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="308bb-152">If present, the *szDisplayName* parameter will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="308bb-153">Si no se proporciona el nombre para mostrar, se usará en su lugar el parámetro *szInstanceName* único, si está presente; de lo contrario, se devolverá una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="308bb-153">If the display name is not provided, the unique *szInstanceName* parameter will be used instead, if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="308bb-154">Si el motor no tenía establecido el modo de ejecución, después de esta llamada se establecerá en modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="308bb-154">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="308bb-155">La secuencia de inicio típica para un proceso que puede ejecutar varias instancias de jet sería:</span><span class="sxs-lookup"><span data-stu-id="308bb-155">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="308bb-156">Una llamada a **JetCreateInstance2** que asignará y denominará a la instancia.</span><span class="sxs-lookup"><span data-stu-id="308bb-156">A call to **JetCreateInstance2** which will allocate and name the instance.</span></span>

  - <span data-ttu-id="308bb-157">Varias llamadas a [JetSetSystemParameter](./jetsetsystemparameter-function.md) para esa instancia con el fin de establecer diferentes parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="308bb-157">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="308bb-158">Tenga en cuenta que algunos parámetros del sistema deben ser únicos para cada instancia (como *JET_paramSystemPath* o *JET_paramLogFilePath*), lo más probable es que se establezca cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="308bb-158">Note that some system parameters need to be unique for each instance (like *JET_paramSystemPath* or *JET_paramLogFilePath*) so most likely, each of these will need to be set.</span></span>

  - <span data-ttu-id="308bb-159">Inicie la instancia de mediante [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="308bb-159">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="308bb-160">Para finalizar y/o liberar una instancia, use [JetTerm](./jetterm-function.md) o [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="308bb-160">In order to terminate and/or free an instance, use [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="308bb-161">Si esta es la primera instancia que se va a iniciar, hay una serie de pasos adicionales que se ejecutarán durante esta llamada para realizar la inicialización y configuración básicas del sistema.</span><span class="sxs-lookup"><span data-stu-id="308bb-161">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="308bb-162">Algunos de estos pasos pueden dar lugar a errores concretos a partir de JET_errOutOfMemory pero otros también (vea valores devueltos para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="308bb-162">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see Return Values for more information).</span></span>

#### <a name="requirements"></a><span data-ttu-id="308bb-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="308bb-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="308bb-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="308bb-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="308bb-165">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="308bb-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308bb-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="308bb-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="308bb-167">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="308bb-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="308bb-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="308bb-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="308bb-169">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="308bb-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308bb-170"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="308bb-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="308bb-171">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="308bb-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="308bb-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="308bb-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="308bb-173">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="308bb-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="308bb-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="308bb-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="308bb-175">Se implementa como <strong>JetCreateInstance2W</strong> (Unicode) y <strong>JetCreateInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="308bb-175">Implemented as <strong>JetCreateInstance2W</strong> (Unicode) and <strong>JetCreateInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="308bb-176">Consulte también</span><span class="sxs-lookup"><span data-stu-id="308bb-176">See Also</span></span>

[<span data-ttu-id="308bb-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="308bb-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="308bb-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="308bb-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="308bb-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="308bb-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="308bb-180">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="308bb-180">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="308bb-181">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="308bb-181">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="308bb-182">JetInit</span><span class="sxs-lookup"><span data-stu-id="308bb-182">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="308bb-183">JetInit2</span><span class="sxs-lookup"><span data-stu-id="308bb-183">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="308bb-184">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="308bb-184">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="308bb-185">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="308bb-185">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="308bb-186">JetTerm</span><span class="sxs-lookup"><span data-stu-id="308bb-186">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="308bb-187">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="308bb-187">JetTerm2</span></span>](./jetterm2-function.md)
