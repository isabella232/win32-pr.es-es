---
<span data-ttu-id="1dfbd-101">Descripción: el programa ejecutable que interpreta paquetes e instala productos es Msiexec.exe. Nota: msiexec también establece un nivel de error en la devolución que corresponde a los códigos de error del sistema.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-101">description: The executable program that interprets packages and installs products is Msiexec.exe.Note  Msiexec also sets an error level on return that corresponds to System Error Codes.</span></span> <span data-ttu-id="1dfbd-102">En la tabla siguiente se identifican las opciones de línea de comandos estándar para este programa.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-102">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="1dfbd-103">Las opciones de línea de comandos no distinguen mayúsculas de minúsculas. Windows Installer 2,0: las opciones de línea de comandos que se identifican en este tema están disponibles a partir de Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-103">Command-line options are case insensitive.Windows Installer 2.0:  The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="1dfbd-104">Las opciones de Command-Line de Windows Installer están disponibles con Windows Installer&\# 160; 3.0 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-104">The Windows Installer Command-Line Options are available with Windows Installer&\#160;3.0 and earlier versions.</span></span>
<span data-ttu-id="1dfbd-105">MS. AssetID: b1707c88-1cca-45ab-bb23-6002bfd5204e title: instalador estándar Command-Line opciones ms. topic: artículo ms. Date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="1dfbd-105">ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="standard-installer-command-line-options"></a><span data-ttu-id="1dfbd-106">Opciones de Command-Line del instalador estándar</span><span class="sxs-lookup"><span data-stu-id="1dfbd-106">Standard Installer Command-Line Options</span></span>

<span data-ttu-id="1dfbd-107">El programa ejecutable que interpreta paquetes e instala productos es Msiexec.exe.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-107">The executable program that interprets packages and installs products is Msiexec.exe.</span></span>

