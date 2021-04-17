---
description: La clase CommandLineEventConsumer inicia un proceso arbitrario en el sistema local cuando se le entrega un evento.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Clase CommandLineEventConsumer
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
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187938"
---
# <a name="commandlineeventconsumer-class"></a>Clase CommandLineEventConsumer

La clase **CommandLineEventConsumer** inicia un proceso arbitrario en el sistema local cuando se le entrega un evento. Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

> [!Note]  
> Al usar la clase **CommandLineEventConsumer** , proteja el archivo ejecutable que desea iniciar. Si el archivo ejecutable no está en una ubicación segura o está protegido con una lista de control de acceso (ACL) segura, un usuario no autorizado puede reemplazar el archivo ejecutable con un archivo ejecutable malintencionado. Para obtener más información acerca de las ACL, visite la sección seguridad del kit de desarrollo de software (SDK) de Microsoft Windows y consulte [crear un descriptor de seguridad para un nuevo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

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

## <a name="members"></a>Members

La clase **CommandLineEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CommandLineEventConsumer** tiene estas propiedades.

<dl> <dt>

**CommandLineTemplate**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Plantilla de cadena estándar que especifica el proceso que se va a iniciar. Esta propiedad puede ser **null** y la propiedad **ExecutablePath** se usa como línea de comandos.

</dd> <dt>

**CreateNewConsole**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se utiliza. Si se asigna un valor a esta propiedad, se genera un mensaje de seguimiento. Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).

</dd> <dt>

**CreateNewProcessGroup**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, el nuevo proceso es el proceso raíz de un nuevo grupo de procesos. El grupo de procesos incluye todos los procesos que son descendientes de este proceso raíz. El identificador de proceso del nuevo grupo de procesos es el mismo que el de este identificador de proceso. El método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) usa los grupos de procesos para habilitar el envío de una señal CTRL + C o Ctrl + Inter a un grupo de procesos de consola.

</dd> <dt>

**CreateSeparateWowVdm**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, el nuevo proceso se ejecuta en una máquina virtual de dos privada (VDM). Esto solo es válido cuando se inicia una aplicación que se ejecuta en un sistema operativo Windows de 16 bits. Si se establece en **false**, todas las aplicaciones que se ejecutan en un sistema operativo Windows de 16 bits se ejecutan como subprocesos en un solo VDM compartido. Para obtener más información, consulte la sección Comentarios de este tema.

</dd> <dt>

**CreateSharedWowVdm**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es true**, el método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ejecuta el nuevo proceso en la máquina virtual dos compartida (VDM). Esta propiedad puede invalidar el modificador DefaultSeparateVDM en la sección Windows de Win.ini si se establece en **true**. Para obtener más información, consulte la sección Comentarios de este tema.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, dependiendo del sistema operativo. Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**DesktopName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

No se utiliza. Si se asigna un valor a esta propiedad, se genera un mensaje de seguimiento. Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).

</dd> <dt>

**ExecutablePath _s**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Módulo que se va a ejecutar. La cadena puede especificar la ruta de acceso completa y el nombre de archivo del módulo que se va a ejecutar, o puede especificar un nombre parcial. Si se especifica un nombre parcial, se supone la unidad actual y el directorio actual.

La propiedad **ExecutablePath** puede ser **null**. En ese caso, el nombre del módulo debe ser el primer token delimitado por espacios en blanco en el valor de la propiedad **CommandLineTemplate** . Si usa un nombre de archivo largo que contiene un espacio, use cadenas entre comillas para indicar dónde finaliza el nombre de archivo y los argumentos comienzan a aclarar el nombre de archivo.

> [!Note]  
> Dado que la propiedad **CommandLineTemplate** puede ser una plantilla en la que se proporciona el módulo que se va a ejecutar mediante una variable, una propiedad **ExecutablePath** **nula** permite que el módulo que se especifica en el parámetro se ejecute y, a continuación, está fuera del control. Establezca siempre la propiedad **ExecutablePath** en el registro **CommandLineEventConsumer** para incluir el ejecutable necesario, lo que evita que se sobrescriban los parámetros de eventos. Si debe usar una plantilla y una variable para especificar el módulo que se va a ejecutar, tenga cuidado con quién tiene concedido el privilegio de escritura completo en el espacio de nombres.

 

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el texto inicial y los colores de fondo si se crea una nueva ventana de consola en una aplicación de consola.

