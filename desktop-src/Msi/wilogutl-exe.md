---
description: Wilogutl.exe ayuda a analizar los archivos de registro desde una instalación de Windows Installer y muestra soluciones sugeridas a los errores que se encuentran en un archivo de registro.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678586"
---
# <a name="wilogutlexe"></a><span data-ttu-id="b42a3-103">Wilogutl.exe</span><span class="sxs-lookup"><span data-stu-id="b42a3-103">Wilogutl.exe</span></span>

<span data-ttu-id="b42a3-104">Wilogutl.exe ayuda a analizar los archivos de registro desde una instalación de Windows Installer y muestra soluciones sugeridas a los errores que se encuentran en un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b42a3-104">Wilogutl.exe assists the analysis of log files from a Windows Installer installation, and it displays suggested solutions to errors that are found in a log file.</span></span>

<span data-ttu-id="b42a3-105">No se muestran los errores no críticos.</span><span class="sxs-lookup"><span data-stu-id="b42a3-105">Non-critical errors are not displayed.</span></span> <span data-ttu-id="b42a3-106">Wilogutl.exe puede ejecutarse en modo silencioso o con una interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="b42a3-106">Wilogutl.exe can be run in quiet mode or with a user interface (UI).</span></span> <span data-ttu-id="b42a3-107">La herramienta genera informes como archivos de texto en los modos de interfaz de usuario y de modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="b42a3-107">The tool generates reports as text files in both the UI and quiet modes.</span></span> <span data-ttu-id="b42a3-108">Funciona mejor con los archivos de registro detallados de Windows Installer, pero también funciona con registros no detallados.</span><span class="sxs-lookup"><span data-stu-id="b42a3-108">It works best with verbose Windows Installer log files, but also works with non-verbose logs.</span></span> <span data-ttu-id="b42a3-109">Para obtener más información, vea [Registro](logging.md).</span><span class="sxs-lookup"><span data-stu-id="b42a3-109">For more information, see [Logging](logging.md).</span></span>

<span data-ttu-id="b42a3-110">Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b42a3-110">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b42a3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b42a3-111">Syntax</span></span>

<span data-ttu-id="b42a3-112">\**wilogutl.exe\*\*\*\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span><span class="sxs-lookup"><span data-stu-id="b42a3-112">**wilogutl.exe** *\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*</span></span>

<span data-ttu-id="b42a3-113">Puede usar las siguientes líneas de comandos para ejecutarse en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="b42a3-113">You can use the following command lines to run in quiet mode.</span></span>

<span data-ttu-id="b42a3-114">**wilogutl/q/l** *c: \\ mymsilog. log* **/o** *c \\ outputDir \\*</span><span class="sxs-lookup"><span data-stu-id="b42a3-114">**wilogutl /q /l** *c:\\mymsilog.log* **/o** *c\\outputdir\\*</span></span>

<span data-ttu-id="b42a3-115">**wilogutl/q/l** *c: \\ mymsilog. log*</span><span class="sxs-lookup"><span data-stu-id="b42a3-115">**wilogutl /q /l** *c:\\mymsilog.log*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="b42a3-116">Opciones de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="b42a3-116">Command-Line Options</span></span>

<span data-ttu-id="b42a3-117">Wilogutl.exe usa las siguientes opciones de línea de comandos que no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b42a3-117">Wilogutl.exe uses the following case insensitive command-line options.</span></span> <span data-ttu-id="b42a3-118">Se puede usar un delimitador de guiones en lugar de una barra diagonal.</span><span class="sxs-lookup"><span data-stu-id="b42a3-118">A dash delimiter can be used in place of a slash.</span></span>



