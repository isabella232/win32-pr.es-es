---
title: Uso de BITS desde .NET mediante archivos DLL de referencia
description: En los ejemplos siguientes se muestra cómo llamar a la interfaz COM de BITS desde un programa .NET
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: 00f7d6287d86dd1816d7e4b0a7c6e18c9ae4916c5c85b01d0280758cf9d00b5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529155"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Llamada a BITS desde .NET y C# mediante archivos DLL de referencia

Una manera de llamar a las clases COM de BITS desde un programa de .NET es crear un archivo DLL de referencia a partir de los archivos [IDL](/windows/desktop/Midl/midl-start-page) de BITS (lenguaje de definición de interfaz) en el SDK de Windows, mediante las herramientas [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) y [TLBIMP.](/dotnet/framework/tools/tlbimp-exe-type-library-importer) El archivo DLL de referencia es un conjunto de contenedores de clases para las clases COM de BITS; A continuación, puede usar las clases contenedoras directamente desde .NET.

Una alternativa al uso de archivos DLL de referencia creados automáticamente es [](https://github.com/) usar un contenedor de BITS de .NET de terceros de GitHub y [NuGet](https://www.nuget.org/). Estos contenedores suelen tener un estilo de programación de .NET más natural, pero pueden quedarse atrás de los cambios y las actualizaciones en las interfaces bits.

## <a name="creating-the-reference-dlls"></a>Creación de los archivos DLL de referencia
### <a name="bits-idl-files"></a>Archivos IDL de BITS

Comenzará con el conjunto de archivos IDL de BITS. Se trata de archivos que definen completamente la interfaz COM de BITS. Los archivos se encuentran en el directorio **Windows Kits** y se denominan *bits* versión .idl (por ejemplo, bits10_2.idl), excepto el archivo de versión 1.0, que es simplemente Bits.idl. A medida que se crean nuevas versiones de BITS, también se crean nuevos archivos IDL de BITS.

También puede modificar una copia de los archivos IDL de BITS del SDK para usar características de BITS que no se convierten automáticamente en equivalentes de .NET. Más adelante se analizarán los posibles cambios en el archivo IDL.

Los archivos IDL de BITS incluyen otros archivos IDL por referencia. También se anidan para que, si usa una versión, incluya todas las versiones inferiores.

Para cada versión de BITS de destino en el programa necesitará un archivo DLL de referencia para esa versión. Por ejemplo, si desea escribir un programa que funcione en BITS 1.5 y adicionales, pero que tenga características adicionales cuando bits 10.2 esté presente, debe convertir los archivos bits1_5.idl y bits10_2.idl.


### <a name="midl-and-tlbimp-utilities"></a>Utilidades MIDL y TLBIMP

La [utilidad MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Lenguaje de definición de interfaz de Microsoft) convierte los archivos IDL que describen la interfaz COM de BITS en un archivo TLB (biblioteca de tipos). La herramienta MIDL depende de la utilidad CL (preprocesador C) para leer correctamente el archivo de lenguaje IDL. La utilidad CL forma parte de Visual Studio y se instala cuando se incluyen características de C/C++ en la Visual Studio instalación.

La utilidad MIDL normalmente creará un conjunto de archivos C y H (código de lenguaje C y encabezado de lenguaje C). Puede suprimir estos archivos adicionales enviando la salida al dispositivo NUL:. Por ejemplo, al establecer el modificador /dlldata NUL: se suprimirá la creación de un archivo dlldata.c. Los comandos de ejemplo siguientes muestran qué modificadores deben establecerse en NUL:.

La [utilidad TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Importador de la biblioteca de tipos) lee en un archivo TLB y crea el archivo DLL de referencia correspondiente. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Comandos de ejemplo para MIDL y TLBIMP

Este es un ejemplo del conjunto completo de comandos para generar un conjunto de archivos de referencia. Es posible que tenga que modificar los comandos en función de la instalación del SDK de Visual Studio y Windows y en función de las características de BITS y las versiones del sistema operativo de destino. 

En el ejemplo se crea un directorio para colocar los archivos DLL de referencia y se crea una variable de entorno BITSTEMP para que apunte a ese directorio. 

A continuación, los comandos de ejemplo vsdevcmd.bat archivo creado por el Visual Studio instalación. Este archivo BAT configurará las rutas de acceso y algunas variables de entorno para que se ejecuten los comandos MIDL y TLBIMP. También configura las variables WindowsSdkDir y WindowsSDKLibVersion para que apunten a los directorios más recientes Windows SDK.

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
Una vez que se ejecuten estos comandos, tendrá un conjunto de archivos DLL de referencia en el directorio BITSTEMP.

### <a name="adding-the-reference-dlls-to-your-project"></a>Adición de los archivos DLL de referencia al proyecto

Para usar un archivo DLL de referencia en un proyecto de C#, abra el proyecto de C# en Visual Studio. En la Explorador de soluciones, haga clic con el botón derecho en Referencias y haga clic en Agregar referencia. A continuación, haga clic en el botón Examinar y, a continuación, en el botón Agregar. Vaya al directorio con los archivos DLL de referencia, selecciónelos y haga clic en Agregar. En la ventana Administrador de referencias, se comprobarán los archivos DLL de referencia. A continuación, haga clic en Aceptar.

Los archivos DLL de referencia de BITS ahora se agregan al proyecto.

La información de los archivos DLL de referencia se incrustará en el programa final. No es necesario enviar los archivos DLL de referencia con el programa; solo tiene que enviar el .EXE. 

Puede cambiar si los archivos DLL de referencia se insertan en el archivo EXE final. Use la [propiedad Incrustar tipos de](/dotnet/framework/interop/how-to-add-references-to-type-libraries) interoperabilidad para establecer si se incrustarán o no los archivos DLL de referencia. Esto se puede hacer por referencia. El valor predeterminado es True para insertar los archivos DLL.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Modificación de archivos IDL para código .NET más completo

Los archivos IDL de BITS (Lenguaje de definición de interfaz de Microsoft) se pueden usar sin cambios para convertir el archivo DLL backgroundCopyManager. Sin embargo, al archivo DLL de referencia de .NET resultante le faltan algunas uniones no traducibles y tiene nombres difíciles de usar para algunas estructuras y enumeraciones. En esta sección se describen algunos de los cambios que puede realizar para que el archivo DLL de .NET sea más completo y fácil de usar.

### <a name="simpler-enum-names"></a>Nombres ENUM más sencillos

Los archivos IDL de BITS suelen definir valores de enumeración como los siguientes:
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
El BG_AUTH_TARGET es el nombre de la definición de tipo; la enumeración real no tiene nombre. Esto no suele causar problemas con el código de C, pero no se traduce bien para su uso con un programa de .NET. Se creará automáticamente un nuevo nombre, pero podría tener un aspecto parecido a _MIDL___MIDL_itf_bits4_0_0005_0001_0001 en lugar de un valor legible. Para corregir este problema, actualice los archivos MIDL para incluir un nombre de enumeración.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

El nombre de enumeración puede ser el mismo que el nombre de typedef. Algunos programadores tienen una convención de nomenclatura en la que se mantienen diferentes (por ejemplo, colocando un carácter de subrayado delante del nombre de enumeración), pero esto solo confundirá las traducciones de .NET. 

### <a name="string-types-in-unions"></a>Tipos de cadena en uniones

Los archivos IDL de BITS pasan cadenas mediante la convención LPWSTR (puntero largo a cadena de caracteres anchos). Aunque esto funciona al pasar parámetros de función (como el método Job.GetDisplayName([out] LPWSTR *pVal), no funciona cuando las cadenas forman parte de uniones. Por ejemplo, el archivo bits5_0.idl incluye la BITS_FILE_PROPERTY_VALUE unión:

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

El campo LPWSTR no se incluirá en la versión de .NET de la unión. Para solucionar este problema, cambie LPWSTR a WCHAR*. El campo resultante (denominado String) se pasará como IntPtr. Convierta esto en una cadena mediante System.Runtime.InteropServices.Marshal.PtrToStringAuto(value. String); Método.

### <a name="unions-in-structures"></a>Uniones en estructuras

A veces, las uniones incrustadas en estructuras no se incluirán en la estructura. Por ejemplo, en Bits1_5.idl, el BG_AUTH_CREDENTIALS se define de la siguiente manera:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

El BG_AUTH_CREDENTIALS_UNION se define como una unión como se muestra a continuación:
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
El campo Credenciales del BG_AUTH_CREDENTIALS no se incluirá en la definición de clase de .NET.

Tenga en cuenta que la unión se define para ser siempre un BG_BASIC_CREDENTIALS independientemente de la BG_AUTH_SCHEME. Dado que la unión no se usa como unión, podemos pasar una BG_BASIC_CREDENTIALS como esta:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Uso de BITS de C #

### <a name="recommended-using-statement"></a>Instrucción using recomendada

La configuración de algunas instrucciones using en C# reducirá el número de caracteres que debe escribir para usar las distintas versiones de BITS. El nombre "BITSReference" procede del nombre del archivo DLL de referencia.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Ejemplo rápido: descarga de un archivo

A continuación se muestra un fragmento de código de C# corto pero completo para descargar un archivo desde una dirección URL. 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

En este código de ejemplo, se crea un administrador de BITS denominado mgr. Se corresponde directamente con la [interfaz IBackgroundCopyManager.](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) 

Desde el administrador se crea un nuevo trabajo. El trabajo es un parámetro out en el método CreateJob. También se pasa el nombre del trabajo (que no tiene que ser único) y el tipo de descarga, que es un trabajo de descarga. También se rellena un GUID de BITS para el identificador de trabajo.

Una vez creado el trabajo, agregue un nuevo archivo de descarga al trabajo con el método AddFile. Debe pasar dos cadenas, una para el archivo remoto (la dirección URL o el recurso compartido de archivos) y otra para el archivo local. 

Después de agregar el archivo, llame a Resume en el trabajo para iniciarlo. A continuación, el código espera hasta que el trabajo está en un estado final (ERROR o TRANSFERRED) y, a continuación, se completa.

### <a name="bits-versions-casting-and-queryinterface"></a>Versiones de BITS, Conversión y QueryInterface

A menudo, verá que tiene que usar una versión anterior de un objeto BITS y una versión más reciente en el programa.  

Por ejemplo, cuando se realiza un objeto de trabajo, se obtiene un IBackgroundCopyJob (parte de bits versión 1.0) incluso cuando se usa un objeto de administrador más reciente y hay disponible un objeto IBackgroundCopyJob más reciente. Dado que el método CreateJob no acepta una interfaz para la versión más reciente, no puede crear directamente la versión más reciente.

Use una conversión de .NET para convertir un objeto de tipo anterior en un objeto de tipo más reciente. La conversión llamará automáticamente a una queryInterface COM según corresponda. 

En este ejemplo, hay un objeto IBackgroundCopyJob de BITS denominado "job" y queremos convertirlo en un objeto IBackgroundCopyJob5 denominado "job5" para que podamos llamar al método GetProperty de BITS 5.0. Simplemente se convierte al tipo IBackgroundCopyJob5 de la siguiente forma:

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

.NET inicializará la variable job5 mediante la queryinterface correcta. 

Si el código puede ejecutarse en un sistema que no admite una versión determinada de BITS, puede probar la conversión y detectar System.InvalidCastException. 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

Un problema común es cuando se intenta convertir en un tipo de objeto incorrecto. El sistema .NET no conoce la relación real entre las interfaces bits. Si solicita un tipo incorrecto de interfaz, .NET intentará hacerlo por usted y producirá un error con una excepción InvalidCastException y HResult 0x80004002 (E_NOINTERFACE).

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Trabajar con bits versiones 10_1 y 10_2

En algunas versiones de Windows 10 no se puede crear directamente un objeto IBackgroundCopyManager de BITS mediante las interfaces 10.1 o 10.2. En su lugar, tendrá que usar varias versiones de los archivos de referencia dll backgroundCopyManager. Por ejemplo, puede usar la versión 1.5 para crear un objeto IBackgroundCopyManager y, a continuación, convertir los objetos de archivo o trabajo resultantes mediante las versiones 10.1 o 10.2.

