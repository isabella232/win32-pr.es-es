---
description: La clase CommandLineEventConsumer inicia un proceso arbitrario en el sistema local cuando se le entrega un evento.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: CommandLineEventConsumer (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: dce5100ba83a04ef2f6252421ec49068e84730141830e7b01f177c81bbac21b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319594"
---
# <a name="commandlineeventconsumer-class"></a>CommandLineEventConsumer (clase)

La **clase CommandLineEventConsumer** inicia un proceso arbitrario en el sistema local cuando se le entrega un evento. Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener más información, vea [Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

> [!Note]  
> Al usar la **clase CommandLineEventConsumer,** proteja el archivo ejecutable que desea iniciar. Si el ejecutable no está en una ubicación segura o está protegido con una lista de control de acceso seguro (ACL), un usuario no autorizado puede reemplazar el ejecutable por un ejecutable malintencionado. Para obtener más información sobre las ACL, visite la sección Seguridad del Kit de desarrollo de software (SDK) de Microsoft Windows y vea Creación de un descriptor de seguridad [para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a>Miembros

La **clase CommandLineEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CommandLineEventConsumer** tiene estas propiedades.

<dl> <dt>

**CommandLineTemplate**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Plantilla de cadena estándar que especifica el proceso que se va a iniciar. Esta propiedad puede ser **NULL** y la **propiedad ExecutablePath** se usa como línea de comandos.

</dd> <dt>

**CreateNewConsole**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se usa. Si se asigna un valor a esta propiedad, se genera un mensaje de seguimiento. Para obtener más información, vea [Seguimiento de la actividad WMI](tracing-wmi-activity.md).

</dd> <dt>

**CreateNewProcessGroup**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True,** el nuevo proceso es el proceso raíz de un nuevo grupo de procesos. El grupo de procesos incluye todos los procesos que son descendientes de este proceso raíz. El identificador de proceso del nuevo grupo de procesos es el mismo que este identificador de proceso. El método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) usa grupos de procesos para habilitar el envío de una señal CTRL+C o CTRL+BREAK a un grupo de procesos de consola.

</dd> <dt>

**CreateSeparateWowVdm**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True,** el nuevo proceso se ejecuta en una máquina virtual privada de DOS (VDM). Esto solo es válido cuando se inicia una aplicación que se ejecuta en un sistema operativo de 16 Windows bits. Si se establece en **False,** todas las aplicaciones que se ejecutan en un sistema operativo de 16 Windows se ejecutan como subprocesos en un único VDM compartido. Para obtener más información, vea la sección Comentarios de este tema.

</dd> <dt>

**CreateSharedWowVdm**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True,** [**el método CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ejecuta el nuevo proceso en la máquina virtual de DOS (VDM) compartida. Esta propiedad puede invalidar el modificador DefaultSeparateVDM en la Windows de Win.ini si se establece en **True.** Para obtener más información, vea la sección Comentarios de este tema.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, según el sistema operativo. Para obtener más información, vea [Enlazar un filtro de eventos con](binding-an-event-filter-with-a-logical-consumer.md) un consumidor lógico y Supervisar y Responder a eventos con [consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**DesktopName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se usa. Si se asigna un valor a esta propiedad, se genera un mensaje de seguimiento. Para obtener más información, vea [Seguimiento de la actividad WMI](tracing-wmi-activity.md).

</dd> <dt>

**ExecutablePath _s**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Módulo que se ejecutará. La cadena puede especificar la ruta de acceso completa y el nombre de archivo del módulo que se va a ejecutar, o bien puede especificar un nombre parcial. Si se especifica un nombre parcial, se supone que la unidad actual y el directorio actual.

La **propiedad ExecutablePath** puede ser **NULL.** En ese caso, el nombre del módulo debe ser el primer token delimitado por espacios en blanco en el valor de la propiedad **CommandLineTemplate.** Si usa un nombre de archivo largo que contiene un espacio, use cadenas entre comillas para indicar dónde finaliza el nombre de archivo y los argumentos comienzan a aclarar el nombre de archivo.

> [!Note]  
> Dado que la propiedad **CommandLineTemplate** puede ser una plantilla en la que una variable proporciona el módulo que se va a ejecutar, una propiedad **ExecutablePath** **NULL** permite ejecutar el módulo especificado en el parámetro y, a continuación, está fuera de su control. Establezca siempre la **propiedad ExecutablePath** en el registro **CommandLineEventConsumer** para incluir el ejecutable necesario, lo que evita sobrescribir los parámetros de eventos. Si debe usar una plantilla y una variable para especificar el módulo que se va a ejecutar, tenga cuidado con quién se concede el privilegio de escritura completo en el espacio de nombres .

 

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el texto inicial y los colores de fondo si se crea una nueva ventana de consola en una aplicación de consola.

</dd> <dt>

**FillAttributes**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Texto inicial y colores de fondo, si se crea una nueva ventana de consola en una aplicación de consola. Esta propiedad se omite en una aplicación gui. El valor puede ser cualquier combinación de los valores siguientes.

<dt>

1 (0x1)
</dt> <dd>

primer plano azul

</dd> <dt>

2 (0x2)
</dt> <dd>

primer plano verde

</dd> <dt>

4 (0x4)
</dt> <dd>

primer plano rojo

</dd> <dt>

8 (0x8)
</dt> <dd>

intensidad de primer plano

</dd> <dt>

16 (0x10)
</dt> <dd>

fondo azul

</dd> <dt>

32 (0x20)
</dt> <dd>

fondo verde

</dd> <dt>

64 (0x40)
</dt> <dd>

fondo rojo

</dd> <dt>

128 (0x80)
</dt> <dd>

intensidad de fondo

</dd> </dl>

Por ejemplo, las siguientes combinaciones generan texto rojo en un fondo blanco:


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  o  


```mof
0x74
```



</dd> <dt>

**ForceOffFeedback**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True**, el cursor de comentarios se fuerza mientras se inicia el proceso. Se muestra el cursor normal.

</dd> <dt>

**ForceOnFeedback**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True**, el cursor está en modo de comentarios durante dos segundos después de llamar a [**CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) Durante esos dos segundos, si el proceso realiza la primera llamada GUI, el sistema proporciona cinco segundos más al proceso. Durante esos cinco segundos, si el proceso muestra una ventana, el sistema proporciona otros cinco segundos al proceso para terminar de dibujar la ventana.

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número, en segundos, que el servicio WMI espera antes de acabar con un proceso 0 (cero) indica que no se va a acabar un proceso. La ejecución de un proceso impide que un proceso se ejecute indefinidamente.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que Windows Management Instrumentation (WMI) envía eventos.

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima para un consumidor específico, en bytes.

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](key-qualifier.md)
</dt> </dl>

Nombre único de un consumidor.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Programación del nivel de prioridad de los subprocesos de proceso. En la lista siguiente se enumeran los niveles de prioridad disponibles.

<dt>

32 (0x20)
</dt> <dd>

Indica un proceso normal sin necesidad de programación.

</dd> <dt>

64 (0x40)
</dt> <dd>

Indica un proceso cuyos subprocesos se ejecutan solo cuando el sistema está inactivo y son adelantados por los subprocesos de cualquier proceso que se ejecuta en una clase de prioridad más alta. Un ejemplo es un protector de pantalla. Los procesos secundarios heredan la clase de prioridad inactiva.

</dd> <dt>

128 (0x80)
</dt> <dd>

Indica un proceso que realiza tareas críticas de tiempo y prioridad alta. Los subprocesos de un proceso de clase de prioridad alta adelantan los subprocesos de los procesos de clase de prioridad normal o de prioridad inactiva. Un ejemplo es el Lista de tareas, que debe responder rápidamente cuando lo llama el usuario independientemente de la carga en el sistema. Debe tener mucho cuidado al usar la clase de prioridad alta, ya que una aplicación enlazada a la CPU con una clase de prioridad alta puede usar casi todos los ciclos disponibles.

</dd> <dt>

256 (0x100)
</dt> <dd>

Indica un proceso que tiene la prioridad más alta posible. Los subprocesos de un proceso de clase de prioridad en tiempo real adelantan los subprocesos de todos los demás procesos, incluidos los procesos del sistema operativo que realizan tareas importantes. Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un breve intervalo puede hacer que las memorias caché de disco no se vacían o que el mouse deje de responder.

</dd> </dl>

</dd> <dt>

**RunInteractively**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True,** el proceso se inicia en la WinStation interactiva. Si **es False,** el proceso se inicia en el servicio predeterminado WinStation. Esta propiedad invalida la **propiedad DesktopName.** Esta propiedad solo se usa localmente y solo si el usuario interactivo es el mismo usuario que ha configurado el consumidor.

A partir Windows Vista, el proceso que ejecuta la instancia **commandLineEventConsumer** se inicia en la cuenta **LocalSystem** y se encuentra en la sesión 0. Los servicios que se ejecutan en la sesión 0 no pueden interactuar con sesiones de usuario.

</dd> <dt>

**ShowWindowCommand**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de presentación de la ventana. Puede ser cualquiera de los valores que se pueden especificar en el parámetro *nCmdShow* para la [función ShowWindow.](/windows/desktop/api/winuser/nf-winuser-showwindow)

</dd> <dt>

**UseDefaultErrorMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True**, se usa el modo de error predeterminado.

</dd> <dt>

**WindowTitle**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Título que aparece en la barra de título del proceso. Esta propiedad se omite para las aplicaciones gui.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Directorio de trabajo para este proceso.

</dd> <dt>

**XCoordinate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Desplazamiento X, en píxeles, desde el borde izquierdo de la pantalla hasta el borde izquierdo de la ventana, si se crea una nueva ventana.

</dd> <dt>

**XNumCharacters**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho del búfer de pantalla, en columnas de caracteres, si se crea una nueva ventana de consola. Esta propiedad se omite en un proceso de GUI.

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho, en píxeles, de una nueva ventana, si se crea una nueva ventana.

</dd> <dt>

**YCoordinate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Desplazamiento Y, en píxeles, desde el borde superior de la pantalla hasta el borde superior de la ventana, si se crea una nueva ventana.

</dd> <dt>

**YNumCharacters**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Alto del búfer de pantalla, en filas de caracteres, si se crea una nueva ventana de consola. Esta propiedad se omite en un proceso de GUI.

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Alto, en píxeles, de la nueva ventana, si se crea una nueva ventana.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase CommandLineEventConsumer** se deriva de la [**\_ \_ clase abstracta EventConsumer.**](--eventconsumer.md)

La **propiedad CreateSeparateWowVdm** indica si el nuevo proceso se ejecuta o no en una máquina virtual privada de DOS (VDM). La ventaja de ejecutarse por separado es que un bloqueo solo finaliza el VDM único. Los programas que se ejecutan en vdms distintos siguen funcionando con normalidad y las aplicaciones basadas en Windows de 16 bits que se ejecutan en vdms independientes tienen colas de entrada independientes. Esto significa que si una aplicación deja de responder momentáneamente, las aplicaciones de vdms independientes siguen recibiendo entradas. La desventaja de ejecutar por separado es que se necesita mucho más memoria para hacerlo. Debe establecer esta propiedad en **True** solo si el usuario solicita que las aplicaciones basadas en Windows de 16 bits se ejecuten en su propio VDM.

> [!Note]  
> **CommandLineEventConsumer** usa internamente el método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) y pasa las propiedades **ExecutablePath** y **CommandLineTemplate** como los parámetros *lpApplicationName* y *lpCommandLine.* En el Managed Object Format de código de Managed Object Format (MOF) no se **usa CommandLineEventConsumer** correctamente.

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



El [**método CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) pasa *lpCommandLine* como `argv[0]` , , y así `argv[1]` sucesivamente. Dado que en el caso de las aplicaciones de 16 bits que se solían reservar para el nombre de archivo ejecutable, el código MOF anterior da como resultado que el proceso se crea como si el comando siguiente se especificara en el símbolo del `argv[0]` sistema: **c: \\ windows \\ system32 \\cscript.exe param1 param2**.

El comando anterior no se realiza correctamente porque Cscript.exe no mira , por lo que no reconoce que no contiene su propio nombre, sino algo más `argv[0]` ("c: \\ \\ scripts \\ \\MyScript.js"). En el ejemplo siguiente se identifica el uso recomendado de **CommandLineEventConsumer**.


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



El uso anterior de **CommandLineEventConsumer** da como resultado el proceso creado como si se especificara el siguiente comando en el símbolo del **sistema: c: \\ windows \\ system32 \\cscript.exe c: scriptsMyScript.js \\ \\ param1 param2**

Dado que "c: scriptsMyScript.js" es ahora , se ve Cscript.exe \\ \\ y el comando se \\ \\ `argv[1]` ejecuta correctamente.

Para obtener más información, vea la [**función CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo del uso **de CommandLineEventConsumer** para crear un [consumidor,](running-a-program-from-the-command-line-based-on-an-event.md)vea Ejecutar un programa desde la línea de comandos basada en un evento .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Suscripción \\ raíz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Creación de un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