| <span data-ttu-id="b42a3-119">Opción</span><span class="sxs-lookup"><span data-stu-id="b42a3-119">Option</span></span> | <span data-ttu-id="b42a3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b42a3-120">Description</span></span>                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b42a3-121">ninguno</span><span class="sxs-lookup"><span data-stu-id="b42a3-121">none</span></span>   | <span data-ttu-id="b42a3-122">Se ejecuta en modo de interfaz de usuario, sin opciones de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b42a3-122">Runs in UI mode—without command-line options.</span></span>                                                                                                                                                   |
| <span data-ttu-id="b42a3-123">/q</span><span class="sxs-lookup"><span data-stu-id="b42a3-123">/q</span></span>     | <span data-ttu-id="b42a3-124">Especifica el modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="b42a3-124">Specifies the quiet mode.</span></span> <span data-ttu-id="b42a3-125">Wilogutl.exe genera archivos de informe y no muestra ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b42a3-125">Wilogutl.exe generates report files and does not display a user interface.</span></span>                                                                                            |
| <span data-ttu-id="b42a3-126">/l</span><span class="sxs-lookup"><span data-stu-id="b42a3-126">/l</span></span>     | <span data-ttu-id="b42a3-127">Especifica el nombre del archivo de registro que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="b42a3-127">Specifies the name of the log file to be analyzed.</span></span> <span data-ttu-id="b42a3-128">Esta opción es necesaria cuando se usa el modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="b42a3-128">This option is required when using the quiet mode.</span></span>                                                                                           |
| <span data-ttu-id="b42a3-129">/o</span><span class="sxs-lookup"><span data-stu-id="b42a3-129">/o</span></span>     | <span data-ttu-id="b42a3-130">Especifica el directorio de salida para los archivos de informe.</span><span class="sxs-lookup"><span data-stu-id="b42a3-130">Specifies the output directory for report files.</span></span> <span data-ttu-id="b42a3-131">Esta ruta de acceso de salida solo se usa cuando se ejecuta en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="b42a3-131">This output path is used only when running in quiet mode.</span></span> <span data-ttu-id="b42a3-132">Si la opción no está presente, los informes se colocan en el \\ directorio C: WiLogResults</span><span class="sxs-lookup"><span data-stu-id="b42a3-132">If the option is not present, the reports are put in the C:\\WiLogResults directory.</span></span> |



 

