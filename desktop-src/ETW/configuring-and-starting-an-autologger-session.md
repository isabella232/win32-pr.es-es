---
description: La sesión de seguimiento de eventos de AutoLogger registra los eventos que se producen al principio del proceso de arranque del sistema operativo.
ms.assetid: df5a79f4-abbf-4b83-afc3-cbd14b166067
title: Configuración e inicio de una sesión de Registrador automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6560aece87506b1d064981ee5f49a56bbf0da19e
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102044"
---
# <a name="configuring-and-starting-an-autologger-session"></a><span data-ttu-id="f413c-103">Configuración e inicio de una sesión de Registrador automático</span><span class="sxs-lookup"><span data-stu-id="f413c-103">Configuring and Starting an AutoLogger Session</span></span>

<span data-ttu-id="f413c-104">La sesión de seguimiento de eventos de AutoLogger registra los eventos que se producen al principio del proceso de arranque del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f413c-104">The AutoLogger event tracing session records events that occur early in the operating system boot process.</span></span> <span data-ttu-id="f413c-105">Las aplicaciones y los controladores de dispositivos pueden usar la sesión de AutoLogger para capturar seguimientos antes de que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="f413c-105">Applications and device drivers can use the AutoLogger session to capture traces before the user logs in.</span></span> <span data-ttu-id="f413c-106">Tenga en cuenta que algunos controladores de dispositivo, como los controladores de dispositivos de disco, no se cargan en el momento en que comienza la sesión del registrador automático.</span><span class="sxs-lookup"><span data-stu-id="f413c-106">Note that some device drivers, such as disk device drivers, are not loaded at the time the AutoLogger session begins.</span></span>

<span data-ttu-id="f413c-107">El registrador automático difiere del registrador global de las maneras siguientes:</span><span class="sxs-lookup"><span data-stu-id="f413c-107">The AutoLogger differs from the Global Logger in the following ways:</span></span>

