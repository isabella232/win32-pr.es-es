---
description: 'Más información sobre: parámetros de e/s'
title: Parámetros de e/s
TOCTitle: I/O Parameters
ms:assetid: 5df3c106-52ac-4ca0-9a6a-d5d62576bb23
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269260(v=EXCHG.10)
ms:contentKeyID: 32765562
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ba0e89602f7e5d4b9df395e89c73c8dc735692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811641"
---
# <a name="io-parameters"></a><span data-ttu-id="74f78-103">Parámetros de e/s</span><span class="sxs-lookup"><span data-stu-id="74f78-103">I/O Parameters</span></span>


<span data-ttu-id="74f78-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="74f78-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="io-parameters"></a><span data-ttu-id="74f78-105">Parámetros de e/s</span><span class="sxs-lookup"><span data-stu-id="74f78-105">I/O Parameters</span></span>

<span data-ttu-id="74f78-106">Este tema contiene los parámetros que se usan para la entrada y salida (e/s).</span><span class="sxs-lookup"><span data-stu-id="74f78-106">This topic contains parameters that are used for input and output (I/O).</span></span>

<span data-ttu-id="74f78-107">*JET_paramAccessDeniedRetryPeriod*</span><span class="sxs-lookup"><span data-stu-id="74f78-107">*JET_paramAccessDeniedRetryPeriod*</span></span>  
<span data-ttu-id="74f78-108">53</span><span class="sxs-lookup"><span data-stu-id="74f78-108">53</span></span>  

<span data-ttu-id="74f78-109">**Windows XP y versiones posteriores:**  Este parámetro configura el tiempo (en milisegundos) que el motor de base de datos utilizará para tener acceso a un archivo bloqueado antes de que se produzca un error con JET_errFileAccessDenied.</span><span class="sxs-lookup"><span data-stu-id="74f78-109">**Windows XP and later:**  This parameter configures the duration of time (in milliseconds) that the database engine will use to access a file that is locked before failing with JET_errFileAccessDenied.</span></span> <span data-ttu-id="74f78-110">Este retardo está diseñado para evitar el software antivirus que puede contener algunos de los archivos del motor de base de datos abiertos brevemente una vez cerrados.</span><span class="sxs-lookup"><span data-stu-id="74f78-110">This time delay is designed to work around anti-virus software that may hold some of the database engine's files open briefly after they are closed.</span></span>

<span data-ttu-id="74f78-111">**Nota:**  Como resultado de la lógica de reintento anterior, cualquier intento de adjuntar a una base de datos o usar un archivo de registro que ya esté en uso por el motor de base de datos producirá un retraso de este tamaño antes de que la llamada API devuelva un error (legítimo).</span><span class="sxs-lookup"><span data-stu-id="74f78-111">**Note**  As a result of the above retry logic, any attempt to attach to a database or use a log file that is already in use by the database engine will result in a delay of this size before the API call returns a (legitimate) failure.</span></span> <span data-ttu-id="74f78-112">Este parámetro se puede usar para desactivar ese retraso en caso de que se trate de un escenario común.</span><span class="sxs-lookup"><span data-stu-id="74f78-112">This parameter can be used to turn down that delay in case this is a common scenario.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-113">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-113">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-114">10000</span><span class="sxs-lookup"><span data-stu-id="74f78-114">10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-115">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-115">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-116">Entero</span><span class="sxs-lookup"><span data-stu-id="74f78-116">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-117">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-117">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-118">de 0 a 4294967295</span><span class="sxs-lookup"><span data-stu-id="74f78-118">0 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-119">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-119">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-120">Global</span><span class="sxs-lookup"><span data-stu-id="74f78-120">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-121">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-121">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-122">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-122">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-123">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-123">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-124">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-124">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-125">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-125">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-126">No</span><span class="sxs-lookup"><span data-stu-id="74f78-126">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-127">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-127">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-128">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-128">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-129">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-129">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-130">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-130">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-131">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-131">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-132">No</span><span class="sxs-lookup"><span data-stu-id="74f78-132">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-133">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-133">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-134">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74f78-134">Windows XP and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74f78-135">*JET_paramCreatePathIfNotExist*</span><span class="sxs-lookup"><span data-stu-id="74f78-135">*JET_paramCreatePathIfNotExist*</span></span>  
<span data-ttu-id="74f78-136">100</span><span class="sxs-lookup"><span data-stu-id="74f78-136">100</span></span>  