<span data-ttu-id="b42a3-133">Cuando se ejecuta en modo de interfaz de usuario, Wilogutl.exe muestra los siguientes cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b42a3-133">When run in UI mode, Wilogutl.exe displays the following dialog boxes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b42a3-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="b42a3-134">Name</span></span></th>
<th><span data-ttu-id="b42a3-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="b42a3-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b42a3-136">Analizador de registros detallado Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b42a3-136">Windows Installer Verbose Log Analyzer</span></span></td>
<td><span data-ttu-id="b42a3-137">El cuadro de diálogo Windows Installer analizador de registros detallado permite a los usuarios seleccionar un archivo de registro para su análisis:</span><span class="sxs-lookup"><span data-stu-id="b42a3-137">The Windows Installer Verbose Log Analyzer dialog box enables users to select a log file for analysis:</span></span>
<ul>
<li><span data-ttu-id="b42a3-138">El botón <strong>abrir</strong> abre el archivo en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="b42a3-138">The <strong>Open</strong> button opens the file in Notepad.</span></span> <span data-ttu-id="b42a3-139">El área de vista previa se puede usar para comprobar que se ha seleccionado el archivo de registro correcto.</span><span class="sxs-lookup"><span data-stu-id="b42a3-139">The preview area can be used to verify that the correct log file has been selected.</span></span></li>
<li><span data-ttu-id="b42a3-140">El botón <strong>analizar</strong> inicia el análisis del archivo de registro y muestra el cuadro de diálogo vista de archivo de registro detallada.</span><span class="sxs-lookup"><span data-stu-id="b42a3-140">The <strong>Analyze</strong> button begins log file analysis and displays the Detailed Log File View dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b42a3-141">Vista detallada del archivo de registro</span><span class="sxs-lookup"><span data-stu-id="b42a3-141">Detailed Log File View</span></span></td>
<td><span data-ttu-id="b42a3-142">En el cuadro de diálogo vista de archivo de registro detallada se muestra la información de error registrada.</span><span class="sxs-lookup"><span data-stu-id="b42a3-142">The Detailed Log File View dialog box displays logged error information.</span></span> <span data-ttu-id="b42a3-143">Use los botones <strong>atrás</strong> y <strong>siguiente</strong> para navegar por varios errores.</span><span class="sxs-lookup"><span data-stu-id="b42a3-143">Use the <strong>Back</strong> and <strong>Next</strong> buttons to navigate through multiple errors.</span></span> <span data-ttu-id="b42a3-144">Para mostrar los errores no críticos, active la casilla <strong>Mostrar errores de depuración omitidos</strong> .</span><span class="sxs-lookup"><span data-stu-id="b42a3-144">To display non-critical errors select the <strong>Show Ignored Debug Errors</strong> check box.</span></span> <span data-ttu-id="b42a3-145">Se muestra la versión del instalador en el equipo que se usa para ejecutar la instalación registrada.</span><span class="sxs-lookup"><span data-stu-id="b42a3-145">The installer version on the computer used to run the logged installation is displayed.</span></span> <span data-ttu-id="b42a3-146">Si la instalación registrada se ejecutó con permisos elevados, la casilla de <strong>instalación</strong> con privilegios elevados está activada y se proporciona información en los cuadros de texto <strong>detalles de privilegios</strong> del lado del cliente y detalles de los <strong>privilegios del servidor</strong> .</span><span class="sxs-lookup"><span data-stu-id="b42a3-146">If the logged installation was run with elevated permissions, the <strong>Elevated install</strong> check box is selected and information is provided in the <strong>Client Side Privilege Details</strong> and <strong>Server Side Privilege Details</strong> text boxes.</span></span> <span data-ttu-id="b42a3-147">El cuadro de diálogo vista de archivo de registro detallado contiene los siguientes botones:</span><span class="sxs-lookup"><span data-stu-id="b42a3-147">The Detailed Log File View dialog box contains the following buttons:</span></span><br/>
<ul>
<li><span data-ttu-id="b42a3-148"><strong>Estados</strong> - de Muestra el cuadro de diálogo Estados de características y componentes.</span><span class="sxs-lookup"><span data-stu-id="b42a3-148"><strong>States</strong> - Show the Feature and Component States dialog box.</span></span></li>
<li><span data-ttu-id="b42a3-149"><strong>Propiedades</strong> - de Mostrar el cuadro de diálogo Propiedades.</span><span class="sxs-lookup"><span data-stu-id="b42a3-149"><strong>Properties</strong> - Show the Properties dialog box.</span></span></li>
<li><span data-ttu-id="b42a3-150"><strong>Directivas</strong> - de Muestra el cuadro de diálogo directivas.</span><span class="sxs-lookup"><span data-stu-id="b42a3-150"><strong>Policies</strong> - Show the Policies dialog box.</span></span></li>
<li><span data-ttu-id="b42a3-151">Registro anotado <strong>HTML</strong> - Muestra el registro como archivo HTML anotado.</span><span class="sxs-lookup"><span data-stu-id="b42a3-151"><strong>HTML Annotated Log</strong> - Show log as annotated HTML file.</span></span></li>
<li><span data-ttu-id="b42a3-152"><strong>Guardar resultados</strong> - Guardar archivos de informe en el directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="b42a3-152"><strong>Save Results</strong> - Save report files to specified directory.</span></span></li>
<li><span data-ttu-id="b42a3-153">Ayuda del mensaje de <strong>error</strong> - Muestra la ayuda del mensaje de error del instalador.</span><span class="sxs-lookup"><span data-stu-id="b42a3-153"><strong>Error Message Help</strong> - Show installer error message help.</span></span></li>
<li><span data-ttu-id="b42a3-154"><strong>Ayuda</strong> - de Mostrar ayuda para Windows Installer el analizador de registros de instalación.</span><span class="sxs-lookup"><span data-stu-id="b42a3-154"><strong>Help</strong> - Show help for Windows Installer Setup Log Analyzer.</span></span></li>
<li><span data-ttu-id="b42a3-155"><strong>Cómo leer un archivo</strong> - de registro Muestra el documento de ayuda del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b42a3-155"><strong>How to Read a Log File</strong> - Show the log file help document.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b42a3-156">Estados de características y componentes</span><span class="sxs-lookup"><span data-stu-id="b42a3-156">Feature and Component States</span></span></td>
<td><span data-ttu-id="b42a3-157">El cuadro de diálogo Estados de características <strong>y</strong> componentes muestra los Estados de características y componentes:</span><span class="sxs-lookup"><span data-stu-id="b42a3-157">The <strong>Feature and Component States</strong> dialog box displays the states of features and components:</span></span>
<ul>
<li><span data-ttu-id="b42a3-158">La columna <strong>característica</strong> muestra el nombre de la característica en el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="b42a3-158">The <strong>Feature</strong> column shows the name for the feature in the installation package.</span></span></li>
<li><span data-ttu-id="b42a3-159">La columna <strong>componente</strong> muestra el nombre del componente en el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="b42a3-159">The <strong>Component</strong> column shows the name of the component in the installation package.</span></span></li>
<li><span data-ttu-id="b42a3-160">La columna <strong>instalado</strong> muestra la característica o el estado del componente al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="b42a3-160">The <strong>Installed</strong> column shows the feature or component's state at the end of the installation.</span></span></li>
<li><span data-ttu-id="b42a3-161">La columna <strong>solicitud</strong> muestra la selección del usuario durante la instalación del estado de la característica o del componente.</span><span class="sxs-lookup"><span data-stu-id="b42a3-161">The <strong>Request</strong> column shows the user's selection during the installation for the feature or component's state.</span></span></li>
<li><span data-ttu-id="b42a3-162">La columna <strong>acción</strong> muestra la acción realizada por el instalador para la característica o componente.</span><span class="sxs-lookup"><span data-stu-id="b42a3-162">The <strong>Action</strong> column shows the action taken by the installer for the feature or component.</span></span></li>
</ul>
<span data-ttu-id="b42a3-163">Para obtener más información, vea <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> y <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b42a3-163">For more information, see <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> and <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b42a3-164">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b42a3-164">Properties</span></span></td>
<td><span data-ttu-id="b42a3-165">El cuadro de diálogo Propiedades muestra Windows Installer <a href="properties.md">propiedades</a> y sus valores al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="b42a3-165">The Properties dialog box shows Windows Installer <a href="properties.md">Properties</a> and their values at the end of the installation.</span></span> <span data-ttu-id="b42a3-166">Puede ordenar las propiedades por nombre o por valor:</span><span class="sxs-lookup"><span data-stu-id="b42a3-166">You can sort the properties by name or by value:</span></span>
<ul>
<li><span data-ttu-id="b42a3-167">La pestaña <strong>cliente</strong> muestra propiedades y valores durante la parte del cliente de la instalación.</span><span class="sxs-lookup"><span data-stu-id="b42a3-167">The <strong>Client</strong> tab shows properties and values during the client side portion of the installation.</span></span></li>
<li><span data-ttu-id="b42a3-168">En la pestaña <strong>servidor</strong> se muestran las propiedades y los valores durante la parte de servidor de la instalación.</span><span class="sxs-lookup"><span data-stu-id="b42a3-168">The <strong>Server</strong> tab shows properties and values during the server portion of the installation.</span></span></li>
<li><span data-ttu-id="b42a3-169">En la pestaña <strong>anidado</strong> se muestran las propiedades y los valores de las <a href="concurrent-installations.md">instalaciones simultáneas</a>.</span><span class="sxs-lookup"><span data-stu-id="b42a3-169">The <strong>Nested</strong> tab shows the properties and values of any <a href="concurrent-installations.md">Concurrent Installations</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b42a3-170">Directivas</span><span class="sxs-lookup"><span data-stu-id="b42a3-170">Policies</span></span></td>
<td><span data-ttu-id="b42a3-171">En el cuadro de diálogo directivas se muestra el conjunto de <a href="system-policy.md">directivas del sistema</a> después de la instalación:</span><span class="sxs-lookup"><span data-stu-id="b42a3-171">The Policies dialog box displays the <a href="system-policy.md">System Policy</a> set after the installation:</span></span>
<ul>
<li><span data-ttu-id="b42a3-172">Un valor de 0 (cero) establecido para la directiva significa que la Directiva no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b42a3-172">A value of 0 (zero) set for the policy means the policy is not enabled.</span></span></li>
<li><span data-ttu-id="b42a3-173">Un valor de 1 (uno) significa que la Directiva está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b42a3-173">A value of 1 (one) means the policy is enabled.</span></span></li>
<li><span data-ttu-id="b42a3-174">Un valor de?</span><span class="sxs-lookup"><span data-stu-id="b42a3-174">A value of ?</span></span> <span data-ttu-id="b42a3-175">(signo de interrogación) significa que el valor de la Directiva no se registra en el registro.</span><span class="sxs-lookup"><span data-stu-id="b42a3-175">(question mark) means the policy value is not recorded in the log.</span></span></li>
</ul>
<span data-ttu-id="b42a3-176">Si necesita un valor de directiva que no esté en el registro, pruebe a usar Regedit.exe para comprobar las claves del registro en el equipo que no se puede realizar la instalación.</span><span class="sxs-lookup"><span data-stu-id="b42a3-176">If you need a policy value that is not in the log, try using Regedit.exe to check the registry keys on the computer failing the installation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a><span data-ttu-id="b42a3-177">Archivos de informe</span><span class="sxs-lookup"><span data-stu-id="b42a3-177">Report Files</span></span>

