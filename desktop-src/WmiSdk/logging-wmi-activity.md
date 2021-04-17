---
description: Ya no se admiten los archivos de registro de WMI.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Registrar la actividad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697367"
---
# <a name="logging-wmi-activity"></a><span data-ttu-id="b9096-103">Registrar la actividad WMI</span><span class="sxs-lookup"><span data-stu-id="b9096-103">Logging WMI Activity</span></span>

<span data-ttu-id="b9096-104">Ya no se admiten los archivos de registro de WMI.</span><span class="sxs-lookup"><span data-stu-id="b9096-104">The WMI log files are no longer supported.</span></span> <span data-ttu-id="b9096-105">A partir de Windows Vista, WMI utiliza el [seguimiento de eventos para Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) y los eventos que están disponibles a través de la interfaz de usuario de **visor de eventos** o la herramienta de línea de comandos wevtutil.</span><span class="sxs-lookup"><span data-stu-id="b9096-105">Starting with Windows Vista, WMI uses [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) and events that are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="b9096-106">Para obtener más información, vea el proveedor ETW y la documentación de línea de comandos de [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="b9096-106">For more information, see the ETW provider and the [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) command-line documentation.</span></span>

<span data-ttu-id="b9096-107">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="b9096-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="b9096-108">Archivos de registro de WMI antes de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9096-108">WMI Log Files Before Windows Vista</span></span>](#wmi-log-files-before-windows-vista)
-   [<span data-ttu-id="b9096-109">Actividades de registro para componentes principales de WMI antes de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9096-109">Logging Activities for WMI Core Components Before Windows Vista</span></span>](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [<span data-ttu-id="b9096-110">Actividades de registro para componentes de proveedor WMI antes de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9096-110">Logging Activities for WMI Provider Components Before Windows Vista</span></span>](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [<span data-ttu-id="b9096-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9096-111">Related topics</span></span>](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a><span data-ttu-id="b9096-112">Archivos de registro de WMI antes de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9096-112">WMI Log Files Before Windows Vista</span></span>

<span data-ttu-id="b9096-113">Los archivos de registro creados por WMI y varios proveedores registran: eventos, datos de seguimiento o diagnósticos, errores y diversas actividades.</span><span class="sxs-lookup"><span data-stu-id="b9096-113">The log files created by WMI and various providers record: events, trace or diagnostic data, errors, and various activities.</span></span> <span data-ttu-id="b9096-114">Solo los administradores tienen acceso de lectura a la carpeta de registro de WMI que se encuentra en% WINDIR% \\ system32 \\ WBEM \\ logs.</span><span class="sxs-lookup"><span data-stu-id="b9096-114">Only administrators have read access to the WMI log folder found at %windir%\\system32\\wbem\\logs.</span></span>

<span data-ttu-id="b9096-115">Solo los componentes principales de WMI o los proveedores de WMI escriben en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="b9096-115">Only WMI core components or WMI providers write to log files.</span></span> <span data-ttu-id="b9096-116">Solo puede leer o ver los datos de estos registros con fines de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="b9096-116">You can only read or view the data in these logs for diagnostic purposes.</span></span> <span data-ttu-id="b9096-117">Puede crear y almacenar sus propios archivos de registro en el directorio de registro de WMI.</span><span class="sxs-lookup"><span data-stu-id="b9096-117">You can create and store your own log files in the WMI log directory.</span></span>

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a><span data-ttu-id="b9096-118">Actividades de registro para componentes principales de WMI antes de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9096-118">Logging Activities for WMI Core Components Before Windows Vista</span></span>

<span data-ttu-id="b9096-119">Estos archivos no contienen un formato coherente que sea adecuado para leer mediante programación.</span><span class="sxs-lookup"><span data-stu-id="b9096-119">These files do not contain a consistent format that is suitable for reading programmatically.</span></span> <span data-ttu-id="b9096-120">Para obtener más información acerca de registros específicos, consulte [archivos de registro de WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="b9096-120">For more information about specific logs, see [WMI Log Files](wmi-log-files.md).</span></span>

<span data-ttu-id="b9096-121">Las actividades de registro de los componentes principales de WMI se producen cuando se establecen las siguientes claves del registro:</span><span class="sxs-lookup"><span data-stu-id="b9096-121">Logging activities for WMI core components occurs when the following registry keys are set:</span></span>

-   <span data-ttu-id="b9096-122">Nivel de registro</span><span class="sxs-lookup"><span data-stu-id="b9096-122">Logging level</span></span>

    <span data-ttu-id="b9096-123">Los cambios en el valor del registro del nivel de registro surten efecto inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b9096-123">Changes to the logging level registry value take effect immediately.</span></span> <span data-ttu-id="b9096-124">No es necesario reiniciar el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="b9096-124">No restart of the WMI service is necessary.</span></span>

    <span data-ttu-id="b9096-125">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging** = 2</span><span class="sxs-lookup"><span data-stu-id="b9096-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging** = 2</span></span>

    <span data-ttu-id="b9096-126">En la lista siguiente se enumeran los niveles de registro que se pueden definir en el registro.</span><span class="sxs-lookup"><span data-stu-id="b9096-126">The following list lists the logging levels that can be defined in the registry.</span></span>

    

    | <span data-ttu-id="b9096-127">Nivel de registro</span><span class="sxs-lookup"><span data-stu-id="b9096-127">Logging level</span></span> | <span data-ttu-id="b9096-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9096-128">Description</span></span>               |
    |---------------|---------------------------|
    | <span data-ttu-id="b9096-129">0</span><span class="sxs-lookup"><span data-stu-id="b9096-129">0</span></span>             | <span data-ttu-id="b9096-130">Sin registro</span><span class="sxs-lookup"><span data-stu-id="b9096-130">No Logging</span></span>                |
    | <span data-ttu-id="b9096-131">1</span><span class="sxs-lookup"><span data-stu-id="b9096-131">1</span></span>             | <span data-ttu-id="b9096-132">Registrar solo errores</span><span class="sxs-lookup"><span data-stu-id="b9096-132">Log only errors</span></span>           |
    | <span data-ttu-id="b9096-133">2</span><span class="sxs-lookup"><span data-stu-id="b9096-133">2</span></span>             | <span data-ttu-id="b9096-134">Registro detallado (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="b9096-134">Verbose Logging (default)</span></span> |

    

     

-   <span data-ttu-id="b9096-135">Ubicación del archivo de registro</span><span class="sxs-lookup"><span data-stu-id="b9096-135">Log file location</span></span>

    <span data-ttu-id="b9096-136">Para que los cambios en la ubicación del archivo de registro surtan efecto, reinicie el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="b9096-136">For changes to log file location to take effect, restart the WMI service.</span></span>

    <span data-ttu-id="b9096-137">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Logging Directory** =% WINDIR% \\ system32 \\ WBEM \\ registros</span><span class="sxs-lookup"><span data-stu-id="b9096-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging Directory** = %windir%\\system32\\wbem\\logs</span></span>

-   <span data-ttu-id="b9096-138">Tamaño máximo del archivo de registro, en bytes</span><span class="sxs-lookup"><span data-stu-id="b9096-138">Maximum log file size, in bytes</span></span>

    <span data-ttu-id="b9096-139">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **archivo de registro tamaño máximo** = 65536</span><span class="sxs-lookup"><span data-stu-id="b9096-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Log File Max Size** = 65536</span></span>

<span data-ttu-id="b9096-140">Puede cambiar estos valores de clave del registro a través del editor del registro o mediante el complemento WMI de Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="b9096-140">You can change these registry key values through the Registry Editor or through the WMI snap-in for the Microsoft Management Console.</span></span>

<span data-ttu-id="b9096-141">**Para establecer el nivel de registro para WMI antes de Windows Vista**</span><span class="sxs-lookup"><span data-stu-id="b9096-141">**To set the logging level for WMI before Windows Vista**</span></span>

1.  <span data-ttu-id="b9096-142">Haga clic en **Inicio** y, a continuación, haga clic en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="b9096-142">Click **Start**, and then click **Run**.</span></span>
2.  <span data-ttu-id="b9096-143">Escriba **wmimgmt. msc**</span><span class="sxs-lookup"><span data-stu-id="b9096-143">Type **wmimgmt.msc**</span></span>
3.  <span data-ttu-id="b9096-144">En el menú **Acción**, haga clic en **Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="b9096-144">On the **Action** menu, click **Properties**.</span></span>
4.  <span data-ttu-id="b9096-145">En la pestaña **registro** , establezca el nivel de registro en **deshabilitado**, **habilitado** o **detallado**.</span><span class="sxs-lookup"><span data-stu-id="b9096-145">On the **Logging** tab, set the logging level to **Disabled**, **Enabled**, or **Verbose**.</span></span>
5.  <span data-ttu-id="b9096-146">En **Ubicación:**, escriba la ruta de acceso a la carpeta del archivo de registro y en **tamaño máximo (bytes):**, establezca el tamaño máximo, en bytes, del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b9096-146">In **Location:**, type the path to the log file folder and in **Maximum size (bytes):**, set the maximum size, in bytes, of the log file.</span></span>

<span data-ttu-id="b9096-147">Para obtener más información acerca de cómo establecer las propiedades del archivo de registro, vea la ayuda en pantalla de la aplicación de control WMI.</span><span class="sxs-lookup"><span data-stu-id="b9096-147">For more information about setting the log file properties, see the online Help for the WMI Control application.</span></span>

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a><span data-ttu-id="b9096-148">Actividades de registro para componentes de proveedor WMI antes de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9096-148">Logging Activities for WMI Provider Components Before Windows Vista</span></span>

<span data-ttu-id="b9096-149">Cuando está habilitado el registro de componentes principales de WMI, el registro también está habilitado para cualquier proveedor con capacidades de registro.</span><span class="sxs-lookup"><span data-stu-id="b9096-149">When logging for WMI core components is enabled, logging is also enabled for any provider with logging capabilities.</span></span>

<span data-ttu-id="b9096-150">En la lista siguiente se enumeran los valores necesarios.</span><span class="sxs-lookup"><span data-stu-id="b9096-150">The following list lists the required values.</span></span>

<dl> <dt>

<span data-ttu-id="b9096-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**Filesystem**</span><span class="sxs-lookup"><span data-stu-id="b9096-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span></span>
</dt> <dd>

<span data-ttu-id="b9096-152">Ruta de acceso completa y nombre de archivo del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b9096-152">Full path and file name of the log file.</span></span> <span data-ttu-id="b9096-153">El valor predeterminado es% WINDIR% \\ system32 \\ WBEM \\ logs.</span><span class="sxs-lookup"><span data-stu-id="b9096-153">The default value is %windir%\\system32\\wbem\\logs.</span></span> <span data-ttu-id="b9096-154">El **tipo** denominado Value debe establecerse en = file para que se use este valor con nombre.</span><span class="sxs-lookup"><span data-stu-id="b9096-154">The **Type** named value must be set to = File for this named value to be used.</span></span>

</dd> <dt>

<span data-ttu-id="b9096-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Dosis**</span><span class="sxs-lookup"><span data-stu-id="b9096-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Level**</span></span>
</dt> <dd>

<span data-ttu-id="b9096-156">Máscara lógica de 32 bits que define el tipo de resultado de depuración generado por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="b9096-156">A 32-bit logical mask that defines the type of debugging output generated by the provider.</span></span> <span data-ttu-id="b9096-157">Este valor depende del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b9096-157">This value is provider-dependent.</span></span> <span data-ttu-id="b9096-158">El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="b9096-158">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="b9096-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="b9096-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span></span>
</dt> <dd>

<span data-ttu-id="b9096-160">Tamaño máximo de archivo, en bytes, del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b9096-160">Maximum file size, in bytes, of the log file.</span></span> <span data-ttu-id="b9096-161">Este valor entero debe estar en el intervalo de 1024 a 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="b9096-161">This integer value must be in the range 1024 to 2^32-1.</span></span> <span data-ttu-id="b9096-162">Cuando el tamaño del archivo supera este valor, se cambia el nombre del archivo a **~ filename** y se crea un nuevo archivo de registro vacío.</span><span class="sxs-lookup"><span data-stu-id="b9096-162">When the file size exceeds this value, the file is renamed to **~filename** and a new, empty log file is created.</span></span> <span data-ttu-id="b9096-163">El espacio en disco necesario para el archivo de registro es dos veces el valor de **maxfilesize**.</span><span class="sxs-lookup"><span data-stu-id="b9096-163">The disk space required for the log file is twice the value of **MaxFileSize**.</span></span> <span data-ttu-id="b9096-164">El valor predeterminado es 65.535.</span><span class="sxs-lookup"><span data-stu-id="b9096-164">The default value is 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="b9096-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Automáticamente**</span><span class="sxs-lookup"><span data-stu-id="b9096-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span>
</dt> <dd>

<span data-ttu-id="b9096-166">Se puede establecer en = File o = Debugger.</span><span class="sxs-lookup"><span data-stu-id="b9096-166">Can be set to = File or = Debugger.</span></span> <span data-ttu-id="b9096-167">Si se establece en = File, la información de seguimiento se escribe en el archivo de registro especificado en el **archivo** denominado Value.</span><span class="sxs-lookup"><span data-stu-id="b9096-167">If set to = File, the trace information is written to the log file specified in the **File** named value.</span></span> <span data-ttu-id="b9096-168">El valor predeterminado es = archivo.</span><span class="sxs-lookup"><span data-stu-id="b9096-168">The default value is = File.</span></span>

</dd> </dl>

<span data-ttu-id="b9096-169">Por ejemplo, para registrar consultas y obtener llamadas de instancia desde el proveedor de vistas, use los siguientes valores de clave del registro.</span><span class="sxs-lookup"><span data-stu-id="b9096-169">For example, to log query and get instance calls from the View Provider, use the following registry key values.</span></span> <span data-ttu-id="b9096-170">El registro se ubicará en la carpeta de registro y tendrá el tamaño de archivo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b9096-170">The log will be located in the log folder and will be the default file size.</span></span>

<span data-ttu-id="b9096-171">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **File** = C: \\ Windows \\ system32 \\ WBEM \\ logs \\ ViewProvider. log</span><span class="sxs-lookup"><span data-stu-id="b9096-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**File** = C:\\Windows\\system32\\WBEM\\Logs\\ViewProvider.log</span></span>

<span data-ttu-id="b9096-172">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **LEVEL** = 2</span><span class="sxs-lookup"><span data-stu-id="b9096-172">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Level** = 2</span></span>

<span data-ttu-id="b9096-173">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **maxfilesize** = 65535</span><span class="sxs-lookup"><span data-stu-id="b9096-173">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**MaxFileSize** = 65535</span></span>

<span data-ttu-id="b9096-174">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **providers** \\ **Logging** \\ **ViewProvider** \\ **Type** = File</span><span class="sxs-lookup"><span data-stu-id="b9096-174">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Type** = File</span></span>

> [!Note]  
> <span data-ttu-id="b9096-175">Para sus propios proveedores con capacidades de registro, debe escribir las claves y los valores del registro necesarios para habilitar el registro.</span><span class="sxs-lookup"><span data-stu-id="b9096-175">For your own providers with logging capabilities, you need to write the necessary registry keys and values to enable logging.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b9096-176">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9096-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9096-177">Solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="b9096-177">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="b9096-178">Archivos de registro de WMI</span><span class="sxs-lookup"><span data-stu-id="b9096-178">WMI Log Files</span></span>](wmi-log-files.md)
</dt> <dt>

[<span data-ttu-id="b9096-179">Clases de solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="b9096-179">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> <dt>

[<span data-ttu-id="b9096-180">Seguimiento de la actividad WMI</span><span class="sxs-lookup"><span data-stu-id="b9096-180">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> </dl>

 

 
