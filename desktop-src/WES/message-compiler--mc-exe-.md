---
title: Compilador de mensajes (MC.exe)
description: Se usa para compilar manifiestos de instrumentación y archivos de texto de mensaje.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Registro de eventos del compilador de mensajes (MC.exe)
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 1ba213a1d7047b61ba7ba875adf9c281726eaae123ae018aea9920050b201644
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470945"
---
# <a name="message-compiler-mcexe"></a>Compilador de mensajes (MC.exe)

Se usa para compilar manifiestos de instrumentación y archivos de texto de mensaje. El compilador genera los archivos de recursos de mensaje a los que se vincula la aplicación.

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [Argumentos comunes tanto a los archivos de texto de mensaje como a los archivos de manifiesto](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [Argumentos específicos de los archivos de manifiesto](#arguments-specific-to-manifest-files)
-   [Argumentos específicos de la generación de código que el proveedor usaría para registrar eventos](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [Argumentos específicos de los archivos de texto del mensaje](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>Argumentos comunes tanto a los archivos de texto de mensaje como a los archivos de manifiesto

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Muestra la información de uso del compilador de mensajes.

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

Use este argumento para que el compilador establezca el bit del cliente (bit 28) en todos los iD de mensaje. Para obtener información sobre el bit del cliente, consulte winerror.h.

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**-cp** *encoding*
</dt> <dd>

Use este argumento para especificar la codificación de caracteres utilizada para todos los archivos de texto generados. Los nombres válidos incluyen "ansi" (valor predeterminado), "utf-8" y "utf-16". Las codificaciones Unicode agregarán una marca de orden de bytes.

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *extensión*
</dt> <dd>

Use este argumento para especificar la extensión que se usará para el archivo de encabezado. Puede especificar hasta una extensión de tres caracteres, sin incluir el punto. El valor predeterminado es .h.

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h** *ruta de acceso*
</dt> <dd>

Use este argumento para especificar la carpeta en la que desea que el compilador coloque el archivo de encabezado generado. El valor predeterminado es el directorio actual.

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *length*
</dt> <dd>

Use este argumento para que el compilador genere una advertencia si el mensaje supera los *caracteres de* longitud.

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*
</dt> <dd>

Use este argumento para especificar la carpeta en la que desea que el compilador coloque el script del compilador de recursos generado (archivo .rc) y los archivos .bin generados (recursos binarios) que incluye el script del compilador de recursos. El valor predeterminado es el directorio actual.

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *name*
</dt> <dd>

Use este argumento para invalidar el nombre base predeterminado que usa el compilador para los archivos que genera. El valor predeterminado es usar el nombre base del archivo de entrada *de nombre de* archivo.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Nombre*
</dt> <dd>

Archivo de manifiesto de instrumentación o archivo de texto de mensaje. El archivo debe existir en el directorio actual. Puede especificar un archivo de manifiesto, un archivo de texto de mensaje o ambos. El nombre de archivo debe incluir la extensión. La convención es usar una extensión .man para los archivos de manifiesto y una extensión .mc para los archivos de texto del mensaje.

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>Argumentos específicos de los archivos de manifiesto

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s ruta de** *acceso*
</dt> <dd>

Use este argumento para crear una línea base de la instrumentación. Especifique la ruta de acceso a la carpeta que contiene los archivos de manifiesto de línea base. En versiones posteriores, usaría el **argumento -t** para comprobar el nuevo manifiesto en la línea de base en busca de problemas de compatibilidad.

**Antes de mc versión 1.12.7051:** No disponible

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t ruta de** *acceso*
</dt> <dd>

Use este argumento cuando cree una nueva versión del manifiesto y desee comprobar la compatibilidad de la aplicación con la línea base que creó con **el argumento -s.** La ruta de acceso debe apuntar a la carpeta que contiene . Archivos BIN creados por la operación de línea base (vea **el modificador -s).**

**Antes de mc versión 1.12.7051:** No disponible

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w ruta de** *acceso*
</dt> <dd>

El compilador omite este argumento y valida automáticamente el manifiesto.

**Antes de mc versión 1.12.7051:** Use este argumento para especificar la carpeta que contiene el archivo de esquema Eventman.xsd, que el compilador usa para validar el manifiesto. El SDK Windows incluye el archivo de esquema Eventman.xsd en la \\ carpeta Include. Si no especifica este argumento, el compilador no valida el manifiesto.

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W ruta de** *acceso*
</dt> <dd>

El compilador omite este argumento.

**Antes de mc versión 1.12.7051:** Use este argumento para especificar la carpeta que contiene el Winmeta.xml archivo. El Winmeta.xml contiene los tipos de entrada y salida reconocidos, así como los canales predefinidos, los niveles y los códigos de operación. El SDK Windows incluye el Winmeta.xml en la \\ carpeta Include.

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>Argumentos específicos de la generación de código que el proveedor usaría para registrar eventos

Puede usar los siguientes argumentos del compilador para generar código en modo kernel o en modo de usuario que puede usar para registrar eventos. También puede solicitar que el compilador genere código para admitir la escritura de eventos en equipos antes de Windows Vista. Si la aplicación está escrita en C#, el compilador puede generar una clase de C# que puede usar para registrar eventos. Estos argumentos están disponibles a partir de la versión 1.12.7051 de MC que se incluye con la versión Windows 7 del SDK de Windows.

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-co**
</dt> <dd>

Use este argumento para que el servicio de registro llame a la función definida por el usuario para cada evento que registre (se llama a la función después de que se haya registrado el evento). La función definida por el usuario debe tener la firma siguiente.


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



También debe incluir la siguiente directiva en el código.

`#define MCGEN_CALLOUT pFnUserFunction`

Debe mantener la implementación lo más corta posible para evitar problemas de registro. El servicio ya no registrará los eventos hasta que se devuelva la función.

Puede usar este argumento con el **argumento -km** o **-um.**

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs (espacio de** *nombres)*
</dt> <dd>

Use este argumento para que el compilador genere una clase de C# basada en la clase [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) de .NET 3.5.

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css (espacio de nombres)** 
</dt> <dd>

Use este argumento para que el compilador genere una clase estática de C# basada en la clase [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) de .NET 3.5.

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-km**
</dt> <dd>

Use este argumento para que el compilador genere el código en modo kernel que usaría para registrar los eventos definidos en el manifiesto.

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-mof**
</dt> <dd>

Obsoleto. Use este argumento para que el compilador genere código que pueda usar para registrar eventos en equipos antes de Windows Vista. Esta opción también crea un archivo MOF que contiene las clases MOF para cada evento definido en el manifiesto. Para registrar las clases en el archivo MOF para que los consumidores puedan descodificar los eventos, use el compilador MOF (Mofcomp.exe). Para obtener más información sobre el uso del compilador MOF, [vea Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).

Para usar este modificador, debe cumplir las restricciones siguientes:

-   Cada definición de evento debe incluir los atributos task y opcode
-   Cada tarea debe incluir el atributo eventGuid
-   Los datos de plantilla a los que hace referencia el evento no pueden contener:
    -   Elementos de datos que especifican los tipos de entrada win:Binary o win:SYSTEMTIME
    -   Estructuras
    -   Matrices de tamaño variable; sin embargo, puede especificar matrices de longitud fija
    -   Los tipos de datos de cadena no pueden especificar el atributo length

Debe usar este argumento con el **argumento -um**, **-cs**, **-css** o **-km**

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefijo*
</dt> <dd>

Use este argumento para invalidar el prefijo predeterminado que el compilador usa para los nombres de macro de registro y los nombres de método. El prefijo predeterminado es "EventWrite". La cadena distingue mayúsculas de minúsculas.

Puede usar este argumento con el **argumento -um**, **-cs,** **-css** o **-km.**

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**Prefijo -P** 
</dt> <dd>

Use este argumento para quitar caracteres del principio del nombre simbólico que especificó para el evento. La comparación distingue entre mayúsculas y minúsculas. El compilador usa el nombre simbólico para formar los nombres de macro de registro y los nombres de método.

El nombre predeterminado de una macro de registro es EventWrite *SymbolName*, donde *SymbolName* es el nombre simbólico que especificó para el evento. Por ejemplo, si establece el atributo de símbolo del evento en PrinterConnection, el nombre de la macro sería EventWritePrinterConnection. Para quitar Printer del nombre, use **-P** **Printer**, lo que da como resultado EventWriteConnection.

Puede usar este argumento con el **argumento -um**, **-cs**, **-css** o **-km.**

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-um**
</dt> <dd>

Use este argumento para que el compilador genere el código en modo de usuario que usaría para registrar los eventos definidos en el manifiesto.

</dd> </dl>

Para que el compilador genere código de registro, debe especificar el **argumento -um**, **-cs**, **-css** o **-km;** estos argumentos son mutuamente excluyentes.

Para especificar dónde colocar los archivos .h, .cs y .mof que genera el compilador, use **el argumento -h.** Si no especifica el **argumento -h,** los archivos se colocan en la carpeta actual.

Para especificar dónde colocar el archivo .rc y los archivos binarios (que contienen los recursos de metadatos) que genera el compilador, use **el argumento -r.** Si no especifica el **argumento -r,** los archivos se colocan en la carpeta actual.

El compilador usa el nombre base del archivo de entrada como nombre base de los archivos que genera. Para especificar un nombre base, use el **argumento -z.**

### <a name="arguments-specific-to-message-text-files"></a>Argumentos específicos de los archivos de texto de mensaje

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

Use este argumento para especificar que el archivo de entrada de nombre *de* archivo contiene contenido en la página de códigos ANSI Windows predeterminada del sistema (CP_ACP). Este es el valor predeterminado. Use **-u** para Unicode. Si el archivo de entrada contiene una MARCA BOM, este argumento se omitirá.

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

Obsoleto. Use este argumento para especificar que los mensajes del archivo .bin de salida deben ser ANSI.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

Use este argumento para que el compilador use el nombre base del archivo de entrada de nombre *de* archivo para los nombres de archivo .bin. El valor predeterminado es usar "MSG".

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Use este argumento para usar valores decimales para las constantes Severity y Facility en el archivo de encabezado en lugar de valores hexadecimales.

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

Use este argumento para especificar que los mensajes finalicen inmediatamente después del cuerpo del mensaje. El valor predeterminado es finalizar el cuerpo del mensaje con un CR/LF.

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

Use este argumento para que el compilador genere un archivo de encabezado OLE2 mediante **definiciones HRESULT** en lugar de códigos de estado. El uso de códigos de estado es el valor predeterminado.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

Use este argumento para especificar que el archivo *de entrada de nombre de* archivo contiene contenido UTF-16LE. El valor predeterminado es contenido ANSI. Si el archivo de entrada contiene una MARCA BOM, este argumento se omitirá.

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

Use este argumento para especificar que los mensajes del archivo .bin de salida deben ser Unicode. Este es el valor predeterminado.

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

Use este argumento para generar una salida detallada.

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**-x** *ruta de acceso*
</dt> <dd>

Use este argumento para especificar la carpeta en la que desea que el compilador coloque el archivo de incluir C .dbg. El archivo .dbg asigna los ID de mensaje a sus nombres simbólicos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los **argumentos -A** **y -mof** están en desuso y se quitarán en el futuro.

El compilador acepta como entrada un archivo de manifiesto (.man) o un archivo de texto de mensaje (.mc) y genera los siguientes archivos:

-   *filename*.h

    Un archivo de encabezado de C/C++ que contiene los descriptores de eventos, el GUID del proveedor y los nombres de símbolos a los que se hace referencia en la aplicación.

-   *filename* TEMP.bin

    Un archivo de recursos binario que contiene los metadatos del proveedor y del evento. Este es el recurso de plantilla, que se indica mediante el sufijo TEMP del nombre base del archivo.

-   Msg00001.bin

    Un archivo de recursos binario para cada lenguaje que especifique (por ejemplo, si el manifiesto contiene cadenas de mensaje en en-US y fr-FR, el compilador generaría Msg00001.bin y Msg00002.bin).

-   *filename*.rc

    Script del compilador de recursos que contiene las instrucciones para incluir cada archivo .bin como un recurso.

En el caso de los argumentos que toman una ruta de acceso, la ruta de acceso puede ser una ruta de acceso absoluta, relativa o UNC y puede contener variables de entorno.

**Antes de MC, versión 1.12.7051:** El compilador no permite rutas de acceso relativas ni variables de entorno.

El SDK Windows incluye el compilador (mc.exe) en la \\ carpeta Bin.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se compila un manifiesto con los valores predeterminados del compilador.

``` syntax
mc spooler.man
```

En el ejemplo siguiente se compila el manifiesto y se coloca el encabezado y los archivos de recursos en las carpetas especificadas.

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------------|
| Cliente mínimo compatible | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional |
| Servidor mínimo compatible | \[Solo aplicaciones de escritorio\] de Windows 2000 Server       |