<span data-ttu-id="b42a3-178">Al realizar un análisis de modo silencioso o al hacer clic en el botón **Guardar resultados** en el cuadro de diálogo **vista detallada del archivo de registro** , la herramienta analizador de instalación de Windows Installer genera tres archivos de texto y un archivo de registro anotado en HTML.</span><span class="sxs-lookup"><span data-stu-id="b42a3-178">When performing a quiet mode analysis or clicking the **Save Results** button on the **Detailed Log File View** dialog, the Windows Installer Setup Analyzer tool generates three text files and an HTML annotated log file.</span></span>

<span data-ttu-id="b42a3-179">En la tabla siguiente se identifican los nombres y el contenido de los archivos de informe.</span><span class="sxs-lookup"><span data-stu-id="b42a3-179">The following table identifies the names and contents in the report files.</span></span>



| <span data-ttu-id="b42a3-180">Nombre</span><span class="sxs-lookup"><span data-stu-id="b42a3-180">Name</span></span>                      | <span data-ttu-id="b42a3-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="b42a3-181">Description</span></span>                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b42a3-182">nombreDeArchivoDeRegistro \_summary.txt</span><span class="sxs-lookup"><span data-stu-id="b42a3-182">logfilename\_summary.txt</span></span>  | <span data-ttu-id="b42a3-183">Resume el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b42a3-183">Summarizes the log file.</span></span> <span data-ttu-id="b42a3-184">Muestra la información que se muestra en el cuadro de diálogo vista de archivo de registro detallada y el primer error.</span><span class="sxs-lookup"><span data-stu-id="b42a3-184">Lists the information displayed by the Detailed Log File View dialog box and the first error.</span></span>         |
| <span data-ttu-id="b42a3-185">nombreDeArchivoDeRegistro \_errors.txt</span><span class="sxs-lookup"><span data-stu-id="b42a3-185">logfilename\_errors.txt</span></span>   | <span data-ttu-id="b42a3-186">Identifica el número de errores, los errores y las soluciones recomendadas.</span><span class="sxs-lookup"><span data-stu-id="b42a3-186">Identifies the number of errors, the errors, and recommended solutions.</span></span> <span data-ttu-id="b42a3-187">En este archivo se enumeran los errores críticos y no críticos.</span><span class="sxs-lookup"><span data-stu-id="b42a3-187">This file lists both critical and non-critical errors.</span></span> |
| <span data-ttu-id="b42a3-188">nombreDeArchivoDeRegistro \_policies.txt</span><span class="sxs-lookup"><span data-stu-id="b42a3-188">logfilename\_policies.txt</span></span> | <span data-ttu-id="b42a3-189">Identifica los nombres de directiva y los valores establecidos al final de la instalación, como en el cuadro de diálogo directivas.</span><span class="sxs-lookup"><span data-stu-id="b42a3-189">Identifies the policy names and values set at the end of the installation as in the Policies dialog box.</span></span>                       |
| <span data-ttu-id="b42a3-190">detalles \_logfilename.htm</span><span class="sxs-lookup"><span data-stu-id="b42a3-190">details\_logfilename.htm</span></span>  | <span data-ttu-id="b42a3-191">Un registro anotado en HTML con una leyenda para la codificación de colores.</span><span class="sxs-lookup"><span data-stu-id="b42a3-191">An HTML annotated log with a legend for the color coding.</span></span>                                                                      |



 