<span data-ttu-id="74f78-137">Cuando este parámetro se establece en true, cualquier carpeta que no se encuentre en una ruta de acceso del sistema de archivos utilizada por el motor de base de datos se creará en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="74f78-137">When this parameter is set to true then any folder that is missing in a file system path in use by the database engine will be silently created.</span></span> <span data-ttu-id="74f78-138">De lo contrario, se producirá un error en la operación que utiliza la ruta de acceso del sistema de archivos que faltan con JET_errInvalidPath.</span><span class="sxs-lookup"><span data-stu-id="74f78-138">Otherwise, the operation that uses the missing file system path will fail with JET_errInvalidPath.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-139">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-140">False</span><span class="sxs-lookup"><span data-stu-id="74f78-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-141">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="74f78-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-143">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-144">False, True</span><span class="sxs-lookup"><span data-stu-id="74f78-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-145">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-146">Instancia</span><span class="sxs-lookup"><span data-stu-id="74f78-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-147">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-148">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-149">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-150">No</span><span class="sxs-lookup"><span data-stu-id="74f78-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-151">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-152">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-153">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-154">No</span><span class="sxs-lookup"><span data-stu-id="74f78-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-155">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-156">No</span><span class="sxs-lookup"><span data-stu-id="74f78-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-157">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-158">No</span><span class="sxs-lookup"><span data-stu-id="74f78-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-159">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-160">All</span><span class="sxs-lookup"><span data-stu-id="74f78-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74f78-161">*JET_paramEnableFileCache*</span><span class="sxs-lookup"><span data-stu-id="74f78-161">*JET_paramEnableFileCache*</span></span>  
<span data-ttu-id="74f78-162">126</span><span class="sxs-lookup"><span data-stu-id="74f78-162">126</span></span>  

<span data-ttu-id="74f78-163">Cuando este parámetro es **true**, el motor de base de datos utilizará la caché de archivos de Windows como caché de lectura para todos sus archivos.</span><span class="sxs-lookup"><span data-stu-id="74f78-163">When this parameter is **True**, the database engine will use the Windows file cache as a read cache for all of its various files.</span></span> <span data-ttu-id="74f78-164">También lo usará como caché de escritura para la base de datos temporal o para las bases de datos que se abren con la recuperación deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="74f78-164">It will also use it as a write cache for the temporary database or for databases that are opened with recovery disabled.</span></span> <span data-ttu-id="74f78-165">El motor de base de datos debe deshabilitar el almacenamiento en caché de escritura para las bases de datos normales, los archivos de registro de transacciones y los archivos de punto de comprobación para proteger la integridad transaccional de las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="74f78-165">The database engine must disable write caching for ordinary databases, transaction log files, and checkpoint files to protect the transactional integrity of the databases.</span></span>

<span data-ttu-id="74f78-166">Es importante tener en cuenta que el uso de la caché de archivos de Windows agregará una segunda disposición en capas del almacenamiento en caché para los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="74f78-166">It is important to note that the use of the Windows file cache will add a second layering of caching for database files.</span></span> <span data-ttu-id="74f78-167">La caché de base de datos seguirá usando su propia memoria para almacenar en caché los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="74f78-167">The database cache will still use its own memory to cache the database files.</span></span> <span data-ttu-id="74f78-168">La intención de este modo es permitir a la aplicación configurar el motor de base de datos con una pequeña memoria caché dedicada y permitir que Windows condone memoria reservada para mejorar aún más el almacenamiento en caché de los datos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="74f78-168">The intent of this mode is to allow the application to configure the database engine with a small dedicated cache and to allow Windows to donate spare memory to further improve the caching of database data.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-169">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-170">False</span><span class="sxs-lookup"><span data-stu-id="74f78-170">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-171">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="74f78-172">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-173">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-174">False, True</span><span class="sxs-lookup"><span data-stu-id="74f78-174">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-175">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-176">Global</span><span class="sxs-lookup"><span data-stu-id="74f78-176">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-177">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-178">No</span><span class="sxs-lookup"><span data-stu-id="74f78-178">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-179">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-180">No</span><span class="sxs-lookup"><span data-stu-id="74f78-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-181">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-182">No</span><span class="sxs-lookup"><span data-stu-id="74f78-182">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-183">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-184">No</span><span class="sxs-lookup"><span data-stu-id="74f78-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-185">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-186">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-187">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-188">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-188">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-189">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-190">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="74f78-190">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74f78-191">*JET_paramIOPriority*</span><span class="sxs-lookup"><span data-stu-id="74f78-191">*JET_paramIOPriority*</span></span>  
<span data-ttu-id="74f78-192">152</span><span class="sxs-lookup"><span data-stu-id="74f78-192">152</span></span>  

