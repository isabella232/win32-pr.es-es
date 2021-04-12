---
description: 'Más información acerca de: JetInit (función)'
title: Función JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104362842"
---
# <a name="jetinit-function"></a><span data-ttu-id="f05c6-103">Función JetInit</span><span class="sxs-lookup"><span data-stu-id="f05c6-103">JetInit Function</span></span>


<span data-ttu-id="f05c6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f05c6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit-function"></a><span data-ttu-id="f05c6-105">Función JetInit</span><span class="sxs-lookup"><span data-stu-id="f05c6-105">JetInit Function</span></span>

<span data-ttu-id="f05c6-106">La función **JetInit** coloca el motor de base de datos en un estado en el que pueda admitir el uso de aplicaciones de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="f05c6-106">The **JetInit** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="f05c6-107">El motor ya debe estar configurado correctamente para la inicialización mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="f05c6-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="f05c6-108">La recuperación tras bloqueo de la base de datos se realiza automáticamente como parte del proceso de inicialización.</span><span class="sxs-lookup"><span data-stu-id="f05c6-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a><span data-ttu-id="f05c6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f05c6-109">Parameters</span></span>

<span data-ttu-id="f05c6-110">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="f05c6-110">*pinstance*</span></span>

<span data-ttu-id="f05c6-111">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="f05c6-111">The instance to use for this call.</span></span>

