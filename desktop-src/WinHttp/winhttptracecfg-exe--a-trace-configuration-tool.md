---
description: La herramienta de configuración de seguimiento de servicios HTTP de Microsoft Windows (WinHTTP), WinHttpTraceCfg.exe, se usa para configurar las capacidades de seguimiento para la depuración y el examen de paquetes.
ms.assetid: 744cae92-9c64-459e-96eb-eb609e62183c
title: WinHttpTraceCfg.exe, una herramienta de configuración de seguimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c6423c581a51f0cf6b55856f2e8cd0ea670515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715158"
---
# <a name="winhttptracecfgexe-a-trace-configuration-tool"></a><span data-ttu-id="560cb-103">WinHttpTraceCfg.exe, una herramienta de configuración de seguimiento</span><span class="sxs-lookup"><span data-stu-id="560cb-103">WinHttpTraceCfg.exe, a Trace Configuration Tool</span></span>

<span data-ttu-id="560cb-104">La herramienta de configuración de seguimiento de [servicios http de Microsoft Windows (WinHTTP)](about-winhttp.md) , WinHttpTraceCfg.exe, se usa para configurar las capacidades de seguimiento para la depuración y el examen de paquetes.</span><span class="sxs-lookup"><span data-stu-id="560cb-104">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) trace configuration tool, WinHttpTraceCfg.exe, is used to configure trace capabilities for debugging and packet-sniffing purposes.</span></span> <span data-ttu-id="560cb-105">Es importante la capacidad de supervisar las funciones WinHTTP y el tráfico de red correspondiente.</span><span class="sxs-lookup"><span data-stu-id="560cb-105">The ability to monitor WinHTTP functions and their corresponding network traffic is important.</span></span> <span data-ttu-id="560cb-106">La depuración de aplicaciones que usan protocolos de conexión cifrados, como Capa de sockets seguros (SSL), impide el examen de paquetes en la capa de transporte de red y requiere la capacidad de interceptar el tráfico entre el cliente y el servidor una vez descifrado.</span><span class="sxs-lookup"><span data-stu-id="560cb-106">Debugging applications that utilize encrypted wire protocols, such as Secure Sockets Layer (SSL), preclude sniffing packets at the network transport layer and require the ability to intercept traffic between the client and server after it has been decrypted.</span></span> <span data-ttu-id="560cb-107">Los servicios HTTP de Microsoft Windows (WinHTTP) proporcionan una utilidad de seguimiento que tiene una gran variedad de capacidades para interceptar el flujo de tráfico entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="560cb-107">Microsoft Windows HTTP Services (WinHTTP) provides a trace facility that has a range of capabilities for intercepting the traffic stream between the client and server.</span></span>

<span data-ttu-id="560cb-108">Esta utilidad de seguimiento puede ser una valiosa herramienta para la depuración.</span><span class="sxs-lookup"><span data-stu-id="560cb-108">This trace facility can be a valuable tool for debugging.</span></span> <span data-ttu-id="560cb-109">Se puede usar, por ejemplo, para ver los parámetros que se pasan a varias llamadas de función, así como para ver los datos reales enviados y recibidos por una aplicación WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="560cb-109">It can be used, for example, to view parameters passed to various function calls, as well as to view actual data sent and received by a WinHTTP application.</span></span>