<span data-ttu-id="74f78-193">Este parámetro controla el modo en que ESE controla las operaciones de e/s.</span><span class="sxs-lookup"><span data-stu-id="74f78-193">This parameter controls how ESE handles I/O operations.</span></span> <span data-ttu-id="74f78-194">Los valores se pueden establecer en 0 (JET_IOPriorityNormal) para el funcionamiento normal o en 1 (JET_IOPriorityLow) para una operación de prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="74f78-194">The values can be set to 0 (JET_IOPriorityNormal) for normal operation, or 1 (JET_IOPriorityLow) for low priority operation.</span></span> <span data-ttu-id="74f78-195">Cuando la prioridad se establece en JET_IOPriorityLow, ESE usa la nueva funcionalidad de prioridad de e/s de subprocesos disponible en Windows Vista para reducir la prioridad de e/s en el subproceso, de modo que las operaciones de e/s posteriores se emitan en la nueva prioridad baja.</span><span class="sxs-lookup"><span data-stu-id="74f78-195">When the priority is set to JET_IOPriorityLow, ESE uses the new thread I/O priority functionality available in Windows Vista to reduce the I/O priority on the thread so that subsequent I/O operations are issued at the new low priority.</span></span>

<span data-ttu-id="74f78-196">**Windows Vista:**  JET_paramIOPriority se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="74f78-196">**Windows Vista:**  JET_paramIOPriority is introduced in Windows Vista.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-197">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-197">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-198">0</span><span class="sxs-lookup"><span data-stu-id="74f78-198">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-199">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-199">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-200">Entero</span><span class="sxs-lookup"><span data-stu-id="74f78-200">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-201">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-201">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-202">0 - 1</span><span class="sxs-lookup"><span data-stu-id="74f78-202">0 - 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-203">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-203">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-204">Instancia</span><span class="sxs-lookup"><span data-stu-id="74f78-204">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-205">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-205">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-206">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-206">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-207">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-207">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-208">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-208">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-209">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-209">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-210">No</span><span class="sxs-lookup"><span data-stu-id="74f78-210">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-211">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-211">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-212">No</span><span class="sxs-lookup"><span data-stu-id="74f78-212">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-213">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-213">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-214">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-214">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-215">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-215">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-216">No</span><span class="sxs-lookup"><span data-stu-id="74f78-216">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-217">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-217">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74f78-218">Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74f78-219">*JET_paramOutstandingIOMax*</span><span class="sxs-lookup"><span data-stu-id="74f78-219">*JET_paramOutstandingIOMax*</span></span>  
<span data-ttu-id="74f78-220">30</span><span class="sxs-lookup"><span data-stu-id="74f78-220">30</span></span> 

<span data-ttu-id="74f78-221">Este parámetro controla el número de operaciones de e/s de archivos de base de datos que se pueden poner en cola en el sistema operativo host al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="74f78-221">This parameter controls how many database file I/Os can be queued in the host operating system at one time.</span></span>

