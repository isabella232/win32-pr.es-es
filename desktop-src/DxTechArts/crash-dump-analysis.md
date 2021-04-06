---
title: 'Análisis del volcado de memoria '
description: En este artículo técnico se proporciona información sobre cómo escribir y usar un minivolcado.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7558e47d08cb0183b8d9cefa5f22f0750fd1c598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078005"
---
# <a name="crash-dump-analysis"></a><span data-ttu-id="c6bc6-103">Análisis del volcado de memoria </span><span class="sxs-lookup"><span data-stu-id="c6bc6-103">Crash Dump Analysis</span></span>

<span data-ttu-id="c6bc6-104">No todos los errores se pueden encontrar antes de la versión, lo que significa que no todos los errores que inician excepciones se pueden encontrar antes de la versión.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-104">Not all bugs can be found prior to release, which means not all bugs that throw exceptions can be found before release.</span></span> <span data-ttu-id="c6bc6-105">Afortunadamente, Microsoft ha incluido en el SDK de la plataforma una función que ayuda a los desarrolladores a recopilar información sobre las excepciones detectadas por los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-105">Fortunately, Microsoft has included in the Platform SDK a function to help developers collect information on exceptions that are discovered by users.</span></span> <span data-ttu-id="c6bc6-106">La función [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) escribe la información de volcado de memoria necesaria en un archivo sin guardar todo el espacio de proceso.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-106">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function writes the necessary crash dump information to a file without saving the whole process space.</span></span> <span data-ttu-id="c6bc6-107">Este archivo de información de volcado de memoria se denomina minivolcado.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-107">This crash dump information file is called a minidump.</span></span> <span data-ttu-id="c6bc6-108">En este artículo técnico se proporciona información sobre cómo escribir y usar un minivolcado.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-108">This technical article provides info about how to write and use a minidump.</span></span>

