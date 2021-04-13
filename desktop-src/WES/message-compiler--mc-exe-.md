---
title: Compilador de mensajes (MC.exe)
description: Se utiliza para compilar manifiestos de instrumentación y archivos de texto de mensaje.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- EventLog del compilador de mensajes (MC.exe)
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539333"
---
# <a name="message-compiler-mcexe"></a><span data-ttu-id="a669d-104">Compilador de mensajes (MC.exe)</span><span class="sxs-lookup"><span data-stu-id="a669d-104">Message Compiler (MC.exe)</span></span>

<span data-ttu-id="a669d-105">Se utiliza para compilar manifiestos de instrumentación y archivos de texto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a669d-105">Used to compile instrumentation manifests and message text files.</span></span> <span data-ttu-id="a669d-106">El compilador genera los archivos de recursos de mensajes a los que se vincula la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a669d-106">The compiler generates the message resource files to which your application links.</span></span>

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [<span data-ttu-id="a669d-107">Argumentos comunes para archivos de texto de mensaje y archivos de manifiesto</span><span class="sxs-lookup"><span data-stu-id="a669d-107">Arguments common to both message text files and manifest files</span></span>](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [<span data-ttu-id="a669d-108">Argumentos específicos de los archivos de manifiesto</span><span class="sxs-lookup"><span data-stu-id="a669d-108">Arguments specific to manifest files</span></span>](#arguments-specific-to-manifest-files)
-   [<span data-ttu-id="a669d-109">Argumentos específicos de la generación de código que el proveedor usaría para registrar eventos</span><span class="sxs-lookup"><span data-stu-id="a669d-109">Arguments specific to generating code that your provider would use to log events</span></span>](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [<span data-ttu-id="a669d-110">Argumentos específicos de los archivos de texto de mensaje</span><span class="sxs-lookup"><span data-stu-id="a669d-110">Arguments specific to message text files</span></span>](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a><span data-ttu-id="a669d-111">Argumentos comunes para archivos de texto de mensaje y archivos de manifiesto</span><span class="sxs-lookup"><span data-stu-id="a669d-111">Arguments common to both message text files and manifest files</span></span>

<dl> <dt>

<span data-ttu-id="a669d-112"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="a669d-112"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-113">Muestra la información de uso del compilador de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a669d-113">Displays the usage information for the Message Compiler.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-114"><span id="-c"></span><span id="-C"></span>**-c**</span><span class="sxs-lookup"><span data-stu-id="a669d-114"><span id="-c"></span><span id="-C"></span>**-c**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-115">Use este argumento para que el compilador establezca el bit de cliente (bit 28) en todos los identificadores de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a669d-115">Use this argument to have the compiler set the customer bit (bit 28) in all message IDs.</span></span> <span data-ttu-id="a669d-116">Para obtener información sobre el bit de cliente, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a669d-116">For information on the customer bit, see winerror.h.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-117"><span id="-cp"></span><span id="-CP"></span>**-codificación de CP** </span><span class="sxs-lookup"><span data-stu-id="a669d-117"><span id="-cp"></span><span id="-CP"></span>**-cp** *encoding*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-118">Use este argumento para especificar la codificación de caracteres utilizada para todos los archivos de texto generados.</span><span class="sxs-lookup"><span data-stu-id="a669d-118">Use this argument to specify the character encoding used for all generated text files.</span></span> <span data-ttu-id="a669d-119">Los nombres válidos son "ANSI" (predeterminado), "UTF-8" y "UTF-16".</span><span class="sxs-lookup"><span data-stu-id="a669d-119">Valid names include "ansi" (default), "utf-8", and "utf-16".</span></span> <span data-ttu-id="a669d-120">Las codificaciones Unicode agregarán una marca de orden de bytes.</span><span class="sxs-lookup"><span data-stu-id="a669d-120">The Unicode encodings will add a byte order mark.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>*extensión* **-e**</span><span class="sxs-lookup"><span data-stu-id="a669d-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *extension*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-122">Use este argumento para especificar la extensión que se va a usar para el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="a669d-122">Use this argument to specify the extension to use for the header file.</span></span> <span data-ttu-id="a669d-123">Puede especificar hasta una extensión de tres caracteres, sin incluir el punto.</span><span class="sxs-lookup"><span data-stu-id="a669d-123">You can specify up to a three characters extension, not including the period.</span></span> <span data-ttu-id="a669d-124">El valor predeterminado es. h.</span><span class="sxs-lookup"><span data-stu-id="a669d-124">The default is .h.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h ruta de** *acceso*</span><span class="sxs-lookup"><span data-stu-id="a669d-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-126">Use este argumento para especificar la carpeta en la que desea que el compilador Coloque el archivo de encabezado generado.</span><span class="sxs-lookup"><span data-stu-id="a669d-126">Use this argument to specify the folder into which you want the compiler to place the generated header file.</span></span> <span data-ttu-id="a669d-127">El valor predeterminado es el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="a669d-127">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *longitud*</span><span class="sxs-lookup"><span data-stu-id="a669d-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *length*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-129">Utilice este argumento para que el compilador genere una advertencia si el mensaje any supera los caracteres de *longitud* .</span><span class="sxs-lookup"><span data-stu-id="a669d-129">Use this argument to have the compiler generate a warning if the any message exceeds *length* characters.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r ruta de** *acceso*</span><span class="sxs-lookup"><span data-stu-id="a669d-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-131">Use este argumento para especificar la carpeta en la que desea que el compilador Coloque el script del compilador de recursos generado (archivo. RC) y los archivos. bin generados (recursos binarios) que incluye el script del compilador de recursos.</span><span class="sxs-lookup"><span data-stu-id="a669d-131">Use this argument to specify the folder into which you want the compiler to place the generated resource compiler script (.rc file) and the generated .bin files (binary resources) that the resource compiler script includes.</span></span> <span data-ttu-id="a669d-132">El valor predeterminado es el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="a669d-132">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *nombre*</span><span class="sxs-lookup"><span data-stu-id="a669d-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *name*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-134">Utilice este argumento para reemplazar el nombre base predeterminado que el compilador utiliza para los archivos que genera.</span><span class="sxs-lookup"><span data-stu-id="a669d-134">Use this argument to override the default base name that the compiler uses for the files that it generates.</span></span> <span data-ttu-id="a669d-135">El valor predeterminado es usar el nombre base del archivo de entrada de *nombre* de archivo.</span><span class="sxs-lookup"><span data-stu-id="a669d-135">The default is to use the base name of the *filename* input file.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-136"><span id="filename"></span><span id="FILENAME"></span>*extensión*</span><span class="sxs-lookup"><span data-stu-id="a669d-136"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-137">Archivo de manifiesto de instrumentación o archivo de texto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a669d-137">The instrumentation manifest file or message text file.</span></span> <span data-ttu-id="a669d-138">El archivo debe existir en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="a669d-138">The file must exist in the current directory.</span></span> <span data-ttu-id="a669d-139">Puede especificar un archivo de manifiesto, un archivo de texto de mensaje o ambos.</span><span class="sxs-lookup"><span data-stu-id="a669d-139">You can specify a manifest file, message text file, or both.</span></span> <span data-ttu-id="a669d-140">El nombre de archivo debe incluir la extensión.</span><span class="sxs-lookup"><span data-stu-id="a669d-140">The file name must include the extension.</span></span> <span data-ttu-id="a669d-141">La Convención es usar una extensión. Man para los archivos de manifiesto y una extensión. MC para los archivos de texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a669d-141">The convention is to use a .man extension for manifest files and a .mc extension for message text files.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a><span data-ttu-id="a669d-142">Argumentos específicos de los archivos de manifiesto</span><span class="sxs-lookup"><span data-stu-id="a669d-142">Arguments specific to manifest files</span></span>

<dl> <dt>

<span data-ttu-id="a669d-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s ruta de** *acceso*</span><span class="sxs-lookup"><span data-stu-id="a669d-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-144">Use este argumento para crear una línea base de la instrumentación.</span><span class="sxs-lookup"><span data-stu-id="a669d-144">Use this argument to create a baseline of your instrumentation.</span></span> <span data-ttu-id="a669d-145">Especifique la ruta de acceso a la carpeta que contiene los archivos de manifiesto de línea de base.</span><span class="sxs-lookup"><span data-stu-id="a669d-145">Specify the path to the folder that contains your baseline manifest files.</span></span> <span data-ttu-id="a669d-146">En las versiones posteriores, usaría el argumento **-t** para comprobar el nuevo manifiesto en la línea base para los problemas de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="a669d-146">For subsequent releases, you would then use the **-t** argument to check the new manifest against the baseline for compatibility issues.</span></span>

<span data-ttu-id="a669d-147">**Antes de la versión de MC 1.12.7051:** No disponible</span><span class="sxs-lookup"><span data-stu-id="a669d-147">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="a669d-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t ruta de** *acceso*</span><span class="sxs-lookup"><span data-stu-id="a669d-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-149">Use este argumento al crear una nueva versión del manifiesto y desea comprobar la compatibilidad de las aplicaciones con la línea de base que creó con el argumento **-s** .</span><span class="sxs-lookup"><span data-stu-id="a669d-149">Use this argument when you create a new version of your manifest and want to check it for application compatibility against the baseline that you created using the **-s** argument.</span></span> <span data-ttu-id="a669d-150">La ruta de acceso debe apuntar a la carpeta que contiene. Archivos BIN creados por la operación de línea de base (vea el conmutador **-s** ).</span><span class="sxs-lookup"><span data-stu-id="a669d-150">The path must point to the folder that contains the .BIN files that the baseline operation created (see the **-s** switch).</span></span>

<span data-ttu-id="a669d-151">**Antes de la versión de MC 1.12.7051:** No disponible</span><span class="sxs-lookup"><span data-stu-id="a669d-151">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="a669d-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w ruta de** *acceso*</span><span class="sxs-lookup"><span data-stu-id="a669d-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-153">El compilador omite este argumento y valida automáticamente el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a669d-153">The compiler ignores this argument and automatically validates the manifest.</span></span>

<span data-ttu-id="a669d-154">**Antes de la versión de MC 1.12.7051:** Use este argumento para especificar la carpeta que contiene el archivo de esquema Event-. xsd, que el compilador usa para validar el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a669d-154">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Eventman.xsd schema file, which the compiler uses to validate your manifest.</span></span> <span data-ttu-id="a669d-155">El Windows SDK incluye el archivo de esquema Event-. xsd en la \\ carpeta include.</span><span class="sxs-lookup"><span data-stu-id="a669d-155">The Windows SDK includes the Eventman.xsd schema file in the \\Include folder.</span></span> <span data-ttu-id="a669d-156">Si no especifica este argumento, el compilador no valida el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a669d-156">If you do not specify this argument, the compiler does not validate your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W ruta de** *acceso*</span><span class="sxs-lookup"><span data-stu-id="a669d-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-158">El compilador omite este argumento.</span><span class="sxs-lookup"><span data-stu-id="a669d-158">The compiler ignores this argument.</span></span>

<span data-ttu-id="a669d-159">**Antes de la versión de MC 1.12.7051:** Use este argumento para especificar la carpeta que contiene el archivo de Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="a669d-159">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Winmeta.xml file.</span></span> <span data-ttu-id="a669d-160">El archivo Winmeta.xml contiene los tipos de entrada y salida reconocidos, así como los canales, niveles y códigos de acceso predefinidos.</span><span class="sxs-lookup"><span data-stu-id="a669d-160">The Winmeta.xml file contains the recognized input and output types as well as the predefined channels, levels, and opcodes.</span></span> <span data-ttu-id="a669d-161">El Windows SDK incluye el archivo de Winmeta.xml en la \\ carpeta de inclusión.</span><span class="sxs-lookup"><span data-stu-id="a669d-161">The Windows SDK includes the Winmeta.xml file in the \\Include folder.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a><span data-ttu-id="a669d-162">Argumentos específicos de la generación de código que el proveedor usaría para registrar eventos</span><span class="sxs-lookup"><span data-stu-id="a669d-162">Arguments specific to generating code that your provider would use to log events</span></span>

<span data-ttu-id="a669d-163">Puede usar los siguientes argumentos del compilador para generar código en modo kernel o en modo de usuario que puede usar para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="a669d-163">You can use the following compiler arguments to generate kernel-mode or user-mode code that you can use to log events.</span></span> <span data-ttu-id="a669d-164">También puede solicitar que el compilador genere código para admitir la escritura de eventos en equipos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a669d-164">You can also request that the compiler generate code to support writing events on computers prior to Windows Vista.</span></span> <span data-ttu-id="a669d-165">Si la aplicación está escrita en C#, el compilador puede generar una clase de C# que se puede usar para registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="a669d-165">If your application is written C#, the compiler can generate a C# class that you can use to log events.</span></span> <span data-ttu-id="a669d-166">Estos argumentos están disponibles a partir de la versión de MC 1.12.7051 que se incluye con la versión de Windows 7 del SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="a669d-166">These arguments are available beginning with MC version 1.12.7051 that ships with the Windows 7 version of the Window SDK.</span></span>

<dl> <dt>

<span data-ttu-id="a669d-167"><span id="-co"></span><span id="-CO"></span>**-Co**</span><span class="sxs-lookup"><span data-stu-id="a669d-167"><span id="-co"></span><span id="-CO"></span>**-co**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-168">Use este argumento para que el servicio de registro llame a la función definida por el usuario para cada evento que registre (se llama a la función una vez que se ha registrado el evento).</span><span class="sxs-lookup"><span data-stu-id="a669d-168">Use this argument to have the logging service call your user-defined function for each event that you log (the function is called after the event has been logged).</span></span> <span data-ttu-id="a669d-169">La función definida por el usuario debe tener la siguiente firma.</span><span class="sxs-lookup"><span data-stu-id="a669d-169">Your user-defined function must have the following signature.</span></span>


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



<span data-ttu-id="a669d-170">También debe incluir la siguiente directiva en el código.</span><span class="sxs-lookup"><span data-stu-id="a669d-170">You must also include the following directive in your code.</span></span>

`#define MCGEN_CALLOUT pFnUserFunction`

<span data-ttu-id="a669d-171">Debe mantener la implementación lo más corta posible para evitar problemas de registro. el servicio no registrará ya los eventos hasta que vuelva la función.</span><span class="sxs-lookup"><span data-stu-id="a669d-171">You should keep your implementation as short as possible to prevent logging issues; the service will not log anymore of your events until the function returns.</span></span>

<span data-ttu-id="a669d-172">Puede usar este argumento con el argumento **-km** o **-Um** .</span><span class="sxs-lookup"><span data-stu-id="a669d-172">You can use this argument with the **-km** or **-um** argument.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-espacio de** *nombres* CS</span><span class="sxs-lookup"><span data-stu-id="a669d-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-174">Use este argumento para que el compilador genere una clase de C# basada en la clase [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) de .net 3,5.</span><span class="sxs-lookup"><span data-stu-id="a669d-174">Use this argument to have the compiler generate a C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-espacio de** *nombres* CSS</span><span class="sxs-lookup"><span data-stu-id="a669d-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-176">Use este argumento para que el compilador genere una clase de C# estática basada en la clase [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) de .net 3,5.</span><span class="sxs-lookup"><span data-stu-id="a669d-176">Use this argument to have the compiler generate a static C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-177"><span id="-km"></span><span id="-KM"></span>**-km**</span><span class="sxs-lookup"><span data-stu-id="a669d-177"><span id="-km"></span><span id="-KM"></span>**-km**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-178">Utilice este argumento para que el compilador genere el código en modo kernel que se usaría para registrar los eventos definidos en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a669d-178">Use this argument to have the compiler generate the kernel-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-179"><span id="-mof"></span><span id="-MOF"></span>**-MOF**</span><span class="sxs-lookup"><span data-stu-id="a669d-179"><span id="-mof"></span><span id="-MOF"></span>**-mof**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-180">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a669d-180">DEPRECATED.</span></span> <span data-ttu-id="a669d-181">Use este argumento para que el compilador genere código que pueda usar para registrar eventos en equipos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a669d-181">Use this argument to have the compiler generate code that you can use to log events on computers prior to Windows Vista.</span></span> <span data-ttu-id="a669d-182">Esta opción también crea un archivo MOF que contiene las clases MOF para cada evento definido en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a669d-182">This option also creates a MOF file that contains the MOF classes for each event defined in the manifest.</span></span> <span data-ttu-id="a669d-183">Para registrar las clases en el archivo MOF para que los consumidores puedan descodificar los eventos, utilice el compilador MOF (Mofcomp.exe).</span><span class="sxs-lookup"><span data-stu-id="a669d-183">To register the classes in the MOF file so that consumers can decode the events, use the MOF compiler (Mofcomp.exe).</span></span> <span data-ttu-id="a669d-184">Para obtener información detallada sobre el uso del compilador MOF, vea [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a669d-184">For details on using the MOF compiler, see [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

<span data-ttu-id="a669d-185">Para usar este modificador, debe cumplir las restricciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a669d-185">To use this switch, you must adhere to the following restrictions:</span></span>

-   <span data-ttu-id="a669d-186">Cada definición de evento debe incluir los atributos Task y OpCode.</span><span class="sxs-lookup"><span data-stu-id="a669d-186">Every event definition must include the task and opcode attributes</span></span>
-   <span data-ttu-id="a669d-187">Cada tarea debe incluir el atributo eventGuid</span><span class="sxs-lookup"><span data-stu-id="a669d-187">Every task must include the eventGuid attribute</span></span>
-   <span data-ttu-id="a669d-188">Los datos de plantilla a los que hace referencia el evento no pueden contener:</span><span class="sxs-lookup"><span data-stu-id="a669d-188">The template data that the event references cannot contain:</span></span>
    -   <span data-ttu-id="a669d-189">Elementos de datos que especifican los tipos de entrada Win: binary o Win: SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="a669d-189">Data items that specify the win:Binary or win:SYSTEMTIME input types</span></span>
    -   <span data-ttu-id="a669d-190">Estructuras</span><span class="sxs-lookup"><span data-stu-id="a669d-190">Structures</span></span>
    -   <span data-ttu-id="a669d-191">Matrices de tamaño variable; sin embargo, puede especificar matrices de longitud fija</span><span class="sxs-lookup"><span data-stu-id="a669d-191">Variable sized arrays; however, you can specify fixed length arrays</span></span>
    -   <span data-ttu-id="a669d-192">Los tipos de datos de cadena no pueden especificar el atributo de longitud</span><span class="sxs-lookup"><span data-stu-id="a669d-192">String data types cannot specify the length attribute</span></span>

<span data-ttu-id="a669d-193">Debe usar este argumento con el argumento **-Um**, **-CS**, **-CSS** o **-km** .</span><span class="sxs-lookup"><span data-stu-id="a669d-193">You must use this argument with the **-um**, **-cs**, **-css**, or **-km** argument</span></span>

</dd> <dt>

<span data-ttu-id="a669d-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p (** *prefijo* )</span><span class="sxs-lookup"><span data-stu-id="a669d-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-195">Use este argumento para reemplazar el prefijo predeterminado que el compilador utiliza para los nombres de macro y los nombres de método de registro.</span><span class="sxs-lookup"><span data-stu-id="a669d-195">Use this argument to override the default prefix that the compiler uses for the logging macro names and method names.</span></span> <span data-ttu-id="a669d-196">El prefijo predeterminado es "EventWrite".</span><span class="sxs-lookup"><span data-stu-id="a669d-196">The default prefix is "EventWrite".</span></span> <span data-ttu-id="a669d-197">La cadena distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a669d-197">The string is case-sensitive.</span></span>

<span data-ttu-id="a669d-198">Puede usar este argumento con el argumento **-Um**, **-CS**, **-CSS** o **-km** .</span><span class="sxs-lookup"><span data-stu-id="a669d-198">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P (** *prefijo* )</span><span class="sxs-lookup"><span data-stu-id="a669d-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-200">Use este argumento para quitar caracteres del principio del nombre simbólico que especificó para el evento.</span><span class="sxs-lookup"><span data-stu-id="a669d-200">Use this argument to remove characters from the beginning of the symbolic name that you specified for the event.</span></span> <span data-ttu-id="a669d-201">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a669d-201">The comparison is case-insensitive.</span></span> <span data-ttu-id="a669d-202">El compilador utiliza el nombre simbólico para formar los nombres de macro y los nombres de método de registro.</span><span class="sxs-lookup"><span data-stu-id="a669d-202">The compiler uses the symbolic name to form the logging macro names and method names.</span></span>

<span data-ttu-id="a669d-203">El nombre predeterminado de una macro de registro es EventWrite *SymbolName*, donde *SymbolName* es el nombre simbólico que especificó para el evento.</span><span class="sxs-lookup"><span data-stu-id="a669d-203">The default name for a logging macro is EventWrite *SymbolName*, where *SymbolName* is the symbolic name that you specified for the event.</span></span> <span data-ttu-id="a669d-204">Por ejemplo, si establece el atributo Symbol del evento en PrinterConnection, el nombre de la macro sería EventWritePrinterConnection.</span><span class="sxs-lookup"><span data-stu-id="a669d-204">For example, if you set the symbol attribute of the event to PrinterConnection, the macro name would be EventWritePrinterConnection.</span></span> <span data-ttu-id="a669d-205">Para quitar la impresora del nombre, use **-P** **Printer**, lo que da como resultado EventWriteConnection.</span><span class="sxs-lookup"><span data-stu-id="a669d-205">To remove Printer from the name, use **-P** **Printer**, which results in EventWriteConnection.</span></span>

<span data-ttu-id="a669d-206">Puede usar este argumento con el argumento **-Um**, **-CS**, **-CSS** o **-km** .</span><span class="sxs-lookup"><span data-stu-id="a669d-206">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-207"><span id="-um"></span><span id="-UM"></span>**-Um**</span><span class="sxs-lookup"><span data-stu-id="a669d-207"><span id="-um"></span><span id="-UM"></span>**-um**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-208">Utilice este argumento para que el compilador genere el código de modo de usuario que se usaría para registrar los eventos definidos en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a669d-208">Use this argument to have the compiler generate the user-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> </dl>

<span data-ttu-id="a669d-209">Para que el compilador genere código de registro, debe especificar el argumento **-Um**, **-CS**, **-CSS** o **-km** ; estos argumentos son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="a669d-209">To have the compiler generate logging code, you must specify the **-um**, **-cs**, **-css**, or **-km** argument; these arguments are mutually exclusive.</span></span>

<span data-ttu-id="a669d-210">Para especificar dónde se colocarán los archivos. h,. CS y. mof generados por el compilador, utilice el argumento **-h** .</span><span class="sxs-lookup"><span data-stu-id="a669d-210">To specify where to place the .h, .cs, and .mof files that the compiler generates, use the **-h** argument.</span></span> <span data-ttu-id="a669d-211">Si no se especifica el argumento **-h** , los archivos se colocan en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="a669d-211">If you do not specify the **-h** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="a669d-212">Para especificar dónde colocar el archivo. RC y los archivos binarios (que contienen los recursos de metadatos) que genera el compilador, utilice el argumento **-r** .</span><span class="sxs-lookup"><span data-stu-id="a669d-212">To specify where to place the .rc file and binary files (that contain the metadata resources) that the compiler generates, use the **-r** argument.</span></span> <span data-ttu-id="a669d-213">Si no se especifica el argumento **-r** , los archivos se colocan en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="a669d-213">If you do not specify the **-r** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="a669d-214">El compilador utiliza el nombre base del archivo de entrada como nombre base de los archivos que genera.</span><span class="sxs-lookup"><span data-stu-id="a669d-214">The compiler uses the base name of the input file as the base name of the files that it generates.</span></span> <span data-ttu-id="a669d-215">Para especificar un nombre base, use el argumento **-z** .</span><span class="sxs-lookup"><span data-stu-id="a669d-215">To specify a base name, use the **-z** argument.</span></span>

### <a name="arguments-specific-to-message-text-files"></a><span data-ttu-id="a669d-216">Argumentos específicos de los archivos de texto de mensaje</span><span class="sxs-lookup"><span data-stu-id="a669d-216">Arguments specific to message text files</span></span>

<dl> <dt>

<span data-ttu-id="a669d-217"><span id="-a"></span><span id="-A"></span>**-a**</span><span class="sxs-lookup"><span data-stu-id="a669d-217"><span id="-a"></span><span id="-A"></span>**-a**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-218">Utilice este argumento para especificar que el archivo de entrada de *nombre* de archivo contiene contenido en la página de códigos ANSI predeterminada de Windows (CP_ACP).</span><span class="sxs-lookup"><span data-stu-id="a669d-218">Use this argument to specify that the *filename* input file contains content in the system-default Windows ANSI code page (CP_ACP).</span></span> <span data-ttu-id="a669d-219">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a669d-219">This is the default.</span></span> <span data-ttu-id="a669d-220">Use **-u** para Unicode.</span><span class="sxs-lookup"><span data-stu-id="a669d-220">Use **-u** for Unicode.</span></span> <span data-ttu-id="a669d-221">Si el archivo de entrada contiene una marca BOM, este argumento se omitirá.</span><span class="sxs-lookup"><span data-stu-id="a669d-221">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-222"><span id="-A"></span><span id="-a"></span>**-A**</span><span class="sxs-lookup"><span data-stu-id="a669d-222"><span id="-A"></span><span id="-a"></span>**-A**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-223">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a669d-223">DEPRECATED.</span></span> <span data-ttu-id="a669d-224">Use este argumento para especificar que los mensajes del archivo output. bin deben ser ANSI.</span><span class="sxs-lookup"><span data-stu-id="a669d-224">Use this argument to specify that the messages in the output .bin file should be ANSI.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-225"><span id="-b"></span><span id="-B"></span>**-b**</span><span class="sxs-lookup"><span data-stu-id="a669d-225"><span id="-b"></span><span id="-B"></span>**-b**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-226">Use este argumento para que el compilador use el nombre base del archivo de entrada de *nombre* de archivo para los nombres de archivo. bin.</span><span class="sxs-lookup"><span data-stu-id="a669d-226">Use this argument to have the compiler use the base name of the *filename* input file for the .bin file names.</span></span> <span data-ttu-id="a669d-227">El valor predeterminado es usar "MSG".</span><span class="sxs-lookup"><span data-stu-id="a669d-227">The default is to use "MSG".</span></span>

</dd> <dt>

<span data-ttu-id="a669d-228"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="a669d-228"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-229">Use este argumento para usar valores decimales para las constantes Severity y Facility en el archivo de encabezado en lugar de valores hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="a669d-229">Use this argument to use decimal values for the Severity and Facility constants in the header file instead of hexadecimal values.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-230"><span id="-n"></span><span id="-N"></span>**-n**</span><span class="sxs-lookup"><span data-stu-id="a669d-230"><span id="-n"></span><span id="-N"></span>**-n**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-231">Utilice este argumento para especificar que los mensajes se cierren inmediatamente después del cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a669d-231">Use this argument to specify that messages terminate immediately after the message body.</span></span> <span data-ttu-id="a669d-232">El valor predeterminado es terminar el cuerpo del mensaje con un CR/LF.</span><span class="sxs-lookup"><span data-stu-id="a669d-232">The default is to terminate the message body with a CR/LF.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-233"><span id="-o"></span><span id="-O"></span>**-o**</span><span class="sxs-lookup"><span data-stu-id="a669d-233"><span id="-o"></span><span id="-O"></span>**-o**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-234">Use este argumento para que el compilador genere un archivo de encabezado OLE2 mediante definiciones **HRESULT** en lugar de códigos de estado.</span><span class="sxs-lookup"><span data-stu-id="a669d-234">Use this argument to have the compiler generate an OLE2 header file using **HRESULT** definitions instead of status codes.</span></span> <span data-ttu-id="a669d-235">El uso de códigos de estado es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a669d-235">Using status codes is the default.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-236"><span id="-u"></span><span id="-U"></span>**-u**</span><span class="sxs-lookup"><span data-stu-id="a669d-236"><span id="-u"></span><span id="-U"></span>**-u**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-237">Use este argumento para especificar que el archivo de entrada del *nombre* de archivo contiene contenido UTF-16LE.</span><span class="sxs-lookup"><span data-stu-id="a669d-237">Use this argument to specify that the *filename* input file contains UTF-16LE content.</span></span> <span data-ttu-id="a669d-238">El valor predeterminado es contenido ANSI.</span><span class="sxs-lookup"><span data-stu-id="a669d-238">The default is ANSI content.</span></span> <span data-ttu-id="a669d-239">Si el archivo de entrada contiene una marca BOM, este argumento se omitirá.</span><span class="sxs-lookup"><span data-stu-id="a669d-239">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-240"><span id="-U"></span><span id="-u"></span>**-U**</span><span class="sxs-lookup"><span data-stu-id="a669d-240"><span id="-U"></span><span id="-u"></span>**-U**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-241">Use este argumento para especificar que los mensajes del archivo output. bin deben ser Unicode.</span><span class="sxs-lookup"><span data-stu-id="a669d-241">Use this argument to specify that the messages in the output .bin file should be Unicode.</span></span> <span data-ttu-id="a669d-242">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a669d-242">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-243"><span id="-v"></span><span id="-V"></span>**-v**</span><span class="sxs-lookup"><span data-stu-id="a669d-243"><span id="-v"></span><span id="-V"></span>**-v**</span></span>
</dt> <dd>

<span data-ttu-id="a669d-244">Use este argumento para generar resultados detallados.</span><span class="sxs-lookup"><span data-stu-id="a669d-244">Use this argument to generate verbose output.</span></span>

</dd> <dt>

<span data-ttu-id="a669d-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*</span><span class="sxs-lookup"><span data-stu-id="a669d-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*</span></span>
</dt> <dd>

<span data-ttu-id="a669d-246">Use este argumento para especificar la carpeta en la que desea que el compilador Coloque el archivo de inclusión. dbg de C.</span><span class="sxs-lookup"><span data-stu-id="a669d-246">Use this argument to specify the folder into which you want the compiler to place the .dbg C include file.</span></span> <span data-ttu-id="a669d-247">El archivo. dbg asigna los identificadores de mensaje a sus nombres simbólicos.</span><span class="sxs-lookup"><span data-stu-id="a669d-247">The .dbg file maps message IDs to their symbolic names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a669d-248">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a669d-248">Remarks</span></span>

<span data-ttu-id="a669d-249">Los argumentos **-a** y **-MOF** están desusados y se quitarán en el futuro.</span><span class="sxs-lookup"><span data-stu-id="a669d-249">The **-A** and **-mof** arguments are deprecated and will be removed in the future.</span></span>

<span data-ttu-id="a669d-250">El compilador acepta como entrada un archivo de manifiesto (. Man) o un archivo de texto de mensaje (. MC) y genera los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="a669d-250">The compiler accepts as input a manifest (.man) file or a message text (.mc) file and generates the following files:</span></span>

-   <span data-ttu-id="a669d-251">*nombre de archivo*. h</span><span class="sxs-lookup"><span data-stu-id="a669d-251">*filename*.h</span></span>

    <span data-ttu-id="a669d-252">Un archivo de encabezado de C/C++ que contiene los descriptores de eventos, el GUID del proveedor y los nombres de símbolos a los que se hace referencia en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a669d-252">A C/C++ header file that contains the event descriptors, provider GUID, and symbol names that you reference in your application.</span></span>

-   <span data-ttu-id="a669d-253">*nombre de archivo* TEMP. bin</span><span class="sxs-lookup"><span data-stu-id="a669d-253">*filename* TEMP.bin</span></span>

    <span data-ttu-id="a669d-254">Un archivo de recursos binario que contiene los metadatos del proveedor y del evento.</span><span class="sxs-lookup"><span data-stu-id="a669d-254">A binary resource file that contains the provider and event metadata.</span></span> <span data-ttu-id="a669d-255">Este es el recurso de plantilla, que se indica mediante el sufijo temporal del nombre base del archivo.</span><span class="sxs-lookup"><span data-stu-id="a669d-255">This is the template resource, which is signified by the TEMP suffix of the base name of the file.</span></span>

-   <span data-ttu-id="a669d-256">Msg00001. bin</span><span class="sxs-lookup"><span data-stu-id="a669d-256">Msg00001.bin</span></span>

    <span data-ttu-id="a669d-257">Un archivo de recursos binario para cada idioma que especifique (por ejemplo, si el manifiesto contiene cadenas de mensaje en-US y fr-FR, el compilador generará Msg00001. bin y Msg00002. bin).</span><span class="sxs-lookup"><span data-stu-id="a669d-257">A binary resource file for each language that you specify (for example, if your manifest contains message strings in en-US and fr-FR, the compiler would generate Msg00001.bin and Msg00002.bin).</span></span>

-   <span data-ttu-id="a669d-258">*nombre de archivo*. RC</span><span class="sxs-lookup"><span data-stu-id="a669d-258">*filename*.rc</span></span>

    <span data-ttu-id="a669d-259">Un script del compilador de recursos que contiene las instrucciones para incluir cada archivo. bin como un recurso.</span><span class="sxs-lookup"><span data-stu-id="a669d-259">A resource compiler script that contains the statements to include each .bin file as a resource.</span></span>

<span data-ttu-id="a669d-260">En el caso de los argumentos que toman una ruta de acceso, la ruta de acceso puede ser una ruta de acceso absoluta, relativa o UNC, y puede contener variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="a669d-260">For arguments that take a path, the path can be an absolute, relative, or UNC path and it can contain environment variables.</span></span>

<span data-ttu-id="a669d-261">**Antes de la versión de MC 1.12.7051:** El compilador no permite rutas de acceso relativas o variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="a669d-261">**Prior to MC version 1.12.7051:** The compiler does not allow relative paths or environment variables.</span></span>

<span data-ttu-id="a669d-262">El Windows SDK incluye el compilador (mc.exe) en la \\ carpeta bin.</span><span class="sxs-lookup"><span data-stu-id="a669d-262">The Windows SDK includes the compiler (mc.exe) in the \\Bin folder.</span></span>

## <a name="examples"></a><span data-ttu-id="a669d-263">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a669d-263">Examples</span></span>

<span data-ttu-id="a669d-264">En el ejemplo siguiente se compila un manifiesto con los valores predeterminados del compilador.</span><span class="sxs-lookup"><span data-stu-id="a669d-264">The following example compiles a manifest using the compiler defaults.</span></span>

``` syntax
mc spooler.man
```

<span data-ttu-id="a669d-265">En el ejemplo siguiente se compila el manifiesto y se colocan los archivos de encabezado y de recursos en las carpetas especificadas.</span><span class="sxs-lookup"><span data-stu-id="a669d-265">The following example compiles the manifest and places the header and resource files in the specified folders.</span></span>

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a><span data-ttu-id="a669d-266">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a669d-266">Requirements</span></span>

| <span data-ttu-id="a669d-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="a669d-267">Requirement</span></span> | <span data-ttu-id="a669d-268">Value</span><span class="sxs-lookup"><span data-stu-id="a669d-268">Value</span></span> |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="a669d-269">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a669d-269">Minimum supported client</span></span> | <span data-ttu-id="a669d-270">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a669d-270">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="a669d-271">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a669d-271">Minimum supported server</span></span> | <span data-ttu-id="a669d-272">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a669d-272">Windows 2000 Server \[desktop apps only\]</span></span>       |
