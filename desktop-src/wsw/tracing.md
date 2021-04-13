---
title: Traza
description: El seguimiento utiliza el seguimiento de eventos para Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Seguimiento de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421635"
---
# <a name="tracing"></a><span data-ttu-id="900bb-106">Seguimiento</span><span class="sxs-lookup"><span data-stu-id="900bb-106">Tracing</span></span>

<span data-ttu-id="900bb-107">El seguimiento utiliza el seguimiento de eventos para Windows (ETW).</span><span class="sxs-lookup"><span data-stu-id="900bb-107">Tracing uses Event Tracing for Windows (ETW).</span></span> <span data-ttu-id="900bb-108">Para beneficiarse de las herramientas de seguimiento disponibles con Windows Server 2008 R2, instale el Microsoft Windows SDK desde el sitio de [descargas de MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .</span><span class="sxs-lookup"><span data-stu-id="900bb-108">To take advantage of the tracing tools available with Windows Server 2008 R2, install the Microsoft Windows SDK from the [MSDN Downloads](https://www.microsoft.com/download/details.aspx?id=8279) site.</span></span>


<span data-ttu-id="900bb-109">Se admiten tres niveles de seguimiento:</span><span class="sxs-lookup"><span data-stu-id="900bb-109">There are three tracing levels supported:</span></span>

-   <span data-ttu-id="900bb-110">Detallado (todos los seguimientos disponibles).</span><span class="sxs-lookup"><span data-stu-id="900bb-110">Verbose (all available traces).</span></span>
-   <span data-ttu-id="900bb-111">Info (seguimientos informativos).</span><span class="sxs-lookup"><span data-stu-id="900bb-111">Info (informational traces).</span></span>
-   <span data-ttu-id="900bb-112">Error (seguimientos de errores).</span><span class="sxs-lookup"><span data-stu-id="900bb-112">Error (error traces).</span></span>

<span data-ttu-id="900bb-113">Se realiza un seguimiento de los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="900bb-113">The following events are traced:</span></span>

-   <span data-ttu-id="900bb-114">Cualquier error (LEVEL = error, Level = info o LEVEL = verbose).</span><span class="sxs-lookup"><span data-stu-id="900bb-114">Any errors (Level=Error, Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="900bb-115">Entrada/salida de una API (LEVEL = info o LEVEL = verbose).</span><span class="sxs-lookup"><span data-stu-id="900bb-115">Entry/Exit of an API (Level=Info or Level=Verbose).</span></span>
-   <span data-ttu-id="900bb-116">Inicio y finalización de cualquier e/s (LEVEL = info o LEVEL = verbose)</span><span class="sxs-lookup"><span data-stu-id="900bb-116">Start and completion of any IO (Level=Info or Level=Verbose)</span></span>
-   <span data-ttu-id="900bb-117">Mensajes SOAP intercambiados (LEVEL = verbose, disponible en Windows 2003 SP1 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="900bb-117">Exchanged SOAP messages (Level=Verbose, available on Windows 2003 SP1 and later)</span></span>

## <a name="generating-and-viewing-wwsapi-traces"></a><span data-ttu-id="900bb-118">Generar y ver seguimientos de WWSAPI</span><span class="sxs-lookup"><span data-stu-id="900bb-118">Generating and Viewing WWSAPI Traces</span></span>

<span data-ttu-id="900bb-119">WWSAPI usa los eventos basados en manifiesto en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="900bb-119">WWSAPI uses the manifest based events on Windows Vista and above.</span></span> <span data-ttu-id="900bb-120">Como resultado, la experiencia de seguimiento tiene algunas diferencias en función de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="900bb-120">As a result, the tracing experience has some differences based on the operating system version.</span></span> <span data-ttu-id="900bb-121">La generación de seguimientos de ETW se puede realizar mediante las herramientas de ETW integradas en todas las plataformas compatibles.</span><span class="sxs-lookup"><span data-stu-id="900bb-121">Generating ETW traces can be done by using the in-box ETW tools on all supported platforms.</span></span> <span data-ttu-id="900bb-122">Sin embargo, la visualización de los seguimientos de ETW en un formato agradable requiere herramientas personalizadas en Windows XP SP2 y Windows 2003 SP1.</span><span class="sxs-lookup"><span data-stu-id="900bb-122">However viewing the ETW traces in a nice format requires custom tools on Windows XP SP2 and Windows 2003 SP1.</span></span> <span data-ttu-id="900bb-123">Hay algunas maneras diferentes de recopilar y ver los seguimientos de eventos ETW de WWSAPI en función de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="900bb-123">There are few different ways of collecting and viewing WWSAPI ETW event traces depending on the operating system version.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a><span data-ttu-id="900bb-124">Habilitar y ver seguimientos de WWSAPI en Visor de eventos (funciona en Windows Vista y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="900bb-124">Enabling and Viewing WWSAPI traces in Event Viewer (works on Windows Vista and above)</span></span>

-   <span data-ttu-id="900bb-125">Ejecute eventvwr. msc desde la línea de comandos o desde el menú ejecutar.</span><span class="sxs-lookup"><span data-stu-id="900bb-125">Run eventvwr.msc from command line or run menu.</span></span>
-   <span data-ttu-id="900bb-126">Haga clic en el vínculo ver del panel acciones de la derecha y habilite la opción Mostrar registros analíticos y de depuración.</span><span class="sxs-lookup"><span data-stu-id="900bb-126">Click the view link on the Actions pane on the right and enable Show Analytic and Debug logs option.</span></span>
-   <span data-ttu-id="900bb-127">Vaya a registros de aplicaciones y \\ servicios \\ \\ proveedores de servicios de Microsoft Windows en el panel izquierdo.</span><span class="sxs-lookup"><span data-stu-id="900bb-127">Browse to Application and Service Logs\\Microsoft\\Windows\\WebServices providers on the left pane.</span></span>
-   <span data-ttu-id="900bb-128">Haga clic con el botón derecho en el proveedor de seguimiento y seleccione Habilitar registro.</span><span class="sxs-lookup"><span data-stu-id="900bb-128">Right click the Tracing provider and select Enable log.</span></span>
-   <span data-ttu-id="900bb-129">Ejecute el escenario.</span><span class="sxs-lookup"><span data-stu-id="900bb-129">Run your scenario.</span></span>
-   <span data-ttu-id="900bb-130">Al actualizar la página del visor de eventos, debería empezar a ver las entradas de seguimiento de WWSAPI.</span><span class="sxs-lookup"><span data-stu-id="900bb-130">When you refresh the event viewer page, you should start seeing the WWSAPI tracing entries.</span></span>

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a><span data-ttu-id="900bb-131">Habilitación y visualización de seguimientos de WWSAPI mediante Wstrace.bat script (Works en XPSP2 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="900bb-131">Enabling and Viewing WWSAPI traces using Wstrace.bat Script (works on XPSP2 and above)</span></span>

<span data-ttu-id="900bb-132">El archivo por lotes wstrace.bat proporciona una manera cómoda de:</span><span class="sxs-lookup"><span data-stu-id="900bb-132">The wstrace.bat batch file provides a convenient way to:</span></span>

-   <span data-ttu-id="900bb-133">Crear un registro de seguimiento</span><span class="sxs-lookup"><span data-stu-id="900bb-133">Create a trace log</span></span>
-   <span data-ttu-id="900bb-134">Eliminar un registro de seguimiento</span><span class="sxs-lookup"><span data-stu-id="900bb-134">Delete a trace log</span></span>
-   <span data-ttu-id="900bb-135">Habilitar y deshabilitar el seguimiento</span><span class="sxs-lookup"><span data-stu-id="900bb-135">Enable and disable tracing</span></span>
-   <span data-ttu-id="900bb-136">Actualizar el nivel de seguimiento (info/error/verbose)</span><span class="sxs-lookup"><span data-stu-id="900bb-136">Update the tracing level (info/error/verbose)</span></span>
-   <span data-ttu-id="900bb-137">Convertir registros de seguimiento en archivos CSV</span><span class="sxs-lookup"><span data-stu-id="900bb-137">Converting trace logs to CSV files</span></span>

<span data-ttu-id="900bb-138">El archivo por lotes usa logman.exe para todos los comandos, a excepción de la conversión de los registros a un archivo CSV, que requiere una herramienta personalizada (wstracedump.exe).</span><span class="sxs-lookup"><span data-stu-id="900bb-138">The batch file uses logman.exe for all commands, with the exception of converting the logs to CSV file, which requires a custom tool (wstracedump.exe).</span></span>

## <a name="using-tracing-commands"></a><span data-ttu-id="900bb-139">Usar comandos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="900bb-139">Using tracing commands</span></span>

<span data-ttu-id="900bb-140">El siguiente comando crea un registro que usa información, un error o un nivel detallado.</span><span class="sxs-lookup"><span data-stu-id="900bb-140">The following command creates a log that uses info, error or verbose level.</span></span> <span data-ttu-id="900bb-141">Este comando requiere privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="900bb-141">This command requires elevated privileges.</span></span>

<span data-ttu-id="900bb-142">**wstrace.bat Create \[ info \| error \| verbose\]**</span><span class="sxs-lookup"><span data-stu-id="900bb-142">**wstrace.bat create \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="900bb-143">El siguiente comando elimina el registro.</span><span class="sxs-lookup"><span data-stu-id="900bb-143">The following command deletes the log.</span></span> <span data-ttu-id="900bb-144">Este comando requiere privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="900bb-144">This command requires elevated privileges.</span></span>

<span data-ttu-id="900bb-145">**wstrace.bat eliminar**</span><span class="sxs-lookup"><span data-stu-id="900bb-145">**wstrace.bat delete**</span></span>

<span data-ttu-id="900bb-146">El siguiente comando habilita el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="900bb-146">The following command enables tracing.</span></span> <span data-ttu-id="900bb-147">Primero debe crear un registro.</span><span class="sxs-lookup"><span data-stu-id="900bb-147">You must first create a log.</span></span>

<span data-ttu-id="900bb-148">**wstrace.bat en**</span><span class="sxs-lookup"><span data-stu-id="900bb-148">**wstrace.bat on**</span></span>

<span data-ttu-id="900bb-149">El nivel de seguimiento (info, error o verbose) se puede modificar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="900bb-149">The tracing level (info, error or verbose) can be modified as follows:</span></span>

<span data-ttu-id="900bb-150">**wstrace.bat error de información de actualización \[ \| \| detallado\]**</span><span class="sxs-lookup"><span data-stu-id="900bb-150">**wstrace.bat update \[info \| error \| verbose\]**</span></span>

<span data-ttu-id="900bb-151">Para volcar la salida del seguimiento, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="900bb-151">To dump the trace output, use the following command:</span></span>

<span data-ttu-id="900bb-152">**wstrace.bat > de volcado de memoria temp.csv**</span><span class="sxs-lookup"><span data-stu-id="900bb-152">**wstrace.bat dump > temp.csv**</span></span>

<span data-ttu-id="900bb-153">Los eventos se volcarán en el archivo CSV hasta que se presione Ctrl + C o se deshabilite el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="900bb-153">The events will be dumped to the CSV file until Ctrl-C is pressed or tracing is disabled.</span></span>

## <a name="tracing-file-format"></a><span data-ttu-id="900bb-154">Formato de archivo de seguimiento</span><span class="sxs-lookup"><span data-stu-id="900bb-154">Tracing File format</span></span>

<span data-ttu-id="900bb-155">Los archivos CSV creados por wstrace.bat son archivos de texto de variables separadas por comas simples.</span><span class="sxs-lookup"><span data-stu-id="900bb-155">The CSV files created by wstrace.bat are simple comma-separated-variable text files.</span></span> <span data-ttu-id="900bb-156">Estos archivos se pueden abrir en Excel, Bloc de notas, etc.</span><span class="sxs-lookup"><span data-stu-id="900bb-156">These files may be opened in Excel, Notepad, etc.</span></span>

<span data-ttu-id="900bb-157">Las columnas del archivo son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="900bb-157">The columns of the file are as follows:</span></span>

-   <span data-ttu-id="900bb-158">Marca de tiempo de fecha y hora en que se registró el evento</span><span class="sxs-lookup"><span data-stu-id="900bb-158">TimeStamp - Time stamp of when the event was recorded</span></span>
-   <span data-ttu-id="900bb-159">ProcessID-ULONG ID. del proceso que registra el evento</span><span class="sxs-lookup"><span data-stu-id="900bb-159">ProcessID - ULONG ID of the process recording the event</span></span>
-   <span data-ttu-id="900bb-160">ThreadID: ID. de ULONG del subproceso que registra el evento</span><span class="sxs-lookup"><span data-stu-id="900bb-160">ThreadID - ULONG ID of the thread recording the event</span></span>
-   <span data-ttu-id="900bb-161">El valor enumerado de eventos del tipo de evento puede ser ("API Enter" \| "API Pending" "API ExitSyncSuccess" "API ExitSyncFailure" "API \| \| \| ExitAsyncSuccess" \| "API ExitAsyncFailure" " \| IO Started" " \| e/s completada" "error de \| e/s" " \| error" "recepción de \| mensaje recibido" \| "mensaje recibido" "se \| ha recibido el mensaje \| \| \| "</span><span class="sxs-lookup"><span data-stu-id="900bb-161">Event - Enumerated value of the event type may be ("api enter" \| "api pending" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io completed" \| "io failed" \| "error" \| "received message start" \| "received message" \| "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")</span></span>
-   <span data-ttu-id="900bb-162">Operación: el nombre de la operación que se va a invocar.</span><span class="sxs-lookup"><span data-stu-id="900bb-162">Operation - The name of the operation being invoked.</span></span> <span data-ttu-id="900bb-163">Normalmente, se asigna a la API a la que se llama.</span><span class="sxs-lookup"><span data-stu-id="900bb-163">Typically this maps to the API being called.</span></span>
-   <span data-ttu-id="900bb-164">Error: número de error opcional de HRESULT</span><span class="sxs-lookup"><span data-stu-id="900bb-164">Error - Optional HRESULT error number</span></span>
-   <span data-ttu-id="900bb-165">Info: información opcional sobre el evento</span><span class="sxs-lookup"><span data-stu-id="900bb-165">Info - Optional information about the event</span></span>

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a><span data-ttu-id="900bb-166">Recopilación del archivo de seguimiento de ETW de WWSAPI con las herramientas de ETW (funciona en XPSP2 y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="900bb-166">Collecting WWSAPI ETW Trace File using ETW tools (works on XPSP2 and above)</span></span>

<span data-ttu-id="900bb-167">Habilitación del seguimiento de ETW para WWSAPI</span><span class="sxs-lookup"><span data-stu-id="900bb-167">Enabling ETW tracing for WWSAPI</span></span>

<span data-ttu-id="900bb-168">**Logman Start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-webservices \[ Flags \[ LEVEL \] \] \[ -o <EtlLogFileName> \] -ETS**</span><span class="sxs-lookup"><span data-stu-id="900bb-168">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[flags \[level\]\] \[-o <EtlLogFileName>\] -ets**</span></span>

<span data-ttu-id="900bb-169">para crear e iniciar la sesión de seguimiento de ETW.</span><span class="sxs-lookup"><span data-stu-id="900bb-169">to create and start the ETW tracing session.</span></span> <span data-ttu-id="900bb-170">Logman.exe es una herramienta de ETW integrada disponible en todas las plataformas compatibles.</span><span class="sxs-lookup"><span data-stu-id="900bb-170">Logman.exe is an in-box ETW tool available on all supported platforms.</span></span> <span data-ttu-id="900bb-171">Tenga en cuenta que debe usar \_ \_ los servicios WebService de Microsoft Windows como nombre del proveedor en xpsp2 y W2K3.</span><span class="sxs-lookup"><span data-stu-id="900bb-171">Note that you need to use Microsoft\_Windows\_WebServices as the provider name on XPSP2 and W2K3.</span></span> <span data-ttu-id="900bb-172">Puede ejecutar los proveedores de consultas Logman para ver la lista de proveedores registrados.</span><span class="sxs-lookup"><span data-stu-id="900bb-172">You can run logman query providers to see the list of registered providers.</span></span> <span data-ttu-id="900bb-173">El proveedor Microsoft-Windows-WebServices (o Microsoft \_ Windows \_ WebServices) debe aparecer en la lista a menos que no esté registrado.</span><span class="sxs-lookup"><span data-stu-id="900bb-173">Microsoft-Windows-WebServices (or Microsoft\_Windows\_WebServices) provider should be listed unless it is not registered.</span></span> <span data-ttu-id="900bb-174">Normalmente, el proveedor se registra durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="900bb-174">The provider is normally registered during setup.</span></span> <span data-ttu-id="900bb-175">Sin embargo, también se puede registrar manualmente mediante la ejecución de wevtutil.exe im <ManifestFileName> (en Windows Vista y versiones posteriores) o mofcomp.exe <MofFileName> (en xpsp2 y W2K3).</span><span class="sxs-lookup"><span data-stu-id="900bb-175">However it can also be manually registered by running wevtutil.exe im <ManifestFileName> (on Windows Vista and Later) or mofcomp.exe <MofFileName> (on XPSP2 and W2K3).</span></span>

<span data-ttu-id="900bb-176">Las marcas se pueden utilizar para filtrar los seguimientos por su tipo.</span><span class="sxs-lookup"><span data-stu-id="900bb-176">Flags can be used to filter the traces by their kind.</span></span> <span data-ttu-id="900bb-177">Puede ser o ser el valor de los siguientes tipos de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="900bb-177">It can be OR'd value of the following trace kinds.</span></span> <span data-ttu-id="900bb-178">Si no se proporciona, se habilitan todos los tipos de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="900bb-178">If not supplied, all trace kinds are enabled.</span></span>

-   <span data-ttu-id="900bb-179">0x1: seguimientos de entrada y salida de la API.</span><span class="sxs-lookup"><span data-stu-id="900bb-179">0x1 - API entry/exit traces.</span></span>
-   <span data-ttu-id="900bb-180">0X2: seguimientos de errores.</span><span class="sxs-lookup"><span data-stu-id="900bb-180">0x2 - Error traces.</span></span>
-   <span data-ttu-id="900bb-181">0x4: seguimientos de e/s.</span><span class="sxs-lookup"><span data-stu-id="900bb-181">0x4 - IO traces.</span></span>
-   <span data-ttu-id="900bb-182">0x8: seguimientos de mensajes SOAP.</span><span class="sxs-lookup"><span data-stu-id="900bb-182">0x8 - SOAP message traces.</span></span>
-   <span data-ttu-id="900bb-183">0x10: seguimientos de mensajes binarios.</span><span class="sxs-lookup"><span data-stu-id="900bb-183">0x10 - Binary message traces.</span></span>

<span data-ttu-id="900bb-184">El nivel se puede usar para filtrar los seguimientos por su nivel.</span><span class="sxs-lookup"><span data-stu-id="900bb-184">Level can be used to filter the traces by their level.</span></span> <span data-ttu-id="900bb-185">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="900bb-185">It should be one of the following values.</span></span> <span data-ttu-id="900bb-186">Si no se proporciona, se habilitan todos los niveles de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="900bb-186">If not supplied, all trace levels are enabled.</span></span>

-   <span data-ttu-id="900bb-187">0x1-seguimientos irrecuperables.</span><span class="sxs-lookup"><span data-stu-id="900bb-187">0x1 - Fatal traces.</span></span>
-   <span data-ttu-id="900bb-188">0X2: seguimientos de errores.</span><span class="sxs-lookup"><span data-stu-id="900bb-188">0x2 - Error traces.</span></span>
-   <span data-ttu-id="900bb-189">0X3: seguimientos de advertencia.</span><span class="sxs-lookup"><span data-stu-id="900bb-189">0x3 - Warning traces.</span></span>
-   <span data-ttu-id="900bb-190">0x4: seguimientos informativos.</span><span class="sxs-lookup"><span data-stu-id="900bb-190">0x4 - Informational traces.</span></span>
-   <span data-ttu-id="900bb-191">0X5: seguimientos detallados.</span><span class="sxs-lookup"><span data-stu-id="900bb-191">0x5 - Verbose traces.</span></span>

<span data-ttu-id="900bb-192">EtlLogFileName es la ruta de acceso al archivo de registro de eventos ETW que se va a crear (use la extensión. ETL).</span><span class="sxs-lookup"><span data-stu-id="900bb-192">EtlLogFileName is the path to the ETW event log file to be created (use .etl extension).</span></span> <span data-ttu-id="900bb-193">Si no se proporciona, ETW elegirá un nombre aleatorio que se puede consultar más adelante.</span><span class="sxs-lookup"><span data-stu-id="900bb-193">If not provided, ETW will pick a random name which can be queried later.</span></span> <span data-ttu-id="900bb-194">Este archivo no debe residir en el directorio del perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="900bb-194">This file should not reside on user's profile directory.</span></span> <span data-ttu-id="900bb-195">El archivo de registro de eventos ETW (archivo. ETL) está en formato binario.</span><span class="sxs-lookup"><span data-stu-id="900bb-195">ETW event log file (.etl file) is in binary format.</span></span> <span data-ttu-id="900bb-196">Puede ser utilizado por aplicaciones ETW, pero no está en formato legible.</span><span class="sxs-lookup"><span data-stu-id="900bb-196">It can be consumed by ETW applications, but it is not in human readable format.</span></span> <span data-ttu-id="900bb-197">El paso siguiente describe cómo ver su contenido.</span><span class="sxs-lookup"><span data-stu-id="900bb-197">Next step describes how to view its content.</span></span>

<span data-ttu-id="900bb-198">Ejecutar el escenario</span><span class="sxs-lookup"><span data-stu-id="900bb-198">Run your scenario</span></span>

<span data-ttu-id="900bb-199">Recopilando archivo de registro de eventos ETW.</span><span class="sxs-lookup"><span data-stu-id="900bb-199">Collecting ETW event log file.</span></span>

<span data-ttu-id="900bb-200">**Logman STOP wstrace-ETS**</span><span class="sxs-lookup"><span data-stu-id="900bb-200">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="900bb-201">para detener la sesión de seguimiento de ETW.</span><span class="sxs-lookup"><span data-stu-id="900bb-201">to stop the ETW tracing session.</span></span> <span data-ttu-id="900bb-202">Es cuando ETW detiene el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="900bb-202">This is when ETW stops logging the events.</span></span> <span data-ttu-id="900bb-203">El archivo de registro de eventos ETW (especificado en el parámetro EtlLogFileName) está listo para consumir.</span><span class="sxs-lookup"><span data-stu-id="900bb-203">ETW event log file (specified in EtlLogFileName parameter) is ready to consume.</span></span> <span data-ttu-id="900bb-204">Puede verse localmente (las instrucciones se proporcionan a continuación) o enviarse al grupo de productos para su investigación.</span><span class="sxs-lookup"><span data-stu-id="900bb-204">It can either be viewed locally (instructions are given below) or sent to the product group for investigation.</span></span>

<span data-ttu-id="900bb-205">Ejemplo de un extremo a otro con las herramientas de ETW:</span><span class="sxs-lookup"><span data-stu-id="900bb-205">End to end example using ETW tools:</span></span>

<span data-ttu-id="900bb-206">**Logman Start wstrace-BS 64-ft 1-RT-p Microsoft-Windows-webservices-o mi Trace. ETL-ETS**</span><span class="sxs-lookup"><span data-stu-id="900bb-206">**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**</span></span>

<span data-ttu-id="900bb-207">**echo... Ejecute el escenario.**</span><span class="sxs-lookup"><span data-stu-id="900bb-207">**echo .. run your scenario..**</span></span>

<span data-ttu-id="900bb-208">**Logman STOP wstrace-ETS**</span><span class="sxs-lookup"><span data-stu-id="900bb-208">**logman stop wstrace -ets**</span></span>

<span data-ttu-id="900bb-209">**tracerpt sutrace. ETL-o mytrace.xml**</span><span class="sxs-lookup"><span data-stu-id="900bb-209">**tracerpt mytrace.etl -o mytrace.xml**</span></span>

<span data-ttu-id="900bb-210">**wstrace.htm**</span><span class="sxs-lookup"><span data-stu-id="900bb-210">**wstrace.htm**</span></span>

<span data-ttu-id="900bb-211">**echo... Utilice mytrace.xml y wstrace. xsl en la página abierta.**</span><span class="sxs-lookup"><span data-stu-id="900bb-211">**echo .. use mytrace.xml and wstrace.xsl in the opened page ..**</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a><span data-ttu-id="900bb-212">Ver seguimientos de archivos de seguimiento de WWSAPI ETW mediante wstracedump.exe Tool (funciona en Windows XP y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="900bb-212">Viewing WWSAPI ETW Trace File traces using wstracedump.exe tool (works on Windows XP and above)</span></span>

<span data-ttu-id="900bb-213">Wstracedump.exe es una herramienta de consumidor de ETW desarrollada personalizada que procesa los eventos en el archivo de seguimiento de ETW de WWSAPI y genera una salida legible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="900bb-213">Wstracedump.exe is a custom developed ETW consumer tool which processes events in the WWSAPI ETW trace file and produces human readable output.</span></span> <span data-ttu-id="900bb-214">Puede generar resultados de todas las plataformas admitidas.</span><span class="sxs-lookup"><span data-stu-id="900bb-214">It can produce output from all supported platforms.</span></span> <span data-ttu-id="900bb-215">Para obtener más información, vea su uso (wstracedump.exe-?).</span><span class="sxs-lookup"><span data-stu-id="900bb-215">See its usage (wstracedump.exe -?) for more information.</span></span>

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a><span data-ttu-id="900bb-216">Ver seguimientos de archivos de seguimiento de WWSAPI ETW mediante las herramientas de ETW (funciona en Windows Vista y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="900bb-216">Viewing WWSAPI ETW Trace File traces using ETW tools (works on Windows Vista and above)</span></span>

<span data-ttu-id="900bb-217">Tracerpt.exe es la herramienta para ver el contenido de un archivo de registro de eventos ETW y disponible en todas las plataformas admitidas.</span><span class="sxs-lookup"><span data-stu-id="900bb-217">Tracerpt.exe is the tool to view the content of an ETW event log file and available on all supported platforms.</span></span> <span data-ttu-id="900bb-218">Se puede utilizar para generar archivos de volcado de memoria de CSV, EVTX o XML a partir de un archivo de registro de eventos ETW.</span><span class="sxs-lookup"><span data-stu-id="900bb-218">It can be used to generate CSV, EVTX or XML dump files from an ETW event log file.</span></span> <span data-ttu-id="900bb-219">Sin embargo, el archivo de salida generado solo tiene seguimientos legibles para el usuario en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="900bb-219">However the generated output file has human readable traces only on Windows Vista and later.</span></span> <span data-ttu-id="900bb-220">Estas instrucciones describen cómo generar el archivo de volcado XML y usarlo junto con un archivo XSL para mostrar los seguimientos en un formato bonito (el archivo XSL es muy trivial y se puede modificar si se quieren formatos diferentes).</span><span class="sxs-lookup"><span data-stu-id="900bb-220">These instructions describes how to generate the XML dump file and use it along with an xsl file to display the traces in a nice format (xsl file is very trivial and may be altered if different formats are desired).</span></span>

-   <span data-ttu-id="900bb-221">Ejecutar</span><span class="sxs-lookup"><span data-stu-id="900bb-221">Run</span></span>

    <span data-ttu-id="900bb-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span><span class="sxs-lookup"><span data-stu-id="900bb-222">**tracerpt <EtlLogFileName> -o <OutputXMLFileName>**</span></span>

    <span data-ttu-id="900bb-223">para crear un volcado XML a partir del archivo ETL binario (tracerpt.exe crea el archivo de salida en formato XML de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="900bb-223">to create an XML dump from the binary ETL file (tracerpt.exe creates the output file in XML format by default.</span></span> <span data-ttu-id="900bb-224">Ejecute tracerpt-?</span><span class="sxs-lookup"><span data-stu-id="900bb-224">Run tracerpt -?</span></span> <span data-ttu-id="900bb-225">Para ver otros formatos disponibles).</span><span class="sxs-lookup"><span data-stu-id="900bb-225">To see other available formats).</span></span>

-   <span data-ttu-id="900bb-226">Llegados a este punto, puede ver la información de seguimiento en el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="900bb-226">At this point, you can see the tracing information in the XML file.</span></span> <span data-ttu-id="900bb-227">Además, puede abrir el archivo wstrace.htm y utilizar el archivo de volcado de memoria XML y el archivo wstrace. xsl para ver los seguimientos en un formato más agradable.</span><span class="sxs-lookup"><span data-stu-id="900bb-227">Additionally, you can open the wstrace.htm file and use the xml dump file and the wstrace.xsl file to see the traces in a nicer format.</span></span> <span data-ttu-id="900bb-228">Tenga en cuenta que los archivos deben estar en el equipo local para poder usar este archivo HTML en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="900bb-228">Note that the files need to be on the local machine to be able to use this html file on IE.</span></span>

## <a name="security"></a><span data-ttu-id="900bb-229">Seguridad</span><span class="sxs-lookup"><span data-stu-id="900bb-229">Security</span></span>

<span data-ttu-id="900bb-230">Al habilitar el seguimiento, los administradores deben tener en cuenta que consume espacio en disco adicional y potencia de cálculo.</span><span class="sxs-lookup"><span data-stu-id="900bb-230">When enabling tracing, administrators should take into account that it consumes additional disk space and computation power.</span></span> <span data-ttu-id="900bb-231">Un cliente o aplicación malintencionado puede agotar los recursos del sistema a menos que la configuración de seguimiento se configure con límites razonables.</span><span class="sxs-lookup"><span data-stu-id="900bb-231">A malicious client or application may exhaust system resources unless tracing settings are configured with reasonable limits.</span></span> <span data-ttu-id="900bb-232">Al usar la característica de seguimiento de mensajes, los mensajes que llevan información confidencial, como las credenciales, la información personal, etc., pueden persistir en el disco o ser vistos por cualquier persona que tenga acceso al visor de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="900bb-232">When using message tracing feature, messages carrying sensitive information such as credentials, personal information, etc. may be persisted to the disk or be viewed by anyone who has access to the system event viewer.</span></span> <span data-ttu-id="900bb-233">Como mitigación de este problema, los usuarios del sistema o administradores pueden habilitar el seguimiento en Windows 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="900bb-233">As a mitigation to this issue, tracing can be enabled by System or Administrator users on Windows 2003 and later.</span></span> <span data-ttu-id="900bb-234">El seguimiento de mensajes está deshabilitado en Windows XP en el que cualquier usuario puede activar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="900bb-234">Message tracing is disabled on Windows XP on which any user can turn tracing on.</span></span>

<span data-ttu-id="900bb-235">La siguiente enumeración se usa con el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="900bb-235">The following enumeration is used with tracing:</span></span>

-   [<span data-ttu-id="900bb-236">**\_API de seguimiento de WS \_**</span><span class="sxs-lookup"><span data-stu-id="900bb-236">**WS\_TRACE\_API**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