</dd> <dt>

**FillAttributes**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Texto inicial y colores de fondo, si se crea una nueva ventana de consola en una aplicación de consola. Esta propiedad se omite en una aplicación GUI. El valor puede ser cualquier combinación de los siguientes valores.

<dt>

1 (0x1)
</dt> <dd>

primer plano azul

</dd> <dt>

2 (0X2)
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

Fondo azul

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

Por ejemplo, las siguientes combinaciones producen texto rojo en un fondo blanco:


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  or  


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

Si es **true**, se fuerza el cursor de comentarios mientras se inicia el proceso. Se muestra el cursor normal.

</dd> <dt>

**ForceOnFeedback**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, el cursor está en modo de comentarios durante dos segundos después de que se llame a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Durante esos dos segundos, si el proceso realiza la primera llamada a la interfaz gráfica de usuario, el sistema proporciona cinco segundos más al proceso. Durante esos cinco segundos, si el proceso muestra una ventana, el sistema proporciona otros cinco segundos al proceso para terminar de dibujar la ventana.

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número, en segundos, que el servicio WMI espera antes de que se elimine un proceso 0 (cero) indica que no se va a eliminar un proceso. El sacrificio de un proceso impide que un proceso se ejecute indefinidamente.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima para un consumidor específico, en bytes.

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](key-qualifier.md)
</dt> </dl>

Nombre único de un consumidor.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nivel de prioridad de programación de los subprocesos del proceso. En la lista siguiente se enumeran los niveles de prioridad disponibles.

<dt>

32 (0x20)
</dt> <dd>

Indica un proceso normal sin necesidad de programar.

</dd> <dt>

64 (0x40)
</dt> <dd>

Indica un proceso cuyos subprocesos se ejecutan solo cuando el sistema está inactivo y son retenidos por los subprocesos de cualquier proceso que se ejecute en una clase de prioridad más alta. Un ejemplo es un protector de pantalla. Los procesos secundarios heredan la clase de prioridad inactiva.

</dd> <dt>

128 (0x80)
</dt> <dd>

Indica un proceso que realiza tareas críticas en el tiempo de alta prioridad. Los subprocesos de un proceso de clase de prioridad alta se adelantan a los subprocesos de procesos de clase de prioridad normal o de prioridad inactiva. Un ejemplo es el Lista de tareas, que debe responder rápidamente cuando el usuario lo llama, independientemente de la carga del sistema. Extreme las precauciones al usar la clase de prioridad alta, ya que una aplicación enlazada a la CPU con una clase de prioridad alta puede usar casi todos los ciclos disponibles.

</dd> <dt>

256 (0x100)
</dt> <dd>

Indica un proceso que tiene la prioridad más alta posible. Los subprocesos de un proceso de clase de prioridad en tiempo real tienen preferencia sobre los subprocesos de todos los demás procesos, incluidos los procesos del sistema operativo que realizan tareas importantes. Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un intervalo breve puede hacer que las cachés del disco no se vacíen o hacer que el mouse deje de responder.

</dd> </dl>

</dd> <dt>

**RunInteractively**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, el proceso se inicia en la estación de inicio interactiva. Si es **false**, el proceso se inicia en la estación de servicio predeterminada. Esta propiedad invalida la propiedad **DesktopName** . Esta propiedad solo se usa localmente y solo si el usuario interactivo es el mismo usuario que configura el consumidor.

A partir de Windows Vista, el proceso que ejecuta la instancia de **CommandLineEventConsumer** se inicia con la cuenta **LocalSystem** y se encuentra en la sesión 0. Los servicios que se ejecutan en la sesión 0 no pueden interactuar con las sesiones de usuario.