-   [<span data-ttu-id="560cb-110">Uso de la utilidad de seguimiento</span><span class="sxs-lookup"><span data-stu-id="560cb-110">Using the Trace Facility</span></span>](#using-the-trace-facility)
-   [<span data-ttu-id="560cb-111">Interpretar los datos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="560cb-111">Interpreting Trace Data</span></span>](#interpreting-trace-data)

## <a name="using-the-trace-facility"></a><span data-ttu-id="560cb-112">Uso de la utilidad de seguimiento</span><span class="sxs-lookup"><span data-stu-id="560cb-112">Using the Trace Facility</span></span>

<span data-ttu-id="560cb-113">WinHTTP obtiene los parámetros de control de seguimiento del registro.</span><span class="sxs-lookup"><span data-stu-id="560cb-113">WinHTTP obtains tracing control parameters from the registry.</span></span> <span data-ttu-id="560cb-114">Estos parámetros de control afectan a cómo WinHTTP produce la salida del seguimiento y cómo se da formato a esa salida.</span><span class="sxs-lookup"><span data-stu-id="560cb-114">These control parameters affect how WinHTTP produces trace output, and how that output is formatted.</span></span> <span data-ttu-id="560cb-115">Todas las aplicaciones que usan WinHTTP comparten la misma configuración.</span><span class="sxs-lookup"><span data-stu-id="560cb-115">All applications that use WinHTTP share the same settings.</span></span>

<span data-ttu-id="560cb-116">Una herramienta de configuración de las instalaciones de seguimiento, WinHttpTraceCfg.exe, está disponible como descarga en el sitio web de [herramientas del kit de recursos de Windows Server 2003](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="560cb-116">A trace facility configuration tool, WinHttpTraceCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="560cb-117">La herramienta de configuración establece o recupera los valores del registro de la utilidad de seguimiento en función de los parámetros de línea de comandos especificados.</span><span class="sxs-lookup"><span data-stu-id="560cb-117">The configuration tool sets or retrieves the trace facility registry settings based on the specified command line parameters.</span></span>

``` syntax
WinHttpTraceCfg [-e <0|1>] [-l [log-file]] [-d <0|1>] [-s <0|1|2>] 
                [-t <0|1>] [-?] [-m <file size>]
```

<span data-ttu-id="560cb-118">En la tabla siguiente se enumeran los posibles parámetros de la herramienta de configuración de.</span><span class="sxs-lookup"><span data-stu-id="560cb-118">The following table lists possible parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="560cb-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="560cb-119">Parameter</span></span></th>
<th><span data-ttu-id="560cb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="560cb-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="560cb-121">-?</span><span class="sxs-lookup"><span data-stu-id="560cb-121">-?</span></span></td>
<td><span data-ttu-id="560cb-122">Muestra datos de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="560cb-122">Displays syntax data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560cb-123">-E</span><span class="sxs-lookup"><span data-stu-id="560cb-123">-e</span></span></td>
<td><span data-ttu-id="560cb-124">Especifica si la utilidad de seguimiento está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="560cb-124">Specifies whether the trace facility is enabled or disabled.</span></span> <br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="560cb-125">0</span><span class="sxs-lookup"><span data-stu-id="560cb-125">0</span></span></td>
<td><span data-ttu-id="560cb-126">Configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="560cb-126">Default setting.</span></span> <span data-ttu-id="560cb-127">Deshabilita el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-127">Disables tracing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560cb-128">1</span><span class="sxs-lookup"><span data-stu-id="560cb-128">1</span></span></td>
<td><span data-ttu-id="560cb-129">Habilita el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-129">Enables tracing.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="560cb-130">-l</span><span class="sxs-lookup"><span data-stu-id="560cb-130">-l</span></span></td>
<td><p><span data-ttu-id="560cb-131">Especifica un prefijo para el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="560cb-131">Specifies a prefix for the log file.</span></span> <span data-ttu-id="560cb-132">El prefijo puede incluir una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="560cb-132">The prefix can include a path.</span></span> <span data-ttu-id="560cb-133">El archivo de registro se escribe en el directorio actual o en el directorio especificado en el prefijo y tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="560cb-133">The log file is written to the current directory or the directory specified in the prefix and has the following format.</span></span></p>
<p><span data-ttu-id="560cb-134"><<em>prefijo</em> > -< <em>nombre de la aplicación</em> > . <<em>Time</em> > . log</span><span class="sxs-lookup"><span data-stu-id="560cb-134"><<em>prefix</em>>-<<em>application name</em>>.<<em>time</em>>.log</span></span></p>
<p><span data-ttu-id="560cb-135">Si no se especifica un prefijo, se usa una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="560cb-135">If a prefix is not specified, an empty string is used.</span></span> <span data-ttu-id="560cb-136">Especifique &quot; \* &quot; para eliminar un prefijo existente.</span><span class="sxs-lookup"><span data-stu-id="560cb-136">Specify &quot;\*&quot; to delete an existing prefix.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560cb-137">-d</span><span class="sxs-lookup"><span data-stu-id="560cb-137">-d</span></span></td>
<td><p><span data-ttu-id="560cb-138">Especifica si el resultado del seguimiento se muestra en un depurador o se escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="560cb-138">Specifies whether the trace output is displayed in a debugger or written to a file.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="560cb-139">0</span><span class="sxs-lookup"><span data-stu-id="560cb-139">0</span></span></td>
<td><span data-ttu-id="560cb-140">Configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="560cb-140">Default setting.</span></span> <span data-ttu-id="560cb-141">Escribe en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="560cb-141">Writes to log file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560cb-142">1</span><span class="sxs-lookup"><span data-stu-id="560cb-142">1</span></span></td>
<td><span data-ttu-id="560cb-143">Muestra en un depurador.</span><span class="sxs-lookup"><span data-stu-id="560cb-143">Displays in a debugger.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="560cb-144">-S</span><span class="sxs-lookup"><span data-stu-id="560cb-144">-s</span></span></td>
<td><p><span data-ttu-id="560cb-145">Especifica cómo se muestra el tráfico de red (solicitudes y respuestas).</span><span class="sxs-lookup"><span data-stu-id="560cb-145">Specifies how network traffic (requests and responses) is displayed.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="560cb-146">0</span><span class="sxs-lookup"><span data-stu-id="560cb-146">0</span></span></td>
<td><span data-ttu-id="560cb-147">Solo muestra los encabezados HTTP.</span><span class="sxs-lookup"><span data-stu-id="560cb-147">Only displays HTTP headers.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560cb-148">1</span><span class="sxs-lookup"><span data-stu-id="560cb-148">1</span></span></td>
<td><span data-ttu-id="560cb-149">Configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="560cb-149">Default setting.</span></span> <span data-ttu-id="560cb-150">Muestra el tráfico de red en formato American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="560cb-150">Shows network traffic in American National Standards Institute (ANSI) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="560cb-151">2</span><span class="sxs-lookup"><span data-stu-id="560cb-151">2</span></span></td>
<td><span data-ttu-id="560cb-152">Muestra el tráfico de red en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="560cb-152">Shows network traffic in hexadecimal format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560cb-153">-T</span><span class="sxs-lookup"><span data-stu-id="560cb-153">-t</span></span></td>
<td><p><span data-ttu-id="560cb-154">Especifica si las llamadas de función de nivel superior se registran en el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-154">Specifies whether top-level function calls are recorded in the trace.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="560cb-155">0</span><span class="sxs-lookup"><span data-stu-id="560cb-155">0</span></span></td>
<td><span data-ttu-id="560cb-156">Configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="560cb-156">Default setting.</span></span> <span data-ttu-id="560cb-157">No se registran las llamadas de función.</span><span class="sxs-lookup"><span data-stu-id="560cb-157">Function calls are not recorded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="560cb-158">1</span><span class="sxs-lookup"><span data-stu-id="560cb-158">1</span></span></td>
<td><span data-ttu-id="560cb-159">Se registran las llamadas de función de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="560cb-159">Top-level function calls are recorded.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="560cb-160">-M</span><span class="sxs-lookup"><span data-stu-id="560cb-160">-m</span></span></td>
<td><p><span data-ttu-id="560cb-161">Especifica el tamaño máximo, en bytes, de un archivo de registro generado por la utilidad de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-161">Specifies the maximum size, in bytes, of a log file generated by the tracing facility.</span></span> <span data-ttu-id="560cb-162">Si se especifica esta opción sin un tamaño, el valor mínimo es 65.535 bytes.</span><span class="sxs-lookup"><span data-stu-id="560cb-162">If this option is specified without a size, the minimum value is 65,535 bytes.</span></span> <span data-ttu-id="560cb-163">Si un archivo de registro alcanza el tamaño máximo, se borra el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="560cb-163">If a log file reaches the maximum size, the contents of the file are erased.</span></span> <span data-ttu-id="560cb-164">Los datos de seguimiento continúan escribiendo en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="560cb-164">Trace data continues to be written to the log file.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="560cb-165">La ejecución de la herramienta de configuración de la utilidad de seguimiento y la especificación de ningún parámetro recupera y muestra la configuración actual del registro.</span><span class="sxs-lookup"><span data-stu-id="560cb-165">Running the trace facility configuration tool and specifying no parameters retrieves and displays the current registry settings.</span></span>

> [!Note]  
> <span data-ttu-id="560cb-166">Los archivos de registro crecen rápidamente y reducen el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="560cb-166">Log files grow rapidly and degrade application performance.</span></span> <span data-ttu-id="560cb-167">Asegúrese de que el espacio de la unidad de disco duro necesario está disponible antes de habilitar el servicio de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-167">Ensure that the required hard disk drive space is available before enabling the trace facility.</span></span>

 

## <a name="interpreting-trace-data"></a><span data-ttu-id="560cb-168">Interpretar los datos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="560cb-168">Interpreting Trace Data</span></span>

<span data-ttu-id="560cb-169">El flujo de datos de las instalaciones de seguimiento refleja las funciones WinHTTP llamadas en la aplicación y los datos HTTP enviados o recibidos.</span><span class="sxs-lookup"><span data-stu-id="560cb-169">The trace facility data stream reflects WinHTTP functions called in the application and any HTTP data sent or received.</span></span> <span data-ttu-id="560cb-170">En algunos casos, también se muestran las funciones a las que se llama internamente en WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="560cb-170">In some cases, functions called internally by WinHTTP are also shown.</span></span>

<span data-ttu-id="560cb-171">En la imagen siguiente se muestra una parte de un archivo de registro generado por la utilidad de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-171">The following image shows a portion of a log file generated by the trace facility.</span></span> <span data-ttu-id="560cb-172">Varios elementos se resaltan y etiquetan.</span><span class="sxs-lookup"><span data-stu-id="560cb-172">Several items are highlighted and labeled.</span></span>

![seguimiento de ejemplo](images/ss-tracer-wco.png)

<span data-ttu-id="560cb-174">Cada línea de la salida del seguimiento contiene información en tres columnas.</span><span class="sxs-lookup"><span data-stu-id="560cb-174">Each line of trace output contains information in three columns.</span></span> <span data-ttu-id="560cb-175">La primera columna muestra la fecha y la hora en que se registró la entrada.</span><span class="sxs-lookup"><span data-stu-id="560cb-175">The first column shows the date and time when the entry was recorded.</span></span> <span data-ttu-id="560cb-176">La segunda columna muestra un identificador de solicitud (ID.) que se puede utilizar para diferenciar entre varias solicitudes.</span><span class="sxs-lookup"><span data-stu-id="560cb-176">The second column shows a request identifier (ID) that can be used to differentiate between multiple requests.</span></span> <span data-ttu-id="560cb-177">Si la entrada de registro no se corresponde con una solicitud específica, \* \* se muestra "sesión" en esta columna.</span><span class="sxs-lookup"><span data-stu-id="560cb-177">If the log entry does not correspond to a specific request, "\*Session\*" is displayed in this column.</span></span> <span data-ttu-id="560cb-178">Puede ser útil ordenar el archivo de registro en función de este identificador para ver solo los eventos que se producen para una única solicitud.</span><span class="sxs-lookup"><span data-stu-id="560cb-178">It can be useful to sort the log file based on this ID to see only events that occur for a single request.</span></span> <span data-ttu-id="560cb-179">En el ejemplo siguiente se muestra un comando que puede usar para ordenar el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="560cb-179">The following example shows a command you can use to sort the log file.</span></span>

<span data-ttu-id="560cb-180">**Findstr 00000001 LogFile. log**</span><span class="sxs-lookup"><span data-stu-id="560cb-180">**findstr 00000001 LogFile.log**</span></span>

<span data-ttu-id="560cb-181">La tercera columna muestra una llamada de función, el tráfico HTTP o un mensaje de estado incluido para ayudar a interpretar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-181">The third column shows a function call, HTTP traffic, or a status message included to help interpret the trace.</span></span>

<span data-ttu-id="560cb-182">Cuando una entrada de registro corresponde a una llamada de función, también se registran los parámetros de la función.</span><span class="sxs-lookup"><span data-stu-id="560cb-182">When a log entry corresponds to a function call, the parameters of the function are also recorded.</span></span> <span data-ttu-id="560cb-183">Las direcciones de memoria se muestran en formato hexadecimal mientras que todos los demás valores se muestran como una cadena ASCII.</span><span class="sxs-lookup"><span data-stu-id="560cb-183">Memory addresses are displayed in hexadecimal while all other values are displayed as an ASCII string.</span></span> <span data-ttu-id="560cb-184">La utilidad de seguimiento registra también el tiempo y el valor de retorno de cada función.</span><span class="sxs-lookup"><span data-stu-id="560cb-184">The trace facility also records the return time and value for each function.</span></span>

<span data-ttu-id="560cb-185">El formato de los datos HTTP depende de la configuración del registro especificada con la herramienta de configuración del servicio de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-185">The format of HTTP data depends on the registry settings specified with the trace facility configuration tool.</span></span> <span data-ttu-id="560cb-186">Cuando se cifran los datos HTTP, los datos descifrados también se muestran en el resultado del seguimiento.</span><span class="sxs-lookup"><span data-stu-id="560cb-186">When HTTP data is encrypted, the decrypted data is also shown in the trace output.</span></span>

 

 




