---
title: Configuración del registro de errores de la API del servidor HTTP
description: El registro de errores de la API del servidor HTTP se controla mediante tres valores del registro bajo una \\ clave http Parameters.
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- API de servidor HTTP, configurar registros de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418676"
---
# <a name="configuring-http-server-api-error-logging"></a><span data-ttu-id="b518d-104">Configuración del registro de errores de la API del servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="b518d-104">Configuring HTTP Server API Error Logging</span></span>

<span data-ttu-id="b518d-105">El registro de errores de la API del servidor HTTP se controla mediante tres valores del registro bajo una clave **http** \\ **Parameters** , que se encuentra en:</span><span class="sxs-lookup"><span data-stu-id="b518d-105">The HTTP Server API error logging is controlled by three registry values under an **HTTP**\\**Parameters** key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> <span data-ttu-id="b518d-106">La ubicación y la forma de los valores de configuración pueden cambiar en versiones futuras del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="b518d-106">The location and form of the configuration values may change in future versions of the Windows operating system.</span></span>

 

<span data-ttu-id="b518d-107">Un usuario debe tener privilegios de administrador o sistema local para modificar los valores del registro y ver o modificar los archivos de registro y la carpeta que los contiene.</span><span class="sxs-lookup"><span data-stu-id="b518d-107">A user must have Administrator/Local System privileges to modify the registry values, and view or modify the log files and the folder that contains them.</span></span>

<span data-ttu-id="b518d-108">La información de configuración de los valores del registro se lee cuando se inicia el controlador de la API del servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="b518d-108">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="b518d-109">Como resultado, si se cambia la configuración, el controlador debe detenerse y reiniciarse para leer los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="b518d-109">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="b518d-110">Esto puede realizarse mediante los siguientes comandos de la consola:</span><span class="sxs-lookup"><span data-stu-id="b518d-110">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="b518d-111">**net stop http**</span><span class="sxs-lookup"><span data-stu-id="b518d-111">**net stop http**</span></span>

<span data-ttu-id="b518d-112">**net start http**</span><span class="sxs-lookup"><span data-stu-id="b518d-112">**net start http**</span></span>

<span data-ttu-id="b518d-113">Los nombres de los archivos de registro se denominan mediante la Convención siguiente:</span><span class="sxs-lookup"><span data-stu-id="b518d-113">The log files are named by using the following convention:</span></span>

<span data-ttu-id="b518d-114">**httperr +** *SequenceNumber* **+. log**</span><span class="sxs-lookup"><span data-stu-id="b518d-114">**httperr +** *SequenceNumber* **+ .log**</span></span>

<span data-ttu-id="b518d-115">Por ejemplo: "httperr4. log".</span><span class="sxs-lookup"><span data-stu-id="b518d-115">For example: "httperr4.log".</span></span>

<span data-ttu-id="b518d-116">Los archivos de registro se recorren cuando alcanzan el tamaño máximo especificado por el valor del registro **ErrorLogFileTruncateSize** y el valor no puede ser inferior a un megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="b518d-116">Log files are cycled when they reach the maximum size specified by the **ErrorLogFileTruncateSize** registry value, and the value cannot be less than one megabyte (MB).</span></span>

<span data-ttu-id="b518d-117">Si la configuración del registro de errores no es válida o se produce algún tipo de error al escribir en los archivos de registro, la API del servidor HTTP utiliza el registro de eventos para notificar a los administradores que no se ha producido el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="b518d-117">If the configuration of error logging is invalid or any kind of failure occurs while writing to the log files, the HTTP Server API uses event logging to notify administrators that error logging did not take place.</span></span>

<span data-ttu-id="b518d-118">En la tabla siguiente se describen los valores de configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="b518d-118">Registry configuration values are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b518d-119">Valor del registro</span><span class="sxs-lookup"><span data-stu-id="b518d-119">Registry Value</span></span></th>
<th><span data-ttu-id="b518d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b518d-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b518d-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span><span class="sxs-lookup"><span data-stu-id="b518d-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span></span><br/></td>
<td><span data-ttu-id="b518d-122">Un <strong>valor DWORD</strong> que se puede establecer en <strong>true</strong> para habilitar el registro de errores o <strong>false</strong> para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="b518d-122">A <strong>DWORD</strong> that can be set to <strong>TRUE</strong> to enable error logging, or <strong>FALSE</strong> to disable it.</span></span> <span data-ttu-id="b518d-123">El valor predeterminado es <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="b518d-123">The default value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b518d-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span><span class="sxs-lookup"><span data-stu-id="b518d-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span></span><br/></td>
<td><span data-ttu-id="b518d-125"><strong>DWORD</strong> que especifica el tamaño máximo de un archivo de registro de errores, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b518d-125">A <strong>DWORD</strong> that specifies the maximum size of an error log file, in bytes.</span></span> <span data-ttu-id="b518d-126">El valor predeterminado es 1 MB (0x100000).</span><span class="sxs-lookup"><span data-stu-id="b518d-126">The default value is one MB (0x100000).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b518d-127">El valor especificado no puede ser menor que el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b518d-127">The specified value cannot be smaller than the default value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b518d-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span><span class="sxs-lookup"><span data-stu-id="b518d-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span></span><br/></td>
<td><span data-ttu-id="b518d-129"><strong>Cadena</strong> que especifica la carpeta en la que la API del servidor http coloca los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="b518d-129">A <strong>String</strong> that specifies the folder under which the HTTP Server API places its logging files.</span></span> <br/> <span data-ttu-id="b518d-130">La API del servidor HTTP crea una subcarpeta denominada &quot; HTTPERR &quot; en la carpeta especificada en la que se colocan los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="b518d-130">The HTTP Server API creates a subfolder named &quot;HTTPERR&quot; under the specified folder into which the log files are placed.</span></span> <span data-ttu-id="b518d-131">Esta subcarpeta y los archivos de registro reciben la misma configuración de permisos, lo que significa que las cuentas de administrador y del sistema local tienen acceso completo, mientras que otros usuarios no tienen acceso.</span><span class="sxs-lookup"><span data-stu-id="b518d-131">This subfolder and the log files receive the same permission settings, which means that Administrator and Local System Accounts have full access, while other users do not have access.</span></span><br/> <span data-ttu-id="b518d-132">Si no se especifica una carpeta en el registro, la carpeta predeterminada es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="b518d-132">If a folder is not specified in the registry, the default folder is the following:</span></span><br/> <span data-ttu-id="b518d-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span><span class="sxs-lookup"><span data-stu-id="b518d-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b518d-134">El valor de cadena ErrorLoggingDir debe ser una ruta de acceso completa, pero puede contener &quot; % systemroot% &quot; .</span><span class="sxs-lookup"><span data-stu-id="b518d-134">The ErrorLoggingDir string value must be a fully qualified path, but it can contain &quot;%SystemRoot%&quot;.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





