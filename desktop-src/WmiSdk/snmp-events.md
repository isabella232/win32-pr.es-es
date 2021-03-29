---
description: El proveedor SNMP permite escribir en archivos de registro y en el depurador.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventos de SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648279"
---
# <a name="snmp-events"></a><span data-ttu-id="fff85-103">Eventos de SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-103">SNMP Events</span></span>

<span data-ttu-id="fff85-104">El proveedor SNMP permite escribir en archivos de registro y en el depurador.</span><span class="sxs-lookup"><span data-stu-id="fff85-104">The SNMP provider supports writing to log files and to the debugger.</span></span>

> [!Note]  
> <span data-ttu-id="fff85-105">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fff85-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="fff85-106">Un número de claves y valores del registro define el nivel y el tipo de registro que se está generando actualmente:</span><span class="sxs-lookup"><span data-stu-id="fff85-106">A number of registry keys and values define the level and type of logging currently being generated:</span></span>

-   <span data-ttu-id="fff85-107">Depuración</span><span class="sxs-lookup"><span data-stu-id="fff85-107">Debugging</span></span>

    <span data-ttu-id="fff85-108">La clave del registro **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ providers \\ Logging** contiene el valor de registro que indica si la información se puede escribir en el depurador.</span><span class="sxs-lookup"><span data-stu-id="fff85-108">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING** registry key contains the logging value that indicates whether information can be written to the debugger.</span></span> <span data-ttu-id="fff85-109">El valor de registro se establece en 0 para deshabilitar la salida de la depuración o en 1 para habilitarla.</span><span class="sxs-lookup"><span data-stu-id="fff85-109">The logging value is set either to 0 to disable debugging output or 1 to enable it.</span></span> <span data-ttu-id="fff85-110">El registro es un \_ valor de REG DWORD.</span><span class="sxs-lookup"><span data-stu-id="fff85-110">Logging is a REG\_DWORD value.</span></span>

-   <span data-ttu-id="fff85-111">Registro</span><span class="sxs-lookup"><span data-stu-id="fff85-111">Logging</span></span>

    <span data-ttu-id="fff85-112">La clave del registro **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ providers \\ Logging \\ WBEMSNMP** contiene toda la información de registro específica del proveedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="fff85-112">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING\\WBEMSNMP** registry key holds all of the logging information specific to the SNMP provider.</span></span> <span data-ttu-id="fff85-113">En la tabla siguiente se enumeran los valores asociados a esta clave.</span><span class="sxs-lookup"><span data-stu-id="fff85-113">The following table lists the values associated with this key.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fff85-114">Value</span><span class="sxs-lookup"><span data-stu-id="fff85-114">Value</span></span></th>
