---
description: 'Más información acerca de: JetCreateInstance (función)'
title: Función JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717168"
---
# <a name="jetcreateinstance-function"></a><span data-ttu-id="0de4f-103">Función JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="0de4f-103">JetCreateInstance Function</span></span>


<span data-ttu-id="0de4f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0de4f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcreateinstance-function"></a><span data-ttu-id="0de4f-105">Función JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="0de4f-105">JetCreateInstance Function</span></span>

<span data-ttu-id="0de4f-106">La función **JetCreateInstance** asigna una nueva instancia del motor de base de datos para su uso en un único proceso.</span><span class="sxs-lookup"><span data-stu-id="0de4f-106">The **JetCreateInstance** function allocates a new instance of the database engine for use in a single process.</span></span>

<span data-ttu-id="0de4f-107">**Windows XP: JetCreateInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0de4f-107">**Windows XP:  JetCreateInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a><span data-ttu-id="0de4f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0de4f-108">Parameters</span></span>

<span data-ttu-id="0de4f-109">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="0de4f-109">*pinstance*</span></span>

<span data-ttu-id="0de4f-110">Búfer de salida que recibe la instancia creada recientemente.</span><span class="sxs-lookup"><span data-stu-id="0de4f-110">The output buffer that receives the newly-created instance.</span></span>

<span data-ttu-id="0de4f-111">*szInstanceName*</span><span class="sxs-lookup"><span data-stu-id="0de4f-111">*szInstanceName*</span></span>

<span data-ttu-id="0de4f-112">Identificador de cadena único para la instancia que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="0de4f-112">A unique string identifier for the instance to be created.</span></span> <span data-ttu-id="0de4f-113">Esta cadena debe ser única dentro de un proceso determinado que hospede el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="0de4f-113">This string must be unique within a given process hosting the database engine.</span></span>

<span data-ttu-id="0de4f-114">**Nota:** Un valor NULL se trata como un identificador de cadena válido para una instancia de.</span><span class="sxs-lookup"><span data-stu-id="0de4f-114">**Note** A NULL value is treated as a valid string identifier for an instance.</span></span> <span data-ttu-id="0de4f-115">Solo una instancia puede tener un identificador de cadena NULL.</span><span class="sxs-lookup"><span data-stu-id="0de4f-115">Only one instance may have a NULL string identifier.</span></span>

### <a name="return-value"></a><span data-ttu-id="0de4f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0de4f-116">Return Value</span></span>