-   [<span data-ttu-id="c6bc6-109">Escribir un minivolcado</span><span class="sxs-lookup"><span data-stu-id="c6bc6-109">Writing a Minidump</span></span>](#writing-a-minidump)
-   [<span data-ttu-id="c6bc6-110">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="c6bc6-110">Thread safety</span></span>](#thread-safety)
-   [<span data-ttu-id="c6bc6-111">Escribir un minivolcado con código</span><span class="sxs-lookup"><span data-stu-id="c6bc6-111">Writing a Minidump with Code</span></span>](#writing-a-minidump-with-code)
-   [<span data-ttu-id="c6bc6-112">Usar Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="c6bc6-112">Using Dumpchk.exe</span></span>](#using-dumpchkexe)
-   [<span data-ttu-id="c6bc6-113">Analizar un minivolcado</span><span class="sxs-lookup"><span data-stu-id="c6bc6-113">Analyzing a Minidump</span></span>](#analyzing-a-minidump)
    -   [<span data-ttu-id="c6bc6-114">Usar el servidor de símbolos públicos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c6bc6-114">Using the Microsoft Public Symbol Server</span></span>](#using-the-microsoft-public-symbol-server)
    -   [<span data-ttu-id="c6bc6-115">Depurar un minivolcado con WinDbg</span><span class="sxs-lookup"><span data-stu-id="c6bc6-115">Debugging a Minidump with WinDbg</span></span>](#debugging-a-minidump-with-windbg)
    -   [<span data-ttu-id="c6bc6-116">Usar herramientas de Copy-Protection con Minivolcados</span><span class="sxs-lookup"><span data-stu-id="c6bc6-116">Using Copy-Protection Tools with Minidumps</span></span>](#using-copy-protection-tools-with-minidumps)
-   [<span data-ttu-id="c6bc6-117">Resumen</span><span class="sxs-lookup"><span data-stu-id="c6bc6-117">Summary</span></span>](#summary)

## <a name="writing-a-minidump"></a><span data-ttu-id="c6bc6-118">Escribir un minivolcado</span><span class="sxs-lookup"><span data-stu-id="c6bc6-118">Writing a Minidump</span></span>

<span data-ttu-id="c6bc6-119">Las opciones básicas para escribir un minivolcado son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6bc6-119">The basic options for writing a minidump are as follows:</span></span>

-   <span data-ttu-id="c6bc6-120">No haga nada.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-120">Do nothing.</span></span> <span data-ttu-id="c6bc6-121">Windows genera automáticamente un minivolcado cada vez que un programa produce una excepción no controlada.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-121">Windows automatically generates a minidump whenever a program throws an unhandled exception.</span></span> <span data-ttu-id="c6bc6-122">La generación automática de un minivolcado está disponible desde Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-122">Automatic generation of a minidump is available since Windows XP.</span></span> <span data-ttu-id="c6bc6-123">Si el usuario lo permite, el minivolcado se enviará a Microsoft y no al desarrollador a través de Informe de errores de Windows (WER).</span><span class="sxs-lookup"><span data-stu-id="c6bc6-123">If the user allows it, the minidump will be sent to Microsoft, and not to the developer, through Windows Error Reporting (WER).</span></span> <span data-ttu-id="c6bc6-124">Los desarrolladores pueden obtener acceso a estos minivolcados a través del [programa de aplicación de escritorio de Windows](../appxpkg/windows-desktop-application-program.md).</span><span class="sxs-lookup"><span data-stu-id="c6bc6-124">Developers can gain access to these minidumps through the [Windows Desktop Application Program](../appxpkg/windows-desktop-application-program.md).</span></span>

    <span data-ttu-id="c6bc6-125">El uso de WER requiere:</span><span class="sxs-lookup"><span data-stu-id="c6bc6-125">Use of WER requires:</span></span>

    -   <span data-ttu-id="c6bc6-126">Desarrolladores para firmar sus aplicaciones con Authenticode</span><span class="sxs-lookup"><span data-stu-id="c6bc6-126">Developers to sign their applications using Authenticode</span></span>
    -   <span data-ttu-id="c6bc6-127">Las aplicaciones tienen un recurso VERSIONINFO válido en cada archivo ejecutable y DLL</span><span class="sxs-lookup"><span data-stu-id="c6bc6-127">Applications have valid VERSIONINFO resource in every executable and DLL</span></span>

    <span data-ttu-id="c6bc6-128">Si implementa una rutina personalizada para las excepciones no controladas, se recomienda encarecidamente usar la función [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) en el controlador de excepciones para enviar también un minivolcado automatizado a wer.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-128">If you implement a custom routine for unhandled exceptions, you are strongly urged to use the [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) function in the exception handler to also send an automated minidump to WER.</span></span> <span data-ttu-id="c6bc6-129">La función **ReportFault** controla todos los problemas de conexión y envío del MINIVOLCADO a wer.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-129">The **ReportFault** function handles all of the issues of connecting to and sending the minidump to WER.</span></span> <span data-ttu-id="c6bc6-130">No enviar minivolcados a WER infringe los requisitos de juegos para Windows.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-130">Not sending minidumps to WER violates the requirements of Games for Windows.</span></span>

    <span data-ttu-id="c6bc6-131">Para obtener más información sobre cómo funciona WER, vea [Cómo funciona informe de errores de Windows](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span><span class="sxs-lookup"><span data-stu-id="c6bc6-131">For more information on how WER works, see [How Windows Error Reporting Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span></span> <span data-ttu-id="c6bc6-132">Para obtener una explicación de los detalles de registro, consulte [Introducción a informe de errores de Windows](https://msdn.microsoft.com/) en la [zona de ISV](https://msdn.microsoft.com/)de MSDN.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-132">For an explanation of registration details, see [Introducing Windows Error Reporting](https://msdn.microsoft.com/) on MSDN's [ISV Zone](https://msdn.microsoft.com/).</span></span>

-   <span data-ttu-id="c6bc6-133">Use un producto de Microsoft Visual Studio Team System.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-133">Use a product from the Microsoft Visual Studio Team System.</span></span> <span data-ttu-id="c6bc6-134">En el menú **depurar** , haga clic en **Guardar volcado como** para guardar una copia de un volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-134">On the **Debug** menu, click **Save Dump As** to save a copy of a dump.</span></span> <span data-ttu-id="c6bc6-135">El uso de un volcado guardado localmente es solo una opción para las pruebas internas y la depuración.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-135">Use of a locally saved dump is only an option for in-house testing and debugging.</span></span>
-   <span data-ttu-id="c6bc6-136">Agregue código al proyecto.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-136">Add code to your project.</span></span> <span data-ttu-id="c6bc6-137">Agregue la función [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) y el código de control de excepciones adecuado para guardar y enviar un minivolcado directamente al desarrollador.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-137">Add the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function and the appropriate exception handling code to save and send a minidump directly to the developer.</span></span> <span data-ttu-id="c6bc6-138">En este artículo se muestra cómo implementar esta opción.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-138">This article demonstrates how to implement this option.</span></span> <span data-ttu-id="c6bc6-139">Sin embargo, tenga en cuenta que **MiniDumpWriteDump** no funciona actualmente con código administrado y solo está disponible en Windows XP, Windows Vista, Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-139">However, note that **MiniDumpWriteDump** does not currently work with managed code and is only available on Windows XP, Windows Vista, Windows 7.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="c6bc6-140">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="c6bc6-140">Thread safety</span></span>

<span data-ttu-id="c6bc6-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) forma parte de la biblioteca DBGHELP.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) is part of the DBGHELP library.</span></span> <span data-ttu-id="c6bc6-142">Esta biblioteca no es segura para subprocesos, por lo que cualquier programa que use **MiniDumpWriteDump** debe sincronizar todos los subprocesos antes de intentar llamar a **MiniDumpWriteDump**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-142">This library is not thread-safe, so any program that uses **MiniDumpWriteDump** should synchronize all threads before attempting to call **MiniDumpWriteDump**.</span></span>

## <a name="writing-a-minidump-with-code"></a><span data-ttu-id="c6bc6-143">Escribir un minivolcado con código</span><span class="sxs-lookup"><span data-stu-id="c6bc6-143">Writing a Minidump with Code</span></span>

<span data-ttu-id="c6bc6-144">La implementación real es sencilla.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-144">The actual implementation is straightforward.</span></span> <span data-ttu-id="c6bc6-145">A continuación se facilita un ejemplo de cómo usar [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="c6bc6-145">The following is a simple example of how to use [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



<span data-ttu-id="c6bc6-146">En este ejemplo se muestra el uso básico de [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) y la información mínima necesaria para llamarlo.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-146">This example demonstrates the basic usage of [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) and the minimum information necessary to call it.</span></span> <span data-ttu-id="c6bc6-147">El nombre del archivo de volcado de memoria es el desarrollador. sin embargo, para evitar conflictos de nombres de archivo, es aconsejable generar el nombre de archivo a partir del nombre y el número de versión de la aplicación, los identificadores de proceso y de subproceso, y la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-147">The name of the dump file is up to the developer; however, to avoid file name collisions, it is advisable to generate the file name from the application's name and version number, the process and thread IDs, and the date and time.</span></span> <span data-ttu-id="c6bc6-148">Esto también le ayudará a mantener los minivolcados agrupados por aplicación y versión.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-148">This will also help to keep the minidumps grouped by application and version.</span></span> <span data-ttu-id="c6bc6-149">Depende del desarrollador decidir cuánta información se usa para diferenciar los nombres de los archivos de minivolcado.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-149">It is up to the developer to decide how much information is used to differentiate minidump file names.</span></span>

<span data-ttu-id="c6bc6-150">Se debe observar que el nombre de la ruta de acceso en el ejemplo anterior se generó mediante una llamada a la función [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) para recuperar la ruta de acceso del directorio designado para los archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-150">It should be noted that the path name in the preceding example was generated by calling the [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files.</span></span> <span data-ttu-id="c6bc6-151">El uso de este directorio funciona incluso con cuentas de usuario con privilegios mínimos y también evita que el minivolcado ocupe el espacio de la unidad de disco duro una vez que ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-151">Use of this directory works even with least-privileged user accounts, and it also prevents the minidump from taking up hard drive space after it is no longer needed.</span></span>

<span data-ttu-id="c6bc6-152">Si archiva el producto durante el proceso de compilación diario, asegúrese también de incluir símbolos para la compilación, de modo que pueda depurar una versión anterior del producto, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-152">If you archive the product during your daily build process, also be sure to include symbols for the build so that you can debug an old version of the product, if necessary.</span></span> <span data-ttu-id="c6bc6-153">También debe seguir los pasos para mantener todas las optimizaciones del compilador mientras genera símbolos.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-153">You also need to take steps to maintain full compiler optimizations while generating symbols.</span></span> <span data-ttu-id="c6bc6-154">Para ello, abra las propiedades del proyecto en el entorno de desarrollo y, para la configuración de lanzamiento, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c6bc6-154">This can be done by opening your project's properties in the development environment and, for the release configuration, doing the following:</span></span>

1.  <span data-ttu-id="c6bc6-155">En el lado izquierdo de la página de propiedades del proyecto, haga clic en C/C++.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-155">On the left side of the project's property page, click C/C++.</span></span> <span data-ttu-id="c6bc6-156">De forma predeterminada, se muestra la configuración **General** .</span><span class="sxs-lookup"><span data-stu-id="c6bc6-156">By default, this displays **General** settings.</span></span> <span data-ttu-id="c6bc6-157">En el lado derecho de la página de propiedades del proyecto, establezca **formato de información de depuración** en **base de datos de programa (/Zi)**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-157">On the right side of the project's property page, set **Debug Information Format** to **Program Database (/Zi)**.</span></span>
2.  <span data-ttu-id="c6bc6-158">En el lado izquierdo de la página de propiedades, expanda **vinculador** y, a continuación, haga clic en **depuración**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-158">On the left side of the property page, expand **Linker**, and then click **Debugging**.</span></span> <span data-ttu-id="c6bc6-159">En el lado derecho de la página de propiedades, establezca **generar información de depuración** en **sí (/debug)**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-159">On the right side of the property page, set **Generate Debug Info** to **Yes (/DEBUG)**.</span></span>
3.  <span data-ttu-id="c6bc6-160">Haga clic en **optimización** y establezca **referencias** en E **liminate datos sin referencia (/OPT: Ref)**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-160">Click **Optimization**, and set **References** to E **liminate Unreferenced Data (/OPT:REF)**.</span></span>
4.  <span data-ttu-id="c6bc6-161">Establezca **Habilitar plegamiento de COMDAT** para **quitar COMDAT redundantes (/OPT: ICF)**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-161">Set **Enable COMDAT Folding** to **Remove Redundant COMDATs (/OPT:ICF)**.</span></span>

<span data-ttu-id="c6bc6-162">MSDN tiene información más detallada sobre la estructura de [**\_ \_ información de excepción de minivolcado**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) y la función [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .</span><span class="sxs-lookup"><span data-stu-id="c6bc6-162">MSDN has more detailed information on the [**MINIDUMP\_EXCEPTION\_INFORMATION**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) structure and the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function.</span></span>

## <a name="using-dumpchkexe"></a><span data-ttu-id="c6bc6-163">Usar Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="c6bc6-163">Using Dumpchk.exe</span></span>

<span data-ttu-id="c6bc6-164">Dumpchk.exe es una utilidad de línea de comandos que se puede utilizar para comprobar que un archivo de volcado de memoria se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-164">Dumpchk.exe is a command-line utility that can be used to verify that a dump file was created correctly.</span></span> <span data-ttu-id="c6bc6-165">Si Dumpchk.exe genera un error, el archivo de volcado de memoria está dañado y no se puede analizar.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-165">If Dumpchk.exe generates an error, then the dump file is corrupt and cannot be analyzed.</span></span> <span data-ttu-id="c6bc6-166">Para obtener información sobre el uso de Dumpchk.exe, consulte [Cómo usar Dumpchk.exe para comprobar un archivo de volcado de memoria](https://support.microsoft.com/kb/315271/).</span><span class="sxs-lookup"><span data-stu-id="c6bc6-166">For information on using Dumpchk.exe, see [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).</span></span>

<span data-ttu-id="c6bc6-167">Dumpchk.exe se incluye en el CD del producto de Windows XP y se puede instalar en las herramientas de soporte técnico de los archivos de programa de la unidad del sistema \\ \\ mediante la \\ ejecución de Setup.exe en la carpeta Herramientas de soporte del \\ \\ CD del producto de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-167">Dumpchk.exe is included on the Windows XP product CD and can be installed to System Drive\\Program Files\\Support Tools\\ by running Setup.exe in the Support\\Tools\\ folder on the Windows XP product CD.</span></span> <span data-ttu-id="c6bc6-168">También puede obtener la versión más reciente de Dumpchk.exe si descarga e instala las herramientas de depuración disponibles en [las herramientas de depuración de Windows](https://www.microsoft.com/whdc/devtools/debugging/) en el [centro de desarrollo de hardware de Windows](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="c6bc6-168">You can also get the latest version of Dumpchk.exe by download and installing the debugging tools available from [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

## <a name="analyzing-a-minidump"></a><span data-ttu-id="c6bc6-169">Analizar un minivolcado</span><span class="sxs-lookup"><span data-stu-id="c6bc6-169">Analyzing a Minidump</span></span>

<span data-ttu-id="c6bc6-170">Abrir un minivolcado para el análisis es tan sencillo como crear uno.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-170">Opening a minidump for analysis is as easy as creating one.</span></span>

<span data-ttu-id="c6bc6-171">**Para analizar un minivolcado**</span><span class="sxs-lookup"><span data-stu-id="c6bc6-171">**To analyze a minidump**</span></span>

1.  <span data-ttu-id="c6bc6-172">Abra Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-172">Open Visual Studio.</span></span>
2.  <span data-ttu-id="c6bc6-173">En el menú **archivo** , haga clic en **Abrir proyecto**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-173">On the **File** menu, click **Open Project**.</span></span>
3.  <span data-ttu-id="c6bc6-174">Establezca **archivos de tipo** en **archivos de volcado** de memoria, desplácese hasta el archivo de volcado de memoria, selecciónelo y haga clic en **abrir.**</span><span class="sxs-lookup"><span data-stu-id="c6bc6-174">Set **Files of type** to **Dump Files**, navigate to the dump file, select it, and click **Open.**</span></span>
4.  <span data-ttu-id="c6bc6-175">Ejecutar el depurador.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-175">Run the debugger.</span></span>

<span data-ttu-id="c6bc6-176">El depurador creará un proceso simulado.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-176">The debugger will create a simulated process.</span></span> <span data-ttu-id="c6bc6-177">El proceso simulado se detendrá en la instrucción que provocó el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-177">The simulated process will be halted at the instruction that caused the crash.</span></span>

### <a name="using-the-microsoft-public-symbol-server"></a><span data-ttu-id="c6bc6-178">Usar el servidor de símbolos públicos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c6bc6-178">Using the Microsoft Public Symbol Server</span></span>

<span data-ttu-id="c6bc6-179">Para obtener la pila de bloqueos de nivel de controlador o de sistema, podría ser necesario configurar Visual Studio para que apunte al servidor de símbolos públicos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-179">To get the stack for driver- or system-level crashes, it might be necessary to configure Visual Studio to point to the Microsoft public symbol server.</span></span>

<span data-ttu-id="c6bc6-180">**Para establecer una ruta de acceso al servidor de símbolos de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="c6bc6-180">**To set a path to the Microsoft symbol server**</span></span>

1.  <span data-ttu-id="c6bc6-181">En el menú **depurar** , haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-181">On the **Debug** menu, click **Options**.</span></span>
2.  <span data-ttu-id="c6bc6-182">En el cuadro de diálogo **Opciones** , abra el nodo **depuración** y haga clic en **símbolos**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-182">In the **Options** dialog box, open the **Debugging** node, and click **Symbols**.</span></span>
3.  <span data-ttu-id="c6bc6-183">Asegúrese de que **la opción Buscar en las ubicaciones anteriores solo cuando los símbolos se cargan manualmente** no esté seleccionada, a menos que desee cargar símbolos manualmente al depurar.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-183">Make sure **Search the above locations only when symbols are loaded manually** is not selected, unless you want to load symbols manually when you debug.</span></span>
4.  <span data-ttu-id="c6bc6-184">Si usa símbolos en un servidor de símbolos remoto, puede mejorar el rendimiento especificando un directorio local en el que se pueden copiar los símbolos.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-184">If you are using symbols on a remote symbol server, you can improve performance by specifying a local directory that symbols can be copied to.</span></span> <span data-ttu-id="c6bc6-185">Para ello, escriba una ruta de acceso para **almacenar en caché los símbolos del servidor de símbolos en este directorio**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-185">To do this, enter a path for **Cache symbols from symbol server to this directory**.</span></span> <span data-ttu-id="c6bc6-186">Para conectarse al servidor de símbolos públicos de Microsoft, debe habilitar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-186">To connect to the Microsoft public symbol server, you need to enable this setting.</span></span> <span data-ttu-id="c6bc6-187">Tenga en cuenta que si está depurando un programa en un equipo remoto, el directorio de caché hace referencia a un directorio del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-187">Note that if you are debugging a program on a remote computer, the cache directory refers to a directory on the remote computer.</span></span>
5.  <span data-ttu-id="c6bc6-188">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-188">Click **OK**.</span></span>
6.  <span data-ttu-id="c6bc6-189">Dado que está utilizando el servidor de símbolos públicos de Microsoft, aparece un cuadro de diálogo contrato de licencia para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-189">Because you are using the Microsoft public symbol server, an End User License Agreement dialog box appears.</span></span> <span data-ttu-id="c6bc6-190">Haga clic en **sí** para aceptar el contrato y descargar los símbolos en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-190">Click **Yes** to accept the agreement and download symbols to your local cache.</span></span>

### <a name="debugging-a-minidump-with-windbg"></a><span data-ttu-id="c6bc6-191">Depurar un minivolcado con WinDbg</span><span class="sxs-lookup"><span data-stu-id="c6bc6-191">Debugging a Minidump with WinDbg</span></span>

<span data-ttu-id="c6bc6-192">También puede usar WinDbg, un depurador que forma parte de las herramientas de depuración de Windows, para depurar un minivolcado.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-192">You can also use WinDbg, a debugger that is part of the Windows Debugging Tools, to debug a minidump.</span></span> <span data-ttu-id="c6bc6-193">WinDbg le permite depurar sin tener que usar Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-193">WinDbg allows you to debug without having to use Visual Studio.</span></span> <span data-ttu-id="c6bc6-194">Para descargar las herramientas de depuración de Windows, vea [herramientas de depuración](https://www.microsoft.com/whdc/devtools/debugging/) de Windows en [Centro para desarrolladores de hardware de Windows](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="c6bc6-194">To download Windows Debugging Tools, see [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

<span data-ttu-id="c6bc6-195">Después de instalar las herramientas de depuración de Windows, debe escribir la ruta de acceso de símbolos en WinDbg.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-195">After installing Windows Debugging Tools, you must enter the symbol path in WinDbg.</span></span>

<span data-ttu-id="c6bc6-196">**Para especificar una ruta de acceso de símbolos en WinDbg**</span><span class="sxs-lookup"><span data-stu-id="c6bc6-196">**To enter a symbol path in WinDbg**</span></span>

1.  <span data-ttu-id="c6bc6-197">En el menú **archivo** , haga clic en **ruta de acceso de símbolos**.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-197">On the **File** menu, click **Symbol Path**.</span></span>
2.  <span data-ttu-id="c6bc6-198">En la ventana **ruta de acceso de búsqueda de símbolos** , escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c6bc6-198">In the **Symbol Search Path** window, enter the following:</span></span>

    <span data-ttu-id="c6bc6-199">"SRV \* c: \\ caché \* https://msdl.microsoft.com/download/symbols ;"</span><span class="sxs-lookup"><span data-stu-id="c6bc6-199">"srv\*c:\\cache\*https://msdl.microsoft.com/download/symbols;"</span></span>

### <a name="using-copy-protection-tools-with-minidumps"></a><span data-ttu-id="c6bc6-200">Usar herramientas de Copy-Protection con Minivolcados</span><span class="sxs-lookup"><span data-stu-id="c6bc6-200">Using Copy-Protection Tools with Minidumps</span></span>

<span data-ttu-id="c6bc6-201">Los desarrolladores también deben tener en cuenta la forma en que su esquema de protección de copia podría afectar al minivolcado.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-201">Developers also need to be aware of how their copy-protection scheme might affect the minidump.</span></span> <span data-ttu-id="c6bc6-202">La mayoría de los esquemas de protección de copia tienen sus propias herramientas de descifrado, y depende del desarrollador obtener información sobre cómo usar esas herramientas con [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="c6bc6-202">Most copy-protection schemes have their own descramble tools, and it is up to the developer to learn how to use those tools with [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>

## <a name="summary"></a><span data-ttu-id="c6bc6-203">Resumen</span><span class="sxs-lookup"><span data-stu-id="c6bc6-203">Summary</span></span>

<span data-ttu-id="c6bc6-204">La función [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) puede ser una herramienta muy útil para recopilar y resolver errores una vez que se ha lanzado el producto.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-204">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function can be an extremely useful tool in collecting and solving bugs after the product has been released.</span></span> <span data-ttu-id="c6bc6-205">La escritura de un controlador de excepciones personalizado que utiliza **MiniDumpWriteDump** permite al desarrollador personalizar la colección de información y mejorar el proceso de depuración.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-205">Writing a custom exception handler that uses **MiniDumpWriteDump** allows the developer to customize the information collection and improve the debugging process.</span></span> <span data-ttu-id="c6bc6-206">La función es lo suficientemente flexible como para ser utilizada en cualquier proyecto basado en C++ y debe considerarse parte del proceso de estabilidad de un proyecto.</span><span class="sxs-lookup"><span data-stu-id="c6bc6-206">The function is flexible enough to be used in any C++-based project and should be considered part of any project's stability process.</span></span>

 

 