---
description: La sesión de seguimiento de eventos de registradores automáticos registra los eventos que se producen al principio del proceso de arranque del sistema operativo.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configurar e iniciar una sesión de registrador automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b17e7e818193aa4fa316d17a0e4392e41b55dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986138"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="645ce-103">Configurar e iniciar una sesión de registrador automático</span><span class="sxs-lookup"><span data-stu-id="645ce-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="645ce-104">La sesión de seguimiento de eventos de registradores automáticos registra los eventos que se producen al principio del proceso de arranque del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="645ce-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="645ce-105">Las aplicaciones y los controladores de dispositivos pueden usar la sesión del registrador automático para capturar seguimientos antes de que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="645ce-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="645ce-106">Tenga en cuenta que algunos controladores de dispositivos, como los controladores de dispositivos de disco, no se cargan en el momento en que comienza la sesión de registrador automático.</span><span class="sxs-lookup"><span data-stu-id="645ce-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="645ce-107">El registrador automático difiere del registrador global de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="645ce-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="645ce-108">Puede especificar una o más sesiones del registrador automático (el registrador global era una sesión única en la que todos los eventos registraron).</span><span class="sxs-lookup"><span data-stu-id="645ce-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="645ce-109">El registrador automático envía una notificación de habilitación a los proveedores cuando se inicia la sesión (el registrador global no envió una notificación de habilitación a los proveedores, por lo que los proveedores tenían que confiar en otros medios para saber si se inició la sesión del registrador global para empezar a registrar eventos).</span><span class="sxs-lookup"><span data-stu-id="645ce-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="645ce-110">El registrador automático no admite el registro de eventos del registrador del kernel de NT (vea el miembro **EnableFlags** de [**\_ \_ las propiedades de seguimiento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span><span class="sxs-lookup"><span data-stu-id="645ce-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="645ce-111">Para registrar los eventos del registrador del kernel de NT, debe usar el [registrador global](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="645ce-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="645ce-112">Para obtener más información sobre la audiencia global del registrador, vea [configurar e iniciar la sesión del registrador global](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="645ce-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="645ce-113">ETW es compatible con el registrador automático en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="645ce-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="645ce-114">Usar el [registrador global](configuring-and-starting-the-global-logger-session.md) en sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="645ce-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="645ce-115">El registro se utiliza para configurar la sesión del registrador automático.</span><span class="sxs-lookup"><span data-stu-id="645ce-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="645ce-116">Agregue la siguiente clave del registro, si aún no está presente:</span><span class="sxs-lookup"><span data-stu-id="645ce-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="645ce-117">En la clave de **registrador automático** , cree una clave para cada sesión del registrador automático que desee configurar, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="645ce-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="645ce-118">Para cada sesión, cree una clave para cada proveedor que desee habilitar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="645ce-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="645ce-119">Utilice el GUID del proveedor como la clave.</span><span class="sxs-lookup"><span data-stu-id="645ce-119">Use the provider's GUID as the key.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
                  \Logger Session A
                     \{ProviderGuid1}
                     \{ProviderGuid2}
                  \Logger Session B
                  \Logger Session C
```

<span data-ttu-id="645ce-120">En la tabla siguiente se describen los valores que se pueden definir para cada sesión del registrador automático.</span><span class="sxs-lookup"><span data-stu-id="645ce-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="645ce-121">Debe tener privilegios de administrador para especificar estos valores del registro.</span><span class="sxs-lookup"><span data-stu-id="645ce-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="645ce-122">El valor **inicial** y el **GUID** son los únicos valores necesarios para iniciar la sesión del registrador automático; todos los demás valores tienen valores predeterminados que se utilizan si el valor no está presente en el registro.</span><span class="sxs-lookup"><span data-stu-id="645ce-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="645ce-123">Normalmente, se deben usar los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="645ce-123">Typically, you should use the default values.</span></span> <span data-ttu-id="645ce-124">Si especifica un valor que ETW no admite, ETW invalidará el valor.</span><span class="sxs-lookup"><span data-stu-id="645ce-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="645ce-125">Value</span><span class="sxs-lookup"><span data-stu-id="645ce-125">Value</span></span></th>
<th><span data-ttu-id="645ce-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="645ce-126">Type</span></span></th>
<th><span data-ttu-id="645ce-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="645ce-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="645ce-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="645ce-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-130">Tamaño de cada búfer, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="645ce-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="645ce-131">Debe ser inferior a un megabyte.</span><span class="sxs-lookup"><span data-stu-id="645ce-131">Should be less than one megabyte.</span></span> <span data-ttu-id="645ce-132">ETW utiliza el tamaño de la memoria física para calcular este valor.</span><span class="sxs-lookup"><span data-stu-id="645ce-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-133"><strong>ClockType</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="645ce-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-135">Temporizador que se va a usar al registrar la marca de tiempo para cada evento.</span><span class="sxs-lookup"><span data-stu-id="645ce-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="645ce-136">1 = valor del contador de rendimiento (alta resolución)</span><span class="sxs-lookup"><span data-stu-id="645ce-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="645ce-137">2 = temporizador del sistema</span><span class="sxs-lookup"><span data-stu-id="645ce-137">2 = System timer</span></span></li>
<li><span data-ttu-id="645ce-138">3 = contador de ciclo de CPU</span><span class="sxs-lookup"><span data-stu-id="645ce-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="645ce-139">Para obtener una descripción de cada tipo de reloj, vea el miembro <strong>ClientContext</strong> de <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="645ce-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="645ce-140">El valor predeterminado es 1 (valor del contador de rendimiento) en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="645ce-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="645ce-141">Antes de Windows Vista, el valor predeterminado es 2 (temporizador del sistema).</span><span class="sxs-lookup"><span data-stu-id="645ce-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645ce-142"><strong>DisableRealtimePersistence</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="645ce-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-144">Para deshabilitar la persistencia en tiempo real, establezca este valor en 1.</span><span class="sxs-lookup"><span data-stu-id="645ce-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="645ce-145">El valor predeterminado es 0 (habilitado) para las sesiones en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="645ce-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="645ce-146">Si está habilitada la persistencia en tiempo real, se conservarán los eventos en tiempo real que no se hayan entregado en el momento en que se cerró el equipo.</span><span class="sxs-lookup"><span data-stu-id="645ce-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="645ce-147">Los eventos se entregarán al consumidor la próxima vez que el consumidor se conecte a la sesión.</span><span class="sxs-lookup"><span data-stu-id="645ce-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-148"><strong>FileCounter</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="645ce-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-150">No establezca ni modifique este valor.</span><span class="sxs-lookup"><span data-stu-id="645ce-150">Do not set or modify this value.</span></span> <span data-ttu-id="645ce-151">Este valor es el número de serie que se usa para incrementar el nombre del archivo de registro si se especifica <strong>FileMax</strong> .</span><span class="sxs-lookup"><span data-stu-id="645ce-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="645ce-152">Si el valor no es válido, se asumirá 1.</span><span class="sxs-lookup"><span data-stu-id="645ce-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645ce-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="645ce-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="645ce-155">Ruta de acceso completa del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="645ce-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="645ce-156">La ruta de acceso a este archivo debe existir.</span><span class="sxs-lookup"><span data-stu-id="645ce-156">The path to this file must exist.</span></span> <span data-ttu-id="645ce-157">El archivo de registro es un archivo de registro secuencial.</span><span class="sxs-lookup"><span data-stu-id="645ce-157">The log file is a sequential log file.</span></span> <span data-ttu-id="645ce-158">La ruta de acceso está limitada a 1024 caracteres.</span><span class="sxs-lookup"><span data-stu-id="645ce-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="645ce-159">Si no se especifica <strong>filename</strong> , los eventos se escriben en%systemroot%\System32\LogFiles\WMI\ <sessionname> . ETL.</span><span class="sxs-lookup"><span data-stu-id="645ce-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-160"><strong>FileMax</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="645ce-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-162">Número máximo de instancias del archivo de registro que ETW crea.</span><span class="sxs-lookup"><span data-stu-id="645ce-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="645ce-163">Si el archivo de registro especificado en <strong>filename</strong> existe, ETW anexa el valor de <strong>FileCounter</strong> al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="645ce-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="645ce-164">Por ejemplo, si se usa el nombre de archivo de registro predeterminado, el formulario es%SystemRoot%\System32\LogFiles\WMI\ <sessionname> . ETL. NNNN.</span><span class="sxs-lookup"><span data-stu-id="645ce-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\<sessionname>.etl.NNNN.</span></span> <br/> <span data-ttu-id="645ce-165">La primera vez que se inicia el equipo, el nombre de archivo es <sessionname> . ETL. 0001, la segunda vez que el nombre de archivo es <sessionname> . ETL. 0002, etc.</span><span class="sxs-lookup"><span data-stu-id="645ce-165">The first time the computer is started, the file name is <sessionname>.etl.0001, the second time the file name is <sessionname>.etl.0002, and so on.</span></span> <span data-ttu-id="645ce-166">Si <strong>FileMax</strong> es 3, en el cuarto reinicio del equipo, ETW restablece el contador en 1 y sobrescribe <sessionname> . ETL. 0001, si existe.</span><span class="sxs-lookup"><span data-stu-id="645ce-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites <sessionname>.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="645ce-167">El número máximo de instancias del archivo de registro que se admiten es 16.</span><span class="sxs-lookup"><span data-stu-id="645ce-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="645ce-168">No use esta característica con el modo de archivo de registro de <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> .</span><span class="sxs-lookup"><span data-stu-id="645ce-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645ce-169"><strong>FlushTimer</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="645ce-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-171">Frecuencia, en segundos, con la que se eliminan forzosamente los búferes de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="645ce-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="645ce-172">El tiempo mínimo de vaciado es de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="645ce-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="645ce-173">Este vaciado forzado se suma al vaciado automático que se produce cuando un búfer está lleno y cuando se detiene la sesión de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="645ce-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="645ce-174">En el caso de un registrador en tiempo real, un valor de cero (el valor predeterminado) significa que el tiempo de vaciado se establecerá en 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="645ce-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="645ce-175">Un registrador en tiempo real es cuando <strong>LogFileMode</strong> se establece en <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="645ce-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="645ce-176">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="645ce-176">The default value is 0.</span></span> <span data-ttu-id="645ce-177">De forma predeterminada, los búferes se vacían solo cuando están llenos.</span><span class="sxs-lookup"><span data-stu-id="645ce-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-178"><strong>Guid</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="645ce-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="645ce-180">Cadena que contiene un GUID que identifica de forma única la sesión.</span><span class="sxs-lookup"><span data-stu-id="645ce-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="645ce-181">Este valor es necesario.</span><span class="sxs-lookup"><span data-stu-id="645ce-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645ce-182"><strong>LogFileMode</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="645ce-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-184">Especifique uno o más modos de registro.</span><span class="sxs-lookup"><span data-stu-id="645ce-184">Specify one or more log modes.</span></span> <span data-ttu-id="645ce-185">Para ver los valores posibles, consulte <a href="logging-mode-constants.md">constantes del modo de registro</a>.</span><span class="sxs-lookup"><span data-stu-id="645ce-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="645ce-186">El valor predeterminado es <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="645ce-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="645ce-187">En lugar de escribir en un archivo de registro, puede especificar <strong>EVENT_TRACE_BUFFERING_MODE</strong> o <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="645ce-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="645ce-188">La especificación de <strong>EVENT_TRACE_BUFFERING_MODE</strong> evita el costo de vaciar el contenido de la sesión en el disco cuando el sistema de archivos está disponible.</span><span class="sxs-lookup"><span data-stu-id="645ce-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="645ce-189">Tenga en cuenta que el uso de <strong>EVENT_TRACE_BUFFERING_MODE</strong> hará que el sistema omita el valor <strong>MaximumBuffers</strong> , ya que el tamaño del búfer es el producto de <strong>MinimumBuffers</strong> y <strong>BufferSize</strong>.</span><span class="sxs-lookup"><span data-stu-id="645ce-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="645ce-190">Las sesiones del registrador automático no admiten el modo de registro de <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> .</span><span class="sxs-lookup"><span data-stu-id="645ce-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="645ce-191">Si se especifica <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> , <strong>BufferSize</strong> se debe proporcionar explícitamente y debe ser el mismo tanto en el registrador como en el archivo que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="645ce-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-192"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="645ce-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-194">Tamaño máximo de archivo del archivo de registro, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="645ce-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="645ce-195">La sesión se cierra cuando se alcanza el tamaño máximo, a menos que esté en modo de archivo de registro circular.</span><span class="sxs-lookup"><span data-stu-id="645ce-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="645ce-196">Para no especificar ningún límite, establezca el valor en 0.</span><span class="sxs-lookup"><span data-stu-id="645ce-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="645ce-197">El valor predeterminado es 100 MB, si no se establece.</span><span class="sxs-lookup"><span data-stu-id="645ce-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="645ce-198">El comportamiento que se produce cuando se alcanza el tamaño máximo de archivo depende del valor de <strong>LogFileMode</strong>.</span><span class="sxs-lookup"><span data-stu-id="645ce-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645ce-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="645ce-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-201">Número máximo de búferes que se van a asignar.</span><span class="sxs-lookup"><span data-stu-id="645ce-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="645ce-202">Normalmente, este valor es el número mínimo de búferes más veinte.</span><span class="sxs-lookup"><span data-stu-id="645ce-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="645ce-203">ETW usa el tamaño de búfer y el tamaño de la memoria física para calcular este valor.</span><span class="sxs-lookup"><span data-stu-id="645ce-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="645ce-204">Este valor debe ser mayor o igual que el valor de <strong>MinimumBuffers</strong>.</span><span class="sxs-lookup"><span data-stu-id="645ce-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="645ce-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-207">Número mínimo de búferes que se van a asignar en el inicio.</span><span class="sxs-lookup"><span data-stu-id="645ce-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="645ce-208">El número mínimo de búferes que se pueden especificar es de dos búferes por procesador.</span><span class="sxs-lookup"><span data-stu-id="645ce-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="645ce-209">Por ejemplo, en un equipo con un solo procesador, el número mínimo de búferes es dos.</span><span class="sxs-lookup"><span data-stu-id="645ce-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645ce-210"><strong>Iniciar</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="645ce-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-212">Para que la sesión del registrador automático se inicie la próxima vez que se reinicie el equipo, establezca este valor en 1; en caso contrario, establezca este valor en 0.</span><span class="sxs-lookup"><span data-stu-id="645ce-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-213"><strong>Estado</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="645ce-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-215">El estado de inicio del registrador automático.</span><span class="sxs-lookup"><span data-stu-id="645ce-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="645ce-216">Si no se pudo iniciar el registrador automático, el valor de esta clave es el código de error de Win32 adecuado.</span><span class="sxs-lookup"><span data-stu-id="645ce-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="645ce-217">Si el registrador automático se inició correctamente, el valor de esta clave es <strong>ERROR_SUCCESS</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="645ce-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="645ce-218">En la tabla siguiente se describen los valores que puede definir para cada proveedor que desea habilitar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="645ce-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="645ce-219">Debe tener privilegios de administrador para especificar estos valores del registro.</span><span class="sxs-lookup"><span data-stu-id="645ce-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="645ce-220">Si especifica un valor que ETW no admite, ETW invalidará el valor.</span><span class="sxs-lookup"><span data-stu-id="645ce-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="645ce-221">Value</span><span class="sxs-lookup"><span data-stu-id="645ce-221">Value</span></span></th>
<th><span data-ttu-id="645ce-222">Tipo</span><span class="sxs-lookup"><span data-stu-id="645ce-222">Type</span></span></th>
<th><span data-ttu-id="645ce-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="645ce-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="645ce-224"><strong>Enabled</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="645ce-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-226">Determina si el proveedor está habilitado.</span><span class="sxs-lookup"><span data-stu-id="645ce-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="645ce-227">Para habilitar el proveedor, establezca este valor en 1.</span><span class="sxs-lookup"><span data-stu-id="645ce-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="645ce-228">Para deshabilitar el proveedor, establezca este valor en 0.</span><span class="sxs-lookup"><span data-stu-id="645ce-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="645ce-229">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="645ce-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-230"><strong>EnableFlags</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="645ce-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-232">Valor definido por el proveedor que especifica la clase de eventos para los que el proveedor genera eventos.</span><span class="sxs-lookup"><span data-stu-id="645ce-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="645ce-233">Para obtener más información, consulte el parámetro <em>EnableFlags</em> de la función <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="645ce-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="645ce-234">Especifique este nombre de valor si el proveedor no admite <strong>MatchAnyKeyword</strong> o <strong>MatchAllKeyword</strong>.</span><span class="sxs-lookup"><span data-stu-id="645ce-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645ce-235"><strong>EnableLevel</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="645ce-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-237">Valor definido por el proveedor que especifica el nivel de detalle incluido en el evento.</span><span class="sxs-lookup"><span data-stu-id="645ce-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="645ce-238">Por ejemplo, puede usar este valor para indicar el nivel de gravedad de los eventos (informativo, ADVERTENCIA, error) que genera el proveedor.</span><span class="sxs-lookup"><span data-stu-id="645ce-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="645ce-239">Para obtener una lista de niveles predefinidos, vea el parámetro <em>LEVEL</em> de la función <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="645ce-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-240"><strong>EnableProperty</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="645ce-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-242">Use este valor para incluir uno o varios de los siguientes elementos en el archivo de registro:</span><span class="sxs-lookup"><span data-stu-id="645ce-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="645ce-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = incluir en los datos extendidos el identificador de seguridad (SID) del usuario.</span><span class="sxs-lookup"><span data-stu-id="645ce-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="645ce-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = incluir en los datos extendidos el identificador de la sesión de terminal.</span><span class="sxs-lookup"><span data-stu-id="645ce-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="645ce-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = incluir en los datos extendidos seguimiento de la pila de llamadas para los eventos escritos mediante <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="645ce-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="645ce-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtra todos los eventos que no tienen una palabra clave distinta de cero especificada.</span><span class="sxs-lookup"><span data-stu-id="645ce-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="645ce-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = indica que esta llamada a <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> debe habilitar un <a href="provider-traits.md">grupo de proveedores</a> en lugar de un proveedor de eventos individual.</span><span class="sxs-lookup"><span data-stu-id="645ce-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="645ce-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = incluir la clave de inicio del proceso en los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="645ce-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="645ce-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = incluir la clave de evento en los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="645ce-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="645ce-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtra todos los eventos que están marcados como eventos InPrivate o provienen de un proceso marcado como InPrivate.</span><span class="sxs-lookup"><span data-stu-id="645ce-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="645ce-251">Para obtener más información sobre estos elementos, vea <strong>EnableProperty</strong> de la estructura <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="645ce-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="645ce-252"><strong>MatchAnyKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="645ce-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-254">Máscara de claves de palabras clave que determinan la categoría de eventos que desea que el proveedor escriba.</span><span class="sxs-lookup"><span data-stu-id="645ce-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="645ce-255">El proveedor escribe el evento si cualquiera de los bits de la palabra clave del evento coincide con cualquiera de los bits establecidos en esta máscara.</span><span class="sxs-lookup"><span data-stu-id="645ce-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="645ce-256">Para especificar que el proveedor escriba todos los eventos, establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="645ce-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="645ce-257">Para obtener un ejemplo, vea la sección Comentarios de la función <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="645ce-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="645ce-258"><strong>MatchAllKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="645ce-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="645ce-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="645ce-260">Esta máscara de máscara es opcional.</span><span class="sxs-lookup"><span data-stu-id="645ce-260">This bitmask is optional.</span></span> <span data-ttu-id="645ce-261">Esta máscara restringe aún más la categoría de eventos que desea que escriba el proveedor.</span><span class="sxs-lookup"><span data-stu-id="645ce-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="645ce-262">Si la palabra clave del evento cumple la condición <em>MatchAnyKeyword</em> , el proveedor escribirá el evento solo si todos los bits de esta máscara existen en la palabra clave del evento.</span><span class="sxs-lookup"><span data-stu-id="645ce-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="645ce-263">Esta máscara no se usa si <em>MatchAnyKeyword</em> es cero.</span><span class="sxs-lookup"><span data-stu-id="645ce-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="645ce-264">Para obtener un ejemplo, vea la sección Comentarios de la función <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="645ce-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="645ce-265">Una vez que se haya modificado el registro, la sesión del registrador automático se iniciará la próxima vez que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="645ce-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="645ce-266">La sesión del registrador automático llama a la función [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar los proveedores.</span><span class="sxs-lookup"><span data-stu-id="645ce-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="645ce-267">Las sesiones del registrador automático aumentan el tiempo de arranque del sistema y deben usarse con moderación.</span><span class="sxs-lookup"><span data-stu-id="645ce-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="645ce-268">Los servicios que deseen capturar información durante el proceso de arranque deben considerar la posibilidad de agregar la lógica del controlador a sí misma en lugar de utilizar la sesión del registrador automático.</span><span class="sxs-lookup"><span data-stu-id="645ce-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="645ce-269">Para detener una sesión del registrador automático, llame a la función [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) .</span><span class="sxs-lookup"><span data-stu-id="645ce-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="645ce-270">El nombre de sesión que se pasa a la función es el nombre de la clave del registro que se usó para definir la sesión en el registro.</span><span class="sxs-lookup"><span data-stu-id="645ce-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="645ce-271">En Windows 8.1, Windows Server 2012 R2 y versiones posteriores, los filtros de carga de eventos, ámbito y recorrido de pila se pueden usar con la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras de [**habilitar \_ \_ parámetros de seguimiento**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**\_ \_ descriptor de filtro de eventos**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) para filtrar según condiciones específicas en una sesión del registrador.</span><span class="sxs-lookup"><span data-stu-id="645ce-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="645ce-272">Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , así como las estructuras de [**\_ \_ predicado**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **habilitar \_ \_ parámetros de seguimiento**, **\_ \_ descriptor de filtro de eventos** y filtro de carga.</span><span class="sxs-lookup"><span data-stu-id="645ce-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="645ce-273">Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [configurar e iniciar una sesión de seguimiento de eventos](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="645ce-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="645ce-274">Para obtener información detallada sobre cómo iniciar una sesión de registrador privada, vea [configurar e iniciar una sesión de registrador privado](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="645ce-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="645ce-275">Para obtener información detallada sobre cómo iniciar una sesión del registrador del kernel de NT, vea [configurar e iniciar la sesión del registrador del kernel de NT](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="645ce-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="645ce-276">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="645ce-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="645ce-277">Configurar e iniciar una sesión de registrador privado</span><span class="sxs-lookup"><span data-stu-id="645ce-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="645ce-278">Configurar e iniciar una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="645ce-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="645ce-279">Configurar e iniciar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="645ce-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="645ce-280">Configuración e inicio de la sesión del registrador del kernel de NT</span><span class="sxs-lookup"><span data-stu-id="645ce-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="645ce-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="645ce-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="645ce-282">**HABILITAR \_ parámetros de seguimiento \_**</span><span class="sxs-lookup"><span data-stu-id="645ce-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="645ce-283">**descriptor de filtro de eventos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="645ce-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="645ce-284">**\_predicado de filtro de carga \_**</span><span class="sxs-lookup"><span data-stu-id="645ce-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="645ce-285">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="645ce-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="645ce-286">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="645ce-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="645ce-287">Actualizar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="645ce-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
