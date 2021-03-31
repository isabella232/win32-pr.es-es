---
description: A partir de Windows Vista, el servicio WMI no utiliza los archivos de registro de WMI. En su lugar, utiliza el seguimiento de eventos para Windows (ETW) y los eventos están disponibles a través de Visor de eventos o la herramienta de línea de comandos wevtutil.
ms.assetid: bb6401e8-caf7-4f39-ab64-b7532723ce9a
ms.tgt_platform: multiple
title: Seguimiento de la actividad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14371a4f18b81019073cd2b428500b12385719e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815699"
---
# <a name="tracing-wmi-activity"></a><span data-ttu-id="2ba15-104">Seguimiento de la actividad WMI</span><span class="sxs-lookup"><span data-stu-id="2ba15-104">Tracing WMI Activity</span></span>

<span data-ttu-id="2ba15-105">A partir de Windows Vista, el servicio WMI no utiliza los [archivos de registro de WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="2ba15-105">Starting with Windows Vista, the WMI service does not use the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="2ba15-106">En su lugar, utiliza el [seguimiento de eventos para Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) y los eventos están disponibles a través de **visor de eventos** o la herramienta de línea de comandos wevtutil.</span><span class="sxs-lookup"><span data-stu-id="2ba15-106">Instead, it uses [Event Tracing for Windows (ETW)](/windows/desktop/ETW/event-tracing-portal) and events are available through **Event Viewer** or the Wevtutil command-line tool.</span></span>

<span data-ttu-id="2ba15-107">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="2ba15-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="2ba15-108">Obtención de eventos de WMI a través de Visor de eventos</span><span class="sxs-lookup"><span data-stu-id="2ba15-108">Obtaining WMI Events Through Event Viewer</span></span>](#obtaining-wmi-events-through-event-viewer)
-   [<span data-ttu-id="2ba15-109">Habilitación del seguimiento de WMI en el símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="2ba15-109">Enabling WMI Tracing at Command Prompt</span></span>](#enabling-wmi-tracing-at-command-prompt)
-   [<span data-ttu-id="2ba15-110">Uso del seguimiento de WMI basado en WPP</span><span class="sxs-lookup"><span data-stu-id="2ba15-110">Using WPP-based WMI Tracing</span></span>](#using-wpp-based-wmi-tracing)
-   [<span data-ttu-id="2ba15-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ba15-111">Related topics</span></span>](#related-topics)

## <a name="obtaining-wmi-events-through-event-viewer"></a><span data-ttu-id="2ba15-112">Obtención de eventos de WMI a través de Visor de eventos</span><span class="sxs-lookup"><span data-stu-id="2ba15-112">Obtaining WMI Events Through Event Viewer</span></span>

<span data-ttu-id="2ba15-113">El archivo WMITracing. log contiene los eventos de seguimiento de WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba15-113">The WMITracing.log file contains the events that WMI traces.</span></span> <span data-ttu-id="2ba15-114">Sin embargo, se trata de un archivo binario.</span><span class="sxs-lookup"><span data-stu-id="2ba15-114">However, this is a binary file.</span></span> <span data-ttu-id="2ba15-115">Para ver estos eventos en un formato legible por los usuarios, use el **visor de eventos**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-115">To see these events in a format readable by humans, use the **Event Viewer**.</span></span>

<span data-ttu-id="2ba15-116">De forma predeterminada, no se realiza un seguimiento de los eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba15-116">By default, WMI events are not traced.</span></span> <span data-ttu-id="2ba15-117">En este procedimiento se describe cómo usar **visor de eventos** para habilitar el seguimiento de eventos WMI y buscar eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba15-117">This procedure describes how to use **Event Viewer** to enable WMI event tracing and locate WMI events.</span></span> <span data-ttu-id="2ba15-118">Puede realizar las mismas operaciones a través de la herramienta de línea de comandos wevtutil.</span><span class="sxs-lookup"><span data-stu-id="2ba15-118">You can do the same operations through the wevtutil command-line tool.</span></span>

<span data-ttu-id="2ba15-119">**Para ver eventos WMI en Visor de eventos**</span><span class="sxs-lookup"><span data-stu-id="2ba15-119">**To view WMI Events in Event Viewer**</span></span>

1.  <span data-ttu-id="2ba15-120">Abra **Visor de eventos**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-120">Open **Event Viewer**.</span></span> <span data-ttu-id="2ba15-121">En el menú **Vista**, haga clic en **Mostrar registros analíticos y de depuración**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-121">On the **View** menu, click **Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="2ba15-122">Busque el registro del canal de **seguimiento** para WMI en registros de aplicaciones y servicios \| actividad de WMI de Microsoft \| Windows \| .</span><span class="sxs-lookup"><span data-stu-id="2ba15-122">Locate the **Trace** channel log for WMI under Applications and Service Logs \| Microsoft \| Windows \| WMI Activity.</span></span>
2.  <span data-ttu-id="2ba15-123">Haga clic con el botón secundario en el registro de **seguimiento** y seleccione **propiedades del registro**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-123">Right-click the **Trace** log and select **Log Properties**.</span></span> <span data-ttu-id="2ba15-124">Haga clic en la casilla **Habilitar registro** para iniciar el seguimiento de eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba15-124">Click the **Enable Logging** check box to start the WMI event tracing.</span></span> <span data-ttu-id="2ba15-125">Para obtener más información acerca de los canales, consulte [registros de eventos y canales en el registro de eventos de Windows](/previous-versions//aa385225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ba15-125">For more information about channels, see [Event Logs and Channels in Windows Event Log](/previous-versions//aa385225(v=vs.85)).</span></span>
3.  <span data-ttu-id="2ba15-126">Los eventos WMI aparecen en la ventana de eventos para **la actividad WMI**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-126">WMI events appear in the event window for **WMI-Activity**.</span></span> <span data-ttu-id="2ba15-127">Haga doble clic en un evento de la lista para ver la información detallada.</span><span class="sxs-lookup"><span data-stu-id="2ba15-127">Double-click an event in the list to see the detailed information.</span></span> <span data-ttu-id="2ba15-128">Puede ver un evento en la **vista XML** o en un formato de **vista descriptivo** .</span><span class="sxs-lookup"><span data-stu-id="2ba15-128">You can view an event in **XML View** or in **Friendly View** format.</span></span>

<span data-ttu-id="2ba15-129">El campo ID. de **evento** muestra un valor que contiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="2ba15-129">The **Event ID** field displays a value that contains the following information.</span></span>

<dl> <dt>

<span data-ttu-id="2ba15-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Evento 1</span><span class="sxs-lookup"><span data-stu-id="2ba15-130"><span id="Event_1"></span><span id="event_1"></span><span id="EVENT_1"></span>Event 1</span></span>
</dt> <dd>

<span data-ttu-id="2ba15-131">Inicio de la secuencia de eventos para una operación específica.</span><span class="sxs-lookup"><span data-stu-id="2ba15-131">Start of the event sequence for a specific operation.</span></span> <span data-ttu-id="2ba15-132">Una repetición para cada secuencia.</span><span class="sxs-lookup"><span data-stu-id="2ba15-132">One occurrence for each sequence.</span></span>

<span data-ttu-id="2ba15-133">Los campos de evento para un evento 1 son:</span><span class="sxs-lookup"><span data-stu-id="2ba15-133">The event fields for an Event 1 are:</span></span>

-   <span data-ttu-id="2ba15-134">**GroupOperationID** es un identificador único que se usa para todos los eventos informados para un cliente específico.</span><span class="sxs-lookup"><span data-stu-id="2ba15-134">**GroupOperationID** is a unique identifier that is used for all events reported for a specific client.</span></span>
-   <span data-ttu-id="2ba15-135">**OperationId** indica la secuencia de la operación.</span><span class="sxs-lookup"><span data-stu-id="2ba15-135">**OperationId** indicates the operation sequence.</span></span>
-   <span data-ttu-id="2ba15-136">**Operación** especifica la conexión o la solicitud a WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba15-136">**Operation** specifies the connection or request to WMI.</span></span>
-   <span data-ttu-id="2ba15-137">El **usuario** indica la cuenta que realiza una solicitud a WMI mediante la ejecución de un script o de CIM Studio.</span><span class="sxs-lookup"><span data-stu-id="2ba15-137">**User** indicates the account that makes a request to WMI by running a script or through CIM Studio.</span></span>
-   <span data-ttu-id="2ba15-138">**Espacio de nombres** muestra el espacio de nombres WMI en el que se realiza la conexión.</span><span class="sxs-lookup"><span data-stu-id="2ba15-138">**Namespace** shows the WMI namespace to which the connection is made.</span></span>

<span data-ttu-id="2ba15-139">Por ejemplo, un script puede solicitar todas las instancias de una clase WMI, como el [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="2ba15-139">For example, a script may request all the instances of a WMI class, such as [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="2ba15-140">La primera operación puede ser una conexión a WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba15-140">The first operation may be a connection to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="2ba15-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Evento 2</span><span class="sxs-lookup"><span data-stu-id="2ba15-141"><span id="Event_2"></span><span id="event_2"></span><span id="EVENT_2"></span>Event 2</span></span>
</dt> <dd>

<span data-ttu-id="2ba15-142">Eventos que componen la operación.</span><span class="sxs-lookup"><span data-stu-id="2ba15-142">Events that make up the operation.</span></span> <span data-ttu-id="2ba15-143">Una o más repeticiones de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2ba15-143">One or more occurrences in the sequence.</span></span>

<span data-ttu-id="2ba15-144">Los campos de evento para un evento 2 son:</span><span class="sxs-lookup"><span data-stu-id="2ba15-144">The event fields for an Event 2 are:</span></span>

-   <span data-ttu-id="2ba15-145">**GroupOperationID** indica la secuencia en la que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="2ba15-145">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="2ba15-146">**GroupOperationID** indica la secuencia en la que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="2ba15-146">**GroupOperationID** indicates the sequence in which the event occurs.</span></span>
-   <span data-ttu-id="2ba15-147">**ProviderName** indica el nombre del proveedor que proporciona los datos.</span><span class="sxs-lookup"><span data-stu-id="2ba15-147">**ProviderName** indicates the name of the provider which supplies the data.</span></span>
-   <span data-ttu-id="2ba15-148">**Path** es la ruta de acceso WMI al objeto.</span><span class="sxs-lookup"><span data-stu-id="2ba15-148">**Path** is the WMI path to the object.</span></span>

<span data-ttu-id="2ba15-149">Por ejemplo, la operación puede ser una enumeración [**del \_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="2ba15-149">For example, the operation may be an enumeration of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="2ba15-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Evento 3</span><span class="sxs-lookup"><span data-stu-id="2ba15-150"><span id="Event_3"></span><span id="event_3"></span><span id="EVENT_3"></span>Event 3</span></span>
</dt> <dd>

<span data-ttu-id="2ba15-151">Final de la secuencia de eventos para una operación específica.</span><span class="sxs-lookup"><span data-stu-id="2ba15-151">End of the event sequence for a specific operation.</span></span> <span data-ttu-id="2ba15-152">Una repetición para cada secuencia.</span><span class="sxs-lookup"><span data-stu-id="2ba15-152">One occurrence for each sequence.</span></span>

<span data-ttu-id="2ba15-153">Solo se muestra el **GroupOperationID** .</span><span class="sxs-lookup"><span data-stu-id="2ba15-153">Only the **GroupOperationID** is shown.</span></span>

</dd> </dl>

## <a name="enabling-wmi-tracing-at-command-prompt"></a><span data-ttu-id="2ba15-154">Habilitación del seguimiento de WMI en el símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="2ba15-154">Enabling WMI Tracing at Command Prompt</span></span>

<span data-ttu-id="2ba15-155">También puede habilitar el seguimiento de eventos WMI mediante la herramienta de línea de comandos wevtutil.</span><span class="sxs-lookup"><span data-stu-id="2ba15-155">You can also enable WMI event tracing through the Wevtutil command-line tool.</span></span> <span data-ttu-id="2ba15-156">Use el comando siguiente: **Wevtutil.exe SL Microsoft-Windows-WMI-Activity/Trace/e: true**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-156">Use the following command: **Wevtutil.exe sl Microsoft-Windows-WMI-Activity/Trace /e:true**.</span></span> <span data-ttu-id="2ba15-157">El origen del evento WMI es Microsoft-Windows-WMI.</span><span class="sxs-lookup"><span data-stu-id="2ba15-157">The WMI event source is Microsoft-Windows-WMI.</span></span> <span data-ttu-id="2ba15-158">Para obtener más información acerca de Wevtutil.exe, consulte [acerca del registro de eventos de Windows](/previous-versions//aa382610(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ba15-158">For more information about Wevtutil.exe, see [About Windows Event Log](/previous-versions//aa382610(v=vs.85)).</span></span>

## <a name="using-wpp-based-wmi-tracing"></a><span data-ttu-id="2ba15-159">Uso del seguimiento de WMI basado en WPP</span><span class="sxs-lookup"><span data-stu-id="2ba15-159">Using WPP-based WMI Tracing</span></span>

<span data-ttu-id="2ba15-160">En los sistemas operativos Windows a partir de Windows Vista, WMI crea un canal de seguimiento activo durante el proceso de arranque.</span><span class="sxs-lookup"><span data-stu-id="2ba15-160">In Windows operating systems starting with Windows Vista, WMI creates an active trace channel during the boot process.</span></span> <span data-ttu-id="2ba15-161">El nombre del canal es sesión de \_ seguimiento de WMI \_ .</span><span class="sxs-lookup"><span data-stu-id="2ba15-161">The name of the channel is WMI\_Trace\_Session.</span></span> <span data-ttu-id="2ba15-162">Solo los errores se registran en el canal.</span><span class="sxs-lookup"><span data-stu-id="2ba15-162">Only errors are logged to the channel.</span></span>

<span data-ttu-id="2ba15-163">El preprocesador de seguimiento de software de Windows (WPP) registra información en un archivo binario.</span><span class="sxs-lookup"><span data-stu-id="2ba15-163">The Windows software trace preprocessor (WPP) records information in a binary file.</span></span> <span data-ttu-id="2ba15-164">Para leer el archivo, primero debe convertirlo a un formato de texto legible.</span><span class="sxs-lookup"><span data-stu-id="2ba15-164">To read the file, you must first translate it into a readable, text format.</span></span> <span data-ttu-id="2ba15-165">Use una herramienta llamada tracefmt.exe del kit de [controladores de Windows (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) para realizar la traducción.</span><span class="sxs-lookup"><span data-stu-id="2ba15-165">You use a tool called tracefmt.exe from the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to do the translation.</span></span> <span data-ttu-id="2ba15-166">La herramienta requiere información almacenada en algunos archivos asociados.</span><span class="sxs-lookup"><span data-stu-id="2ba15-166">The tool requires information stored in some associated files.</span></span> <span data-ttu-id="2ba15-167">Los archivos se encuentran en el directorio% SystemRoot% \\ system32 \\ WBEM \\ TMF y tienen una extensión de nombre de archivo. TMF.</span><span class="sxs-lookup"><span data-stu-id="2ba15-167">The files are located in the %SystemRoot%\\System32\\wbem\\tmf directory and have a .tmf file name extension.</span></span> <span data-ttu-id="2ba15-168">La herramienta realmente requiere un único archivo. TMF.</span><span class="sxs-lookup"><span data-stu-id="2ba15-168">The tool actually requires a single .tmf file .</span></span> <span data-ttu-id="2ba15-169">Para hacerlo, se concatenan todos los archivos. TMF en otro archivo. TMF.</span><span class="sxs-lookup"><span data-stu-id="2ba15-169">You make that single file by concatenating all of the .tmf files into another .tmf file.</span></span> <span data-ttu-id="2ba15-170">Para obtener más información acerca de los archivos. TMF, vea [archivo de formato de mensaje de seguimiento](/windows-hardware/drivers/devtest/trace-message-format-file).</span><span class="sxs-lookup"><span data-stu-id="2ba15-170">For more information about .tmf files, see [Trace Message Format File](/windows-hardware/drivers/devtest/trace-message-format-file).</span></span>

<span data-ttu-id="2ba15-171">Después de instalar [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) para obtener las herramientas de línea de comandos tracelog.exe y tracefmt.exe, realice los pasos siguientes para recopilar un seguimiento WMI basado en WPP.</span><span class="sxs-lookup"><span data-stu-id="2ba15-171">After installing the [Windows Driver Kit (WDK)](https://www.microsoft.com/whdc/DevTools/WDK/WDKpkg.mspx) to get the tracelog.exe and tracefmt.exe command-line tools, perform the following steps to collect a WPP-based WMI trace.</span></span>

<span data-ttu-id="2ba15-172">**Para ver un seguimiento WMI basado en WPP**</span><span class="sxs-lookup"><span data-stu-id="2ba15-172">**To view a WPP-based WMI trace**</span></span>

1.  <span data-ttu-id="2ba15-173">Para crear el archivo. TMF único, abra una ventana de símbolo del sistema con privilegios elevados y navegue hasta el directorio% SystemRoot% \\ system32 \\ WBEM \\ TMF</span><span class="sxs-lookup"><span data-stu-id="2ba15-173">To create the single .tmf file, open an elevated Command Prompt window and navigate to the %SystemRoot%\\System32\\wbem\\tmf directory.</span></span>

2.  <span data-ttu-id="2ba15-174">Escriba **Copy/y% SystemRoot% \\ system32 \\ WBEM \\ TMF \\ \* . TMF% SystemRoot% \\ system32 \\ WBEM \\ TMF \\ WMI. TMF**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-174">Type **copy /y %SystemRoot%\\System32\\wbem\\tmf\\\*.tmf %SystemRoot%\\System32\\wbem\\tmf\\wmi.tmf**.</span></span> <span data-ttu-id="2ba15-175">Se creará un archivo denominado WMI. TMF que incluye el contenido de todos los demás archivos. TMF.</span><span class="sxs-lookup"><span data-stu-id="2ba15-175">This will create a file named wmi.tmf that includes the contents of all of the other .tmf files.</span></span>

3.  <span data-ttu-id="2ba15-176">Escriba **tracelog-vaciar \_ la \_ sesión de seguimiento WMI**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-176">Type **tracelog -flush WMI\_Trace\_Session**.</span></span> <span data-ttu-id="2ba15-177">Esto hará que se vacíen los búferes WPP en el disco.</span><span class="sxs-lookup"><span data-stu-id="2ba15-177">This will flush the WPP buffers on the disk.</span></span>
4.  <span data-ttu-id="2ba15-178">Escriba **set Trace \_ format \_ prefix = \[ %9! d! \] %8! 04X!. %3! 04X!. %3! 04X!:: %4! s! \[ %1! s! \] (%! COMPNAME!:%! FUNC!: %2! s!)**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-178">Type **set TRACE\_FORMAT\_PREFIX = \[%9!d!\]%8!04X!.%3!04X!.%3!04X!::%4!s!\[%1!s!\](%!COMPNAME!:%!FUNC !:%2!s!)**.</span></span> <span data-ttu-id="2ba15-179">La herramienta tracefmt agrega información predeterminada a cada mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="2ba15-179">The tracefmt tool adds some default information to each trace message.</span></span> <span data-ttu-id="2ba15-180">Para configurar la información que se incluye, establezca la \_ variable de \_ entorno prefijo de formato de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="2ba15-180">You can configure what information is included by setting the TRACE\_FORMAT\_PREFIX environment variable.</span></span> <span data-ttu-id="2ba15-181">Para obtener información sobre la sintaxis usada, consulte [Prefijo de mensaje de seguimiento](https://msdn.microsoft.com/library/aa139695.aspx).</span><span class="sxs-lookup"><span data-stu-id="2ba15-181">To learn about the syntax used, see [Trace Message Prefix](https://msdn.microsoft.com/library/aa139695.aspx).</span></span>
5.  <span data-ttu-id="2ba15-182">Escriba **tracefmt-TMF% SystemRoot% \\ system32 \\ WBEM \\ TMF \\ wmi. TMF-o OUTPUT.TXT% SystemRoot% \\ system32 \\ WBEM \\ logs \\ WMITracing. log**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-182">Type **tracefmt -tmf %systemroot%\\system32\\wbem\\tmf\\wmi.tmf -o OUTPUT.TXT %systemroot%\\system32\\wbem\\logs\\WMITracing.log**.</span></span> <span data-ttu-id="2ba15-183">Esto realiza la traducción desde el formato binario al formato de texto legible.</span><span class="sxs-lookup"><span data-stu-id="2ba15-183">This performs the translation from binary format to readable text format.</span></span>
6.  <span data-ttu-id="2ba15-184">Escriba **Notepad% SystemRoot% \\ system32 \\ WBEM \\ TMF \\OUTPUT.TXT**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-184">Type **notepad %systemroot%\\system32\\wbem\\tmf\\OUTPUT.TXT**.</span></span> <span data-ttu-id="2ba15-185">Se abrirá el archivo de seguimiento en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="2ba15-185">This will open the trace file in Notepad.</span></span>

<span data-ttu-id="2ba15-186">A continuación se indican algunas de las tareas relacionadas con WPP que podría necesitar realizar.</span><span class="sxs-lookup"><span data-stu-id="2ba15-186">The following are some other WPP-related tasks you might need to perform.</span></span>

<span data-ttu-id="2ba15-187">**Para detener el seguimiento de WMI basado en WPP**</span><span class="sxs-lookup"><span data-stu-id="2ba15-187">**To stop WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="2ba15-188">Escriba **tracelog-STOP WMI \_ Trace \_ Session**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-188">Type **tracelog -stop WMI\_Trace\_Session**.</span></span>

<span data-ttu-id="2ba15-189">**Para iniciar el seguimiento WMI basado en WPP**</span><span class="sxs-lookup"><span data-stu-id="2ba15-189">**To start WPP-based WMI tracing**</span></span>

-   <span data-ttu-id="2ba15-190">Escriba **tracelog-Start WMI \_ Trace \_ Session-GUID \# 1FF6B227-2CA7-40f9-9A66-980EADAA602E-RT-LEVEL 5-Flag 0X7-f @ Trace. BIN**</span><span class="sxs-lookup"><span data-stu-id="2ba15-190">Type **tracelog -start WMI\_Trace\_Session -guid \#1FF6B227-2CA7-40f9-9A66-980EADAA602E -rt -level 5 -flag 0x7 -f MYTRACE.BIN**</span></span>

<span data-ttu-id="2ba15-191">**Windows Vista:** De forma predeterminada, el seguimiento de WMI basado en WPP se establece en el nivel 2, que incluye solo los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="2ba15-191">**Windows Vista:** By default, WPP-based WMI tracing is set to level 2 which includes only error messages.</span></span> <span data-ttu-id="2ba15-192">Para incluir también los mensajes informativos, establezca el nivel en 4.</span><span class="sxs-lookup"><span data-stu-id="2ba15-192">To include informational messages as well, set the level to 4.</span></span> <span data-ttu-id="2ba15-193">Se realiza un seguimiento de todas las áreas de WMI de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2ba15-193">All areas of WMI are traced by default.</span></span> <span data-ttu-id="2ba15-194">Hay tres áreas distintas de las que se puede realizar un seguimiento: Core (flag = 0x1), ESS (flag = 0X2) y Prov (flag = 0x4).</span><span class="sxs-lookup"><span data-stu-id="2ba15-194">There are three distinct areas that can be traced: Core (flag=0x1), ESS (flag=0x2) and Prov (flag=0x4).</span></span> <span data-ttu-id="2ba15-195">En el comando iniciar anterior, la **marca 0X7** hace que se haga un seguimiento de las tres áreas.</span><span class="sxs-lookup"><span data-stu-id="2ba15-195">In the start command above, **flag 0x7** causes all three areas to be traced.</span></span>

<span data-ttu-id="2ba15-196">**Windows 7:** De forma predeterminada, el seguimiento de WMI basado en WPP está deshabilitado y establecido en el nivel 0.</span><span class="sxs-lookup"><span data-stu-id="2ba15-196">**Windows 7:** By default, WPP-based WMI tracing is disabled and set to level 0.</span></span> <span data-ttu-id="2ba15-197">Para usar el seguimiento WMI basado en WPP, esta característica debe estar habilitada y establecida en el nivel 2 para los mensajes de error o el nivel 4 para los mensajes de error e informativos.</span><span class="sxs-lookup"><span data-stu-id="2ba15-197">To use WPP-based WMI tracing, this feature must be enabled and set to either level 2 for error messages or level 4 for both error and informational messages.</span></span>

<span data-ttu-id="2ba15-198">**Para enumerar todas las sesiones de seguimiento WPP**</span><span class="sxs-lookup"><span data-stu-id="2ba15-198">**To list all WPP trace sessions**</span></span>

-   <span data-ttu-id="2ba15-199">Escriba **tracelog-l**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-199">Type **tracelog -l**.</span></span>

<span data-ttu-id="2ba15-200">**Para mostrar información acerca de la sesión de seguimiento WPP de WMI**</span><span class="sxs-lookup"><span data-stu-id="2ba15-200">**To list info about the WMI WPP trace session**</span></span>

-   <span data-ttu-id="2ba15-201">Escriba **tracelog-l \| Findstr/i "WMI \_ trace"**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-201">Type **tracelog -l \| findstr /i "wmi\_trace"**.</span></span>

<span data-ttu-id="2ba15-202">**Para ver los parámetros de la sesión de seguimiento WPP de WMI**</span><span class="sxs-lookup"><span data-stu-id="2ba15-202">**To view the WMI WPP trace session parameters**</span></span>

-   <span data-ttu-id="2ba15-203">Escriba **tracelog-q \_ \_ sesión de seguimiento de WMI**.</span><span class="sxs-lookup"><span data-stu-id="2ba15-203">Type **tracelog -q WMI\_Trace\_Session**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ba15-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ba15-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ba15-205">Solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="2ba15-205">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="2ba15-206">Archivos de registro de WMI</span><span class="sxs-lookup"><span data-stu-id="2ba15-206">WMI Log Files</span></span>](wmi-log-files.md)
</dt> </dl>

 

 