<span data-ttu-id="74f78-222">Un valor mayor para este parámetro puede ayudar significativamente al rendimiento de una aplicación de base de datos grande.</span><span class="sxs-lookup"><span data-stu-id="74f78-222">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="74f78-223">**Windows XP y Windows Server 2003:**  Este parámetro se omite en Windows XP y Windows Server 2003 y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="74f78-223">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-224">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-224">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-225"><strong>Windows 2000: </strong>  64</span><span class="sxs-lookup"><span data-stu-id="74f78-225"><strong>Windows 2000: </strong>  64</span></span></p>
<p><span data-ttu-id="74f78-226"><strong>Windows Vista:</strong>   1024</span><span class="sxs-lookup"><span data-stu-id="74f78-226"><strong>Windows Vista:</strong>   1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-227">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-227">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-228">Entero</span><span class="sxs-lookup"><span data-stu-id="74f78-228">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-229">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-229">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-230"><strong>Windows 2000:</strong>  8 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="74f78-230"><strong>Windows 2000:</strong>  8 – 2147483647</span></span></p>
<p><span data-ttu-id="74f78-231"><strong>Windows Vista:</strong>  0 – 65536</span><span class="sxs-lookup"><span data-stu-id="74f78-231"><strong>Windows Vista:</strong>  0 – 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-232">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-232">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-233">Global</span><span class="sxs-lookup"><span data-stu-id="74f78-233">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-234">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-234">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-235">No</span><span class="sxs-lookup"><span data-stu-id="74f78-235">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-236">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-236">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-237">No</span><span class="sxs-lookup"><span data-stu-id="74f78-237">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-238">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-238">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-239">No</span><span class="sxs-lookup"><span data-stu-id="74f78-239">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-240">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-240">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-241">No</span><span class="sxs-lookup"><span data-stu-id="74f78-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-242">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-242">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-243">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-243">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-244">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-244">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-245">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-246">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-246">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-247">All</span><span class="sxs-lookup"><span data-stu-id="74f78-247">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74f78-248">*JET_paramMaxCoalesceReadSize*</span><span class="sxs-lookup"><span data-stu-id="74f78-248">*JET_paramMaxCoalesceReadSize*</span></span>  
<span data-ttu-id="74f78-249">164</span><span class="sxs-lookup"><span data-stu-id="74f78-249">164</span></span>  

<span data-ttu-id="74f78-250">Número máximo de bytes que se pueden agrupar para una operación de lectura fusionada.</span><span class="sxs-lookup"><span data-stu-id="74f78-250">Maximum number of bytes that can be grouped for a coalesced read operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-251">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-251">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-252">262 144</span><span class="sxs-lookup"><span data-stu-id="74f78-252">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-253">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-253">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-254">Entero</span><span class="sxs-lookup"><span data-stu-id="74f78-254">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-255">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-255">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-256">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="74f78-256">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-257">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-257">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-258">Global</span><span class="sxs-lookup"><span data-stu-id="74f78-258">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-259">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-259">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-260">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-260">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-261">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-261">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-262">No</span><span class="sxs-lookup"><span data-stu-id="74f78-262">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-263">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-263">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-264">No</span><span class="sxs-lookup"><span data-stu-id="74f78-264">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-265">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-265">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-266">No</span><span class="sxs-lookup"><span data-stu-id="74f78-266">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-267">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-267">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-268">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-268">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-269">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-269">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-270">No</span><span class="sxs-lookup"><span data-stu-id="74f78-270">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-271">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-271">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-272">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74f78-272">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74f78-273">*JET_paramMaxCoalesceWriteSize*</span><span class="sxs-lookup"><span data-stu-id="74f78-273">*JET_paramMaxCoalesceWriteSize*</span></span>  
<span data-ttu-id="74f78-274">165</span><span class="sxs-lookup"><span data-stu-id="74f78-274">165</span></span>  

<span data-ttu-id="74f78-275">Número máximo de bytes que se pueden agrupar para una operación de escritura fusionada.</span><span class="sxs-lookup"><span data-stu-id="74f78-275">Maximum number of bytes that can be grouped for a coalesced write operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-276">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-276">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-277">393216</span><span class="sxs-lookup"><span data-stu-id="74f78-277">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-278">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-278">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-279">Entero</span><span class="sxs-lookup"><span data-stu-id="74f78-279">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-280">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-280">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-281">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="74f78-281">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-282">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-282">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-283">Global</span><span class="sxs-lookup"><span data-stu-id="74f78-283">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-284">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-284">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-285">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-285">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-286">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-286">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-287">No</span><span class="sxs-lookup"><span data-stu-id="74f78-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-288">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-288">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-289">No</span><span class="sxs-lookup"><span data-stu-id="74f78-289">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-290">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-290">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-291">No</span><span class="sxs-lookup"><span data-stu-id="74f78-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-292">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-292">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-293">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-293">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-294">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-294">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-295">No</span><span class="sxs-lookup"><span data-stu-id="74f78-295">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-296">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-296">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-297">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74f78-297">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74f78-298">*JET_paramMaxCoalesceReadGapSize*</span><span class="sxs-lookup"><span data-stu-id="74f78-298">*JET_paramMaxCoalesceReadGapSize*</span></span>  
<span data-ttu-id="74f78-299">166</span><span class="sxs-lookup"><span data-stu-id="74f78-299">166</span></span>  

