---
title: Registro de errores en Windows Server 2003 SP1
description: Registro de errores en Windows Server 2003 SP1
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Registro de errores en Windows Server 2003 con Service Pack 1 (SP1)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/14/2019
ms.locfileid: "103784876"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a><span data-ttu-id="3a13a-104">Registro de errores en Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="3a13a-104">Error Logging in Windows Server 2003 SP1</span></span>

## <a name="addition-of-w3c-style-headers"></a><span data-ttu-id="3a13a-105">Adición de encabezados de estilo W3C</span><span class="sxs-lookup"><span data-stu-id="3a13a-105">Addition of W3C Style Headers</span></span>

<span data-ttu-id="3a13a-106">A partir de Windows Server 2003 con Service Pack 1 (SP1), el registro de errores de la API del servidor HTTP incluye encabezados de estilo W3C que permiten analizar los archivos de registro mediante analizadores de registro estándar.</span><span class="sxs-lookup"><span data-stu-id="3a13a-106">Starting with Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API error log includes W3C style headers allowing log files to be parsed using standard log parsers.</span></span> <span data-ttu-id="3a13a-107">En la plantilla que se muestra a continuación se enumeran todos los campos que se pueden registrar en el archivo de registro de errores http.</span><span class="sxs-lookup"><span data-stu-id="3a13a-107">The template shown below lists all the fields that can be logged in the http error log file.</span></span>

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a><span data-ttu-id="3a13a-108">Registro de campos adicionales</span><span class="sxs-lookup"><span data-stu-id="3a13a-108">Logging Additional Fields</span></span>

<span data-ttu-id="3a13a-109">El registro de errores HTTP se ha ampliado para incluir nueve campos más para registrar los datos de los errores que se producen.</span><span class="sxs-lookup"><span data-stu-id="3a13a-109">The HTTP error log has been extended to include nine more fields to log data about failures that occur.</span></span> <span data-ttu-id="3a13a-110">Los campos de error nuevos se enumeran a continuación:</span><span class="sxs-lookup"><span data-stu-id="3a13a-110">The new error fields are listed below:</span></span>