<span data-ttu-id="f05c6-112">En Windows 2000, este parámetro se omite y siempre debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f05c6-112">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="f05c6-113">En Windows XP y versiones posteriores, el uso de este parámetro depende del modo de funcionamiento del motor.</span><span class="sxs-lookup"><span data-stu-id="f05c6-113">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="f05c6-114">Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser NULL o se puede establecer en un búfer de salida válido que devolverá el identificador de instancia global creado como un efecto secundario de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="f05c6-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported then this parameter may either be NULL or it may be set to a valid output buffer that will return the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="f05c6-115">Este búfer de salida debe establecerse en NULL o en JET_instanceNil.</span><span class="sxs-lookup"><span data-stu-id="f05c6-115">This output buffer must be set to NULL or JET_instanceNil.</span></span> <span data-ttu-id="f05c6-116">Este identificador de instancia se puede pasar a cualquier otra función que use una instancia de.</span><span class="sxs-lookup"><span data-stu-id="f05c6-116">This instance handle can then be passed to any other function that uses an instance.</span></span> <span data-ttu-id="f05c6-117">Si el motor está funcionando en modo de varias instancias, este parámetro debe establecerse en un búfer de entrada válido que contenga el identificador de instancia devuelto por la instancia de la función [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="f05c6-117">If the engine is operating in multi-instance mode then this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function instance that is being initialized.</span></span>


#### <a name="remarks"></a><span data-ttu-id="f05c6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f05c6-118">Remarks</span></span>

<span data-ttu-id="f05c6-119">Una instancia de se debe inicializar con una llamada a **JetInit** para que pueda ser utilizada por cualquier cosa que no sea [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="f05c6-119">An instance must be initialized with a call to **JetInit** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="f05c6-120">Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó con **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="f05c6-120">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using **JetInit**.</span></span> <span data-ttu-id="f05c6-121">Una instancia es la unidad de capacidad de recuperación del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="f05c6-121">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="f05c6-122">Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="f05c6-122">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="f05c6-123">Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="f05c6-123">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="f05c6-124">El número máximo de instancias que se pueden crear en cualquier momento se controla mediante [JET_paramMaxInstances](./resource-parameters.md), que se puede configurar mediante una llamada a [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="f05c6-124">The maximum number of instances that can be created at any one time is controlled by [JET_paramMaxInstances](./resource-parameters.md), which can be configured by a call to [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="f05c6-125">Cuando el motor de base de datos se inicializa por primera vez, **JetInit** creará un conjunto inicial de archivos para admitir esa instancia.</span><span class="sxs-lookup"><span data-stu-id="f05c6-125">When the database engine is initialized for the first time, **JetInit** will create an initial set of files to support that instance.</span></span> <span data-ttu-id="f05c6-126">Estos archivos incluyen un archivo de punto de comprobación (denominado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), un conjunto de archivos de registro de transacciones reservados (denominado RES1. LOG y RES2. LOG), un archivo de registro de transacciones inicial (denominado \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) y un archivo de base de datos temporal (denominado según [JET_paramTempPath](./temporary-database-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="f05c6-126">These files include a checkpoint file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.CHK), a set of reserved transaction log files (named RES1.LOG and RES2.LOG), an initial transaction log file (named \<[JET_paramBaseName](./transaction-log-parameters.md)\>.LOG), and a temporary database file (named according to [JET_paramTempPath](./temporary-database-parameters.md)).</span></span> <span data-ttu-id="f05c6-127">Si [JET_paramRecovery](./transaction-log-parameters.md) se establece en "OFF", no se crearán los archivos de registro y de archivo de punto de comprobación.</span><span class="sxs-lookup"><span data-stu-id="f05c6-127">If [JET_paramRecovery](./transaction-log-parameters.md) is set to "Off" then the checkpoint file and log files will not be created.</span></span> <span data-ttu-id="f05c6-128">Si [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) se establece en cero, no se creará el archivo de base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="f05c6-128">If [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) is set to zero then the temporary database file will not be created.</span></span> <span data-ttu-id="f05c6-129">Estos archivos representan el espacio en disco de una instancia y deben administrarse con cuidado.</span><span class="sxs-lookup"><span data-stu-id="f05c6-129">These files represent the on disk footprint of an instance and must be managed with care.</span></span> <span data-ttu-id="f05c6-130">Si estos archivos están dañados individualmente o con respecto a otro, se pueden perder los datos almacenados en las bases de datos asociadas a la instancia.</span><span class="sxs-lookup"><span data-stu-id="f05c6-130">If these files are corrupted individually or with respect to one another then the data stored in the databases associated with the instance may be lost.</span></span>

<span data-ttu-id="f05c6-131">Cuando el motor de base de datos se inicializa con un conjunto existente de archivos de registro de transacciones, se inspeccionarán esos archivos para ver si la anterior encarnación de la instancia sufrió un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f05c6-131">When the database engine is initialized with an existing set of transaction log files then those files will be inspected to see if the previous incarnation of the instance suffered from a crash.</span></span> <span data-ttu-id="f05c6-132">Si se detecta un bloqueo, se realizará automáticamente la recuperación de bloqueos.</span><span class="sxs-lookup"><span data-stu-id="f05c6-132">If a crash is detected then crash recovery will automatically be performed.</span></span> <span data-ttu-id="f05c6-133">Este proceso reconstruirá las bases de datos adjuntas a la instancia durante la versión anterior del motor y guardará los cambios de nuevo en los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="f05c6-133">This process will reconstruct the databases attached to the instance during the previous incarnation of the engine and save the changes back to the database files.</span></span> <span data-ttu-id="f05c6-134">El resultado serán las bases de datos que son coherentes con las transacciones.</span><span class="sxs-lookup"><span data-stu-id="f05c6-134">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="f05c6-135">Es posible que este proceso tarde bastante tiempo si el número de archivos de registro de transacciones que se van a reproducir en las bases de datos es grande.</span><span class="sxs-lookup"><span data-stu-id="f05c6-135">It is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="f05c6-136">Debido al hecho de que **JetInit** realiza la recuperación de bloqueos, es posible que se devuelva casi cualquier error del motor de base de datos en caso de error.</span><span class="sxs-lookup"><span data-stu-id="f05c6-136">Due to the fact that **JetInit** performs crash recovery, it is possible for almost any database engine error to be returned in the event of a failure.</span></span> <span data-ttu-id="f05c6-137">En la práctica, la mayoría de los errores que se han detectado en la implementación de se dividen en dos categorías: daños en los datos y administración de errores de archivos.</span><span class="sxs-lookup"><span data-stu-id="f05c6-137">In practice, most of the errors seen in deployment fall into two categories: data corruption and file mismanagement.</span></span> <span data-ttu-id="f05c6-138">Los datos dañados se manifestarán a menudo en los siguientes errores o similares:</span><span class="sxs-lookup"><span data-stu-id="f05c6-138">Data corruption will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="f05c6-139">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="f05c6-139">JET_errReadVerifyFailure</span></span>

  - <span data-ttu-id="f05c6-140">JET_errLogFileCorrupt</span><span class="sxs-lookup"><span data-stu-id="f05c6-140">JET_errLogFileCorrupt</span></span>

  - <span data-ttu-id="f05c6-141">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="f05c6-141">JET_errCheckpointCorrupt</span></span>

<span data-ttu-id="f05c6-142">Estos errores casi siempre están causados por problemas de hardware y, por tanto, no se pueden evitar.</span><span class="sxs-lookup"><span data-stu-id="f05c6-142">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="f05c6-143">La administración de errores de archivos se manifestará en la mayoría de los casos siguientes o similares:</span><span class="sxs-lookup"><span data-stu-id="f05c6-143">File mismanagement will manifest itself most often in the following or similar errors:</span></span>

  - <span data-ttu-id="f05c6-144">JET_errMissingLogFile</span><span class="sxs-lookup"><span data-stu-id="f05c6-144">JET_errMissingLogFile</span></span>

  - <span data-ttu-id="f05c6-145">JET_errAttachedDatabaseMismatch</span><span class="sxs-lookup"><span data-stu-id="f05c6-145">JET_errAttachedDatabaseMismatch</span></span>

  - <span data-ttu-id="f05c6-146">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f05c6-146">JET_errDatabaseSharingViolation</span></span>

  - <span data-ttu-id="f05c6-147">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="f05c6-147">JET_errInvalidLogSequence</span></span>

<span data-ttu-id="f05c6-148">Si la recuperación se está ejecutando en un conjunto de registros, para el que no todas las bases de datos están presentes (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, se puede usar el JET_ bitReplayIgnoreMissingDB para continuar la recuperación de las bases de datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="f05c6-148">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB can be used to continue recovery for the available databases.</span></span> <span data-ttu-id="f05c6-149">Estos errores son impidebles por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f05c6-149">These errors are preventable by the application.</span></span> <span data-ttu-id="f05c6-150">La aplicación debe tener cuidado de proteger el repositorio de estos archivos contra la manipulación de las fuerzas externas, como el usuario u otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f05c6-150">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="f05c6-151">Si la aplicación desea destruir una instancia por completo, se deben eliminar todos los archivos asociados a la instancia.</span><span class="sxs-lookup"><span data-stu-id="f05c6-151">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="f05c6-152">Entre ellos se incluyen el archivo de punto de comprobación, los archivos de registro de transacciones y cualquier archivo de base de datos asociado a la instancia.</span><span class="sxs-lookup"><span data-stu-id="f05c6-152">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="f05c6-153">La función **JetInit** se comporta de forma diferente, con respecto a los archivos de base de datos adjuntos a la instancia, entre Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f05c6-153">The **JetInit** function behaves differently, with respect to database files attached to the instance, between Windows 2000 and later releases.</span></span>

<span data-ttu-id="f05c6-154">**Windows 2000:**  En Windows 2000, cualquier base de datos asociada a la instancia durante una encarnación anterior de esa instancia permanece adjunta a la instancia después de que **JetInit** se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="f05c6-154">**Windows 2000:**  In Windows 2000, any database attached to the instance during a previous incarnation of that instance remains attached to the instance after **JetInit** completes successfully.</span></span> <span data-ttu-id="f05c6-155">No es necesario llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después de **JetInit** para garantizar el acceso posterior a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f05c6-155">It is not necessary to call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit** to insure later database access.</span></span> <span data-ttu-id="f05c6-156">Si se llama a la función [JetAttachDatabase](./jetattachdatabase-function.md) después de la función **JetInit** , se devolverá la JET_wrnDatabaseAttached ADVERTENCIA.</span><span class="sxs-lookup"><span data-stu-id="f05c6-156">If the [JetAttachDatabase](./jetattachdatabase-function.md) function is called after the **JetInit** function, the JET_wrnDatabaseAttached warning will be returned.</span></span> <span data-ttu-id="f05c6-157">Esta advertencia indica que los datos adjuntos de base de datos se conservaron y se pueden omitir.</span><span class="sxs-lookup"><span data-stu-id="f05c6-157">This warning indicates that the database attachment was preserved and can be ignored.</span></span>

<span data-ttu-id="f05c6-158">**Windows XP:**  En Windows XP y versiones posteriores, todas las bases de datos se desasocian automáticamente de la instancia de **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="f05c6-158">**Windows XP:**  In Windows XP and later releases, all databases are automatically detached from the instance by **JetInit**.</span></span> <span data-ttu-id="f05c6-159">Esto significa que siempre se debe llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después de **JetInit** en este caso.</span><span class="sxs-lookup"><span data-stu-id="f05c6-159">This means that [JetAttachDatabase](./jetattachdatabase-function.md) must always be called after **JetInit** in this case.</span></span>

<span data-ttu-id="f05c6-160">Cualquier aplicación escrita para ejecutarse en Windows 2000 y en versiones posteriores siempre debe llamar a [JetAttachDatabase](./jetattachdatabase-function.md) después de **JetInit**.</span><span class="sxs-lookup"><span data-stu-id="f05c6-160">Any application written to run on Windows 2000 and on later releases must always call [JetAttachDatabase](./jetattachdatabase-function.md) after **JetInit**.</span></span> <span data-ttu-id="f05c6-161">Si la aplicación se ejecuta en Windows 2000, debe esperar ver JET_wrnDatabaseAttached en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="f05c6-161">If the application runs on Windows 2000 then it must expect to see JET_wrnDatabaseAttached in some cases.</span></span> <span data-ttu-id="f05c6-162">Vea [JetAttachDatabase](./jetattachdatabase-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f05c6-162">See [JetAttachDatabase](./jetattachdatabase-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f05c6-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f05c6-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f05c6-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f05c6-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f05c6-165">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f05c6-165">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f05c6-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f05c6-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f05c6-167">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f05c6-167">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f05c6-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f05c6-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f05c6-169">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="f05c6-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f05c6-170"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="f05c6-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f05c6-171">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f05c6-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f05c6-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f05c6-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f05c6-173">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f05c6-173">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f05c6-174">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f05c6-174">See Also</span></span>

[<span data-ttu-id="f05c6-175">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="f05c6-175">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="f05c6-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f05c6-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f05c6-177">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="f05c6-177">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="f05c6-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="f05c6-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="f05c6-179">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="f05c6-179">JET_paramMaxTemporaryTables</span></span>](./temporary-database-parameters.md)  
[<span data-ttu-id="f05c6-180">JET_paramRecovery</span><span class="sxs-lookup"><span data-stu-id="f05c6-180">JET_paramRecovery</span></span>](./transaction-log-parameters.md)  
[<span data-ttu-id="f05c6-181">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="f05c6-181">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="f05c6-182">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="f05c6-182">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="f05c6-183">JetInit3</span><span class="sxs-lookup"><span data-stu-id="f05c6-183">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="f05c6-184">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="f05c6-184">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