-   <span data-ttu-id="f413c-108">Puede especificar una o varias sesiones de AutoLogger (el registrador global era una sesión única en la que todos los usuarios registraron eventos).</span><span class="sxs-lookup"><span data-stu-id="f413c-108">You can specify one or more AutoLogger sessions (the Global Logger was a single session to which everyone logged events).</span></span>
-   <span data-ttu-id="f413c-109">El registrador automático envía una notificación de habilitación a los proveedores cuando se inicia la sesión (el registrador global no envió una notificación de habilitación a los proveedores, por lo que los proveedores tenían que basarse en otros medios para saber si se inició la sesión del registrador global para iniciar el registro de eventos).</span><span class="sxs-lookup"><span data-stu-id="f413c-109">The AutoLogger sends an enable notification to the providers when the session starts (the Global Logger did not send an enable notification to the providers, so the providers had to rely on other means to know if the Global Logger session was started in order to begin logging events).</span></span>
-   <span data-ttu-id="f413c-110">El registrador automático no admite el registro de eventos del registrador de kernel de NT (vea el **miembro EnableFlags** de [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span><span class="sxs-lookup"><span data-stu-id="f413c-110">The AutoLogger does not support logging NT Kernel Logger events (see the **EnableFlags** member of [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)).</span></span> <span data-ttu-id="f413c-111">Para registrar eventos del registrador de kernel de NT, debe usar [el registrador global](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="f413c-111">To log NT Kernel Logger events, you must use the [Global Logger](configuring-and-starting-the-global-logger-session.md).</span></span>

<span data-ttu-id="f413c-112">Para obtener más información sobre la consulta del registrador global, vea [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="f413c-112">For more information on the Global Logger seesion, see [Configuring and Starting the Global Logger Session](configuring-and-starting-the-global-logger-session.md).</span></span>

> [!Note]  
> <span data-ttu-id="f413c-113">ETW admite AutoLogger en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f413c-113">ETW supports the AutoLogger on Windows Vista and later.</span></span> <span data-ttu-id="f413c-114">Use el [registrador global en](configuring-and-starting-the-global-logger-session.md) sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="f413c-114">Use the [Global Logger](configuring-and-starting-the-global-logger-session.md) on earlier operating systems.</span></span>

 

<span data-ttu-id="f413c-115">Use el Registro para configurar la sesión de AutoLogger.</span><span class="sxs-lookup"><span data-stu-id="f413c-115">You use the registry to configure the AutoLogger session.</span></span> <span data-ttu-id="f413c-116">Agregue la siguiente clave del Registro, si aún no está presente:</span><span class="sxs-lookup"><span data-stu-id="f413c-116">Add the following registry key, if it is not already present:</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Control
            \WMI
               \Autologger
```

<span data-ttu-id="f413c-117">En Clave **de registrador** automático, cree una clave para cada sesión de AutoLogger que desee configurar, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f413c-117">Under the **Autologger** key create a key for each AutoLogger session that you want to configure as shown in the following example.</span></span>

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

<span data-ttu-id="f413c-118">Para cada sesión, cree una clave para cada proveedor que desee habilitar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="f413c-118">For each session, create a key for each provider that you want to enable to the session.</span></span> <span data-ttu-id="f413c-119">Use el GUID del proveedor como clave.</span><span class="sxs-lookup"><span data-stu-id="f413c-119">Use the provider's GUID as the key.</span></span>

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

<span data-ttu-id="f413c-120">En la tabla siguiente se describen los valores que puede definir para cada sesión de AutoLogger.</span><span class="sxs-lookup"><span data-stu-id="f413c-120">The following table describes the values that you can define for each AutoLogger session.</span></span> <span data-ttu-id="f413c-121">Debe tener privilegios de administrador para especificar estos valores del Registro.</span><span class="sxs-lookup"><span data-stu-id="f413c-121">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="f413c-122">Los **valores Start** y **Guid** son los únicos valores necesarios para iniciar la sesión de AutoLogger. todos los demás valores tienen una configuración predeterminada que se usa si el valor no está presente en el Registro.</span><span class="sxs-lookup"><span data-stu-id="f413c-122">The **Start** and **Guid** value are the only values required to start the AutoLogger session; all other values have default settings that are used if the value is not present in the registry.</span></span> <span data-ttu-id="f413c-123">Normalmente, debe usar los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="f413c-123">Typically, you should use the default values.</span></span> <span data-ttu-id="f413c-124">Si especifica un valor que ETW no admite, ETW invalidará el valor.</span><span class="sxs-lookup"><span data-stu-id="f413c-124">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f413c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f413c-125">Value</span></span></th>
<th><span data-ttu-id="f413c-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="f413c-126">Type</span></span></th>
<th><span data-ttu-id="f413c-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="f413c-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f413c-128"><strong>BufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-128"><strong>BufferSize</strong></span></span></td>
<td><span data-ttu-id="f413c-129"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-129"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-130">Tamaño de cada búfer, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="f413c-130">The size of each buffer, in kilobytes.</span></span> <span data-ttu-id="f413c-131">Debe ser menor que un megabyte.</span><span class="sxs-lookup"><span data-stu-id="f413c-131">Should be less than one megabyte.</span></span> <span data-ttu-id="f413c-132">ETW usa el tamaño de la memoria física para calcular este valor.</span><span class="sxs-lookup"><span data-stu-id="f413c-132">ETW uses the size of physical memory to calculate this value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-133"><strong>ClockType</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-133"><strong>ClockType</strong></span></span></td>
<td><span data-ttu-id="f413c-134"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-134"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-135">Temporizador que se usará al registrar la marca de tiempo para cada evento.</span><span class="sxs-lookup"><span data-stu-id="f413c-135">The timer to use when logging the time stamp for each event.</span></span>
<ul>
<li><span data-ttu-id="f413c-136">1 = Valor del contador de rendimiento (alta resolución)</span><span class="sxs-lookup"><span data-stu-id="f413c-136">1 = Performance counter value (high resolution)</span></span></li>
<li><span data-ttu-id="f413c-137">2 = Temporizador del sistema</span><span class="sxs-lookup"><span data-stu-id="f413c-137">2 = System timer</span></span></li>
<li><span data-ttu-id="f413c-138">3 = Contador de ciclo de CPU</span><span class="sxs-lookup"><span data-stu-id="f413c-138">3 = CPU cycle counter</span></span></li>
</ul>
<span data-ttu-id="f413c-139">Para obtener una descripción de cada tipo de reloj, vea el <strong>miembro ClientContext</strong> <a href="wnode-header.md"><strong>de WNODE_HEADER</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f413c-139">For a description of each clock type, see the <strong>ClientContext</strong> member of <a href="wnode-header.md"><strong>WNODE_HEADER</strong></a>.</span></span><br/> <span data-ttu-id="f413c-140">El valor predeterminado es 1 (valor del contador de rendimiento) en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f413c-140">The default value is 1 (performance counter value) on Windows Vista and later.</span></span> <span data-ttu-id="f413c-141">Antes de Windows Vista, el valor predeterminado es 2 (temporizador del sistema).</span><span class="sxs-lookup"><span data-stu-id="f413c-141">Prior to Windows Vista, the default value is 2 (system timer).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f413c-142"><strong>DisableRealtimePersistence</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-142"><strong>DisableRealtimePersistence</strong></span></span></td>
<td><span data-ttu-id="f413c-143"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-143"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-144">Para deshabilitar la persistencia en tiempo real, establezca este valor en 1.</span><span class="sxs-lookup"><span data-stu-id="f413c-144">To disable real time persistence, set this value to 1.</span></span> <span data-ttu-id="f413c-145">El valor predeterminado es 0 (habilitado) para las sesiones en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="f413c-145">The default is 0 (enabled) for real time sessions.</span></span><br/> <span data-ttu-id="f413c-146">Si la persistencia en tiempo real está habilitada, se conservarán los eventos en tiempo real que no se entregaron en el momento en que se apagó el equipo.</span><span class="sxs-lookup"><span data-stu-id="f413c-146">If real time persistence is enabled, real-time events that were not delivered by the time the computer was shutdown will be persisted.</span></span> <span data-ttu-id="f413c-147">Los eventos se entregarán al consumidor la próxima vez que el consumidor se conecte a la sesión.</span><span class="sxs-lookup"><span data-stu-id="f413c-147">The events will then be delivered to the consumer the next time the consumer connects to the session.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-148"><strong>FileCounter</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-148"><strong>FileCounter</strong></span></span></td>
<td><span data-ttu-id="f413c-149"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-149"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-150">No establezca ni modifique este valor.</span><span class="sxs-lookup"><span data-stu-id="f413c-150">Do not set or modify this value.</span></span> <span data-ttu-id="f413c-151">Este valor es el número de serie utilizado para incrementar el nombre del archivo de registro si <strong>se especifica FileMax.</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-151">This value is the serial number used to increment the log file name if <strong>FileMax</strong> is specified.</span></span> <span data-ttu-id="f413c-152">Si el valor no es válido, se asumirá 1.</span><span class="sxs-lookup"><span data-stu-id="f413c-152">If the value is not valid, 1 will be assumed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f413c-153"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-153"><strong>FileName</strong></span></span></td>
<td><span data-ttu-id="f413c-154"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-154"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="f413c-155">Ruta de acceso completa del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="f413c-155">The fully qualified path of the log file.</span></span> <span data-ttu-id="f413c-156">La ruta de acceso a este archivo debe existir.</span><span class="sxs-lookup"><span data-stu-id="f413c-156">The path to this file must exist.</span></span> <span data-ttu-id="f413c-157">El archivo de registro es un archivo de registro secuencial.</span><span class="sxs-lookup"><span data-stu-id="f413c-157">The log file is a sequential log file.</span></span> <span data-ttu-id="f413c-158">La ruta de acceso está limitada a 1024 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f413c-158">The path is limited to 1024 characters.</span></span><br/> <span data-ttu-id="f413c-159">Si <strong>no se especifica FileName,</strong> los eventos se escriben en %SystemRoot%\System32\LogFiles\WMI \& lt;sessionname &gt; .etl.</span><span class="sxs-lookup"><span data-stu-id="f413c-159">If <strong>FileName</strong> is not specified, events are written to %SystemRoot%\System32\LogFiles\WMI\&lt;sessionname&gt;.etl.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-160"><strong>FileMax</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-160"><strong>FileMax</strong></span></span></td>
<td><span data-ttu-id="f413c-161"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-161"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-162">Número máximo de instancias del archivo de registro que crea ETW.</span><span class="sxs-lookup"><span data-stu-id="f413c-162">The maximum number of instances of the log file that ETW creates.</span></span> <span data-ttu-id="f413c-163">Si el archivo de registro especificado en <strong>FileName</strong> existe, ETW anexa el valor <strong>fileCounter</strong> al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="f413c-163">If the log file specified in <strong>FileName</strong> exists, ETW appends the <strong>FileCounter</strong> value to the file name.</span></span> <span data-ttu-id="f413c-164">Por ejemplo, si se usa el nombre de archivo de registro predeterminado, el formulario es %SystemRoot%\System32\LogFiles\WMI \& lt;sessionname &gt; .etl. Nnnn.</span><span class="sxs-lookup"><span data-stu-id="f413c-164">For example, if the default log file name is used, the form is %SystemRoot%\System32\LogFiles\WMI\&lt;sessionname&gt;.etl.NNNN.</span></span> <br/> <span data-ttu-id="f413c-165">La primera vez que se inicia el equipo, el nombre de archivo es sessionname .etl.0001, la segunda vez el nombre de archivo es &lt; &gt; &lt; sessionname &gt; .etl.0002, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f413c-165">The first time the computer is started, the file name is &lt;sessionname&gt;.etl.0001, the second time the file name is &lt;sessionname&gt;.etl.0002, and so on.</span></span> <span data-ttu-id="f413c-166">Si <strong>FileMax</strong> es 3, en el cuarto reinicio del equipo, ETW restablece el contador a 1 y sobrescribe &lt; sessionname &gt; .etl.0001, si existe.</span><span class="sxs-lookup"><span data-stu-id="f413c-166">If <strong>FileMax</strong> is 3, on the fourth restart of the computer, ETW resets the counter to 1 and overwrites &lt;sessionname&gt;.etl.0001, if it exists.</span></span><br/> <span data-ttu-id="f413c-167">El número máximo de instancias del archivo de registro que se admiten es 16.</span><span class="sxs-lookup"><span data-stu-id="f413c-167">The maximum number of instances of the log file that are supported is 16.</span></span><br/> <span data-ttu-id="f413c-168">No use esta característica con el modo de <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> de registro.</span><span class="sxs-lookup"><span data-stu-id="f413c-168">Do not use this feature with the <a href="logging-mode-constants.md">EVENT_TRACE_FILE_MODE_NEWFILE</a> log file mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f413c-169"><strong>FlushTimer</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-169"><strong>FlushTimer</strong></span></span></td>
<td><span data-ttu-id="f413c-170"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-170"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-171">Con qué frecuencia, en segundos, se vacían forzadamente los búferes de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f413c-171">How often, in seconds, the trace buffers are forcibly flushed.</span></span> <span data-ttu-id="f413c-172">El tiempo mínimo de vaciado es de 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="f413c-172">The minimum flush time is 1 second.</span></span> <span data-ttu-id="f413c-173">Este vaciado forzado se suma al vaciado automático que se produce cuando un búfer está lleno y cuando se detiene la sesión de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f413c-173">This forced flush is in addition to the automatic flush that occurs when a buffer is full and when the trace session stops.</span></span> <br/> <span data-ttu-id="f413c-174">En el caso de un registrador en tiempo real, un valor de cero (el valor predeterminado) significa que el tiempo de vaciado se establecerá en 1 segundo.</span><span class="sxs-lookup"><span data-stu-id="f413c-174">For the case of a real-time logger, a value of zero (the default value) means that the flush time will be set to 1 second.</span></span> <span data-ttu-id="f413c-175">Un registrador en tiempo real es cuando <strong>LogFileMode</strong> se establece <strong>en EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="f413c-175">A real-time logger is when <strong>LogFileMode</strong> is set to <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="f413c-176">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="f413c-176">The default value is 0.</span></span> <span data-ttu-id="f413c-177">De forma predeterminada, los búferes solo se vacían cuando están llenos.</span><span class="sxs-lookup"><span data-stu-id="f413c-177">By default, buffers are flushed only when they are full.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-178"><strong>Guid</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-178"><strong>Guid</strong></span></span></td>
<td><span data-ttu-id="f413c-179"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-179"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="f413c-180">Cadena que contiene un GUID que identifica de forma única la sesión.</span><span class="sxs-lookup"><span data-stu-id="f413c-180">A string that contains a GUID that uniquely identifies the session.</span></span> <span data-ttu-id="f413c-181">Este valor es necesario.</span><span class="sxs-lookup"><span data-stu-id="f413c-181">This value is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f413c-182"><strong>LogFileMode</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-182"><strong>LogFileMode</strong></span></span></td>
<td><span data-ttu-id="f413c-183"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-183"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-184">Especifique uno o varios modos de registro.</span><span class="sxs-lookup"><span data-stu-id="f413c-184">Specify one or more log modes.</span></span> <span data-ttu-id="f413c-185">Para ver los valores <a href="logging-mode-constants.md">posibles, vea Constantes de modo de registro.</a></span><span class="sxs-lookup"><span data-stu-id="f413c-185">For possible values, see <a href="logging-mode-constants.md">Logging Mode Constants</a>.</span></span> <span data-ttu-id="f413c-186">El valor predeterminado <strong>es EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="f413c-186">The default is <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.</span></span> <span data-ttu-id="f413c-187">En lugar de escribir en un archivo de registro, puede especificar EVENT_TRACE_BUFFERING_MODE <strong>o</strong> <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span><span class="sxs-lookup"><span data-stu-id="f413c-187">Instead of writing to a log file, you can specify either <strong>EVENT_TRACE_BUFFERING_MODE</strong> or <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.</span></span><br/> <span data-ttu-id="f413c-188">Al especificar <strong>EVENT_TRACE_BUFFERING_MODE</strong> evita el costo de vaciar el contenido de la sesión en el disco cuando el sistema de archivos esté disponible.</span><span class="sxs-lookup"><span data-stu-id="f413c-188">Specifying <strong>EVENT_TRACE_BUFFERING_MODE</strong> avoids the cost of flushing the contents of the session to disk when the file system becomes available.</span></span> <br/> <span data-ttu-id="f413c-189">Tenga en cuenta <strong>que EVENT_TRACE_BUFFERING_MODE</strong> hará que el sistema ignore el valor <strong>MaximumBuffers,</strong> ya que el tamaño del búfer es en su lugar el producto <strong>de MinimumBuffers</strong> y <strong>BufferSize</strong>.</span><span class="sxs-lookup"><span data-stu-id="f413c-189">Note that using <strong>EVENT_TRACE_BUFFERING_MODE</strong> will cause the system to ignore the <strong>MaximumBuffers</strong> value, as the buffer size is instead the product of <strong>MinimumBuffers</strong> and <strong>BufferSize</strong>.</span></span><br/> <span data-ttu-id="f413c-190">Las sesiones de AutoLogger no admiten <strong>el EVENT_TRACE_FILE_MODE_NEWFILE</strong> de registro.</span><span class="sxs-lookup"><span data-stu-id="f413c-190">AutoLogger sessions do not support the <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> logging mode.</span></span><br/> <span data-ttu-id="f413c-191">Si <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> especifica , <strong>BufferSize</strong> debe proporcionarse explícitamente y debe ser el mismo en el registrador y el archivo que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="f413c-191">If <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> is specified, <strong>BufferSize</strong> must be explicitly provided and must be the same in both the logger and the file being appended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-192"><strong>MaxFileSize</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-192"><strong>MaxFileSize</strong></span></span></td>
<td><span data-ttu-id="f413c-193"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-193"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-194">Tamaño máximo del archivo de registro, en megabytes.</span><span class="sxs-lookup"><span data-stu-id="f413c-194">The maximum file size of the log file, in megabytes.</span></span> <span data-ttu-id="f413c-195">La sesión se cierra cuando se alcanza el tamaño máximo, a menos que esté en modo de archivo de registro circular.</span><span class="sxs-lookup"><span data-stu-id="f413c-195">The session is closed when the maximum size is reached, unless you are in circular log file mode.</span></span> <span data-ttu-id="f413c-196">Para especificar ningún límite, establezca el valor en 0.</span><span class="sxs-lookup"><span data-stu-id="f413c-196">To specify no limit, set value to 0.</span></span> <span data-ttu-id="f413c-197">El valor predeterminado es 100 MB, si no se establece.</span><span class="sxs-lookup"><span data-stu-id="f413c-197">The default is 100 MB, if not set.</span></span> <span data-ttu-id="f413c-198">El comportamiento que se produce cuando se alcanza el tamaño máximo de archivo depende del valor de <strong>LogFileMode</strong>.</span><span class="sxs-lookup"><span data-stu-id="f413c-198">The behavior that occurs when the maximum file size is reached depends on the value of <strong>LogFileMode</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f413c-199"><strong>MaximumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-199"><strong>MaximumBuffers</strong></span></span></td>
<td><span data-ttu-id="f413c-200"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-200"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-201">Número máximo de búferes que se asignarán.</span><span class="sxs-lookup"><span data-stu-id="f413c-201">The maximum number of buffers to allocate.</span></span> <span data-ttu-id="f413c-202">Normalmente, este valor es el número mínimo de búferes más veinte.</span><span class="sxs-lookup"><span data-stu-id="f413c-202">Typically, this value is the minimum number of buffers plus twenty.</span></span> <span data-ttu-id="f413c-203">ETW usa el tamaño del búfer y el tamaño de memoria física para calcular este valor.</span><span class="sxs-lookup"><span data-stu-id="f413c-203">ETW uses the buffer size and the size of physical memory to calculate this value.</span></span> <span data-ttu-id="f413c-204">Este valor debe ser mayor o igual que el valor de <strong>MinimumBuffers.</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-204">This value must be greater than or equal to the value for <strong>MinimumBuffers</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-205"><strong>MinimumBuffers</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-205"><strong>MinimumBuffers</strong></span></span></td>
<td><span data-ttu-id="f413c-206"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-206"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-207">Número mínimo de búferes que se asignarán en el inicio.</span><span class="sxs-lookup"><span data-stu-id="f413c-207">The minimum number of buffers to allocate at startup.</span></span> <span data-ttu-id="f413c-208">El número mínimo de búferes que puede especificar es de dos búferes por procesador.</span><span class="sxs-lookup"><span data-stu-id="f413c-208">The minimum number of buffers that you can specify is two buffers per processor.</span></span> <span data-ttu-id="f413c-209">Por ejemplo, en un equipo con un solo procesador, el número mínimo de búferes es dos.</span><span class="sxs-lookup"><span data-stu-id="f413c-209">For example, on a single processor computer, the minimum number of buffers is two.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f413c-210"><strong>Iniciar</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-210"><strong>Start</strong></span></span></td>
<td><span data-ttu-id="f413c-211"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-211"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-212">Para que la sesión de AutoLogger se inicie la próxima vez que se reinicie el equipo, establezca este valor en 1; De lo contrario, establezca este valor en 0.</span><span class="sxs-lookup"><span data-stu-id="f413c-212">To have the AutoLogger session start the next time the computer is restarted, set this value to 1; otherwise, set this value to 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-213"><strong>Estado</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-213"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="f413c-214"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-214"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-215">Estado de inicio del registrador automático.</span><span class="sxs-lookup"><span data-stu-id="f413c-215">The startup status of the AutoLogger.</span></span> <span data-ttu-id="f413c-216">Si el registrador automático no se pudo iniciar, el valor de esta clave es el código de error de Win32 adecuado.</span><span class="sxs-lookup"><span data-stu-id="f413c-216">If the AutoLogger failed to start, the value of this key is the appropriate Win32 error code.</span></span> <span data-ttu-id="f413c-217">Si el registrador automático se inició correctamente, el valor de esta clave <strong>ERROR_SUCCESS</strong> (0).</span><span class="sxs-lookup"><span data-stu-id="f413c-217">If the AutoLogger successfully started, the value of this key is <strong>ERROR_SUCCESS</strong> (0).</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f413c-218">En la tabla siguiente se describen los valores que puede definir para cada proveedor que desea habilitar para la sesión.</span><span class="sxs-lookup"><span data-stu-id="f413c-218">The following table describes the values that you can define for each provider that you want to enable to your session.</span></span> <span data-ttu-id="f413c-219">Debe tener privilegios de administrador para especificar estos valores del Registro.</span><span class="sxs-lookup"><span data-stu-id="f413c-219">You must have administrator privileges to specify these registry values.</span></span> <span data-ttu-id="f413c-220">Si especifica un valor que ETW no admite, ETW invalidará el valor.</span><span class="sxs-lookup"><span data-stu-id="f413c-220">If you specify a value that ETW cannot support, ETW will override the value.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f413c-221">Valor</span><span class="sxs-lookup"><span data-stu-id="f413c-221">Value</span></span></th>
<th><span data-ttu-id="f413c-222">Tipo</span><span class="sxs-lookup"><span data-stu-id="f413c-222">Type</span></span></th>
<th><span data-ttu-id="f413c-223">Descripción</span><span class="sxs-lookup"><span data-stu-id="f413c-223">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f413c-224"><strong>Habilitado</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-224"><strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="f413c-225"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-225"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-226">Determina si el proveedor está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f413c-226">Determines if the provider is enabled.</span></span> <span data-ttu-id="f413c-227">Para habilitar el proveedor, establezca este valor en 1.</span><span class="sxs-lookup"><span data-stu-id="f413c-227">To enable the provider, set this value to 1.</span></span> <span data-ttu-id="f413c-228">Para deshabilitar el proveedor, establezca este valor en 0.</span><span class="sxs-lookup"><span data-stu-id="f413c-228">To disable the provider, set this value to 0.</span></span> <span data-ttu-id="f413c-229">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="f413c-229">The default is 0.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-230"><strong>EnableFlags</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-230"><strong>EnableFlags</strong></span></span></td>
<td><span data-ttu-id="f413c-231"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-231"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-232">Valor definido por el proveedor que especifica la clase de eventos para la que el proveedor genera eventos.</span><span class="sxs-lookup"><span data-stu-id="f413c-232">Provider-defined value that specifies the class of events for which the provider generates events.</span></span> <span data-ttu-id="f413c-233">Para más información, consulte <em>el parámetro EnableFlags</em> de la <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>función EnableTrace.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f413c-233">For details, see the <em>EnableFlags</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletrace"><strong>EnableTrace</strong></a> function.</span></span> <span data-ttu-id="f413c-234">Especifique este nombre de valor si el proveedor no admite <strong>MatchAnyKeyword</strong> o <strong>MatchAllKeyword.</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-234">Specify this value name if the provider does not support <strong>MatchAnyKeyword</strong> or <strong>MatchAllKeyword</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f413c-235"><strong>EnableLevel</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-235"><strong>EnableLevel</strong></span></span></td>
<td><span data-ttu-id="f413c-236"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-236"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-237">Valor definido por el proveedor que especifica el nivel de detalle incluido en el evento.</span><span class="sxs-lookup"><span data-stu-id="f413c-237">Provider-defined value that specifies the level of detail included in the event.</span></span> <span data-ttu-id="f413c-238">Por ejemplo, puede usar este valor para indicar el nivel de gravedad de los eventos (informativo, advertencia, error) que genera el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f413c-238">For example, you can use this value to indicate the severity level of the events (informational, warning, error) that the provider generates.</span></span> <span data-ttu-id="f413c-239">Para obtener una lista de los niveles predefinidos, vea el <em>parámetro level</em> de la <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>función EnableTraceEx.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f413c-239">For a list of predefined levels, see the <em>level</em> parameter of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-240"><strong>EnableProperty</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-240"><strong>EnableProperty</strong></span></span></td>
<td><span data-ttu-id="f413c-241"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-241"><strong>REG_DWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-242">Use este valor para incluir uno o varios de los siguientes elementos en el archivo de registro:</span><span class="sxs-lookup"><span data-stu-id="f413c-242">Use this value to include one or more of the following items in the log file:</span></span>
<ul>
<li><span data-ttu-id="f413c-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Incluir en los datos extendidos el identificador de seguridad (SID) del usuario.</span><span class="sxs-lookup"><span data-stu-id="f413c-243"><strong>EVENT_ENABLE_PROPERTY_SID</strong> (0x00000001) = Include in the extended data the security identifier (SID) of the user.</span></span></li>
<li><span data-ttu-id="f413c-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Incluir en los datos extendidos el identificador de sesión del terminal.</span><span class="sxs-lookup"><span data-stu-id="f413c-244"><strong>EVENT_ENABLE_PROPERTY_TS_ID</strong> (0x00000002) = Include in the extended data the terminal session identifier.</span></span></li>
<li><span data-ttu-id="f413c-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Incluir en los datos extendidos un seguimiento de pila de llamadas para eventos escritos mediante <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f413c-245"><strong>EVENT_ENABLE_PROPERTY_STACK_TRACE</strong> (0x00000004) = Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a>.</span></span></li>
<li><span data-ttu-id="f413c-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = filtra todos los eventos que no tienen especificada una palabra clave que no sea cero.</span><span class="sxs-lookup"><span data-stu-id="f413c-246"><strong>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</strong> (0x00000010) = Filters out all events that do not have a non-zero keyword specified.</span></span></li>
<li><span data-ttu-id="f413c-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indica que esta llamada <a href="provider-traits.md">a</a> <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> debe habilitar un grupo de proveedores en lugar de un proveedor de eventos individual.</span><span class="sxs-lookup"><span data-stu-id="f413c-247"><strong>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</strong> (0x00000020) = Indicates that this call to <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a> should enable a <a href="provider-traits.md">Provider Group</a> rather than an individual Event Provider.</span></span></li>
<li><span data-ttu-id="f413c-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Incluir la clave de inicio del proceso en los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="f413c-248"><strong>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</strong> (0x00000080) = Include the Process Start Key in the extended data.</span></span></li>
<li><span data-ttu-id="f413c-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Incluir la clave de evento en los datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="f413c-249"><strong>EVENT_ENABLE_PROPERTY_EVENT_KEY</strong> (0x00000100) = Include the Event Key in the extended data.</span></span></li>
<li><span data-ttu-id="f413c-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = filtra todos los eventos marcados como un evento InPrivate o proceden de un proceso marcado como InPrivate.</span><span class="sxs-lookup"><span data-stu-id="f413c-250"><strong>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</strong> (0x00000200) = Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.</span></span></li>
</ul>
<span data-ttu-id="f413c-251">Para obtener más información sobre estos elementos, vea <strong>EnableProperty</strong> de la <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> estructura.</span><span class="sxs-lookup"><span data-stu-id="f413c-251">For more information about these items, see the <strong>EnableProperty</strong> of the <a href="/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters"><strong>ENABLE_TRACE_PARAMETERS</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f413c-252"><strong>MatchAnyKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-252"><strong>MatchAnyKeyword</strong></span></span></td>
<td><span data-ttu-id="f413c-253"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-253"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-254">Máscara de bits de palabras clave que determinan la categoría de eventos que desea que escriba el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f413c-254">Bitmask of keywords that determine the category of events that you want the provider to write.</span></span> <span data-ttu-id="f413c-255">El proveedor escribe el evento si alguno de los bits de palabra clave del evento coincide con cualquiera de los bits establecidos en esta máscara.</span><span class="sxs-lookup"><span data-stu-id="f413c-255">The provider writes the event if any of the event's keyword bits match any of the bits set in this mask.</span></span> <span data-ttu-id="f413c-256">Para especificar que el proveedor escriba todos los eventos, establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="f413c-256">To specify that the provider write all events, set this value to zero.</span></span> <span data-ttu-id="f413c-257">Para obtener un ejemplo, vea la sección Comentarios de la <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>función EnableTraceEx.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f413c-257">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f413c-258"><strong>MatchAllKeyword</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-258"><strong>MatchAllKeyword</strong></span></span></td>
<td><span data-ttu-id="f413c-259"><strong>REG_QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="f413c-259"><strong>REG_QWORD</strong></span></span></td>
<td><span data-ttu-id="f413c-260">Esta máscara de bits es opcional.</span><span class="sxs-lookup"><span data-stu-id="f413c-260">This bitmask is optional.</span></span> <span data-ttu-id="f413c-261">Esta máscara restringe aún más la categoría de eventos que desea que escriba el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f413c-261">This mask further restricts the category of events that you want the provider to write.</span></span> <span data-ttu-id="f413c-262">Si la palabra clave del evento cumple la condición <em>MatchAnyKeyword,</em> el proveedor escribirá el evento solo si todos los bits de esta máscara existen en la palabra clave del evento.</span><span class="sxs-lookup"><span data-stu-id="f413c-262">If the event's keyword meets the <em>MatchAnyKeyword</em> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword.</span></span> <span data-ttu-id="f413c-263">Esta máscara no se usa si <em>MatchAnyKeyword</em> es cero.</span><span class="sxs-lookup"><span data-stu-id="f413c-263">This mask is not used if <em>MatchAnyKeyword</em> is zero.</span></span> <span data-ttu-id="f413c-264">Para obtener un ejemplo, vea la sección Comentarios de la <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>función EnableTraceEx.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f413c-264">For an example, see the Remarks section of the <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex"><strong>EnableTraceEx</strong></a> function.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f413c-265">Una vez modificado el Registro, la sesión de AutoLogger se inicia la próxima vez que se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="f413c-265">After the registry has been modified, the AutoLogger session is started the next time the computer is restarted.</span></span> <span data-ttu-id="f413c-266">La sesión de AutoLogger llama a [**la función EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) para habilitar los proveedores.</span><span class="sxs-lookup"><span data-stu-id="f413c-266">The AutoLogger session calls the [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) function to enable the providers.</span></span>

<span data-ttu-id="f413c-267">Las sesiones de AutoLogger aumentan el tiempo de arranque del sistema y se deben usar con moderación.</span><span class="sxs-lookup"><span data-stu-id="f413c-267">The AutoLogger sessions increase the system boot time and should be used sparingly.</span></span> <span data-ttu-id="f413c-268">Los servicios que desean capturar información durante el proceso de arranque deben considerar la posibilidad de agregar lógica de controlador a sí mismo en lugar de usar la sesión de AutoLogger.</span><span class="sxs-lookup"><span data-stu-id="f413c-268">Services that want to capture information during the boot process should consider adding controller logic to itself instead of using the AutoLogger session.</span></span>

<span data-ttu-id="f413c-269">Para detener una sesión de AutoLogger, llame a la [**función ControlTrace.**](/windows/win32/api/evntrace/nf-evntrace-controltracea)</span><span class="sxs-lookup"><span data-stu-id="f413c-269">To stop an AutoLogger session, call the [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) function.</span></span> <span data-ttu-id="f413c-270">El nombre de sesión que pasa a la función es el nombre de la clave del Registro que usó para definir la sesión en el Registro.</span><span class="sxs-lookup"><span data-stu-id="f413c-270">The session name that you pass to the function is the name of the registry key that you used to define the session in the registry.</span></span>

<span data-ttu-id="f413c-271">En Windows 8.1, Windows Server 2012 R2 y versiones posteriores, la función [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) y las estructuras [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) y [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) pueden usar filtros de carga de eventos, ámbito y recorrido de pila para filtrar por condiciones específicas en una sesión de registrador.</span><span class="sxs-lookup"><span data-stu-id="f413c-271">On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) function and the [**ENABLE\_TRACE\_PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) and [**EVENT\_FILTER\_DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) structures to filter on specific conditions in a logger session.</span></span> <span data-ttu-id="f413c-272">Para obtener más información sobre los filtros de carga de eventos, vea las funciones [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)y [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) y las estructuras **ENABLE TRACE \_ \_ PARAMETERS**, **EVENT FILTER \_ \_ DESCRIPTOR** y [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)</span><span class="sxs-lookup"><span data-stu-id="f413c-272">For more information on event payload filters, see the [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter), and [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) functions and the **ENABLE\_TRACE\_PARAMETERS**, **EVENT\_FILTER\_DESCRIPTOR**, and [**PAYLOAD\_FILTER\_PREDICATE**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) structures.</span></span>

<span data-ttu-id="f413c-273">Para obtener más información sobre cómo iniciar una sesión de seguimiento de eventos, vea [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span><span class="sxs-lookup"><span data-stu-id="f413c-273">For details on starting an event tracing session, see [Configuring and Starting an Event Tracing Session](configuring-and-starting-an-event-tracing-session.md).</span></span>

<span data-ttu-id="f413c-274">Para obtener más información sobre cómo iniciar una sesión de registrador privado, vea [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="f413c-274">For details on starting a private logger session, see [Configuring and Starting a Private Logger Session](configuring-and-starting-a-private-logger-session.md).</span></span>

<span data-ttu-id="f413c-275">Para obtener más información sobre cómo iniciar una sesión de registrador de kernel nt, vea [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span><span class="sxs-lookup"><span data-stu-id="f413c-275">For details on starting an NT Kernel Logger session, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f413c-276">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f413c-276">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f413c-277">Configuración e inicio de una sesión de registrador privado</span><span class="sxs-lookup"><span data-stu-id="f413c-277">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="f413c-278">Configuración e inicio de una sesión de SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="f413c-278">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[<span data-ttu-id="f413c-279">Configuración e inicio de una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="f413c-279">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="f413c-280">Configuración e inicio de la sesión del registrador de kernel de NT</span><span class="sxs-lookup"><span data-stu-id="f413c-280">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="f413c-281">**EnableTraceEx2**</span><span class="sxs-lookup"><span data-stu-id="f413c-281">**EnableTraceEx2**</span></span>](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[<span data-ttu-id="f413c-282">**HABILITAR \_ PARÁMETROS DE \_ SEGUIMIENTO**</span><span class="sxs-lookup"><span data-stu-id="f413c-282">**ENABLE\_TRACE\_PARAMETERS**</span></span>](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[<span data-ttu-id="f413c-283">**DESCRIPTOR \_ DE FILTRO DE \_ EVENTOS**</span><span class="sxs-lookup"><span data-stu-id="f413c-283">**EVENT\_FILTER\_DESCRIPTOR**</span></span>](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[<span data-ttu-id="f413c-284">**PREDICADO \_ DE FILTRO DE CARGA \_ ÚTIL**</span><span class="sxs-lookup"><span data-stu-id="f413c-284">**PAYLOAD\_FILTER\_PREDICATE**</span></span>](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[<span data-ttu-id="f413c-285">**TdhAggregatePayloadFilters**</span><span class="sxs-lookup"><span data-stu-id="f413c-285">**TdhAggregatePayloadFilters**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[<span data-ttu-id="f413c-286">**TdhCreatePayloadFilter**</span><span class="sxs-lookup"><span data-stu-id="f413c-286">**TdhCreatePayloadFilter**</span></span>](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[<span data-ttu-id="f413c-287">Actualizar una sesión de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="f413c-287">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>