<span data-ttu-id="0de4f-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="0de4f-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0de4f-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0de4f-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0de4f-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="0de4f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0de4f-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0de4f-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0de4f-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0de4f-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0de4f-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de4f-123">JET_errInstanceNameInUse</span><span class="sxs-lookup"><span data-stu-id="0de4f-123">JET_errInstanceNameInUse</span></span></p></td>
<td><p><span data-ttu-id="0de4f-124">El nombre de instancia especificado ya está en uso para este proceso.</span><span class="sxs-lookup"><span data-stu-id="0de4f-124">The specified instance name is already in use for this process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de4f-125">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0de4f-125">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0de4f-126">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="0de4f-126">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="0de4f-127">Esto puede ocurrir para <strong>JetCreateInstance</strong> cuando <em>pinstance</em> es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="0de4f-127">This can happen for <strong>JetCreateInstance</strong> when <em>pinstance</em> is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de4f-128">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="0de4f-128">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="0de4f-129">No se pudo realizar la operación porque no se puede usar cuando el motor de base de datos está funcionando en modo de instancia única (modo de compatibilidad de Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="0de4f-129">The operation failed because it cannot be used when the database engine is operating in single instance mode (Windows 2000 compatibility mode).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de4f-130">JET_errTooManyInstances</span><span class="sxs-lookup"><span data-stu-id="0de4f-130">JET_errTooManyInstances</span></span></p></td>
<td><p><span data-ttu-id="0de4f-131">No se pudo crear una nueva instancia porque se ha alcanzado el número máximo de instancias.</span><span class="sxs-lookup"><span data-stu-id="0de4f-131">A new instance could not be created because the maximum number of instances has been reached.</span></span> <span data-ttu-id="0de4f-132">El número máximo de instancias admitidas se configura mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <em>JET_paramMaxInstances</em>.</span><span class="sxs-lookup"><span data-stu-id="0de4f-132">The maximum number of supported instances is configured using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> using <em>JET_paramMaxInstances</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0de4f-133">Si se ejecuta correctamente, se asignará una nueva instancia de y se devolverá el identificador de la misma.</span><span class="sxs-lookup"><span data-stu-id="0de4f-133">On success, a new instance will be allocated and the identifier for it will be returned.</span></span> <span data-ttu-id="0de4f-134">En este momento, todos los parámetros del sistema para la instancia de tendrán los valores de los parámetros globales del sistema predeterminados.</span><span class="sxs-lookup"><span data-stu-id="0de4f-134">At this point, all system parameters for the instance will have the values of the global default system parameters.</span></span> <span data-ttu-id="0de4f-135">Una vez que se asigna una instancia, debe terminarse o liberarse más adelante.</span><span class="sxs-lookup"><span data-stu-id="0de4f-135">Once an instance will be allocated, it needs to be terminated and/or freed later on.</span></span>

<span data-ttu-id="0de4f-136">En caso de error, se devolverá un error que representa la causa del error y no se asignará ninguna instancia.</span><span class="sxs-lookup"><span data-stu-id="0de4f-136">On failure, an error representing the cause of failure will be returned and no instance will be allocated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0de4f-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0de4f-137">Remarks</span></span>

<span data-ttu-id="0de4f-138">Una instancia de se debe inicializar con una llamada a [JetInit](./jetinit-function.md) para que pueda ser utilizada por cualquier cosa que no sea [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-138">An instance must be initialized with a call to [JetInit](./jetinit-function.md) before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="0de4f-139">Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó con [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-139">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="0de4f-140">El número máximo de instancias que se pueden crear en un momento determinado se controla mediante [JET_paramMaxInstances](./resource-parameters.md), que se puede configurar mediante una llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-140">The maximum number of instances that may be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="0de4f-141">Una instancia es la unidad de capacidad de recuperación del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="0de4f-141">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="0de4f-142">Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="0de4f-142">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="0de4f-143">Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="0de4f-143">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="0de4f-144">Si la función se ejecuta correctamente, el motor de base de datos se cambiará automáticamente al modo de varias instancias como un efecto secundario de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="0de4f-144">If the function succeeds, the database engine will automatically be changed to multi-instance mode as a side effect of this call.</span></span> <span data-ttu-id="0de4f-145">Si la aplicación desea permitir solo una instancia en el proceso, se debe utilizar [JetInit](./jetinit-function.md) para iniciar el motor de base de datos en el modo de compatibilidad de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0de4f-145">If the application desires to allow only one instance in the process then [JetInit](./jetinit-function.md) should be used to start the database engine in Windows 2000 compatibility mode.</span></span>

<span data-ttu-id="0de4f-146">Si está presente, el *szDisplayName* se usará para identificar la instancia en lugares como el registro de eventos o en otros llamadores como aplicaciones de copia de seguridad (a través de funciones como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) o [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span><span class="sxs-lookup"><span data-stu-id="0de4f-146">If present, the *szDisplayName* will be used to identify the instance in places like Event Log or towards other callers like backup applications (through functions like [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) or [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)).</span></span> <span data-ttu-id="0de4f-147">Si no se proporciona el nombre para mostrar, se usará en su lugar el valor de *szInstanceName* único, si está presente; de lo contrario, se devolverá una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="0de4f-147">If the display name is not provided, the unique *szInstanceName* will be used instead if present, otherwise an empty string will be returned.</span></span> <span data-ttu-id="0de4f-148">Si el motor no tenía establecido el modo de ejecución, después de esta llamada se establecerá en modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="0de4f-148">If the engine did not have the running mode set, after this call, it will be set to multi-instance mode.</span></span>

<span data-ttu-id="0de4f-149">La secuencia de inicio típica para un proceso que puede ejecutar varias instancias de jet sería:</span><span class="sxs-lookup"><span data-stu-id="0de4f-149">The typical start-up sequence for a process potentially running multiple Jet instances would be:</span></span>

  - <span data-ttu-id="0de4f-150">Una llamada a [JetCreateInstance2](./jetcreateinstance2-function.md) que asignará y denominará a la instancia.</span><span class="sxs-lookup"><span data-stu-id="0de4f-150">A call to [JetCreateInstance2](./jetcreateinstance2-function.md) which will allocate and name the instance.</span></span>

  - <span data-ttu-id="0de4f-151">Varias llamadas a [JetSetSystemParameter](./jetsetsystemparameter-function.md) para esa instancia con el fin de establecer diferentes parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="0de4f-151">Multiple calls to [JetSetSystemParameter](./jetsetsystemparameter-function.md) for that instance in order to set different system parameters.</span></span> <span data-ttu-id="0de4f-152">Tenga en cuenta que algunos parámetros del sistema deben ser únicos por cada instancia (como [JET_paramSystemPath](./transaction-log-parameters.md) o [JET_paramLogFilePath](./transaction-log-parameters.md)), por lo que lo más probable es que tenga que establecer cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="0de4f-152">Note that some system parameters need to be unique per instance (like [JET_paramSystemPath](./transaction-log-parameters.md) or [JET_paramLogFilePath](./transaction-log-parameters.md)) so most likely one will need to set each of those.</span></span>

  - <span data-ttu-id="0de4f-153">Inicie la instancia de mediante [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-153">Start the instance using [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md).</span></span> <span data-ttu-id="0de4f-154">Para finalizar y/o liberar una instancia, se debe usar [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0de4f-154">In order to terminate and/or free an instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) needs to be used.</span></span>

<span data-ttu-id="0de4f-155">Si esta es la primera instancia que se va a iniciar, hay una serie de pasos adicionales que se ejecutarán durante esta llamada para realizar la inicialización y configuración básicas del sistema.</span><span class="sxs-lookup"><span data-stu-id="0de4f-155">If this is the first instance to be started, there are a number of additional steps which will be executed during this call in order to make basic system initialization and configuration.</span></span> <span data-ttu-id="0de4f-156">Algunos de estos pasos pueden dar lugar a errores concretos a partir de JET_errOutOfMemory pero otros también (consulte los errores anteriores).</span><span class="sxs-lookup"><span data-stu-id="0de4f-156">A number of those steps might result in specific errors starting with JET_errOutOfMemory but others as well (see errors above).</span></span>

#### <a name="requirements"></a><span data-ttu-id="0de4f-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0de4f-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0de4f-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0de4f-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0de4f-159">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0de4f-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de4f-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0de4f-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0de4f-161">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0de4f-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de4f-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0de4f-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0de4f-163">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="0de4f-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de4f-164"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="0de4f-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0de4f-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0de4f-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de4f-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0de4f-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0de4f-167">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0de4f-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de4f-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0de4f-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0de4f-169">Se implementa como <strong>JetCreateInstanceW</strong> (Unicode) y <strong>JetCreateInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0de4f-169">Implemented as <strong>JetCreateInstanceW</strong> (Unicode) and <strong>JetCreateInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0de4f-170">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0de4f-170">See Also</span></span>

[<span data-ttu-id="0de4f-171">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="0de4f-171">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="0de4f-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0de4f-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0de4f-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0de4f-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0de4f-174">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="0de4f-174">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="0de4f-175">JetEnableMultiInstance</span><span class="sxs-lookup"><span data-stu-id="0de4f-175">JetEnableMultiInstance</span></span>](./jetenablemultiinstance-function.md)  
[<span data-ttu-id="0de4f-176">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="0de4f-176">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)  
[<span data-ttu-id="0de4f-177">JetInit</span><span class="sxs-lookup"><span data-stu-id="0de4f-177">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="0de4f-178">JetInit2</span><span class="sxs-lookup"><span data-stu-id="0de4f-178">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="0de4f-179">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="0de4f-179">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="0de4f-180">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="0de4f-180">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="0de4f-181">JetTerm</span><span class="sxs-lookup"><span data-stu-id="0de4f-181">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="0de4f-182">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="0de4f-182">JetTerm2</span></span>](./jetterm2-function.md)