</dd> <dt>

**ShowWindowCommand**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de la ventana Mostrar. Puede ser cualquiera de los valores que se pueden especificar en el parámetro *nCmdShow* para la función [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> <dt>

**UseDefaultErrorMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, se usa el modo de error predeterminado.

</dd> <dt>

**WindowTitle**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Título que aparece en la barra de título del proceso. Esta propiedad se omite para las aplicaciones GUI.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Directorio de trabajo de este proceso.

</dd> <dt>

**XCoordinate**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Desplazamiento X, en píxeles, desde el borde izquierdo de la pantalla hasta el borde izquierdo de la ventana, si se crea una nueva ventana.

</dd> <dt>

**XNumCharacters**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho del búfer de pantalla, en columnas de caracteres, si se crea una nueva ventana de consola. Esta propiedad se omite en un proceso de GUI.

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho, en píxeles, de una nueva ventana, si se crea una nueva ventana.

</dd> <dt>

**YCoordinate**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Desplazamiento y, en píxeles, desde el borde superior de la pantalla hasta el borde superior de la ventana, si se crea una nueva ventana.

</dd> <dt>

**YNumCharacters**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Alto del búfer de pantalla, en filas de caracteres, si se crea una nueva ventana de consola. Esta propiedad se omite en un proceso de GUI.

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Alto, en píxeles, de la nueva ventana, si se crea una nueva ventana.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CommandLineEventConsumer** se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .

La propiedad **CreateSeparateWowVdm** indica si el nuevo proceso se ejecuta en una máquina virtual de dos privada (VDM). La ventaja de ejecutarse por separado es que un bloqueo solo finaliza el VDM único. Los programas que se ejecutan en VDMs DISTINCT continúan funcionando con normalidad y las aplicaciones de 16 bits basadas en Windows que se ejecutan en VDMs independientes tienen colas de entrada independientes. Esto significa que si una aplicación deja de responder momentáneamente, las aplicaciones en VDMs independientes continúan recibiendo la entrada. El inconveniente de ejecutarse por separado es que requiere mucho más memoria para hacerlo. Debe establecer esta propiedad en **true** solo si el usuario solicita que las aplicaciones basadas en Windows de 16 bits se ejecuten en su propio VDM.

> [!Note]  
> **CommandLineEventConsumer** usa el método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) internamente y pasa las propiedades **ExecutablePath** y **CommandLineTemplate** como parámetros *lpApplicationName* y *lpCommandLine* . En el siguiente ejemplo de código de Managed Object Format (MOF) no se usa correctamente **CommandLineEventConsumer** .

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



El método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) pasa *lpCommandLine* como `argv[0]` , `argv[1]` , etc. Como en el `argv[0]` caso de las aplicaciones de 16 bits que se han reservado para el nombre del archivo ejecutable, el código MOF anterior hace que el proceso se cree como si se escribiera el siguiente comando en el símbolo del sistema: **c: \\ Windows \\ system32 \\cscript.exe parám1 param2**.

El comando anterior no se ejecuta correctamente porque Cscript.exe no examina `argv[0]` , por lo que no reconoce que no contenga su propio nombre, sino algo más ("c: \\ \\ scripts \\ \\MyScript.js"). En el ejemplo siguiente se identifica el uso recomendado de **CommandLineEventConsumer**.


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



El uso anterior de **CommandLineEventConsumer** da como resultado el proceso creado como si se escribiera el siguiente comando en el símbolo del sistema: **c: \\ Windows \\ system32 \\cscript.exe c: \\ scripts \\MyScript.js parám1 parám2**

Como "c: \\ \\ scripts \\ \\MyScript.js" es ahora `argv[1]` , lo verán Cscript.exe y el comando se ejecutará correctamente.

Para obtener más información, vea la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo del uso de **CommandLineEventConsumer** para crear un consumidor, vea [ejecutar un programa desde la línea de comandos en función de un evento](running-a-program-from-the-command-line-based-on-an-event.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\Suscripción raíz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Crear un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

