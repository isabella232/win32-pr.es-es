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
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a><span data-ttu-id="78af8-103">Llamar a BITS desde .NET y C# mediante archivos dll de referencia</span><span class="sxs-lookup"><span data-stu-id="78af8-103">Calling into BITS from .NET and C# using Reference DLLs</span></span>

<span data-ttu-id="78af8-104">Una manera de llamar a las clases COM de BITS desde un programa .NET consiste en crear un archivo DLL de referencia a partir de los archivos de BITS [IDL](/windows/desktop/Midl/midl-start-page) (lenguaje de definición de interfaz) en el Windows SDK, mediante las herramientas [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) y [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) .</span><span class="sxs-lookup"><span data-stu-id="78af8-104">One way to call into the BITS COM classes from a .NET program is to create a reference DLL file starting with the BITS [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) files in the Windows SDK, using the [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) and [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) tools.</span></span> <span data-ttu-id="78af8-105">El archivo DLL de referencia es un conjunto de contenedores de clases para las clases COM de BITS; después, puede usar las clases contenedoras directamente desde .NET.</span><span class="sxs-lookup"><span data-stu-id="78af8-105">The reference DLL is a set of class wrappers for the BITS COM classes; you can then use the wrapper classes directly from .NET.</span></span>

<span data-ttu-id="78af8-106">Una alternativa al uso de archivos dll de referencia creados automáticamente es usar un contenedor de BITS .NET de terceros de [GitHub](https://github.com/) y [NuGet](https://www.nuget.org/).</span><span class="sxs-lookup"><span data-stu-id="78af8-106">An alternative to using automatically-created reference DLLs is to use a 3rd party .NET BITS wrapper from [GitHub](https://github.com/) and [NuGet](https://www.nuget.org/).</span></span> <span data-ttu-id="78af8-107">Estos contenedores suelen tener un estilo de programación de .NET más natural, pero podrían retrasarse detrás de los cambios y las actualizaciones en las interfaces de BITS.</span><span class="sxs-lookup"><span data-stu-id="78af8-107">These wrappers often have a more natural .NET programming style but they might lag behind the changes and updates in the BITS interfaces.</span></span>

## <a name="creating-the-reference-dlls"></a><span data-ttu-id="78af8-108">Crear los archivos dll de referencia</span><span class="sxs-lookup"><span data-stu-id="78af8-108">Creating the reference DLLs</span></span>
### <a name="bits-idl-files"></a><span data-ttu-id="78af8-109">Archivos IDL de BITS</span><span class="sxs-lookup"><span data-stu-id="78af8-109">BITS IDL files</span></span>

<span data-ttu-id="78af8-110">Comenzará con el conjunto de archivos IDL de BITS.</span><span class="sxs-lookup"><span data-stu-id="78af8-110">You will start with the set of BITS IDL files.</span></span> <span data-ttu-id="78af8-111">Se trata de archivos que definen totalmente la interfaz COM de BITS.</span><span class="sxs-lookup"><span data-stu-id="78af8-111">These are files that fully define the BITS COM interface.</span></span> <span data-ttu-id="78af8-112">Los archivos se encuentran en el directorio de **kits de Windows** y se denominan bits *versión*. idl (por ejemplo, bits10_2. idl), excepto el archivo de la versión 1,0, que es simplemente bits. idl.</span><span class="sxs-lookup"><span data-stu-id="78af8-112">The files are located in the **Windows Kits** directory and are named bits *version*.idl (for example, bits10_2.idl) except for the version 1.0 file which is just Bits.idl.</span></span> <span data-ttu-id="78af8-113">A medida que se crean nuevas versiones de BITS, también se crean nuevos archivos IDL de BITS.</span><span class="sxs-lookup"><span data-stu-id="78af8-113">As new versions of BITS are created, new BITS IDL files are also created.</span></span>

<span data-ttu-id="78af8-114">También puede que desee modificar una copia de los archivos IDL de BITS de SDK para usar características de BITS que no se convierten automáticamente en equivalentes de .NET.</span><span class="sxs-lookup"><span data-stu-id="78af8-114">You may also want to modify a copy of the SDK BITS IDL files to use BITS features that aren't automatically converted into .NET equivalents.</span></span> <span data-ttu-id="78af8-115">Los posibles cambios en los archivos IDL se tratan más adelante.</span><span class="sxs-lookup"><span data-stu-id="78af8-115">Possible IDL file changes are discussed later on.</span></span>

<span data-ttu-id="78af8-116">Los archivos IDL de BITS incluyen otros archivos IDL por referencia.</span><span class="sxs-lookup"><span data-stu-id="78af8-116">The BITS IDL files include several other IDL files by reference.</span></span> <span data-ttu-id="78af8-117">También anidan, de modo que si usa una versión, incluye todas las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="78af8-117">They also nest, so that if you use one version, it includes all the lower versions.</span></span>

<span data-ttu-id="78af8-118">Para cada versión de BITS que desee como destino en el programa, necesitará un archivo DLL de referencia para esa versión.</span><span class="sxs-lookup"><span data-stu-id="78af8-118">For each version of BITS that you want to target in your program you will need one reference DLL for that version.</span></span> <span data-ttu-id="78af8-119">Por ejemplo, si desea escribir un programa que funcione en BITS 1,5 y superior, pero tiene características adicionales cuando hay BITS 10,2, debe convertir los archivos bits1_5. idl y bits10_2. idl.</span><span class="sxs-lookup"><span data-stu-id="78af8-119">For example, if you want to write a program that works on BITS 1.5 and up but has additional features when BITS 10.2 is present, you need to convert both the bits1_5.idl and bits10_2.idl files.</span></span>


### <a name="midl-and-tlbimp-utilities"></a><span data-ttu-id="78af8-120">Utilidades MIDL y TLBIMP</span><span class="sxs-lookup"><span data-stu-id="78af8-120">MIDL and TLBIMP utilities</span></span>

<span data-ttu-id="78af8-121">La utilidad [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (lenguaje de definición de interfaz de Microsoft) convierte los archivos IDL que describen la interfaz com de bits en un archivo TLB (biblioteca de tipos).</span><span class="sxs-lookup"><span data-stu-id="78af8-121">The [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) utility converts the IDL files that describe the BITS COM interface into a TLB (Type Library) file.</span></span> <span data-ttu-id="78af8-122">La herramienta MIDL depende de la utilidad CL (preprocesador de C) para leer correctamente el archivo de lenguaje IDL.</span><span class="sxs-lookup"><span data-stu-id="78af8-122">The MIDL tool depends on the CL utility (C preprocessor) to correctly read the IDL language file.</span></span> <span data-ttu-id="78af8-123">La utilidad CL forma parte de Visual Studio y se instala cuando se incluyen las características de C/C++ en la instalación de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="78af8-123">The CL utility is part of Visual Studio and is installed when you include C/C++ features in the Visual Studio installation.</span></span>

<span data-ttu-id="78af8-124">La utilidad MIDL crea normalmente un conjunto de archivos de C y H (código de lenguaje C y de encabezado de lenguaje C).</span><span class="sxs-lookup"><span data-stu-id="78af8-124">The MIDL utility will normally create a set of C and H (C language code and C language header) files.</span></span> <span data-ttu-id="78af8-125">Puede suprimir estos archivos adicionales mediante el envío de la salida al NUL: Device.</span><span class="sxs-lookup"><span data-stu-id="78af8-125">You can suppress these extra files by sending the output to the NUL: device.</span></span> <span data-ttu-id="78af8-126">Por ejemplo, si se establece el modificador NUL:/dlldata, se eliminará la creación de un archivo dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="78af8-126">For example, setting the /dlldata NUL: switch will suppress creating a dlldata.c file.</span></span> <span data-ttu-id="78af8-127">Los comandos de ejemplo siguientes muestran los modificadores que se deben establecer en NUL:.</span><span class="sxs-lookup"><span data-stu-id="78af8-127">The sample commands below shows which switches should be set to NUL:.</span></span>

<span data-ttu-id="78af8-128">La utilidad [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (importador de la biblioteca de tipos) lee en un archivo TLB y crea el archivo dll de referencia correspondiente.</span><span class="sxs-lookup"><span data-stu-id="78af8-128">The [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) utility reads in a TLB file and creates the corresponding reference DLL file.</span></span> 


### <a name="example-commands-for-midl-and-tlbimp"></a><span data-ttu-id="78af8-129">Comandos de ejemplo para MIDL y TLBIMP</span><span class="sxs-lookup"><span data-stu-id="78af8-129">Example commands for MIDL and TLBIMP</span></span>

<span data-ttu-id="78af8-130">Este es un ejemplo del conjunto completo de comandos para generar un conjunto de archivos de referencia.</span><span class="sxs-lookup"><span data-stu-id="78af8-130">This is an example of the complete set of commands to generate a set of reference files.</span></span> <span data-ttu-id="78af8-131">Es posible que tenga que modificar los comandos en función de la instalación de Visual Studio y Windows SDK, y en función de las características de BITS y las versiones de sistema operativo de destino.</span><span class="sxs-lookup"><span data-stu-id="78af8-131">You may need to modify the commands based on your Visual Studio and Windows SDK installation and based on the BITS features and OS versions you are targeting.</span></span> 

<span data-ttu-id="78af8-132">En el ejemplo se crea un directorio para colocar los archivos DLL de referencia y se crea una variable de entorno BITSTEMP para que apunte a ese directorio.</span><span class="sxs-lookup"><span data-stu-id="78af8-132">The example creates a directory to place the reference DLL files and creates an environment variable BITSTEMP to point to that directory.</span></span> 

<span data-ttu-id="78af8-133">Los comandos de ejemplo ejecutan después el archivo vsdevcmd.bat creado por el instalador de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="78af8-133">The example commands then run the vsdevcmd.bat file that's created by the Visual Studio installer.</span></span> <span data-ttu-id="78af8-134">Este archivo BAT configurará las rutas de acceso y algunas variables de entorno para que se ejecuten los comandos MIDL y TLBIMP.</span><span class="sxs-lookup"><span data-stu-id="78af8-134">This BAT file will set up your paths and some environment variables so that the MIDL and TLBIMP commands will run.</span></span> <span data-ttu-id="78af8-135">También configura las variables WindowsSdkDir y WindowsSDKLibVersion para que apunten a los directorios de Windows SDK más recientes.</span><span class="sxs-lookup"><span data-stu-id="78af8-135">It also sets up the WindowsSdkDir and WindowsSDKLibVersion variables to point to the most recent Windows SDK directories.</span></span>

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
<span data-ttu-id="78af8-136">Una vez que se ejecuten estos comandos, tendrá un conjunto de archivos dll de referencia en el directorio BITSTEMP</span><span class="sxs-lookup"><span data-stu-id="78af8-136">Once these commands are run you will have a set of reference DLLs in the BITSTEMP directory.</span></span>

### <a name="adding-the-reference-dlls-to-your-project"></a><span data-ttu-id="78af8-137">Agregar los archivos dll de referencia al proyecto</span><span class="sxs-lookup"><span data-stu-id="78af8-137">Adding the reference DLLs to your project</span></span>

<span data-ttu-id="78af8-138">Para usar un archivo DLL de referencia en un proyecto de C#, abra el proyecto de C# en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="78af8-138">To use a reference DLL in a C# project, open your C# project in Visual Studio.</span></span> <span data-ttu-id="78af8-139">En el Explorador de soluciones, haga clic con el botón secundario en referencias y haga clic en Agregar referencia.</span><span class="sxs-lookup"><span data-stu-id="78af8-139">In the Solution Explorer, right-click the References and click Add Reference.</span></span> <span data-ttu-id="78af8-140">A continuación, haga clic en el botón examinar y luego en el botón Agregar.</span><span class="sxs-lookup"><span data-stu-id="78af8-140">Then click the Browse button and then the Add button.</span></span> <span data-ttu-id="78af8-141">Navegue hasta el directorio con los archivos dll de referencia, selecciónelos y haga clic en Agregar.</span><span class="sxs-lookup"><span data-stu-id="78af8-141">Navigate to the directory with the reference DLLs, select them, and click Add.</span></span> <span data-ttu-id="78af8-142">En la ventana Administrador de referencias se comprueban los archivos dll de referencia.</span><span class="sxs-lookup"><span data-stu-id="78af8-142">In the Reference Manager window the reference DLLs will be checked.</span></span> <span data-ttu-id="78af8-143">A continuación, haga clic en Aceptar.</span><span class="sxs-lookup"><span data-stu-id="78af8-143">Then click OK.</span></span>

<span data-ttu-id="78af8-144">Los archivos dll de referencia de BITS ahora se agregan al proyecto.</span><span class="sxs-lookup"><span data-stu-id="78af8-144">The BITS reference DLLs are now added to your project.</span></span>

<span data-ttu-id="78af8-145">La información de los archivos DLL de referencia se incrustará en el programa final.</span><span class="sxs-lookup"><span data-stu-id="78af8-145">The information in the reference DLL files will be embedded into your final program.</span></span> <span data-ttu-id="78af8-146">No es necesario enviar los archivos DLL de referencia con el programa; solo tiene que enviar el. Ejecutable.</span><span class="sxs-lookup"><span data-stu-id="78af8-146">You do not have to ship the reference DLL files with your program; you just need to ship the .EXE.</span></span> 

<span data-ttu-id="78af8-147">Puede cambiar si los archivos dll de referencia se incrustan en el archivo EXE final.</span><span class="sxs-lookup"><span data-stu-id="78af8-147">You can change whether the reference DLLs are embedded into the final EXE.</span></span> <span data-ttu-id="78af8-148">Utilice la propiedad [incrustar tipos de interoperabilidad](/dotnet/framework/interop/how-to-add-references-to-type-libraries) para establecer si se incrustarán o no los archivos dll de referencia.</span><span class="sxs-lookup"><span data-stu-id="78af8-148">Use the [Embed Interop Types](/dotnet/framework/interop/how-to-add-references-to-type-libraries) property to set whether or not the reference DLLs will be embedded.</span></span> <span data-ttu-id="78af8-149">Esto se puede hacer en función de cada referencia.</span><span class="sxs-lookup"><span data-stu-id="78af8-149">This can be done on a per-reference basis.</span></span> <span data-ttu-id="78af8-150">El valor predeterminado es true para incrustar los archivos dll.</span><span class="sxs-lookup"><span data-stu-id="78af8-150">The default is True to embed the DLLs.</span></span>

## <a name="modifying-idl-files-for-more-complete-net-code"></a><span data-ttu-id="78af8-151">Modificar archivos IDL para obtener un código .NET más completo</span><span class="sxs-lookup"><span data-stu-id="78af8-151">Modifying IDL files for more complete .NET code</span></span>

<span data-ttu-id="78af8-152">Los archivos IDL (Lenguaje de definición de interfaz de Microsoft) de BITS se pueden usar sin cambios para crear el archivo DLL de BackgroundCopyManager.</span><span class="sxs-lookup"><span data-stu-id="78af8-152">The BITS IDL (Microsoft Interface Definition Language) files can be used unchanged to make the BackgroundCopyManager DLL file.</span></span> <span data-ttu-id="78af8-153">Sin embargo, a la DLL de referencia de .NET resultante le faltan algunas uniones que no se pueden traducir y que tienen nombres difíciles de usar para algunas estructuras y enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="78af8-153">However, the resulting .NET reference DLL will be missing some untranslatable unions and has hard-to-use names for some structures and enums.</span></span> <span data-ttu-id="78af8-154">En esta sección se describen algunos de los cambios que puede realizar para que el archivo DLL de .NET sea más completo y fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="78af8-154">This section will describe some of the changes that you can make to make the .NET DLL more complete and easier to use.</span></span>

### <a name="simpler-enum-names"></a><span data-ttu-id="78af8-155">Nombres de ENUMERAción más sencillos</span><span class="sxs-lookup"><span data-stu-id="78af8-155">Simpler ENUM names</span></span>

<span data-ttu-id="78af8-156">Los archivos IDL de BITS suelen definir valores de enumeración como este:</span><span class="sxs-lookup"><span data-stu-id="78af8-156">The BITS IDL files typically define enum values like this:</span></span>
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
<span data-ttu-id="78af8-157">El BG_AUTH_TARGET es el nombre de la definición de tipo; la enumeración real no tiene nombre.</span><span class="sxs-lookup"><span data-stu-id="78af8-157">The BG_AUTH_TARGET is the name of the typedef; the actual enum is not named.</span></span> <span data-ttu-id="78af8-158">Esto no suele causar problemas con el código C, pero no se traduce bien para usarse con un programa .NET.</span><span class="sxs-lookup"><span data-stu-id="78af8-158">This doesn’t typically cause problems with C code but doesn’t translate well for use with a .NET program.</span></span> <span data-ttu-id="78af8-159">Se creará automáticamente un nuevo nombre, pero podría ser similar a _MIDL___MIDL_itf_bits4_0_0005_0001_0001 en lugar de un valor legible.</span><span class="sxs-lookup"><span data-stu-id="78af8-159">A new name will be automatically created, but it might look something like _MIDL___MIDL_itf_bits4_0_0005_0001_0001 instead of a human-readable value.</span></span> <span data-ttu-id="78af8-160">Puede corregir este problema actualizando los archivos MIDL para incluir un nombre de enumeración.</span><span class="sxs-lookup"><span data-stu-id="78af8-160">You can fix this problem by updating the MIDL files to include an enum name.</span></span>

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

<span data-ttu-id="78af8-161">El nombre de la enumeración puede ser el mismo que el nombre de la definición de tipo.</span><span class="sxs-lookup"><span data-stu-id="78af8-161">The enum name is allowed to be the same as the typedef name.</span></span> <span data-ttu-id="78af8-162">Algunos programadores tienen una Convención de nomenclatura en la que se mantienen diferentes (por ejemplo, colocando un carácter de subrayado delante del nombre de la enumeración), pero esto solo confundirá las traducciones de .NET.</span><span class="sxs-lookup"><span data-stu-id="78af8-162">Some programmers have a naming convention where they are kept different (for example, by putting an underscore before the enum name), but this will only confuse the .NET translations.</span></span> 

### <a name="string-types-in-unions"></a><span data-ttu-id="78af8-163">Tipos de cadena en uniones</span><span class="sxs-lookup"><span data-stu-id="78af8-163">String types in unions</span></span>

<span data-ttu-id="78af8-164">Los archivos IDL de BITS pasan cadenas mediante la Convención LPWSTR (puntero largo a cadena de caracteres anchos).</span><span class="sxs-lookup"><span data-stu-id="78af8-164">The BITS IDL files pass strings using the LPWSTR (long pointer to wide-character string) convention.</span></span> <span data-ttu-id="78af8-165">Aunque esto funciona al pasar parámetros de función (como el método Job. GetDisplayName ([out] LPWSTR \* pVal)), no funciona cuando las cadenas forman parte de uniones.</span><span class="sxs-lookup"><span data-stu-id="78af8-165">Although this works when passing function parameters (like the Job.GetDisplayName([out] LPWSTR \*pVal) method), it doesn’t work when the strings are part of unions.</span></span> <span data-ttu-id="78af8-166">Por ejemplo, el archivo bits5_0. idl incluye el BITS_FILE_PROPERTY_VALUE Unión:</span><span class="sxs-lookup"><span data-stu-id="78af8-166">For example, the bits5_0.idl file includes the BITS_FILE_PROPERTY_VALUE union:</span></span>

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

<span data-ttu-id="78af8-167">El campo LPWSTR no se incluirá en la versión .NET de la Unión.</span><span class="sxs-lookup"><span data-stu-id="78af8-167">The LPWSTR field won’t be included in the .NET version of the union.</span></span> <span data-ttu-id="78af8-168">Para corregirlo, cambie LPWSTR a WCHAR \*.</span><span class="sxs-lookup"><span data-stu-id="78af8-168">To fix this, change the LPWSTR to a WCHAR\*.</span></span> <span data-ttu-id="78af8-169">El campo resultante (llamado cadena) se pasará como IntPtr.</span><span class="sxs-lookup"><span data-stu-id="78af8-169">The resulting field (called String) will be passed as a IntPtr.</span></span> <span data-ttu-id="78af8-170">Convierta esto en una cadena mediante el valor de System. Runtime. InteropServices. Marshal. PtrToStringAuto (Value. Cadena); forma.</span><span class="sxs-lookup"><span data-stu-id="78af8-170">Convert this into a string using the  System.Runtime.InteropServices.Marshal.PtrToStringAuto(value.String); method.</span></span>

### <a name="unions-in-structures"></a><span data-ttu-id="78af8-171">Uniones en estructuras</span><span class="sxs-lookup"><span data-stu-id="78af8-171">Unions in structures</span></span>

<span data-ttu-id="78af8-172">A veces, las uniones incrustadas en estructuras no se incluirán en la estructura.</span><span class="sxs-lookup"><span data-stu-id="78af8-172">Sometimes unions that are embedded in structures won't be included in the structure at all.</span></span> <span data-ttu-id="78af8-173">Por ejemplo, en el Bits1_5. idl, el BG_AUTH_CREDENTIALS se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="78af8-173">For example, in the Bits1_5.idl the BG_AUTH_CREDENTIALS is defined as follows:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

<span data-ttu-id="78af8-174">El BG_AUTH_CREDENTIALS_UNION se define como una Unión de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="78af8-174">The BG_AUTH_CREDENTIALS_UNION is defined to be a union as follows:</span></span>
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
<span data-ttu-id="78af8-175">El campo Credentials en el BG_AUTH_CREDENTIALS no se incluirá en la definición de clase .NET.</span><span class="sxs-lookup"><span data-stu-id="78af8-175">The Credentials field in the BG_AUTH_CREDENTIALS will not be included in the .NET class definition.</span></span>

<span data-ttu-id="78af8-176">Tenga en cuenta que la Unión se define para ser siempre un BG_BASIC_CREDENTIALS independientemente de la BG_AUTH_SCHEME.</span><span class="sxs-lookup"><span data-stu-id="78af8-176">Note that the union is defined to always be a BG_BASIC_CREDENTIALS regardless of the BG_AUTH_SCHEME.</span></span> <span data-ttu-id="78af8-177">Dado que la Unión no se usa como Unión, podemos simplemente pasar una BG_BASIC_CREDENTIALS similar a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="78af8-177">Because the union isn’t used as a union, we can just pass a BG_BASIC_CREDENTIALS like this:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a><span data-ttu-id="78af8-178">Usar BITS de C #</span><span class="sxs-lookup"><span data-stu-id="78af8-178">Using BITS from C#</span></span>

### <a name="recommended-using-statement"></a><span data-ttu-id="78af8-179">Instrucción using recomendada</span><span class="sxs-lookup"><span data-stu-id="78af8-179">Recommended using statement</span></span>

<span data-ttu-id="78af8-180">Al configurar algunas instrucciones Using en C#, se reducirá el número de caracteres que se deben escribir para usar las diferentes versiones de BITS.</span><span class="sxs-lookup"><span data-stu-id="78af8-180">Setting up some using statements in C# will reduce the number of characters you need to type to use the different BITS versions.</span></span> <span data-ttu-id="78af8-181">El nombre "BITSReference" procede del nombre del archivo DLL de referencia.</span><span class="sxs-lookup"><span data-stu-id="78af8-181">The name "BITSReference" comes from the name of the reference DLL.</span></span>

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a><span data-ttu-id="78af8-182">Ejemplo rápido: descargar un archivo</span><span class="sxs-lookup"><span data-stu-id="78af8-182">Quick Sample: download a file</span></span>

<span data-ttu-id="78af8-183">A continuación se muestra un fragmento corto pero completo de código C# para descargar un archivo desde una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="78af8-183">A short but complete snippet of C# code to download a file from a URL is given below.</span></span> 

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

<span data-ttu-id="78af8-184">En este código de ejemplo, se crea un administrador de BITS denominado Mgr.</span><span class="sxs-lookup"><span data-stu-id="78af8-184">In this sample code, a BITS manager named mgr is created.</span></span> <span data-ttu-id="78af8-185">Se corresponde directamente con la interfaz [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="78af8-185">It directly corresponds to the [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) interface.</span></span> 

<span data-ttu-id="78af8-186">Desde el administrador se crea un nuevo trabajo.</span><span class="sxs-lookup"><span data-stu-id="78af8-186">From the manager a new job is created.</span></span> <span data-ttu-id="78af8-187">El trabajo es un parámetro de salida en el método CreateJob.</span><span class="sxs-lookup"><span data-stu-id="78af8-187">The job is an out parameter on the CreateJob method.</span></span> <span data-ttu-id="78af8-188">También se pasa es el nombre del trabajo (que no tiene que ser único) y el tipo de descarga, que es un trabajo de descarga.</span><span class="sxs-lookup"><span data-stu-id="78af8-188">Also passed in is the job name (which doesn't have to be unique) and the download type, which is a download job.</span></span> <span data-ttu-id="78af8-189">También se rellena un GUID de BITS para el identificador de trabajo.</span><span class="sxs-lookup"><span data-stu-id="78af8-189">A BITS GUID for the job identifier is also filled in.</span></span>

<span data-ttu-id="78af8-190">Una vez creado el trabajo, agregue un nuevo archivo de descarga al trabajo con el método AddFile.</span><span class="sxs-lookup"><span data-stu-id="78af8-190">Once the job is created you add a new download file to the job with the AddFile method.</span></span> <span data-ttu-id="78af8-191">Debe pasar dos cadenas, una para el archivo remoto (la dirección URL o el recurso compartido de archivos) y otra para el archivo local.</span><span class="sxs-lookup"><span data-stu-id="78af8-191">You need to pass in two strings, one for the remote file (the URL or file share) and one for the local file.</span></span> 

<span data-ttu-id="78af8-192">Después de agregar el archivo, llame a resume en el trabajo para iniciarlo.</span><span class="sxs-lookup"><span data-stu-id="78af8-192">After adding the file, call Resume on the job to start it.</span></span> <span data-ttu-id="78af8-193">Después, el código espera hasta que el trabajo se encuentra en un estado final (ERROR o transferido) y, a continuación, se completa.</span><span class="sxs-lookup"><span data-stu-id="78af8-193">Then the code waits until the job is in a final state (ERROR or TRANSFERRED) and is then completed.</span></span>

### <a name="bits-versions-casting-and-queryinterface"></a><span data-ttu-id="78af8-194">Versiones de BITS, conversión y QueryInterface</span><span class="sxs-lookup"><span data-stu-id="78af8-194">BITS Versions, Casting and QueryInterface</span></span>

<span data-ttu-id="78af8-195">Descubrirá que suele tener que usar una versión temprana de un objeto BITS y una versión más reciente en el programa.</span><span class="sxs-lookup"><span data-stu-id="78af8-195">You'll find that you often have to use both an early version of a BITS object and a more recent version in your program.</span></span>  

<span data-ttu-id="78af8-196">Por ejemplo, al crear un objeto de trabajo, obtendrá un IBackgroundCopyJob (parte de la versión de BITS 1,0) incluso cuando lo esté usando un objeto de administrador más reciente y esté disponible un objeto IBackgroundCopyJob más reciente.</span><span class="sxs-lookup"><span data-stu-id="78af8-196">For example, when you make a job object, you will get an IBackgroundCopyJob (part of BITS version 1.0) even when you're making it using a more recent manager object and a more recent IBackgroundCopyJob object is available.</span></span> <span data-ttu-id="78af8-197">Dado que el método CreateJob no acepta una interfaz para la versión más reciente, no se puede crear directamente la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="78af8-197">Because the CreateJob method doesn't accept an interface for the more recent version, you can't directly make the more recent version.</span></span>

<span data-ttu-id="78af8-198">Use una conversión de .NET para convertir de un objeto de tipo anterior a un objeto de tipo más reciente.</span><span class="sxs-lookup"><span data-stu-id="78af8-198">Use a .NET cast to convert from an older type object to a newer type object.</span></span> <span data-ttu-id="78af8-199">La conversión llamará automáticamente a COM QueryInterface, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="78af8-199">The cast will automatically call a COM QueryInterface as appropriate.</span></span> 

<span data-ttu-id="78af8-200">En este ejemplo, hay un objeto IBackgroundCopyJob de BITS denominado "Job" y queremos convertirlo en un objeto IBackgroundCopyJob5 denominado "job5" para poder llamar al método BITS 5,0 GetProperty.</span><span class="sxs-lookup"><span data-stu-id="78af8-200">In this example, there's a BITS IBackgroundCopyJob object named "job", and we want to convert it to an IBackgroundCopyJob5 object named "job5" so that we can call the BITS 5.0 GetProperty method.</span></span> <span data-ttu-id="78af8-201">Solo se convierten en el tipo IBackgroundCopyJob5 de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="78af8-201">We just cast to the IBackgroundCopyJob5 type like this:</span></span>

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

<span data-ttu-id="78af8-202">.NET inicializará la variable job5 con la función QueryInterface correcta.</span><span class="sxs-lookup"><span data-stu-id="78af8-202">The job5 variable will be initialized by .NET by using the correct QueryInterface.</span></span> 

<span data-ttu-id="78af8-203">Si el código se puede ejecutar en un sistema que no es compatible con una versión determinada de BITS, puede probar la conversión y detectar System. InvalidCastException.</span><span class="sxs-lookup"><span data-stu-id="78af8-203">If your code might run on a system that doesn't support a particular version of BITS, you can try the cast and catch the System.InvalidCastException.</span></span> 

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

<span data-ttu-id="78af8-204">Un problema común es cuando se intenta convertir en un tipo de objeto incorrecto.</span><span class="sxs-lookup"><span data-stu-id="78af8-204">A common problem is when you try to cast into the wrong kind of object.</span></span> <span data-ttu-id="78af8-205">El sistema .NET no conoce la relación real entre las interfaces de BITS.</span><span class="sxs-lookup"><span data-stu-id="78af8-205">The .NET system doesn't know about the real relationship between the BITS interfaces.</span></span> <span data-ttu-id="78af8-206">Si solicita un tipo de interfaz incorrecto, .NET intentará hacerlo por usted y producirá un error con una excepción InvalidCastException y HResult 0x80004002 (E_NOINTERFACE).</span><span class="sxs-lookup"><span data-stu-id="78af8-206">If you ask for the wrong kind of interface, .NET will try to make it for you and will fail with an InvalidCastException and HResult 0x80004002 (E_NOINTERFACE).</span></span>

### <a name="working-with-bits-versions-10_1-and-10_2"></a><span data-ttu-id="78af8-207">Trabajar con versiones de BITS 10_1 y 10_2</span><span class="sxs-lookup"><span data-stu-id="78af8-207">Working with BITS Versions 10_1 and 10_2</span></span>

<span data-ttu-id="78af8-208">En algunas versiones de Windows 10 no se puede crear directamente un objeto IBackgroundCopyManager de BITS con las interfaces 10,1 o 10,2.</span><span class="sxs-lookup"><span data-stu-id="78af8-208">On some versions of Windows 10 you can't directly create a BITS IBackgroundCopyManager object using the 10.1 or 10.2 interfaces.</span></span> <span data-ttu-id="78af8-209">En su lugar, tendrá que usar varias versiones de los archivos de referencia de DLL de BackgroundCopyManager.</span><span class="sxs-lookup"><span data-stu-id="78af8-209">Instead, you'll have to use multiple versions of the BackgroundCopyManager DLL reference files.</span></span> <span data-ttu-id="78af8-210">Por ejemplo, puede usar la versión 1,5 para crear un objeto IBackgroundCopyManager y, a continuación, convertir el trabajo o los objetos de archivo resultantes mediante las versiones 10,1 o 10,2.</span><span class="sxs-lookup"><span data-stu-id="78af8-210">For example, you can use the 1.5 version to make an IBackgroundCopyManager object, and then cast the resulting job or file objects using the 10.1 or 10.2 versions.</span></span>