> [!Note]  
> <span data-ttu-id="1dfbd-108">Msiexec también establece un nivel de error en la devolución que corresponde a los [códigos de error del sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1dfbd-108">Msiexec also sets an error level on return that corresponds to [System Error Codes](../debug/system-error-codes.md).</span></span>

 

<span data-ttu-id="1dfbd-109">En la tabla siguiente se identifican las opciones de línea de comandos estándar para este programa.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-109">The following table identifies the standard command-line options for this program.</span></span> <span data-ttu-id="1dfbd-110">Las opciones de línea de comandos no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-110">Command-line options are case insensitive.</span></span>

<span data-ttu-id="1dfbd-111">**Windows Installer 2,0:** Las opciones de línea de comandos que se identifican en este tema están disponibles a partir de Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-111">**Windows Installer 2.0:** The command-line options that are identified in this topic are available beginning with Windows Installer 3.0.</span></span> <span data-ttu-id="1dfbd-112">Las [Opciones de línea de comandos](command-line-options.md) de Windows Installer están disponibles con Windows Installer 3,0 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-112">The Windows Installer [Command-Line Options](command-line-options.md) are available with Windows Installer 3.0 and earlier versions.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1dfbd-113">Opción</span><span class="sxs-lookup"><span data-stu-id="1dfbd-113">Option</span></span></th>
<th><span data-ttu-id="1dfbd-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dfbd-114">Parameters</span></span></th>
<th><span data-ttu-id="1dfbd-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1dfbd-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1dfbd-116"><strong>/help</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-116"><strong>/help</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="1dfbd-117">Opción de ayuda y referencia rápida.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-117">Help and quick reference option.</span></span> <span data-ttu-id="1dfbd-118">Muestra el uso correcto del comando de instalación, incluida una lista de todos los modificadores y el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-118">Displays the correct usage of the setup command including a list of all switches and behavior.</span></span> <span data-ttu-id="1dfbd-119">La descripción del uso se puede mostrar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-119">The description of usage can be displayed in the user interface.</span></span> <span data-ttu-id="1dfbd-120">El uso incorrecto de cualquier opción invoca esta opción de ayuda.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-120">Incorrect use of any option invokes this help option.</span></span><br/> <span data-ttu-id="1dfbd-121">Ejemplo: <strong>msiexec/Help</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-121">Example: <strong>msiexec /help</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-122">La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/?</strong>.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-122">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/?</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dfbd-123"><strong>/quiet</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-123"><strong>/quiet</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="1dfbd-124">Opción de pantalla silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-124">Quiet display option.</span></span> <span data-ttu-id="1dfbd-125">El instalador ejecuta una instalación sin mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-125">The installer runs an installation without displaying a user interface.</span></span> <span data-ttu-id="1dfbd-126">No se muestra al usuario ningún mensaje, mensaje o cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-126">No prompts, messages, or dialog boxes are displayed to the user.</span></span> <span data-ttu-id="1dfbd-127">El usuario no puede cancelar la instalación.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-127">The user cannot cancel the installation.</span></span> <span data-ttu-id="1dfbd-128">Use las opciones de línea de comandos <strong>/norestart</strong> o <strong>/forcerestart</strong> estándar para controlar los reinicios.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-128">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="1dfbd-129">Si no se especifica ninguna opción de reinicio, el programa de instalación reinicia el equipo siempre que sea necesario sin mostrar ningún mensaje o advertencia al usuario.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-129">If no reboot options are specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span><br/> <span data-ttu-id="1dfbd-130">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="1dfbd-130">Examples:</span></span> <br/> <span data-ttu-id="1dfbd-131"><strong>msiexec/Package Application.msi/Quiet</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-131"><strong>msiexec /package Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="1dfbd-132"><strong>Msiexec/Uninstall Application.msi/Quiet</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-132"><strong>Msiexec /uninstall Application.msi /quiet</strong></span></span><br/> <span data-ttu-id="1dfbd-133"><strong>Msiexec/update msipatch. MSP/Quiet</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-133"><strong>Msiexec /update msipatch.msp /quiet</strong></span></span><br/> <span data-ttu-id="1dfbd-134"><strong>Msiexec/Uninstall msipatch. MSP/Package Application.msi/Quiet</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-134"><strong>Msiexec /uninstall msipatch.msp /package Application.msi / quiet</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-135">La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/QN</strong>.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-135">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qn</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dfbd-136"><strong>/passive</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-136"><strong>/passive</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="1dfbd-137">Opción de presentación pasiva.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-137">Passive display option.</span></span> <span data-ttu-id="1dfbd-138">El instalador muestra una barra de progreso al usuario que indica que hay una instalación en curso, pero no se muestra ningún mensaje de error ni mensajes de error al usuario.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-138">The installer displays a progress bar to the user that indicates that an installation is in progress but no prompts or error messages are displayed to the user.</span></span> <span data-ttu-id="1dfbd-139">El usuario no puede cancelar la instalación.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-139">The user cannot cancel the installation.</span></span> <span data-ttu-id="1dfbd-140">Use las opciones de línea de comandos <strong>/norestart</strong> o <strong>/forcerestart</strong> estándar para controlar los reinicios.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-140">Use the <strong>/norestart</strong> or <strong>/forcerestart</strong> standard command-line options to control reboots.</span></span> <span data-ttu-id="1dfbd-141">Si no se especifica ninguna opción de reinicio, el programa de instalación reinicia el equipo siempre que sea necesario sin mostrar ningún mensaje o advertencia al usuario.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-141">If no reboot option is specified, the installer restarts the computer whenever necessary without displaying any prompt or warning to the user.</span></span> <br/> <span data-ttu-id="1dfbd-142">Ejemplo: <strong>msiexec/package Application.msi/Passive</strong> </span><span class="sxs-lookup"><span data-stu-id="1dfbd-142">Example: <strong>msiexec /package Application.msi /passive</strong> </span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-143">La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S establecida en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-143">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dfbd-144"><strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-144"><strong>/norestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="1dfbd-145">Opción de reinicio nunca.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-145">Never restart option.</span></span> <span data-ttu-id="1dfbd-146">El instalador nunca reinicia el equipo después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-146">The installer never restarts the computer after the installation.</span></span><br/> <span data-ttu-id="1dfbd-147">Ejemplo: msiexec/Package Application.msi <strong>/norestart</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-147">Example: msiexec /package Application.msi <strong>/norestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-148">La línea de comandos de Windows Installer equivalente tiene el <a href="reboot.md"><strong>reinicio</strong></a>= ReallySuppress establecido en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-148">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dfbd-149"><strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-149"><strong>/forcerestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="1dfbd-150">Opción de reinicio siempre.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-150">Always restart option.</span></span> <span data-ttu-id="1dfbd-151">El instalador reinicia siempre el equipo después de cada instalación.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-151">The installer always restarts the computer after every installation.</span></span><br/> <span data-ttu-id="1dfbd-152">Ejemplo: msiexec/Package Application.msi <strong>/forcerestart</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-152">Example: msiexec /package Application.msi <strong>/forcerestart</strong></span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-153">La línea de comandos de Windows Installer equivalente tiene el <a href="reboot.md"><strong>reinicio</strong></a>= Force establecido en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-153">The equivalent Windows Installer command line has <a href="reboot.md"><strong>REBOOT</strong></a>=Force set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dfbd-154"><strong>/promptrestart</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-154"><strong>/promptrestart</strong></span></span></td>
<td> </td>
<td><span data-ttu-id="1dfbd-155">Preguntar antes de reiniciar.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-155">Prompt before restarting option.</span></span> <span data-ttu-id="1dfbd-156">Muestra un mensaje que indica que es necesario reiniciar para completar la instalación y pregunta al usuario si desea reiniciar el sistema ahora.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-156">Displays a message that a restart is required to complete the installation and asks the user whether to restart the system now.</span></span> <span data-ttu-id="1dfbd-157">Esta opción no se puede usar junto con la opción <strong>/Quiet</strong> .</span><span class="sxs-lookup"><span data-stu-id="1dfbd-157">This option cannot be used together with the <strong>/quiet</strong> option.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-158">La línea de comandos de Windows Installer equivalente tiene <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; establecido en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-158">The equivalent Windows Installer command line has <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a> = &quot;&quot; set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dfbd-159"><strong>/uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-159"><strong>/uninstall</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="1dfbd-160">Opción de desinstalación del producto.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-160">Uninstall product option.</span></span> <span data-ttu-id="1dfbd-161">Desinstala un producto.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-161">Uninstalls a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-162">La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/x</strong>.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-162">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/x</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dfbd-163"><strong>/uninstall</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-163"><strong>/uninstall</strong></span></span></td>
<td><span data-ttu-id="1dfbd-164"><em>/Package <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. MSP | PatchGUID2]</em></span><span class="sxs-lookup"><span data-stu-id="1dfbd-164"><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1>[;Update2.msp | PatchGUID2]</em></span></span></td>
<td><span data-ttu-id="1dfbd-165">Desinstalar opción de actualización.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-165">Uninstall update option.</span></span> <span data-ttu-id="1dfbd-166">Desinstala una revisión de actualización.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-166">Uninstalls an update patch.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-167">La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/i</strong> con <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>= update1. MSP | PatchGUID1[; Update2. MSP | PatchGUID2] establecido en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-167">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong> with <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[;Update2.msp | PatchGUID2] set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dfbd-168"><strong>/log</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-168"><strong>/log</strong></span></span></td>
<td><em><logfile></em></td>
<td><span data-ttu-id="1dfbd-169">Opción de registro.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-169">Log option.</span></span> <span data-ttu-id="1dfbd-170">Escribe información de registro en un archivo de registro en la ruta de acceso existente especificada.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-170">Writes logging information into a log file at the specified existing path.</span></span> <span data-ttu-id="1dfbd-171">La ruta de acceso a la ubicación del archivo de registro ya debe existir.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-171">The path to the log file location must already exist.</span></span> <span data-ttu-id="1dfbd-172">El instalador no crea la estructura de directorios para el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-172">The installer does not create the directory structure for the logfile.</span></span><br/> <span data-ttu-id="1dfbd-173">La siguiente información se especifica en el registro:</span><span class="sxs-lookup"><span data-stu-id="1dfbd-173">The following information is entered into the log:</span></span><br/>
<ul>
<li><span data-ttu-id="1dfbd-174">Mensajes de estado</span><span class="sxs-lookup"><span data-stu-id="1dfbd-174">Status messages</span></span></li>
<li><span data-ttu-id="1dfbd-175">Advertencias no graves</span><span class="sxs-lookup"><span data-stu-id="1dfbd-175">Nonfatal warnings</span></span></li>
<li><span data-ttu-id="1dfbd-176">Todos los mensajes de error</span><span class="sxs-lookup"><span data-stu-id="1dfbd-176">All error messages</span></span></li>
<li><span data-ttu-id="1dfbd-177">Inicio de acciones</span><span class="sxs-lookup"><span data-stu-id="1dfbd-177">Start up of actions</span></span></li>
<li><span data-ttu-id="1dfbd-178">Registros específicos de la acción</span><span class="sxs-lookup"><span data-stu-id="1dfbd-178">Action-specific records</span></span></li>
<li><span data-ttu-id="1dfbd-179">Solicitudes de usuario</span><span class="sxs-lookup"><span data-stu-id="1dfbd-179">User requests</span></span></li>
<li><span data-ttu-id="1dfbd-180">Parámetros iniciales de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="1dfbd-180">Initial UI parameters</span></span></li>
<li><span data-ttu-id="1dfbd-181">Memoria insuficiente o información de salida irrecuperable</span><span class="sxs-lookup"><span data-stu-id="1dfbd-181">Out-of-memory or fatal exit information</span></span></li>
<li><span data-ttu-id="1dfbd-182">Mensajes de espacio insuficiente en disco</span><span class="sxs-lookup"><span data-stu-id="1dfbd-182">Out-of-disk-space messages</span></span></li>
<li><span data-ttu-id="1dfbd-183">Propiedades de terminal</span><span class="sxs-lookup"><span data-stu-id="1dfbd-183">Terminal properties</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-184">La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/l \*</strong>.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-184">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/L\*</strong>.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-185">Para obtener más información acerca de todos los métodos que están disponibles para establecer el modo de registro, consulte el <a href="normal-logging.md">registro normal</a> en la sección <a href="windows-installer-logging.md">registro de Windows Installer</a> .</span><span class="sxs-lookup"><span data-stu-id="1dfbd-185">For more information about all the methods that are available for setting the logging mode, see <a href="normal-logging.md">Normal Logging</a> in the <a href="windows-installer-logging.md">Windows Installer Logging</a> section.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1dfbd-186"><strong>/Package</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-186"><strong>/package</strong></span></span></td>
<td><em><Package.msi|ProductCode></em></td>
<td><span data-ttu-id="1dfbd-187">Opción instalar producto.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-187">Install product option.</span></span> <span data-ttu-id="1dfbd-188">Instala o configura un producto.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-188">Installs or configures a product.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-189">La <a href="command-line-options.md">opción de línea de comandos</a> equivalente Windows Installer es <strong>/i</strong>.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-189">The equivalent Windows Installer <a href="command-line-options.md">Command-Line Option</a> is <strong>/I</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1dfbd-190"><strong>/Update</strong></span><span class="sxs-lookup"><span data-stu-id="1dfbd-190"><strong>/update</strong></span></span></td>
<td><span data-ttu-id="1dfbd-191"><em><Update1.msp>[; Update2. MSP]</em></span><span class="sxs-lookup"><span data-stu-id="1dfbd-191"><em><Update1.msp>[;Update2.msp]</em></span></span></td>
<td><span data-ttu-id="1dfbd-192">Opción instalar revisiones.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-192">Install patches option.</span></span> <span data-ttu-id="1dfbd-193">Instala una o varias revisiones.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-193">Installs one or multiple patches.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1dfbd-194">La línea de comandos de Windows Installer equivalente tiene <a href="patch.md"><strong>patch</strong></a> = [msipatch. msp] <; PatchGuid2> establece en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="1dfbd-194">The equivalent Windows Installer command line has <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<;PatchGuid2> set on the command line.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
