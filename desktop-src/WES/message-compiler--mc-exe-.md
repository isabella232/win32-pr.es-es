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
# <a name="message-compiler-mcexe"></a>Compilador de mensajes (MC.exe)

Se utiliza para compilar manifiestos de instrumentación y archivos de texto de mensaje. El compilador genera los archivos de recursos de mensajes a los que se vincula la aplicación.

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [Argumentos comunes para archivos de texto de mensaje y archivos de manifiesto](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [Argumentos específicos de los archivos de manifiesto](#arguments-specific-to-manifest-files)
-   [Argumentos específicos de la generación de código que el proveedor usaría para registrar eventos](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [Argumentos específicos de los archivos de texto de mensaje](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>Argumentos comunes para archivos de texto de mensaje y archivos de manifiesto

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Muestra la información de uso del compilador de mensajes.

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

Use este argumento para que el compilador establezca el bit de cliente (bit 28) en todos los identificadores de mensaje. Para obtener información sobre el bit de cliente, consulte Winerror. h.

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**-codificación de CP** 
</dt> <dd>

Use este argumento para especificar la codificación de caracteres utilizada para todos los archivos de texto generados. Los nombres válidos son "ANSI" (predeterminado), "UTF-8" y "UTF-16". Las codificaciones Unicode agregarán una marca de orden de bytes.

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span>*extensión* **-e**
</dt> <dd>

Use este argumento para especificar la extensión que se va a usar para el archivo de encabezado. Puede especificar hasta una extensión de tres caracteres, sin incluir el punto. El valor predeterminado es. h.

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h ruta de** *acceso*
</dt> <dd>

Use este argumento para especificar la carpeta en la que desea que el compilador Coloque el archivo de encabezado generado. El valor predeterminado es el directorio actual.

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *longitud*
</dt> <dd>

Utilice este argumento para que el compilador genere una advertencia si el mensaje any supera los caracteres de *longitud* .

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r ruta de** *acceso*
</dt> <dd>

Use este argumento para especificar la carpeta en la que desea que el compilador Coloque el script del compilador de recursos generado (archivo. RC) y los archivos. bin generados (recursos binarios) que incluye el script del compilador de recursos. El valor predeterminado es el directorio actual.

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *nombre*
</dt> <dd>

Utilice este argumento para reemplazar el nombre base predeterminado que el compilador utiliza para los archivos que genera. El valor predeterminado es usar el nombre base del archivo de entrada de *nombre* de archivo.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*extensión*
</dt> <dd>

Archivo de manifiesto de instrumentación o archivo de texto de mensaje. El archivo debe existir en el directorio actual. Puede especificar un archivo de manifiesto, un archivo de texto de mensaje o ambos. El nombre de archivo debe incluir la extensión. La Convención es usar una extensión. Man para los archivos de manifiesto y una extensión. MC para los archivos de texto del mensaje.

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>Argumentos específicos de los archivos de manifiesto

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s ruta de** *acceso*
</dt> <dd>

Use este argumento para crear una línea base de la instrumentación. Especifique la ruta de acceso a la carpeta que contiene los archivos de manifiesto de línea de base. En las versiones posteriores, usaría el argumento **-t** para comprobar el nuevo manifiesto en la línea base para los problemas de compatibilidad.

**Antes de la versión de MC 1.12.7051:** No disponible

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t ruta de** *acceso*
</dt> <dd>

Use este argumento al crear una nueva versión del manifiesto y desea comprobar la compatibilidad de las aplicaciones con la línea de base que creó con el argumento **-s** . La ruta de acceso debe apuntar a la carpeta que contiene. Archivos BIN creados por la operación de línea de base (vea el conmutador **-s** ).

**Antes de la versión de MC 1.12.7051:** No disponible

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w ruta de** *acceso*
</dt> <dd>

El compilador omite este argumento y valida automáticamente el manifiesto.

**Antes de la versión de MC 1.12.7051:** Use este argumento para especificar la carpeta que contiene el archivo de esquema Event-. xsd, que el compilador usa para validar el manifiesto. El Windows SDK incluye el archivo de esquema Event-. xsd en la \\ carpeta include. Si no especifica este argumento, el compilador no valida el manifiesto.

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W ruta de** *acceso*
</dt> <dd>

El compilador omite este argumento.

**Antes de la versión de MC 1.12.7051:** Use este argumento para especificar la carpeta que contiene el archivo de Winmeta.xml. El archivo Winmeta.xml contiene los tipos de entrada y salida reconocidos, así como los canales, niveles y códigos de acceso predefinidos. El Windows SDK incluye el archivo de Winmeta.xml en la \\ carpeta de inclusión.

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>Argumentos específicos de la generación de código que el proveedor usaría para registrar eventos

Puede usar los siguientes argumentos del compilador para generar código en modo kernel o en modo de usuario que puede usar para registrar eventos. También puede solicitar que el compilador genere código para admitir la escritura de eventos en equipos anteriores a Windows Vista. Si la aplicación está escrita en C#, el compilador puede generar una clase de C# que se puede usar para registrar eventos. Estos argumentos están disponibles a partir de la versión de MC 1.12.7051 que se incluye con la versión de Windows 7 del SDK de Windows.

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-Co**
</dt> <dd>

Use este argumento para que el servicio de registro llame a la función definida por el usuario para cada evento que registre (se llama a la función una vez que se ha registrado el evento). La función definida por el usuario debe tener la siguiente firma.


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

Debe mantener la implementación lo más corta posible para evitar problemas de registro. el servicio no registrará ya los eventos hasta que vuelva la función.

Puede usar este argumento con el argumento **-km** o **-Um** .

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-espacio de** *nombres* CS
</dt> <dd>

Use este argumento para que el compilador genere una clase de C# basada en la clase [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) de .net 3,5.

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-espacio de** *nombres* CSS
</dt> <dd>

Use este argumento para que el compilador genere una clase de C# estática basada en la clase [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) de .net 3,5.

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-km**
</dt> <dd>

Utilice este argumento para que el compilador genere el código en modo kernel que se usaría para registrar los eventos definidos en el manifiesto.

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-MOF**
</dt> <dd>

En desuso. Use este argumento para que el compilador genere código que pueda usar para registrar eventos en equipos anteriores a Windows Vista. Esta opción también crea un archivo MOF que contiene las clases MOF para cada evento definido en el manifiesto. Para registrar las clases en el archivo MOF para que los consumidores puedan descodificar los eventos, utilice el compilador MOF (Mofcomp.exe). Para obtener información detallada sobre el uso del compilador MOF, vea [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).

Para usar este modificador, debe cumplir las restricciones siguientes:

-   Cada definición de evento debe incluir los atributos Task y OpCode.
-   Cada tarea debe incluir el atributo eventGuid
-   Los datos de plantilla a los que hace referencia el evento no pueden contener:
    -   Elementos de datos que especifican los tipos de entrada Win: binary o Win: SYSTEMTIME
    -   Estructuras
    -   Matrices de tamaño variable; sin embargo, puede especificar matrices de longitud fija
    -   Los tipos de datos de cadena no pueden especificar el atributo de longitud

Debe usar este argumento con el argumento **-Um**, **-CS**, **-CSS** o **-km** .

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p (** *prefijo* )
</dt> <dd>

Use este argumento para reemplazar el prefijo predeterminado que el compilador utiliza para los nombres de macro y los nombres de método de registro. El prefijo predeterminado es "EventWrite". La cadena distingue mayúsculas de minúsculas.

Puede usar este argumento con el argumento **-Um**, **-CS**, **-CSS** o **-km** .

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P (** *prefijo* )
</dt> <dd>

Use este argumento para quitar caracteres del principio del nombre simbólico que especificó para el evento. La comparación distingue entre mayúsculas y minúsculas. El compilador utiliza el nombre simbólico para formar los nombres de macro y los nombres de método de registro.

El nombre predeterminado de una macro de registro es EventWrite *SymbolName*, donde *SymbolName* es el nombre simbólico que especificó para el evento. Por ejemplo, si establece el atributo Symbol del evento en PrinterConnection, el nombre de la macro sería EventWritePrinterConnection. Para quitar la impresora del nombre, use **-P** **Printer**, lo que da como resultado EventWriteConnection.

Puede usar este argumento con el argumento **-Um**, **-CS**, **-CSS** o **-km** .

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-Um**
</dt> <dd>

Utilice este argumento para que el compilador genere el código de modo de usuario que se usaría para registrar los eventos definidos en el manifiesto.

</dd> </dl>

Para que el compilador genere código de registro, debe especificar el argumento **-Um**, **-CS**, **-CSS** o **-km** ; estos argumentos son mutuamente excluyentes.

Para especificar dónde se colocarán los archivos. h,. CS y. mof generados por el compilador, utilice el argumento **-h** . Si no se especifica el argumento **-h** , los archivos se colocan en la carpeta actual.

Para especificar dónde colocar el archivo. RC y los archivos binarios (que contienen los recursos de metadatos) que genera el compilador, utilice el argumento **-r** . Si no se especifica el argumento **-r** , los archivos se colocan en la carpeta actual.

El compilador utiliza el nombre base del archivo de entrada como nombre base de los archivos que genera. Para especificar un nombre base, use el argumento **-z** .

### <a name="arguments-specific-to-message-text-files"></a>Argumentos específicos de los archivos de texto de mensaje

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

Utilice este argumento para especificar que el archivo de entrada de *nombre* de archivo contiene contenido en la página de códigos ANSI predeterminada de Windows (CP_ACP). Este es el valor predeterminado. Use **-u** para Unicode. Si el archivo de entrada contiene una marca BOM, este argumento se omitirá.

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

En desuso. Use este argumento para especificar que los mensajes del archivo output. bin deben ser ANSI.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

Use este argumento para que el compilador use el nombre base del archivo de entrada de *nombre* de archivo para los nombres de archivo. bin. El valor predeterminado es usar "MSG".

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Use este argumento para usar valores decimales para las constantes Severity y Facility en el archivo de encabezado en lugar de valores hexadecimales.

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

Utilice este argumento para especificar que los mensajes se cierren inmediatamente después del cuerpo del mensaje. El valor predeterminado es terminar el cuerpo del mensaje con un CR/LF.

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

Use este argumento para que el compilador genere un archivo de encabezado OLE2 mediante definiciones **HRESULT** en lugar de códigos de estado. El uso de códigos de estado es el valor predeterminado.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

Use este argumento para especificar que el archivo de entrada del *nombre* de archivo contiene contenido UTF-16LE. El valor predeterminado es contenido ANSI. Si el archivo de entrada contiene una marca BOM, este argumento se omitirá.

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

Use este argumento para especificar que los mensajes del archivo output. bin deben ser Unicode. Este es el valor predeterminado.

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

Use este argumento para generar resultados detallados.

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*
</dt> <dd>

Use este argumento para especificar la carpeta en la que desea que el compilador Coloque el archivo de inclusión. dbg de C. El archivo. dbg asigna los identificadores de mensaje a sus nombres simbólicos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los argumentos **-a** y **-MOF** están desusados y se quitarán en el futuro.

El compilador acepta como entrada un archivo de manifiesto (. Man) o un archivo de texto de mensaje (. MC) y genera los siguientes archivos:

-   *nombre de archivo*. h

    Un archivo de encabezado de C/C++ que contiene los descriptores de eventos, el GUID del proveedor y los nombres de símbolos a los que se hace referencia en la aplicación.

-   *nombre de archivo* TEMP. bin

    Un archivo de recursos binario que contiene los metadatos del proveedor y del evento. Este es el recurso de plantilla, que se indica mediante el sufijo temporal del nombre base del archivo.

-   Msg00001. bin

    Un archivo de recursos binario para cada idioma que especifique (por ejemplo, si el manifiesto contiene cadenas de mensaje en-US y fr-FR, el compilador generará Msg00001. bin y Msg00002. bin).

-   *nombre de archivo*. RC

    Un script del compilador de recursos que contiene las instrucciones para incluir cada archivo. bin como un recurso.

En el caso de los argumentos que toman una ruta de acceso, la ruta de acceso puede ser una ruta de acceso absoluta, relativa o UNC, y puede contener variables de entorno.

**Antes de la versión de MC 1.12.7051:** El compilador no permite rutas de acceso relativas o variables de entorno.

El Windows SDK incluye el compilador (mc.exe) en la \\ carpeta bin.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se compila un manifiesto con los valores predeterminados del compilador.

``` syntax
mc spooler.man
```

En el ejemplo siguiente se compila el manifiesto y se colocan los archivos de encabezado y de recursos en las carpetas especificadas.

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------------|
| Cliente mínimo compatible | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional |
| Servidor mínimo compatible | \[Solo aplicaciones de escritorio\] de Windows 2000 Server       |
