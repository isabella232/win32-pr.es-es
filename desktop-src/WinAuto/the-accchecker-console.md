---
title: La consola de AccChecker
description: La consola de AccChecker (AccCheckConsole.exe) es una herramienta de línea de comandos para comprobar la implementación de accesibilidad de la interfaz de usuario de la aplicación.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Consola de AccChecker
- Herramienta de línea de comandos AccChecker
- línea de comandos, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903180"
---
# <a name="the-accchecker-console"></a><span data-ttu-id="c175f-106">La consola de AccChecker</span><span class="sxs-lookup"><span data-stu-id="c175f-106">The AccChecker Console</span></span>

<span data-ttu-id="c175f-107">La consola de AccChecker (AccCheckConsole.exe) es una herramienta de línea de comandos para comprobar la implementación de accesibilidad de la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c175f-107">AccChecker Console (AccCheckConsole.exe) is a command-line tool for verifying the accessibility implementation of your application's UI.</span></span> <span data-ttu-id="c175f-108">La línea de comandos acepta diversas entradas (como HWND, título de ventana y rutina de comprobación) y proporciona un código de salida que corresponde al número de registros de errores.</span><span class="sxs-lookup"><span data-stu-id="c175f-108">The command-line accepts a variety of inputs (such as HWND, window title, and verification routine) and supplies an exit code that corresponds to the error log count.</span></span>

