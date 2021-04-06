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
# <a name="crash-dump-analysis"></a>Análisis del volcado de memoria 

No todos los errores se pueden encontrar antes de la versión, lo que significa que no todos los errores que inician excepciones se pueden encontrar antes de la versión. Afortunadamente, Microsoft ha incluido en el SDK de la plataforma una función que ayuda a los desarrolladores a recopilar información sobre las excepciones detectadas por los usuarios. La función [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) escribe la información de volcado de memoria necesaria en un archivo sin guardar todo el espacio de proceso. Este archivo de información de volcado de memoria se denomina minivolcado. En este artículo técnico se proporciona información sobre cómo escribir y usar un minivolcado.

-   [Escribir un minivolcado](#writing-a-minidump)
-   [Seguridad para subprocesos](#thread-safety)
-   [Escribir un minivolcado con código](#writing-a-minidump-with-code)
-   [Usar Dumpchk.exe](#using-dumpchkexe)
-   [Analizar un minivolcado](#analyzing-a-minidump)
    -   [Usar el servidor de símbolos públicos de Microsoft](#using-the-microsoft-public-symbol-server)
    -   [Depurar un minivolcado con WinDbg](#debugging-a-minidump-with-windbg)
    -   [Usar herramientas de Copy-Protection con Minivolcados](#using-copy-protection-tools-with-minidumps)
-   [Resumen](#summary)

## <a name="writing-a-minidump"></a>Escribir un minivolcado

Las opciones básicas para escribir un minivolcado son las siguientes:

-   No haga nada. Windows genera automáticamente un minivolcado cada vez que un programa produce una excepción no controlada. La generación automática de un minivolcado está disponible desde Windows XP. Si el usuario lo permite, el minivolcado se enviará a Microsoft y no al desarrollador a través de Informe de errores de Windows (WER). Los desarrolladores pueden obtener acceso a estos minivolcados a través del [programa de aplicación de escritorio de Windows](../appxpkg/windows-desktop-application-program.md).

    El uso de WER requiere:

    -   Desarrolladores para firmar sus aplicaciones con Authenticode
    -   Las aplicaciones tienen un recurso VERSIONINFO válido en cada archivo ejecutable y DLL

    Si implementa una rutina personalizada para las excepciones no controladas, se recomienda encarecidamente usar la función [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) en el controlador de excepciones para enviar también un minivolcado automatizado a wer. La función **ReportFault** controla todos los problemas de conexión y envío del MINIVOLCADO a wer. No enviar minivolcados a WER infringe los requisitos de juegos para Windows.

    Para obtener más información sobre cómo funciona WER, vea [Cómo funciona informe de errores de Windows](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx). Para obtener una explicación de los detalles de registro, consulte [Introducción a informe de errores de Windows](https://msdn.microsoft.com/) en la [zona de ISV](https://msdn.microsoft.com/)de MSDN.

-   Use un producto de Microsoft Visual Studio Team System. En el menú **depurar** , haga clic en **Guardar volcado como** para guardar una copia de un volcado de memoria. El uso de un volcado guardado localmente es solo una opción para las pruebas internas y la depuración.
-   Agregue código al proyecto. Agregue la función [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) y el código de control de excepciones adecuado para guardar y enviar un minivolcado directamente al desarrollador. En este artículo se muestra cómo implementar esta opción. Sin embargo, tenga en cuenta que **MiniDumpWriteDump** no funciona actualmente con código administrado y solo está disponible en Windows XP, Windows Vista, Windows 7.

## <a name="thread-safety"></a>Seguridad para subprocesos

[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) forma parte de la biblioteca DBGHELP. Esta biblioteca no es segura para subprocesos, por lo que cualquier programa que use **MiniDumpWriteDump** debe sincronizar todos los subprocesos antes de intentar llamar a **MiniDumpWriteDump**.

## <a name="writing-a-minidump-with-code"></a>Escribir un minivolcado con código

La implementación real es sencilla. A continuación se facilita un ejemplo de cómo usar [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).


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



En este ejemplo se muestra el uso básico de [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) y la información mínima necesaria para llamarlo. El nombre del archivo de volcado de memoria es el desarrollador. sin embargo, para evitar conflictos de nombres de archivo, es aconsejable generar el nombre de archivo a partir del nombre y el número de versión de la aplicación, los identificadores de proceso y de subproceso, y la fecha y la hora. Esto también le ayudará a mantener los minivolcados agrupados por aplicación y versión. Depende del desarrollador decidir cuánta información se usa para diferenciar los nombres de los archivos de minivolcado.

Se debe observar que el nombre de la ruta de acceso en el ejemplo anterior se generó mediante una llamada a la función [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) para recuperar la ruta de acceso del directorio designado para los archivos temporales. El uso de este directorio funciona incluso con cuentas de usuario con privilegios mínimos y también evita que el minivolcado ocupe el espacio de la unidad de disco duro una vez que ya no se necesita.

Si archiva el producto durante el proceso de compilación diario, asegúrese también de incluir símbolos para la compilación, de modo que pueda depurar una versión anterior del producto, si es necesario. También debe seguir los pasos para mantener todas las optimizaciones del compilador mientras genera símbolos. Para ello, abra las propiedades del proyecto en el entorno de desarrollo y, para la configuración de lanzamiento, haga lo siguiente:

1.  En el lado izquierdo de la página de propiedades del proyecto, haga clic en C/C++. De forma predeterminada, se muestra la configuración **General** . En el lado derecho de la página de propiedades del proyecto, establezca **formato de información de depuración** en **base de datos de programa (/Zi)**.
2.  En el lado izquierdo de la página de propiedades, expanda **vinculador** y, a continuación, haga clic en **depuración**. En el lado derecho de la página de propiedades, establezca **generar información de depuración** en **sí (/debug)**.
3.  Haga clic en **optimización** y establezca **referencias** en E **liminate datos sin referencia (/OPT: Ref)**.
4.  Establezca **Habilitar plegamiento de COMDAT** para **quitar COMDAT redundantes (/OPT: ICF)**.

MSDN tiene información más detallada sobre la estructura de [**\_ \_ información de excepción de minivolcado**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) y la función [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .

## <a name="using-dumpchkexe"></a>Usar Dumpchk.exe

Dumpchk.exe es una utilidad de línea de comandos que se puede utilizar para comprobar que un archivo de volcado de memoria se ha creado correctamente. Si Dumpchk.exe genera un error, el archivo de volcado de memoria está dañado y no se puede analizar. Para obtener información sobre el uso de Dumpchk.exe, consulte [Cómo usar Dumpchk.exe para comprobar un archivo de volcado de memoria](https://support.microsoft.com/kb/315271/).

Dumpchk.exe se incluye en el CD del producto de Windows XP y se puede instalar en las herramientas de soporte técnico de los archivos de programa de la unidad del sistema \\ \\ mediante la \\ ejecución de Setup.exe en la carpeta Herramientas de soporte del \\ \\ CD del producto de Windows XP. También puede obtener la versión más reciente de Dumpchk.exe si descarga e instala las herramientas de depuración disponibles en [las herramientas de depuración de Windows](https://www.microsoft.com/whdc/devtools/debugging/) en el [centro de desarrollo de hardware de Windows](https://www.microsoft.com/whdc/).

## <a name="analyzing-a-minidump"></a>Analizar un minivolcado

Abrir un minivolcado para el análisis es tan sencillo como crear uno.

**Para analizar un minivolcado**

1.  Abra Visual Studio.
2.  En el menú **archivo** , haga clic en **Abrir proyecto**.
3.  Establezca **archivos de tipo** en **archivos de volcado** de memoria, desplácese hasta el archivo de volcado de memoria, selecciónelo y haga clic en **abrir.**
4.  Ejecutar el depurador.

El depurador creará un proceso simulado. El proceso simulado se detendrá en la instrucción que provocó el bloqueo.

### <a name="using-the-microsoft-public-symbol-server"></a>Usar el servidor de símbolos públicos de Microsoft

Para obtener la pila de bloqueos de nivel de controlador o de sistema, podría ser necesario configurar Visual Studio para que apunte al servidor de símbolos públicos de Microsoft.

**Para establecer una ruta de acceso al servidor de símbolos de Microsoft**

1.  En el menú **depurar** , haga clic en **Opciones**.
2.  En el cuadro de diálogo **Opciones** , abra el nodo **depuración** y haga clic en **símbolos**.
3.  Asegúrese de que **la opción Buscar en las ubicaciones anteriores solo cuando los símbolos se cargan manualmente** no esté seleccionada, a menos que desee cargar símbolos manualmente al depurar.
4.  Si usa símbolos en un servidor de símbolos remoto, puede mejorar el rendimiento especificando un directorio local en el que se pueden copiar los símbolos. Para ello, escriba una ruta de acceso para **almacenar en caché los símbolos del servidor de símbolos en este directorio**. Para conectarse al servidor de símbolos públicos de Microsoft, debe habilitar esta configuración. Tenga en cuenta que si está depurando un programa en un equipo remoto, el directorio de caché hace referencia a un directorio del equipo remoto.
5.  Haga clic en **OK**.
6.  Dado que está utilizando el servidor de símbolos públicos de Microsoft, aparece un cuadro de diálogo contrato de licencia para el usuario final. Haga clic en **sí** para aceptar el contrato y descargar los símbolos en la memoria caché local.

### <a name="debugging-a-minidump-with-windbg"></a>Depurar un minivolcado con WinDbg

También puede usar WinDbg, un depurador que forma parte de las herramientas de depuración de Windows, para depurar un minivolcado. WinDbg le permite depurar sin tener que usar Visual Studio. Para descargar las herramientas de depuración de Windows, vea [herramientas de depuración](https://www.microsoft.com/whdc/devtools/debugging/) de Windows en [Centro para desarrolladores de hardware de Windows](https://www.microsoft.com/whdc/).

Después de instalar las herramientas de depuración de Windows, debe escribir la ruta de acceso de símbolos en WinDbg.

**Para especificar una ruta de acceso de símbolos en WinDbg**

1.  En el menú **archivo** , haga clic en **ruta de acceso de símbolos**.
2.  En la ventana **ruta de acceso de búsqueda de símbolos** , escriba lo siguiente:

    "SRV \* c: \\ caché \* https://msdl.microsoft.com/download/symbols ;"

### <a name="using-copy-protection-tools-with-minidumps"></a>Usar herramientas de Copy-Protection con Minivolcados

Los desarrolladores también deben tener en cuenta la forma en que su esquema de protección de copia podría afectar al minivolcado. La mayoría de los esquemas de protección de copia tienen sus propias herramientas de descifrado, y depende del desarrollador obtener información sobre cómo usar esas herramientas con [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).

## <a name="summary"></a>Resumen

La función [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) puede ser una herramienta muy útil para recopilar y resolver errores una vez que se ha lanzado el producto. La escritura de un controlador de excepciones personalizado que utiliza **MiniDumpWriteDump** permite al desarrollador personalizar la colección de información y mejorar el proceso de depuración. La función es lo suficientemente flexible como para ser utilizada en cualquier proyecto basado en C++ y debe considerarse parte del proceso de estabilidad de un proyecto.

 

 