<span data-ttu-id="74f78-300">Número máximo de bytes que se pueden espaciar para una operación de e/s de escritura fusionada.</span><span class="sxs-lookup"><span data-stu-id="74f78-300">Maximum number of bytes that can be gapped for a coalesced write I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-301">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-301">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-302">262 144</span><span class="sxs-lookup"><span data-stu-id="74f78-302">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-303">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-303">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-304">Entero</span><span class="sxs-lookup"><span data-stu-id="74f78-304">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-305">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-305">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-306">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="74f78-306">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-307">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-307">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-308">Global</span><span class="sxs-lookup"><span data-stu-id="74f78-308">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-309">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-309">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-310">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-310">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-311">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-311">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-312">No</span><span class="sxs-lookup"><span data-stu-id="74f78-312">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-313">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-313">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-314">No</span><span class="sxs-lookup"><span data-stu-id="74f78-314">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-315">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-315">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-316">No</span><span class="sxs-lookup"><span data-stu-id="74f78-316">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-317">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-317">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-318">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-318">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-319">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-319">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-320">No</span><span class="sxs-lookup"><span data-stu-id="74f78-320">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-321">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-321">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-322">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74f78-322">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74f78-323">*JET_paramMaxCoalesceWriteGapSize*</span><span class="sxs-lookup"><span data-stu-id="74f78-323">*JET_paramMaxCoalesceWriteGapSize*</span></span>  
<span data-ttu-id="74f78-324">167</span><span class="sxs-lookup"><span data-stu-id="74f78-324">167</span></span>  

<span data-ttu-id="74f78-325">Número máximo de bytes que se pueden espaciar para una operación de e/s de lectura fusionada.</span><span class="sxs-lookup"><span data-stu-id="74f78-325">Max number of bytes that can be gapped for a coalesced read I/O operation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-326">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="74f78-326">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="74f78-327">393216</span><span class="sxs-lookup"><span data-stu-id="74f78-327">393216</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-328">Escriba:</span><span class="sxs-lookup"><span data-stu-id="74f78-328">Type:</span></span></p></td>
<td><p><span data-ttu-id="74f78-329">Entero</span><span class="sxs-lookup"><span data-stu-id="74f78-329">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-330">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="74f78-330">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="74f78-331">0-1073741824</span><span class="sxs-lookup"><span data-stu-id="74f78-331">0-1073741824</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-332">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="74f78-332">Scope:</span></span></p></td>
<td><p><span data-ttu-id="74f78-333">Global</span><span class="sxs-lookup"><span data-stu-id="74f78-333">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-334">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-334">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-335">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-335">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-336">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="74f78-336">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="74f78-337">No</span><span class="sxs-lookup"><span data-stu-id="74f78-337">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-338">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="74f78-338">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="74f78-339">No</span><span class="sxs-lookup"><span data-stu-id="74f78-339">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-340">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-340">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-341">No</span><span class="sxs-lookup"><span data-stu-id="74f78-341">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-342">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="74f78-342">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="74f78-343">Sí</span><span class="sxs-lookup"><span data-stu-id="74f78-343">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-344">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="74f78-344">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="74f78-345">No</span><span class="sxs-lookup"><span data-stu-id="74f78-345">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-346">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="74f78-346">Availability:</span></span></p></td>
<td><p><span data-ttu-id="74f78-347">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74f78-347">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="74f78-348">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74f78-348">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f78-349"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="74f78-349"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="74f78-350">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="74f78-350">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f78-351"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="74f78-351"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="74f78-352">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="74f78-352">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f78-353"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="74f78-353"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="74f78-354">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="74f78-354">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="74f78-355">Consulte también</span><span class="sxs-lookup"><span data-stu-id="74f78-355">See Also</span></span>

[<span data-ttu-id="74f78-356">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="74f78-356">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="74f78-357">JetInit</span><span class="sxs-lookup"><span data-stu-id="74f78-357">JetInit</span></span>](./jetinit-function.md)
