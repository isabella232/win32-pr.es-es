---
title: 'Análisis del volcado de memoria '
description: En este artículo técnico se proporciona información sobre cómo escribir y usar un minivolumen.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c68891e2e20938036bd016e6e786a2cdad0096ae44af0e8974a88052963be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075525"
---
# <a name="crash-dump-analysis"></a>Análisis del volcado de memoria 

No todos los errores se pueden encontrar antes de la versión, lo que significa que no todos los errores que inician excepciones se pueden encontrar antes de la versión. Afortunadamente, Microsoft ha incluido en el SDK de plataforma una función para ayudar a los desarrolladores a recopilar información sobre las excepciones detectadas por los usuarios. La [**función MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) escribe la información de volcado de memoria necesaria en un archivo sin guardar todo el espacio de proceso. Este archivo de información de volcado de memoria se denomina minivolca. En este artículo técnico se proporciona información sobre cómo escribir y usar un minivolumen.

-   [Escritura de un minivolumen](#writing-a-minidump)
-   [Seguridad para subprocesos](#thread-safety)
-   [Escritura de un minivolumen con código](#writing-a-minidump-with-code)
-   [Uso de Dumpchk.exe](#using-dumpchkexe)
-   [Análisis de un minivolumen](#analyzing-a-minidump)
    -   [Uso del servidor de símbolos públicos de Microsoft](#using-the-microsoft-public-symbol-server)
    -   [Depuración de un minivolumen con WinDbg](#debugging-a-minidump-with-windbg)
    -   [Uso de Copy-Protection tools con minivolúmpos](#using-copy-protection-tools-with-minidumps)
-   [Resumen](#summary)

## <a name="writing-a-minidump"></a>Escritura de un minivolumen

Las opciones básicas para escribir un minivolumen son las siguientes:

-   No haga nada. Windows genera automáticamente un minivolumen cada vez que un programa produce una excepción no controlada. La generación automática de un minivolumen está disponible desde Windows XP. Si el usuario lo permite, el minivolquete se enviará a Microsoft, y no al desarrollador, a través Informe de errores de Windows (WER). Los desarrolladores pueden obtener acceso a estos minivolúmanes a través del Windows [aplicación de escritorio](../appxpkg/windows-desktop-application-program.md).

    El uso de WER requiere:

    -   Desarrolladores para firmar sus aplicaciones mediante Authenticode
    -   Las aplicaciones tienen un recurso VERSIONINFO válido en todos los archivos ejecutables y DLL

    Si implementa una rutina personalizada para excepciones no controladas, se le pide encarecidamente que use la función [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) en el controlador de excepciones para enviar también un minivolumen automatizado a WER. La **función ReportFault** controla todos los problemas de conexión y envío del minivolumen a WER. Si no se envían minivolúmpos a WER, se infringen los requisitos de Juegos para Windows.

    Para obtener más información sobre cómo funciona WER, vea [How Informe de errores de Windows Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx). Para obtener una explicación de los detalles de registro, [vea Introducción Informe de errores de Windows](https://msdn.microsoft.com/) en la zona [ISV de](https://msdn.microsoft.com/)MSDN.

-   Use un producto de Microsoft Visual Studio Team System. En el **menú Depurar,** haga clic **en Guardar volcado como** para guardar una copia de un volcado de memoria. El uso de un volcado guardado localmente solo es una opción para realizar pruebas y depuraciones internas.
-   Agregue código al proyecto. Agregue la [**función MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) y el código de control de excepciones adecuado para guardar y enviar un minivolumen directamente al desarrollador. En este artículo se muestra cómo implementar esta opción. Sin embargo, tenga en cuenta que **MiniDumpWriteDump** no funciona actualmente con código administrado y solo está disponible en Windows XP, Windows Vista, Windows 7.

## <a name="thread-safety"></a>Seguridad para subprocesos

[**MiniDumpWriteDump forma**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) parte de la biblioteca DBGHELP. Esta biblioteca no es segura para subprocesos, por lo que cualquier programa que use **MiniDumpWriteDump** debe sincronizar todos los subprocesos antes de intentar llamar a **MiniDumpWriteDump**.

## <a name="writing-a-minidump-with-code"></a>Escritura de un minivolumen con código

La implementación real es sencilla. A continuación se muestra un ejemplo sencillo de cómo usar [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).


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



En este ejemplo se muestra el uso básico de [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) y la información mínima necesaria para llamarlo. El nombre del archivo de volcado es del desarrollador; Sin embargo, para evitar conflictos de nombres de archivo, es aconsejable generar el nombre de archivo a partir del nombre y el número de versión de la aplicación, los identificaciónes de proceso y subproceso, y la fecha y hora. Esto también ayudará a mantener los minivolúmedos agrupados por aplicación y versión. Es el desarrollador quien decide cuánta información se usa para diferenciar los nombres de archivo de minivolfón.

Debe tenerse en cuenta que el nombre de ruta de acceso del ejemplo anterior se generó mediante una llamada a la función [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) para recuperar la ruta de acceso del directorio designado para los archivos temporales. El uso de este directorio funciona incluso con cuentas de usuario con privilegios mínimos y también evita que el minivolumen tome espacio en la unidad de disco duro después de que ya no sea necesario.

Si archiva el producto durante el proceso de compilación diario, asegúrese también de incluir símbolos para la compilación para que pueda depurar una versión anterior del producto, si es necesario. También debe tomar medidas para mantener las optimizaciones del compilador completa al generar símbolos. Para ello, abra las propiedades del proyecto en el entorno de desarrollo y, para la configuración de versión, haga lo siguiente:

1.  En el lado izquierdo de la página de propiedades del proyecto, haga clic en C/C++. De forma predeterminada, se **muestra** Configuración general. En el lado derecho de la página de propiedades del proyecto, establezca Formato de información de **depuración** en Base de datos **de programa (/Zi).**
2.  En el lado izquierdo de la página de propiedades, expanda **Vinculador** y, a continuación, haga clic **en Depurar**. En el lado derecho de la página de propiedades, establezca Generar información **de depuración** **en Sí (/DEBUG).**
3.  Haga **clic en** Optimización y establezca **Referencias** en E **liminar datos sin referencia (/OPT:REF).**
4.  Establezca **Habilitar plegado COMDAT para** quitar LOS **COMDAT redundantes (/OPT:ICF).**

MSDN tiene información más detallada sobre la estructura [**MINIDUMP \_ EXCEPTION \_ INFORMATION**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) y la [**función MiniDumpWriteDump.**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)

## <a name="using-dumpchkexe"></a>Uso de Dumpchk.exe

Dumpchk.exe es una utilidad de línea de comandos que se puede usar para comprobar que un archivo de volcado de memoria se ha creado correctamente. Si Dumpchk.exe genera un error, el archivo de volcado de memoria está dañado y no se puede analizar. Para obtener información sobre el Dumpchk.exe, vea [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).

Dumpchk.exe se incluye en el CD del producto Windows XP y se puede instalar en las herramientas de soporte técnico de archivos de programa de unidad del sistema mediante la ejecución de Setup.exe en la carpeta Herramientas de soporte técnico del CD del producto \\ \\ Windows \\ \\ \\ XP. También puede obtener la versión más reciente de Dumpchk.exe descargando e instalando las herramientas de depuración disponibles en herramientas [de](https://www.microsoft.com/whdc/devtools/debugging/) depuración de Windows en [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).

## <a name="analyzing-a-minidump"></a>Análisis de un minivolumen

Abrir un minivolumen para el análisis es tan fácil como crear uno.

**Para analizar un minivolumen**

1.  Abra Visual Studio.
2.  En el **menú Archivo** , haga clic en **Abrir Project**.
3.  Establezca **Archivos de tipo en** Archivos **de** volcado, vaya al archivo de volcado, selecciónelo y haga clic en **Abrir.**
4.  Ejecute el depurador.

El depurador creará un proceso simulado. El proceso simulado se detendrá en la instrucción que produjo el bloqueo.

### <a name="using-the-microsoft-public-symbol-server"></a>Uso del servidor de símbolos públicos de Microsoft

Para obtener la pila de bloqueos de nivel de sistema o controlador, puede que sea necesario configurar Visual Studio para que apunte al servidor de símbolos público de Microsoft.

**Para establecer una ruta de acceso al servidor de símbolos de Microsoft**

1.  En el menú **Depurar** , haga clic en **Opciones**.
2.  En el **cuadro de** diálogo Opciones , abra el **nodo Depuración** y haga clic en **Símbolos**.
3.  Asegúrese de **buscar las ubicaciones anteriores** solo cuando los símbolos se carguen manualmente no esté seleccionado, a menos que desee cargar símbolos manualmente al depurar.
4.  Si usa símbolos en un servidor de símbolos remoto, puede mejorar el rendimiento especificando un directorio local en el que se puedan copiar símbolos. Para ello, escriba una ruta de acceso para Almacenar en caché **símbolos del servidor de símbolos a este directorio.** Para conectarse al servidor de símbolos público de Microsoft, debe habilitar esta configuración. Tenga en cuenta que si está depurando un programa en un equipo remoto, el directorio de caché hace referencia a un directorio en el equipo remoto.
5.  Haga clic en **Aceptar**.
6.  Dado que usa el servidor de símbolos público de Microsoft, aparece un cuadro de diálogo Contrato de licencia de usuario final. Haga **clic en** Sí para aceptar el contrato y descargar símbolos en la memoria caché local.

### <a name="debugging-a-minidump-with-windbg"></a>Depuración de un minivolumen con WinDbg

También puede usar WinDbg, un depurador que forma parte de Windows Debugging Tools, para depurar un minivolumen. WinDbg permite depurar sin tener que usar Visual Studio. Para descargar Windows de depuración, [vea Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on Windows Hardware Developer [Central](https://www.microsoft.com/whdc/).

Después de instalar Windows herramientas de depuración, debe escribir la ruta de acceso de símbolos en WinDbg.

**Para escribir una ruta de acceso de símbolos en WinDbg**

1.  En el menú **Archivo** , haga clic en **Ruta de acceso de símbolos**.
2.  En la **ventana Ruta de búsqueda de** símbolos, escriba lo siguiente:

    "srv \* c: \\ cache \* https://msdl.microsoft.com/download/symbols ;"

### <a name="using-copy-protection-tools-with-minidumps"></a>Uso de Copy-Protection tools con minivolúmpos

Los desarrolladores también deben tener en cuenta cómo su esquema de protección de copia puede afectar al minivolfón. La mayoría de los esquemas de protección de copia tienen sus propias herramientas de descramble y es el desarrollador quien debe aprender a usar esas herramientas con [**MiniDumpWriteDump.**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)

## <a name="summary"></a>Resumen

La [**función MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) puede ser una herramienta muy útil para recopilar y resolver errores una vez publicado el producto. Escribir un controlador de excepciones personalizado que use **MiniDumpWriteDump** permite al desarrollador personalizar la colección de información y mejorar el proceso de depuración. La función es lo suficientemente flexible como para usarse en cualquier proyecto basado en C++ y debe considerarse parte del proceso de estabilidad de cualquier proyecto.

 

 