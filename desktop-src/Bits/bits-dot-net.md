---
title: Usar BITS de .NET mediante archivos dll de referencia
description: En los siguientes ejemplos se muestra cómo llamar a la interfaz COM de BITS desde un programa .NET.
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785117"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Llamar a BITS desde .NET y C# mediante archivos dll de referencia

Una manera de llamar a las clases COM de BITS desde un programa .NET consiste en crear un archivo DLL de referencia a partir de los archivos de BITS [IDL](/windows/desktop/Midl/midl-start-page) (lenguaje de definición de interfaz) en el Windows SDK, mediante las herramientas [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) y [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) . El archivo DLL de referencia es un conjunto de contenedores de clases para las clases COM de BITS; después, puede usar las clases contenedoras directamente desde .NET.

Una alternativa al uso de archivos dll de referencia creados automáticamente es usar un contenedor de BITS .NET de terceros de [GitHub](https://github.com/) y [NuGet](https://www.nuget.org/). Estos contenedores suelen tener un estilo de programación de .NET más natural, pero podrían retrasarse detrás de los cambios y las actualizaciones en las interfaces de BITS.

## <a name="creating-the-reference-dlls"></a>Crear los archivos dll de referencia
### <a name="bits-idl-files"></a>Archivos IDL de BITS

Comenzará con el conjunto de archivos IDL de BITS. Se trata de archivos que definen totalmente la interfaz COM de BITS. Los archivos se encuentran en el directorio de **kits de Windows** y se denominan bits *versión*. idl (por ejemplo, bits10_2. idl), excepto el archivo de la versión 1,0, que es simplemente bits. idl. A medida que se crean nuevas versiones de BITS, también se crean nuevos archivos IDL de BITS.

También puede que desee modificar una copia de los archivos IDL de BITS de SDK para usar características de BITS que no se convierten automáticamente en equivalentes de .NET. Los posibles cambios en los archivos IDL se tratan más adelante.

Los archivos IDL de BITS incluyen otros archivos IDL por referencia. También anidan, de modo que si usa una versión, incluye todas las versiones anteriores.

Para cada versión de BITS que desee como destino en el programa, necesitará un archivo DLL de referencia para esa versión. Por ejemplo, si desea escribir un programa que funcione en BITS 1,5 y superior, pero tiene características adicionales cuando hay BITS 10,2, debe convertir los archivos bits1_5. idl y bits10_2. idl.


### <a name="midl-and-tlbimp-utilities"></a>Utilidades MIDL y TLBIMP

La utilidad [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (lenguaje de definición de interfaz de Microsoft) convierte los archivos IDL que describen la interfaz com de bits en un archivo TLB (biblioteca de tipos). La herramienta MIDL depende de la utilidad CL (preprocesador de C) para leer correctamente el archivo de lenguaje IDL. La utilidad CL forma parte de Visual Studio y se instala cuando se incluyen las características de C/C++ en la instalación de Visual Studio.

La utilidad MIDL crea normalmente un conjunto de archivos de C y H (código de lenguaje C y de encabezado de lenguaje C). Puede suprimir estos archivos adicionales mediante el envío de la salida al NUL: Device. Por ejemplo, si se establece el modificador NUL:/dlldata, se eliminará la creación de un archivo dlldata. c. Los comandos de ejemplo siguientes muestran los modificadores que se deben establecer en NUL:.

La utilidad [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (importador de la biblioteca de tipos) lee en un archivo TLB y crea el archivo dll de referencia correspondiente. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Comandos de ejemplo para MIDL y TLBIMP

Este es un ejemplo del conjunto completo de comandos para generar un conjunto de archivos de referencia. Es posible que tenga que modificar los comandos en función de la instalación de Visual Studio y Windows SDK, y en función de las características de BITS y las versiones de sistema operativo de destino. 

En el ejemplo se crea un directorio para colocar los archivos DLL de referencia y se crea una variable de entorno BITSTEMP para que apunte a ese directorio. 

Los comandos de ejemplo ejecutan después el archivo vsdevcmd.bat creado por el instalador de Visual Studio. Este archivo BAT configurará las rutas de acceso y algunas variables de entorno para que se ejecuten los comandos MIDL y TLBIMP. También configura las variables WindowsSdkDir y WindowsSDKLibVersion para que apunten a los directorios de Windows SDK más recientes.

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
Una vez que se ejecuten estos comandos, tendrá un conjunto de archivos dll de referencia en el directorio BITSTEMP

### <a name="adding-the-reference-dlls-to-your-project"></a>Agregar los archivos dll de referencia al proyecto

Para usar un archivo DLL de referencia en un proyecto de C#, abra el proyecto de C# en Visual Studio. En el Explorador de soluciones, haga clic con el botón secundario en referencias y haga clic en Agregar referencia. A continuación, haga clic en el botón examinar y luego en el botón Agregar. Navegue hasta el directorio con los archivos dll de referencia, selecciónelos y haga clic en Agregar. En la ventana Administrador de referencias se comprueban los archivos dll de referencia. A continuación, haga clic en Aceptar.

Los archivos dll de referencia de BITS ahora se agregan al proyecto.

La información de los archivos DLL de referencia se incrustará en el programa final. No es necesario enviar los archivos DLL de referencia con el programa; solo tiene que enviar el. Ejecutable. 

Puede cambiar si los archivos dll de referencia se incrustan en el archivo EXE final. Utilice la propiedad [incrustar tipos de interoperabilidad](/dotnet/framework/interop/how-to-add-references-to-type-libraries) para establecer si se incrustarán o no los archivos dll de referencia. Esto se puede hacer en función de cada referencia. El valor predeterminado es true para incrustar los archivos dll.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Modificar archivos IDL para obtener un código .NET más completo

Los archivos IDL (Lenguaje de definición de interfaz de Microsoft) de BITS se pueden usar sin cambios para crear el archivo DLL de BackgroundCopyManager. Sin embargo, a la DLL de referencia de .NET resultante le faltan algunas uniones que no se pueden traducir y que tienen nombres difíciles de usar para algunas estructuras y enumeraciones. En esta sección se describen algunos de los cambios que puede realizar para que el archivo DLL de .NET sea más completo y fácil de usar.

### <a name="simpler-enum-names"></a>Nombres de ENUMERAción más sencillos

Los archivos IDL de BITS suelen definir valores de enumeración como este:
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
El BG_AUTH_TARGET es el nombre de la definición de tipo; la enumeración real no tiene nombre. Esto no suele causar problemas con el código C, pero no se traduce bien para usarse con un programa .NET. Se creará automáticamente un nuevo nombre, pero podría ser similar a _MIDL___MIDL_itf_bits4_0_0005_0001_0001 en lugar de un valor legible. Puede corregir este problema actualizando los archivos MIDL para incluir un nombre de enumeración.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

El nombre de la enumeración puede ser el mismo que el nombre de la definición de tipo. Algunos programadores tienen una Convención de nomenclatura en la que se mantienen diferentes (por ejemplo, colocando un carácter de subrayado delante del nombre de la enumeración), pero esto solo confundirá las traducciones de .NET. 

### <a name="string-types-in-unions"></a>Tipos de cadena en uniones

Los archivos IDL de BITS pasan cadenas mediante la Convención LPWSTR (puntero largo a cadena de caracteres anchos). Aunque esto funciona al pasar parámetros de función (como el método Job. GetDisplayName ([out] LPWSTR * pVal)), no funciona cuando las cadenas forman parte de uniones. Por ejemplo, el archivo bits5_0. idl incluye el BITS_FILE_PROPERTY_VALUE Unión:

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

El campo LPWSTR no se incluirá en la versión .NET de la Unión. Para corregirlo, cambie LPWSTR a WCHAR *. El campo resultante (llamado cadena) se pasará como IntPtr. Convierta esto en una cadena mediante el valor de System. Runtime. InteropServices. Marshal. PtrToStringAuto (Value. Cadena); forma.

### <a name="unions-in-structures"></a>Uniones en estructuras

A veces, las uniones incrustadas en estructuras no se incluirán en la estructura. Por ejemplo, en el Bits1_5. idl, el BG_AUTH_CREDENTIALS se define de la siguiente manera:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

El BG_AUTH_CREDENTIALS_UNION se define como una Unión de la manera siguiente:
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
El campo Credentials en el BG_AUTH_CREDENTIALS no se incluirá en la definición de clase .NET.

Tenga en cuenta que la Unión se define para ser siempre un BG_BASIC_CREDENTIALS independientemente de la BG_AUTH_SCHEME. Dado que la Unión no se usa como Unión, podemos simplemente pasar una BG_BASIC_CREDENTIALS similar a la siguiente:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Usar BITS de C #

### <a name="recommended-using-statement"></a>Instrucción using recomendada

Al configurar algunas instrucciones Using en C#, se reducirá el número de caracteres que se deben escribir para usar las diferentes versiones de BITS. El nombre "BITSReference" procede del nombre del archivo DLL de referencia.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Ejemplo rápido: descargar un archivo

A continuación se muestra un fragmento corto pero completo de código C# para descargar un archivo desde una dirección URL. 

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

En este código de ejemplo, se crea un administrador de BITS denominado Mgr. Se corresponde directamente con la interfaz [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) . 

Desde el administrador se crea un nuevo trabajo. El trabajo es un parámetro de salida en el método CreateJob. También se pasa es el nombre del trabajo (que no tiene que ser único) y el tipo de descarga, que es un trabajo de descarga. También se rellena un GUID de BITS para el identificador de trabajo.

Una vez creado el trabajo, agregue un nuevo archivo de descarga al trabajo con el método AddFile. Debe pasar dos cadenas, una para el archivo remoto (la dirección URL o el recurso compartido de archivos) y otra para el archivo local. 

Después de agregar el archivo, llame a resume en el trabajo para iniciarlo. Después, el código espera hasta que el trabajo se encuentra en un estado final (ERROR o transferido) y, a continuación, se completa.

### <a name="bits-versions-casting-and-queryinterface"></a>Versiones de BITS, conversión y QueryInterface

Descubrirá que suele tener que usar una versión temprana de un objeto BITS y una versión más reciente en el programa.  

Por ejemplo, al crear un objeto de trabajo, obtendrá un IBackgroundCopyJob (parte de la versión de BITS 1,0) incluso cuando lo esté usando un objeto de administrador más reciente y esté disponible un objeto IBackgroundCopyJob más reciente. Dado que el método CreateJob no acepta una interfaz para la versión más reciente, no se puede crear directamente la versión más reciente.

Use una conversión de .NET para convertir de un objeto de tipo anterior a un objeto de tipo más reciente. La conversión llamará automáticamente a COM QueryInterface, según corresponda. 

En este ejemplo, hay un objeto IBackgroundCopyJob de BITS denominado "Job" y queremos convertirlo en un objeto IBackgroundCopyJob5 denominado "job5" para poder llamar al método BITS 5,0 GetProperty. Solo se convierten en el tipo IBackgroundCopyJob5 de la siguiente manera:

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

.NET inicializará la variable job5 con la función QueryInterface correcta. 

Si el código se puede ejecutar en un sistema que no es compatible con una versión determinada de BITS, puede probar la conversión y detectar System. InvalidCastException. 

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

Un problema común es cuando se intenta convertir en un tipo de objeto incorrecto. El sistema .NET no conoce la relación real entre las interfaces de BITS. Si solicita un tipo de interfaz incorrecto, .NET intentará hacerlo por usted y producirá un error con una excepción InvalidCastException y HResult 0x80004002 (E_NOINTERFACE).

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Trabajar con versiones de BITS 10_1 y 10_2

En algunas versiones de Windows 10 no se puede crear directamente un objeto IBackgroundCopyManager de BITS con las interfaces 10,1 o 10,2. En su lugar, tendrá que usar varias versiones de los archivos de referencia de DLL de BackgroundCopyManager. Por ejemplo, puede usar la versión 1,5 para crear un objeto IBackgroundCopyManager y, a continuación, convertir el trabajo o los objetos de archivo resultantes mediante las versiones 10,1 o 10,2.