## <a name="return-values"></a><span data-ttu-id="b42a3-192">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b42a3-192">Return Values</span></span>

<span data-ttu-id="b42a3-193">Si se pasan argumentos de línea de comandos no válidos para las operaciones de modo silencioso, Wilogutl.exe no hace nada y el proceso devuelve uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b42a3-193">If invalid command-line arguments are passed for quiet mode operations, Wilogutl.exe does nothing, and the process returns one of the values in the following table.</span></span>



| <span data-ttu-id="b42a3-194">Value</span><span class="sxs-lookup"><span data-stu-id="b42a3-194">Value</span></span> | <span data-ttu-id="b42a3-195">Significado</span><span class="sxs-lookup"><span data-stu-id="b42a3-195">Meaning</span></span>                                                                 |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="b42a3-196">1</span><span class="sxs-lookup"><span data-stu-id="b42a3-196">1</span></span>     | <span data-ttu-id="b42a3-197">Se ha especificado un directorio de salida incorrecto.</span><span class="sxs-lookup"><span data-stu-id="b42a3-197">Bad output directory is specified.</span></span>                                      |
| <span data-ttu-id="b42a3-198">2</span><span class="sxs-lookup"><span data-stu-id="b42a3-198">2</span></span>     | <span data-ttu-id="b42a3-199">Se ha especificado un nombre de archivo de registro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="b42a3-199">Bad log file name is specified.</span></span>                                         |
| <span data-ttu-id="b42a3-200">3</span><span class="sxs-lookup"><span data-stu-id="b42a3-200">3</span></span>     | <span data-ttu-id="b42a3-201">Se pasó/q, pero falta el modificador/l necesario para el nombre del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b42a3-201">Passed /q, but is missing the required switch /l for the log file name.</span></span> |
| <span data-ttu-id="b42a3-202">4</span><span class="sxs-lookup"><span data-stu-id="b42a3-202">4</span></span>     | <span data-ttu-id="b42a3-203">Se pasó/l, pero falta el modificador "/q" necesario para el modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="b42a3-203">Passed /l, but is missing the required switch /q for quiet mode.</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b42a3-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b42a3-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b42a3-205">Versiones publicadas, herramientas y redistribuibles</span><span class="sxs-lookup"><span data-stu-id="b42a3-205">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> <dt>

[<span data-ttu-id="b42a3-206">Herramientas de desarrollo de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="b42a3-206">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> </dl>

 

 