-   <span data-ttu-id="3a13a-111">Nombre de equipo \[ del servidor S-COMPUTERNAME\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-111">Server Computer Name \[S-COMPUTERNAME\]</span></span>
-   <span data-ttu-id="3a13a-112">User Agent \[ CS (agente de usuario \_ )\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-112">User Agent \[CS(USER\_AGENT)\]</span></span>
-   <span data-ttu-id="3a13a-113">Cookie \[ CS (cookie)\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-113">Cookie \[CS(COOKIE)\]</span></span>
-   <span data-ttu-id="3a13a-114">referencia \[ CS (referrer)\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-114">referrer \[CS(referrer)\]</span></span>
-   <span data-ttu-id="3a13a-115">Nombre \[ de host CS-host\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-115">Host Name \[CS-HOST\]</span></span>
-   <span data-ttu-id="3a13a-116">Bytes recibidos por el servidor \[ SC-bytes\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-116">Bytes received by the server \[SC-BYTES\]</span></span>
-   <span data-ttu-id="3a13a-117">Bytes recibidos y procesados por el servidor \[ CS-bytes\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-117">Bytes received and processed by the server \[CS-BYTES\]</span></span>
-   <span data-ttu-id="3a13a-118">Tiempo necesario para procesar el \[ tiempo de solicitud\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-118">Time Taken to process the request \[TIME-TAKEN\]</span></span>
-   <span data-ttu-id="3a13a-119">Queue-Name (reservado para IIS) \[ S-QUEUENAME\]</span><span class="sxs-lookup"><span data-stu-id="3a13a-119">Queue-Name (Reserved for IIS) \[S-QUEUENAME\]</span></span>

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a><span data-ttu-id="3a13a-120">Selección de los archivos que se van a registrar en el archivo de registro de errores HTTP</span><span class="sxs-lookup"><span data-stu-id="3a13a-120">Selecting Fileds to Log in the HTTP Error Log File</span></span>

<span data-ttu-id="3a13a-121">La clave del registro **ErrorLoggingFields** se ha agregado para controlar los campos que se registran en el registro de errores http.</span><span class="sxs-lookup"><span data-stu-id="3a13a-121">The **ErrorLoggingFields** registry key has been added to control the fields logged into the HTTP error log.</span></span> <span data-ttu-id="3a13a-122">Estos valores del registro se encuentran en una \\ clave http Parameters, que se encuentra en:</span><span class="sxs-lookup"><span data-stu-id="3a13a-122">This registry values is located under an HTTP\\Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

<span data-ttu-id="3a13a-123">El valor del registro **ErrorLoggingFields** es un valor DWORD que contiene valores de bits para cada uno de los campos que se pueden registrar.</span><span class="sxs-lookup"><span data-stu-id="3a13a-123">The **ErrorLoggingFields** registry value is a DWORD value that contains bit values for each of the fields that can be logged.</span></span> <span data-ttu-id="3a13a-124">Para habilitar el registro de un campo específico, establezca el valor de bit correspondiente en 1 y reinicie el servicio HTTP.</span><span class="sxs-lookup"><span data-stu-id="3a13a-124">To enable logging of a specific field, set its corresponding bit value to 1 and restart the HTTP service.</span></span> <span data-ttu-id="3a13a-125">Para deshabilitar el registro, establezca el valor de bit en 0.</span><span class="sxs-lookup"><span data-stu-id="3a13a-125">To disable logging, set the bit value to 0.</span></span> <span data-ttu-id="3a13a-126">Para configurar varios campos, use una operación OR bit a bit de los valores individuales.</span><span class="sxs-lookup"><span data-stu-id="3a13a-126">To configure multiple fields, use a bitwise OR of the individual values.</span></span> <span data-ttu-id="3a13a-127">Por ejemplo, para activar los campos cookie y registro de referencia, el valor debe ser 0x00020000 \| 0x00040000 = 0x00060000.</span><span class="sxs-lookup"><span data-stu-id="3a13a-127">For example, to turn on the Cookie and Referrer logging fields, the value should be 0x00020000 \| 0x00040000 = 0x00060000.</span></span> <span data-ttu-id="3a13a-128">Si la clave del registro **ErrorLoggingFields** está ausente, se registran los campos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="3a13a-128">If the **ErrorLoggingFields** registry key is absent, the default fields are logged.</span></span> <span data-ttu-id="3a13a-129">El valor de **ErrorLoggingFields** para registrar los campos predeterminados es 0x7c884c7.</span><span class="sxs-lookup"><span data-stu-id="3a13a-129">The **ErrorLoggingFields** value to log the default fields is 0x7c884c7.</span></span> <span data-ttu-id="3a13a-130">Para habilitar el registro de todos los campos que se muestran en la tabla siguiente, establezca el valor en 0x7dff4e7.</span><span class="sxs-lookup"><span data-stu-id="3a13a-130">To enable logging for all the fields shown in the table below, set the value to 0x7dff4e7.</span></span>

<span data-ttu-id="3a13a-131">Los campos de registro de errores se muestran en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a13a-131">The error logging fields are listed in the following table:</span></span>



| <span data-ttu-id="3a13a-132">Campo de registro</span><span class="sxs-lookup"><span data-stu-id="3a13a-132">Log field</span></span>            | <span data-ttu-id="3a13a-133">Registrado de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="3a13a-133">Logged by default</span></span> | <span data-ttu-id="3a13a-134">Valor de bit</span><span class="sxs-lookup"><span data-stu-id="3a13a-134">Bit value</span></span>  |
|----------------------|-------------------|------------|
| <span data-ttu-id="3a13a-135">Date</span><span class="sxs-lookup"><span data-stu-id="3a13a-135">Date</span></span>                 | <span data-ttu-id="3a13a-136">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-136">Yes</span></span>               | <span data-ttu-id="3a13a-137">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3a13a-137">0x00000001</span></span> |
| <span data-ttu-id="3a13a-138">Hora</span><span class="sxs-lookup"><span data-stu-id="3a13a-138">Time</span></span>                 | <span data-ttu-id="3a13a-139">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-139">Yes</span></span>               | <span data-ttu-id="3a13a-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3a13a-140">0x00000002</span></span> |
| <span data-ttu-id="3a13a-141">Nombre del equipo servidor</span><span class="sxs-lookup"><span data-stu-id="3a13a-141">Server Computer Name</span></span> | <span data-ttu-id="3a13a-142">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-142">No</span></span>                | <span data-ttu-id="3a13a-143">0x00000020</span><span class="sxs-lookup"><span data-stu-id="3a13a-143">0x00000020</span></span> |
| <span data-ttu-id="3a13a-144">Dirección IP de cliente</span><span class="sxs-lookup"><span data-stu-id="3a13a-144">Client IP Address</span></span>    | <span data-ttu-id="3a13a-145">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-145">Yes</span></span>               | <span data-ttu-id="3a13a-146">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3a13a-146">0x00000004</span></span> |
| <span data-ttu-id="3a13a-147">Puerto de cliente</span><span class="sxs-lookup"><span data-stu-id="3a13a-147">Client Port</span></span>          | <span data-ttu-id="3a13a-148">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-148">Yes</span></span>               | <span data-ttu-id="3a13a-149">0x00400000</span><span class="sxs-lookup"><span data-stu-id="3a13a-149">0x00400000</span></span> |
| <span data-ttu-id="3a13a-150">Dirección IP del servidor</span><span class="sxs-lookup"><span data-stu-id="3a13a-150">Server IP Address</span></span>    | <span data-ttu-id="3a13a-151">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-151">Yes</span></span>               | <span data-ttu-id="3a13a-152">0x00000040</span><span class="sxs-lookup"><span data-stu-id="3a13a-152">0x00000040</span></span> |
| <span data-ttu-id="3a13a-153">Puerto del servidor</span><span class="sxs-lookup"><span data-stu-id="3a13a-153">Server Port</span></span>          | <span data-ttu-id="3a13a-154">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-154">Yes</span></span>               | <span data-ttu-id="3a13a-155">0x00008000</span><span class="sxs-lookup"><span data-stu-id="3a13a-155">0x00008000</span></span> |
| <span data-ttu-id="3a13a-156">Versión de protocolo</span><span class="sxs-lookup"><span data-stu-id="3a13a-156">Protocol Version</span></span>     | <span data-ttu-id="3a13a-157">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-157">Yes</span></span>               | <span data-ttu-id="3a13a-158">0x00080000</span><span class="sxs-lookup"><span data-stu-id="3a13a-158">0x00080000</span></span> |
| <span data-ttu-id="3a13a-159">Método</span><span class="sxs-lookup"><span data-stu-id="3a13a-159">Method</span></span>               | <span data-ttu-id="3a13a-160">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-160">Yes</span></span>               | <span data-ttu-id="3a13a-161">0x00000080</span><span class="sxs-lookup"><span data-stu-id="3a13a-161">0x00000080</span></span> |
| <span data-ttu-id="3a13a-162">URI</span><span class="sxs-lookup"><span data-stu-id="3a13a-162">URI</span></span>                  | <span data-ttu-id="3a13a-163">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-163">Yes</span></span>               | <span data-ttu-id="3a13a-164">0x00800000</span><span class="sxs-lookup"><span data-stu-id="3a13a-164">0x00800000</span></span> |
| <span data-ttu-id="3a13a-165">User Agent</span><span class="sxs-lookup"><span data-stu-id="3a13a-165">User Agent</span></span>           | <span data-ttu-id="3a13a-166">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-166">No</span></span>                | <span data-ttu-id="3a13a-167">0x00010000</span><span class="sxs-lookup"><span data-stu-id="3a13a-167">0x00010000</span></span> |
| <span data-ttu-id="3a13a-168">Cookie</span><span class="sxs-lookup"><span data-stu-id="3a13a-168">Cookie</span></span>               | <span data-ttu-id="3a13a-169">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-169">No</span></span>                | <span data-ttu-id="3a13a-170">0x00020000</span><span class="sxs-lookup"><span data-stu-id="3a13a-170">0x00020000</span></span> |
| <span data-ttu-id="3a13a-171">referencia</span><span class="sxs-lookup"><span data-stu-id="3a13a-171">referrer</span></span>             | <span data-ttu-id="3a13a-172">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-172">No</span></span>                | <span data-ttu-id="3a13a-173">0x00040000</span><span class="sxs-lookup"><span data-stu-id="3a13a-173">0x00040000</span></span> |
| <span data-ttu-id="3a13a-174">Host</span><span class="sxs-lookup"><span data-stu-id="3a13a-174">Host</span></span>                 | <span data-ttu-id="3a13a-175">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-175">No</span></span>                | <span data-ttu-id="3a13a-176">0x00100000</span><span class="sxs-lookup"><span data-stu-id="3a13a-176">0x00100000</span></span> |
| <span data-ttu-id="3a13a-177">Estado del Protocolo</span><span class="sxs-lookup"><span data-stu-id="3a13a-177">Protocol Status</span></span>      | <span data-ttu-id="3a13a-178">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-178">Yes</span></span>               | <span data-ttu-id="3a13a-179">0x00000400</span><span class="sxs-lookup"><span data-stu-id="3a13a-179">0x00000400</span></span> |
| <span data-ttu-id="3a13a-180">SC-Bytes</span><span class="sxs-lookup"><span data-stu-id="3a13a-180">SC-Bytes</span></span>             | <span data-ttu-id="3a13a-181">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-181">No</span></span>                | <span data-ttu-id="3a13a-182">0x00001000</span><span class="sxs-lookup"><span data-stu-id="3a13a-182">0x00001000</span></span> |
| <span data-ttu-id="3a13a-183">CS-Bytes</span><span class="sxs-lookup"><span data-stu-id="3a13a-183">CS-Bytes</span></span>             | <span data-ttu-id="3a13a-184">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-184">No</span></span>                | <span data-ttu-id="3a13a-185">0x00002000</span><span class="sxs-lookup"><span data-stu-id="3a13a-185">0x00002000</span></span> |
| <span data-ttu-id="3a13a-186">Tiempo empleado</span><span class="sxs-lookup"><span data-stu-id="3a13a-186">Time Taken</span></span>           | <span data-ttu-id="3a13a-187">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-187">No</span></span>                | <span data-ttu-id="3a13a-188">0x00004000</span><span class="sxs-lookup"><span data-stu-id="3a13a-188">0x00004000</span></span> |
| <span data-ttu-id="3a13a-189">Cuyo</span><span class="sxs-lookup"><span data-stu-id="3a13a-189">SiteId</span></span>               | <span data-ttu-id="3a13a-190">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-190">Yes</span></span>               | <span data-ttu-id="3a13a-191">0x01000000</span><span class="sxs-lookup"><span data-stu-id="3a13a-191">0x01000000</span></span> |
| <span data-ttu-id="3a13a-192">Frase del motivo</span><span class="sxs-lookup"><span data-stu-id="3a13a-192">Reason Phrase</span></span>        | <span data-ttu-id="3a13a-193">Sí</span><span class="sxs-lookup"><span data-stu-id="3a13a-193">Yes</span></span>               | <span data-ttu-id="3a13a-194">0x02000000</span><span class="sxs-lookup"><span data-stu-id="3a13a-194">0x02000000</span></span> |
| <span data-ttu-id="3a13a-195">Nombre de la cola</span><span class="sxs-lookup"><span data-stu-id="3a13a-195">Queue Name</span></span>           | <span data-ttu-id="3a13a-196">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-196">No</span></span>                | <span data-ttu-id="3a13a-197">0x04000000</span><span class="sxs-lookup"><span data-stu-id="3a13a-197">0x04000000</span></span> |
| <span data-ttu-id="3a13a-198">Identificador de flujo</span><span class="sxs-lookup"><span data-stu-id="3a13a-198">Stream Id</span></span>            | <span data-ttu-id="3a13a-199">No</span><span class="sxs-lookup"><span data-stu-id="3a13a-199">No</span></span>                | <span data-ttu-id="3a13a-200">0x????????</span><span class="sxs-lookup"><span data-stu-id="3a13a-200">0x????????</span></span> |



 

## <a name="time-and-date-rollover"></a><span data-ttu-id="3a13a-201">Sustitución de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="3a13a-201">Time and Date Rollover</span></span>

<span data-ttu-id="3a13a-202">De forma predeterminada, se crea un nuevo archivo de registro de errores HTTP (sustitución de archivos con términos) cuando el archivo de registro actual alcanza un tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="3a13a-202">By default, a new HTTP error log file is created (termed file rollover) when the current log file reaches a specified size.</span></span> <span data-ttu-id="3a13a-203">A partir de Windows Server 2003 con SP1, se pueden crear nuevos archivos de registro de errores en función de la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="3a13a-203">Starting with Windows Server 2003 with SP1, new error log files can be created based on date and time.</span></span> <span data-ttu-id="3a13a-204">La sustitución de fecha y hora se controla mediante dos nuevos valores del registro: **ErrorLoggingRolloverType** y **ErrorLoggingLocaltimeRollover**.</span><span class="sxs-lookup"><span data-stu-id="3a13a-204">Time and date rollover are controlled by two new registry values: **ErrorLoggingRolloverType** and **ErrorLoggingLocaltimeRollover**.</span></span> <span data-ttu-id="3a13a-205">Para habilitar la sustitución de fecha y hora, estos valores del registro se deben agregar al registro.</span><span class="sxs-lookup"><span data-stu-id="3a13a-205">To enable time and date rollover, these registry values must be added to the registry.</span></span> <span data-ttu-id="3a13a-206">El servicio http debe reiniciarse cuando estas claves se agreguen al registro.</span><span class="sxs-lookup"><span data-stu-id="3a13a-206">The Http service must be restarted when these keys are added to the registry.</span></span> <span data-ttu-id="3a13a-207">Las claves del registro de sustitución del archivo de registro se crean con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="3a13a-207">The log file rollover registry keys are created under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

<span data-ttu-id="3a13a-208">La clave del registro **ErrorLoggingRolloverType** indica el tipo de sustitución deseada y se establece de forma predeterminada en sustitución basada en el tamaño.</span><span class="sxs-lookup"><span data-stu-id="3a13a-208">The **ErrorLoggingRolloverType** registry key indicates the type of rollover desired and is by default set to size based rollover.</span></span> <span data-ttu-id="3a13a-209">La sustitución también puede configurarse para que se produzca diariamente, semanalmente, mensualmente o cada hora.</span><span class="sxs-lookup"><span data-stu-id="3a13a-209">Rollover can also be set to occur on a daily, weekly, monthly, or hourly basis.</span></span> <span data-ttu-id="3a13a-210">Cuando la sustitución de archivos se basa en el tiempo, un valor de **ErrorLoggingLocaltimeRollover** de 0 indica que la hora de sustitución se expresa en GMT y un valor de 1 indica que la hora de sustitución se expresa en hora local.</span><span class="sxs-lookup"><span data-stu-id="3a13a-210">When file rollover is based on time, an **ErrorLoggingLocaltimeRollover** value of 0 indicates that the rollover time is expressed in GMT, and a value of 1 indicates that the rollover time is expressed in local time.</span></span> <span data-ttu-id="3a13a-211">La clave **ErrorLoggingRolloverType** puede tomar un valor de 0 a 4, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="3a13a-211">The **ErrorLoggingRolloverType** key can take a value from 0 to 4 as listed in the following table.</span></span>



| <span data-ttu-id="3a13a-212">Valor de tipo de sustitución incremental</span><span class="sxs-lookup"><span data-stu-id="3a13a-212">Rollover type value</span></span> | <span data-ttu-id="3a13a-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a13a-213">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a13a-214">0</span><span class="sxs-lookup"><span data-stu-id="3a13a-214">0</span></span>                   | <span data-ttu-id="3a13a-215">Sustitución basada en el tamaño.</span><span class="sxs-lookup"><span data-stu-id="3a13a-215">Size based rollover.</span></span> <span data-ttu-id="3a13a-216">Los archivos de registro se revierten cuando el archivo alcanza el tamaño definido en la clave del registro **ErrorLogFileTruncateSize** .</span><span class="sxs-lookup"><span data-stu-id="3a13a-216">Log files are rolled over when the file reaches the size defined in the **ErrorLogFileTruncateSize** registry key.</span></span> |
| <span data-ttu-id="3a13a-217">1</span><span class="sxs-lookup"><span data-stu-id="3a13a-217">1</span></span>                   | <span data-ttu-id="3a13a-218">La sustitución del archivo de registro se produce diariamente.</span><span class="sxs-lookup"><span data-stu-id="3a13a-218">Log file rollover occurs daily.</span></span>                                                                                                         |
| <span data-ttu-id="3a13a-219">2</span><span class="sxs-lookup"><span data-stu-id="3a13a-219">2</span></span>                   | <span data-ttu-id="3a13a-220">La sustitución del archivo de registro se produce semanalmente.</span><span class="sxs-lookup"><span data-stu-id="3a13a-220">Log file rollover occurs weekly.</span></span>                                                                                                        |
| <span data-ttu-id="3a13a-221">3</span><span class="sxs-lookup"><span data-stu-id="3a13a-221">3</span></span>                   | <span data-ttu-id="3a13a-222">La sustitución del archivo de registro se produce mensualmente.</span><span class="sxs-lookup"><span data-stu-id="3a13a-222">Log file rollover occurs monthly.</span></span>                                                                                                       |
| <span data-ttu-id="3a13a-223">4</span><span class="sxs-lookup"><span data-stu-id="3a13a-223">4</span></span>                   | <span data-ttu-id="3a13a-224">La sustitución del archivo de registro se produce cada hora.</span><span class="sxs-lookup"><span data-stu-id="3a13a-224">Log file rollover occurs hourly.</span></span>                                                                                                        |



 

<span data-ttu-id="3a13a-225">Las convenciones de nomenclatura para los archivos que almacenan los registros de errores son diferentes para el tamaño, la fecha y la sustitución basada en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a13a-225">The naming conventions for files that store the error logs are different for size, date, and time based rollover.</span></span> <span data-ttu-id="3a13a-226">En la tabla siguiente se enumeran las convenciones de nomenclatura para los archivos de registro http.</span><span class="sxs-lookup"><span data-stu-id="3a13a-226">The following table lists the naming conventions for Http log files.</span></span>



| <span data-ttu-id="3a13a-227">Tipo Tollover</span><span class="sxs-lookup"><span data-stu-id="3a13a-227">Tollover type</span></span> | <span data-ttu-id="3a13a-228">Nombre del archivo de registro</span><span class="sxs-lookup"><span data-stu-id="3a13a-228">Log file name</span></span>  | <span data-ttu-id="3a13a-229">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a13a-229">Description</span></span>                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a13a-230">Size</span><span class="sxs-lookup"><span data-stu-id="3a13a-230">Size</span></span>          | <span data-ttu-id="3a13a-231">HTTPERRn. LOG</span><span class="sxs-lookup"><span data-stu-id="3a13a-231">HTTPERRn.LOG</span></span>   | <span data-ttu-id="3a13a-232">El archivo de registro se recicla cuando alcanza un tamaño específico.</span><span class="sxs-lookup"><span data-stu-id="3a13a-232">The log file is recycled when it reaches a specific size.</span></span> <span data-ttu-id="3a13a-233">n es el número de archivo y se incrementa cuando el archivo de registro se revierte.</span><span class="sxs-lookup"><span data-stu-id="3a13a-233">n is the file number and is incremented when the log file is rolled over.</span></span> |
| <span data-ttu-id="3a13a-234">Diario</span><span class="sxs-lookup"><span data-stu-id="3a13a-234">Daily</span></span>         | <span data-ttu-id="3a13a-235">htYYMMDD. log</span><span class="sxs-lookup"><span data-stu-id="3a13a-235">htYYMMDD.log</span></span>   | <span data-ttu-id="3a13a-236">El archivo de registro se recicla diariamente.</span><span class="sxs-lookup"><span data-stu-id="3a13a-236">The log file is recycled daily.</span></span>                                                                                                     |
| <span data-ttu-id="3a13a-237">Cada semana</span><span class="sxs-lookup"><span data-stu-id="3a13a-237">Weekly</span></span>        | <span data-ttu-id="3a13a-238">htYYMMww. log</span><span class="sxs-lookup"><span data-stu-id="3a13a-238">htYYMMww.log</span></span>   | <span data-ttu-id="3a13a-239">El archivo de registro se recicla semanalmente, donde WW es la semana del mes.</span><span class="sxs-lookup"><span data-stu-id="3a13a-239">The log file is recycled weekly, where ww is the week of the month.</span></span>                                                                 |
| <span data-ttu-id="3a13a-240">Mensual</span><span class="sxs-lookup"><span data-stu-id="3a13a-240">Monthly</span></span>       | <span data-ttu-id="3a13a-241">htYYMM. log</span><span class="sxs-lookup"><span data-stu-id="3a13a-241">htYYMM.log</span></span>     | <span data-ttu-id="3a13a-242">El archivo de registro se recicla cada mes.</span><span class="sxs-lookup"><span data-stu-id="3a13a-242">The log file is recycled every month.</span></span>                                                                                               |
| <span data-ttu-id="3a13a-243">Cada hora</span><span class="sxs-lookup"><span data-stu-id="3a13a-243">Hourly</span></span>        | <span data-ttu-id="3a13a-244">htYYMMDDhh. log</span><span class="sxs-lookup"><span data-stu-id="3a13a-244">htYYMMDDhh.log</span></span> | <span data-ttu-id="3a13a-245">El archivo de registro se recicla cada hora, donde HH es la hora del día expresada en notación de 0-24 hora.</span><span class="sxs-lookup"><span data-stu-id="3a13a-245">The log file is recycled hourly, where hh is the hour of the day expressed in 0-24 hour notation.</span></span>                                   |



 

 

 