<th><span data-ttu-id="fff85-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fff85-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fff85-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="fff85-116">Type</span></span></td>
<td><span data-ttu-id="fff85-117"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="fff85-117"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="fff85-118">Toma uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="fff85-118">Takes one of the following values:</span></span><br/> <span data-ttu-id="fff85-119">&quot;File &quot; = (valor predeterminado) envía la salida de depuración a un archivo.</span><span class="sxs-lookup"><span data-stu-id="fff85-119">&quot;File&quot; = (Default) Sends debugging output to a file.</span></span><br/> <span data-ttu-id="fff85-120">&quot;Debugger &quot; = envía la salida de depuración al depurador.</span><span class="sxs-lookup"><span data-stu-id="fff85-120">&quot;Debugger&quot; = Sends debugging output to the debugger.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fff85-121">MaxFileSize</span><span class="sxs-lookup"><span data-stu-id="fff85-121">MaxFileSize</span></span></td>
<td><span data-ttu-id="fff85-122"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="fff85-122"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="fff85-123">Toma valores enteros de 1024 a 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="fff85-123">Takes integer values from 1024 to 2^32-1.</span></span> <span data-ttu-id="fff85-124">El valor es el tamaño máximo permitido en bytes para el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="fff85-124">The value is the maximum allowed size in bytes for the log file.</span></span> <span data-ttu-id="fff85-125">Si es menor que 1024, el mecanismo de registro usa un valor de 1024.</span><span class="sxs-lookup"><span data-stu-id="fff85-125">If less than 1024, the logging mechanism uses a value of 1024.</span></span> <span data-ttu-id="fff85-126">Se recomienda un tamaño mínimo de 8 KB para este valor.</span><span class="sxs-lookup"><span data-stu-id="fff85-126">A minimum size of 8 KB is recommended for this value.</span></span> <span data-ttu-id="fff85-127">Cuando el archivo alcanza el tamaño especificado por MaxFileSize, el nombre de archivo se antepone con un carácter ' ~ ' y se crea un archivo nuevo.</span><span class="sxs-lookup"><span data-stu-id="fff85-127">When the file reaches the size specified by MaxFileSize, the file name is prepended with a '~' character and a new file is created.</span></span> <span data-ttu-id="fff85-128">Por lo tanto, el espacio en disco máximo necesario para el registro es el doble de este valor.</span><span class="sxs-lookup"><span data-stu-id="fff85-128">Therefore, the maximum disk space required for logging is twice this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fff85-129">Archivo</span><span class="sxs-lookup"><span data-stu-id="fff85-129">File</span></span></td>
<td><span data-ttu-id="fff85-130"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="fff85-130"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="fff85-131">Define el nombre del archivo al que se envía la salida de depuración cuando el tipo de registro se establece en ' file '.</span><span class="sxs-lookup"><span data-stu-id="fff85-131">Defines the name of the file to which the debugging output is sent when the logging type is set to 'File'.</span></span> <span data-ttu-id="fff85-132">El valor predeterminado es " <WBEMLOGS> \wbemsnmp.log.".</span><span class="sxs-lookup"><span data-stu-id="fff85-132">The default value is '<WBEMLOGS>\wbemsnmp.log.'</span></span> <span data-ttu-id="fff85-133">Si <WBEMLOGS> no se puede determinar el directorio en la sección del registro WMI, el valor predeterminado es "c:\wbemsnmp.log".</span><span class="sxs-lookup"><span data-stu-id="fff85-133">If the <WBEMLOGS> directory cannot be determined from the WMI registry section, the value defaults to 'c:\wbemsnmp.log'.</span></span> <span data-ttu-id="fff85-134">Si se usa un recurso compartido, como \\ machine\share\wbemsnmp.log o M:\wbemsnmp.log, donde M: es \\ machine\share, la cuenta de sistema local en la que se ejecuta WMI debe tener derechos de acceso de lectura y escritura en \\ machine\share.</span><span class="sxs-lookup"><span data-stu-id="fff85-134">If a share is used, such as \\machine\share\wbemsnmp.log or M:\wbemsnmp.log where M: is \\machine\share, the local SYSTEM account on which WMI runs must have read/write access rights to the \\machine\share.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fff85-135">Nivel</span><span class="sxs-lookup"><span data-stu-id="fff85-135">Level</span></span></td>
<td><span data-ttu-id="fff85-136"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="fff85-136"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="fff85-137">Toma valores enteros de 0 a 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="fff85-137">Takes integer values from 0 through 2^32-1.</span></span> <span data-ttu-id="fff85-138">El valor es una máscara lógica que consta de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fff85-138">The value is a logical mask consisting of 32 bits.</span></span> <span data-ttu-id="fff85-139">Las siguientes máscaras de bits se combinan para definir el tipo de salida de depuración generada:</span><span class="sxs-lookup"><span data-stu-id="fff85-139">The following bit masks are combined to define the type of debugging output generated:</span></span><br/>
<ul>
<li><span data-ttu-id="fff85-140">0: invocación del método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del proveedor de clases SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-140">0: SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="fff85-141">1: implementación del proveedor de clase SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-141">1: SNMP class provider implementation</span></span></li>
<li><span data-ttu-id="fff85-142">2: invocaciones del método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del proveedor de instancias SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-142">2: SNMP instance provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="fff85-143">3: implementación del proveedor de instancias SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-143">3: SNMP instance provider implementation</span></span></li>
<li><span data-ttu-id="fff85-144">4: biblioteca de clases SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-144">4: SNMP class library</span></span></li>
<li><span data-ttu-id="fff85-145">5: SNMP SMIR</span><span class="sxs-lookup"><span data-stu-id="fff85-145">5: SNMP SMIR</span></span></li>
<li><span data-ttu-id="fff85-146">6: correlación de SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-146">6: SNMP correlator</span></span></li>
<li><span data-ttu-id="fff85-147">7: código de asignación de tipo de SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-147">7: SNMP type mapping code</span></span></li>
<li><span data-ttu-id="fff85-148">8: código de subprocesos SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-148">8: SNMP threading code</span></span></li>
<li><span data-ttu-id="fff85-149">9: implementación e interfaces del proveedor de eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="fff85-149">9: SNMP event provider interfaces and implementation</span></span></li>
</ul>
<span data-ttu-id="fff85-150">Establezca el nivel en (2 ^ 0 + 2 ^ 8 =) 257 para las operaciones que implican llamadas a los métodos <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> del proveedor de clase SNMP y las operaciones que usan código de subprocesos SNMP.</span><span class="sxs-lookup"><span data-stu-id="fff85-150">Set Level to (2^0 + 2^8=) 257 for operations involving calls to the SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> methods, and operations using SNMP threading code.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