-   [<span data-ttu-id="c175f-109">Sintaxis de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="c175f-109">Command-line Syntax</span></span>](#command-line-syntax)
-   [<span data-ttu-id="c175f-110">Códigos de error de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="c175f-110">Command-line Error Codes</span></span>](#command-line-error-codes)
-   [<span data-ttu-id="c175f-111">Ejemplos de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="c175f-111">Command-line Examples</span></span>](#command-line-examples)
-   [<span data-ttu-id="c175f-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c175f-112">Related topics</span></span>](#related-topics)

![herramienta de línea de comandos de la consola de accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a><span data-ttu-id="c175f-114">Sintaxis de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="c175f-114">Command-line Syntax</span></span>

<span data-ttu-id="c175f-115">La consola de AccChecker tiene la siguiente sintaxis de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="c175f-115">AccChecker Console has the following command-line syntax.</span></span>

<span data-ttu-id="c175f-116">**\[Opciones \] de AccCheckConsole (-HWND <hwnd> \| -Process <name> )\[<dlls>\]**</span><span class="sxs-lookup"><span data-stu-id="c175f-116">**AccCheckConsole \[options\] (-hwnd <hwnd> \| -process <name>) \[<dlls>\]**</span></span>

<span data-ttu-id="c175f-117">Las opciones de línea de comandos son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="c175f-117">The command-line options are as follows.</span></span>



| <span data-ttu-id="c175f-118">Opciones</span><span class="sxs-lookup"><span data-stu-id="c175f-118">Options</span></span>                                                                                                                                                         | <span data-ttu-id="c175f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c175f-119">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c175f-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd></span><span class="sxs-lookup"><span data-stu-id="c175f-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd></span></span><br/>                                                                     | <span data-ttu-id="c175f-121">Valida la ventana que tiene el identificador especificado (HWND).</span><span class="sxs-lookup"><span data-stu-id="c175f-121">Validates the window that has the specified handle (HWND).</span></span> <span data-ttu-id="c175f-122">El identificador se puede especificar en valores hexadecimales o decimales.</span><span class="sxs-lookup"><span data-stu-id="c175f-122">The handle can be specified in hexidecimal or decimal.</span></span><br/> |
| <span data-ttu-id="c175f-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-Window <title></span><span class="sxs-lookup"><span data-stu-id="c175f-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window <title></span></span><br/>                                                            | <span data-ttu-id="c175f-124">Valida la ventana que tiene el título especificado.</span><span class="sxs-lookup"><span data-stu-id="c175f-124">Validates the window that has the specified title.</span></span><br/>                                                                |
| <span data-ttu-id="c175f-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -proceso <name></span><span class="sxs-lookup"><span data-stu-id="c175f-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process <name></span></span><br/>                       | <span data-ttu-id="c175f-126">Valida la ventana principal del proceso que tiene el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="c175f-126">Validates the main window of the process that has the specified name.</span></span><br/>                                             |
| <span data-ttu-id="c175f-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -lista</span><span class="sxs-lookup"><span data-stu-id="c175f-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list</span></span><br/>                                       | <span data-ttu-id="c175f-128">Muestra todas las rutinas de comprobación disponibles.</span><span class="sxs-lookup"><span data-stu-id="c175f-128">Lists all of the available verification routines.</span></span><br/>                                                                 |
| <span data-ttu-id="c175f-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -habilitar <name></span><span class="sxs-lookup"><span data-stu-id="c175f-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable <name></span></span><br/>                          | <span data-ttu-id="c175f-130">Ejecuta la rutina de comprobación especificada.</span><span class="sxs-lookup"><span data-stu-id="c175f-130">Runs the specified verification routine.</span></span> <span data-ttu-id="c175f-131">Esta opción se puede especificar más de una vez.</span><span class="sxs-lookup"><span data-stu-id="c175f-131">This option can be specified more than once.</span></span><br/>                             |
| <span data-ttu-id="c175f-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -Disable <name></span><span class="sxs-lookup"><span data-stu-id="c175f-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable <name></span></span><br/> | <span data-ttu-id="c175f-133">Ejecuta todo excepto la rutina de comprobación especificada.</span><span class="sxs-lookup"><span data-stu-id="c175f-133">Runs all but the specified verification routine.</span></span> <span data-ttu-id="c175f-134">Esta opción se puede especificar más de una vez.</span><span class="sxs-lookup"><span data-stu-id="c175f-134">This option can be specified more than once.</span></span><br/>                     |
| <span data-ttu-id="c175f-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (información \| WARN \| Err)</span><span class="sxs-lookup"><span data-stu-id="c175f-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info\|warn\|err)</span></span><br/>                          | <span data-ttu-id="c175f-136">La clasificación de eventos más baja que se registrará.</span><span class="sxs-lookup"><span data-stu-id="c175f-136">The lowest event rating that will be logged.</span></span><br/>                                                                      |
| <span data-ttu-id="c175f-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span><span class="sxs-lookup"><span data-stu-id="c175f-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span></span><br/>                       | <span data-ttu-id="c175f-138">Escriba la salida en el archivo de registro especificado.</span><span class="sxs-lookup"><span data-stu-id="c175f-138">Write the output to the specified log file.</span></span> <span data-ttu-id="c175f-139">Esta opción se puede especificar más de una vez.</span><span class="sxs-lookup"><span data-stu-id="c175f-139">This option can be specified more than once.</span></span><br/>                          |
| <span data-ttu-id="c175f-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suprimir <file></span><span class="sxs-lookup"><span data-stu-id="c175f-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress <file></span></span><br/>                                                         | <span data-ttu-id="c175f-141">Use el archivo XML especificado para suprimir los errores.</span><span class="sxs-lookup"><span data-stu-id="c175f-141">Use the specified XML file to suppress errors.</span></span> <br/>                                                                   |
| <span data-ttu-id="c175f-142"><span id="-quiet"></span><span id="-QUIET"></span>-Quiet</span><span class="sxs-lookup"><span data-stu-id="c175f-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span></span><br/>                                                                                             | <span data-ttu-id="c175f-143">No escriba la salida del registro en stdout.</span><span class="sxs-lookup"><span data-stu-id="c175f-143">Do not write logging output to stdout.</span></span><br/>                                                                            |
| <span data-ttu-id="c175f-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-Help</span><span class="sxs-lookup"><span data-stu-id="c175f-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help</span></span> <br/>                           | <span data-ttu-id="c175f-145">Muestra la ayuda rápida.</span><span class="sxs-lookup"><span data-stu-id="c175f-145">Displays quick help.</span></span> <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a><span data-ttu-id="c175f-146">Códigos de error de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="c175f-146">Command-line Error Codes</span></span>

<span data-ttu-id="c175f-147">A continuación se muestran los códigos de error devueltos por AccCheckConsole cuando se usa "echo% ERRORLEVEL%"</span><span class="sxs-lookup"><span data-stu-id="c175f-147">Following are error codes returned from AccCheckConsole when using "echo %errorlevel%"</span></span>



| <span data-ttu-id="c175f-148">Código de error</span><span class="sxs-lookup"><span data-stu-id="c175f-148">Error code</span></span>                       | <span data-ttu-id="c175f-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="c175f-149">Description</span></span>                                 |
|----------------------------------|---------------------------------------------|
| <span data-ttu-id="c175f-150"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="c175f-150"><span id="0"></span>0</span></span><br/> | <span data-ttu-id="c175f-151">Sin errores ni advertencias.</span><span class="sxs-lookup"><span data-stu-id="c175f-151">No errors and no warnings.</span></span><br/>       |
| <span data-ttu-id="c175f-152"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="c175f-152"><span id="1"></span>1</span></span><br/> | <span data-ttu-id="c175f-153">Se solicitó la instrucción Usages.</span><span class="sxs-lookup"><span data-stu-id="c175f-153">Usages statement was requested.</span></span> <br/> |
| <span data-ttu-id="c175f-154"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="c175f-154"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="c175f-155">Errores y sin advertencias.</span><span class="sxs-lookup"><span data-stu-id="c175f-155">Errors and no warnings.</span></span><br/>          |
| <span data-ttu-id="c175f-156"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="c175f-156"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="c175f-157">Errores y advertencias.</span><span class="sxs-lookup"><span data-stu-id="c175f-157">Errors and warnings.</span></span><br/>             |
| <span data-ttu-id="c175f-158"><span id="4"></span>4</span><span class="sxs-lookup"><span data-stu-id="c175f-158"><span id="4"></span>4</span></span><br/> | <span data-ttu-id="c175f-159">ADVERTENCIAS pero sin errores.</span><span class="sxs-lookup"><span data-stu-id="c175f-159">Warnings but no errors.</span></span><br/>          |
| <span data-ttu-id="c175f-160"><span id="5"></span>5</span><span class="sxs-lookup"><span data-stu-id="c175f-160"><span id="5"></span>5</span></span><br/> | <span data-ttu-id="c175f-161">Línea de comandos no válida.</span><span class="sxs-lookup"><span data-stu-id="c175f-161">Invalid command line.</span></span> <br/>           |



 

## <a name="command-line-examples"></a><span data-ttu-id="c175f-162">Ejemplos de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="c175f-162">Command-line Examples</span></span>

<span data-ttu-id="c175f-163">A continuación se muestran varios ejemplos de línea de comandos de la consola de AccChecker.</span><span class="sxs-lookup"><span data-stu-id="c175f-163">Following are several AccChecker Console command-line examples.</span></span>

-   <span data-ttu-id="c175f-164">Ejecutar todas las comprobaciones en una ventana con un nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="c175f-164">Run all verifications on a window with a specified name.</span></span>

    <span data-ttu-id="c175f-165">**AccCheckConsole: ventana "sin título: Bloc de notas"**</span><span class="sxs-lookup"><span data-stu-id="c175f-165">**AccCheckConsole -window "Untitled - Notepad"**</span></span>

-   <span data-ttu-id="c175f-166">Ejecutar un subconjunto de las comprobaciones con respecto a un HWND, especificando un archivo de supresión.</span><span class="sxs-lookup"><span data-stu-id="c175f-166">Run a subset of the verifications against an HWND, specifying a suppression file.</span></span>

    <span data-ttu-id="c175f-167">**AccCheckConsole-HWND 0x00382f00-enable CheckTabbing-enable CheckName-Suppress suppress.xml**</span><span class="sxs-lookup"><span data-stu-id="c175f-167">**AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**</span></span>

-   <span data-ttu-id="c175f-168">Ejecutar todas las comprobaciones de una nueva DLL de comprobación.</span><span class="sxs-lookup"><span data-stu-id="c175f-168">Run all verifications from a new verification DLL.</span></span>

    <span data-ttu-id="c175f-169">**AccCheckConsole-Window "Untitled-Notepad" VerificationRoutine1.dll**</span><span class="sxs-lookup"><span data-stu-id="c175f-169">**AccCheckConsole -window "Untitled - Notepad" VerificationRoutine1.dll**</span></span>

## <a name="related-topics"></a><span data-ttu-id="c175f-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c175f-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c175f-171">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="c175f-171">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





