---
description: La clase WMI abstracta ProcessStartup de Win32 representa la configuración \_ de inicio de un Windows basado en datos.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Win32_ProcessStartup clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174369"
---
# <a name="win32_processstartup-class"></a>Clase ProcessStartup de Win32 \_

La clase [WMI](../wmisdk/retrieving-a-class.md) **\_ abstracta ProcessStartup de Win32** representa la configuración de inicio de un Windows basado en procesos. La clase se define como una definición de tipo de método, lo que significa que solo se usa para pasar información al método [**Create**](create-method-in-class-win32-process.md) de la [**clase Process \_ de Win32.**](win32-process.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a>Members

La **clase \_ ProcessStartup de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ProcessStartup de Win32** tiene estas propiedades.

<dl> <dt>

**CreateFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Functions \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags")
</dt> </dl>

Valores adicionales que controlan la clase de prioridad y la creación del proceso. Los siguientes valores de creación se pueden especificar en cualquier combinación, excepto como se indica.

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Depuración \_ Proceso** (1)


</dt> <dd>

Si se establece esta marca, el proceso de llamada se trata como un depurador y se depura el nuevo proceso. El sistema notifica al depurador todos los eventos de depuración que se producen en el proceso que se está depurando.

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Depuración \_ Solo \_ este \_ proceso** (2)


</dt> <dd>

Si no se establece esta marca y se depura el proceso de llamada, el nuevo proceso se convierte en otro proceso que se está depurando. Si el proceso de llamada no es un proceso de depuración, no se produce ninguna acción relacionada con la depuración.

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Crear \_ Suspendido** (4)


</dt> <dd>

El subproceso principal del nuevo proceso se crea en un estado suspendido y no se ejecuta hasta que se llama al [**método ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Desasociado \_ Proceso** (8)


</dt> <dd>

Para los procesos de consola, el nuevo proceso no tiene acceso a la consola del proceso primario. Esta marca no se puede usar si se **establece la \_ \_ marca** Crear nueva consola.

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Crear \_ Nueva \_ consola** (16)


</dt> <dd>

Este nuevo proceso tiene una nueva consola, en lugar de heredar la consola primaria. Esta marca no se puede usar con la **marca Proceso \_ desasociado.**

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Crear \_ Nuevo \_ grupo \_ de procesos** (512)


</dt> <dd>

Este nuevo proceso es el proceso raíz de un nuevo grupo de procesos. El grupo de procesos incluye todos los procesos que son descendientes de este proceso raíz. El identificador de proceso del nuevo grupo de procesos es el mismo que el identificador de proceso que se devuelve en la **propiedad ProcessID** de la [**clase Win32 \_ Process.**](win32-process.md) El método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) usa grupos de procesos para permitir el envío de una señal CTRL+C o una señal CTRL+BREAK a un grupo de procesos de consola.

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Crear \_ Entorno \_ Unicode** (1024)


</dt> <dd>

La configuración del entorno enumerada en **la propiedad EnvironmentVariables** usa caracteres Unicode. Si no se establece esta marca, el bloque de entorno usa caracteres ANSI.

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Crear \_ Modo \_ de error \_ predeterminado** (67108864)


</dt> <dd>

A los procesos recién creados se les da el modo de error predeterminado del sistema del proceso de llamada en lugar de heredar el modo de error del proceso primario. Esta marca es útil para las aplicaciones de shell multiproceso que se ejecutan con errores graves deshabilitados.

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE \_ INTERRUPCIÓN \_ DEL \_ TRABAJO** (16777216)


</dt> <dd>

Se usa para que el proceso creado no esté limitado por el objeto de trabajo.

</dd> </dl>

</dd> <dt>

**EnvironmentVariables**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ CURRENT USER \_ \\ \\ Environment")
</dt> </dl>

Lista de valores para la configuración de un equipo. Las variables de entorno especifican rutas de búsqueda para archivos, directorios para archivos temporales, opciones específicas de la aplicación y otra información similar. El sistema mantiene un bloque de configuración de entorno para cada usuario y uno para el equipo. El bloque de entorno del sistema representa variables de entorno para todos los usuarios de un equipo específico. El bloque de entorno de un usuario representa las variables de entorno que el sistema mantiene para un usuario específico e incluye el conjunto de variables de entorno del sistema. De forma predeterminada, cada proceso recibe una copia del bloque de entorno para su proceso primario. Normalmente, este es el bloque de entorno para el usuario que ha iniciado sesión. Un proceso puede especificar distintos bloques de entorno para sus procesos secundarios.

</dd> <dt>

**ErrorMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funciones de error de Win32API \| \| SetErrorMode")
</dt> </dl>

En algunos procesadores que no son x86, las referencias de memoria mal alineadas provocan una excepción de error de alineación. La marca Sin errores de alineación excepto permite controlar si un sistema operativo corrige automáticamente dichos errores de alineación o los hace visibles para una aplicación. **\_ \_ \_** En una plataforma de millones de instrucciones por segundo (MIPS), una aplicación debe llamar explícitamente a [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) con la marca Sin error de alineación excepto para que el sistema operativo corrija automáticamente los errores de alineación. **\_ \_ \_**

Cómo un sistema operativo procesa varios tipos de errores graves. Puede especificar que el sistema operativo procese los errores o que una aplicación pueda recibir y procesar errores.

El valor predeterminado es que el sistema operativo haga que los errores de alineación sean visibles para una aplicación. Dado que la plataforma x86 no hace que los errores de alineación sean visibles para una aplicación, la marca Sin errores de alineación excepto no hace que el sistema operativo genera un error de alineación, incluso si la marca no está establecida. **\_ \_ \_** El estado predeterminado de [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) es establecer todas las marcas en 0 (cero).

<dt>



 (1)


</dt> <dd>

Valor predeterminado

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Error \_ Errores \_ críticos** (2)


</dt> <dd>

Si se establece esta marca, el sistema operativo no muestra el cuadro de mensaje del controlador de errores crítico cuando se produce este tipo de error. En su lugar, el sistema operativo envía el error al proceso de llamada.

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No \_ Error \_ de \_ alineación excepto** (4)


</dt> <dd>

Si se establece esta marca, el sistema operativo corrige automáticamente los errores de alineación de memoria y los hace invisibles para la aplicación. Lo hace para los procesos de llamada y descendientes. Esta marca solo se aplica a la informática de conjunto de instrucciones reducida (RISC) y no tiene ningún efecto en los procesadores x86.

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No \_ Cuadro \_ de error de \_ \_ GP** (8)


</dt> <dd>

Si se establece esta marca, el sistema operativo no muestra el cuadro de mensaje de error de protección general (GP) cuando se produce un error de GP. Esta marca solo se debe establecer mediante la depuración de aplicaciones que controlan errores de GP.

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No \_ Cuadro \_ de error Abrir \_ \_ archivo** (16)


</dt> <dd>

Si se establece esta marca, el sistema operativo no muestra un cuadro de mensaje cuando no encuentra un archivo. En su lugar, el error se devuelve al proceso de llamada. Esta marca se omite actualmente.

</dd> </dl>

</dd> <dt>

**FillAttribute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")
</dt> </dl>

El texto y los colores de fondo si se crea una nueva ventana de consola en una aplicación de consola. Estos valores se omiten en las aplicaciones de interfaz gráfica de usuario (GUI). Para especificar los colores de primer plano y de fondo, agregue los valores juntos. Por ejemplo, para tener el tipo rojo (4) en un fondo azul (16), establezca FillAttribute en 20.

<dt>

1
</dt> <dd>

Azul de \_ primer plano

</dd> <dt>

2
</dt> <dd>

Verde \_ de primer plano

</dd> <dt>

4
</dt> <dd>

Rojo en \_ primer plano

</dd> <dt>

8
</dt> <dd>

Intensidad de \_ primer plano

</dd> <dt>

16
</dt> <dd>

Azul de \_ fondo

</dd> <dt>

32
</dt> <dd>

Fondo \_ verde

</dd> <dt>

64
</dt> <dd>

Rojo de \_ fondo

</dd> <dt>

128
</dt> <dd>

Intensidad de \_ fondo

</dd> </dl>

</dd> <dt>

**PriorityClass**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**JOBOBJECT BASIC LIMIT \_ \_ \_ INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")
</dt> </dl>

Clase priority del nuevo proceso. Use esta propiedad para determinar las prioridades de programación de los subprocesos del proceso. Si la propiedad se deja null, el valor predeterminado de la clase priority es Normal, a menos que la clase de prioridad del proceso de creación sea Idle o Below \_ Normal. En estos casos, el proceso secundario recibe la clase de prioridad predeterminada del proceso que realiza la llamada.

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Indica un proceso normal sin necesidad de programación especial.

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactivo** (64)


</dt> <dd>

Indica un proceso con subprocesos que se ejecutan solo cuando el sistema está inactivo y son adelantados por los subprocesos de cualquier proceso que se ejecuta en una clase de prioridad más alta. Un ejemplo es un protector de pantalla. Los procesos secundarios heredan la clase de prioridad inactiva.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (128)


</dt> <dd>

Indica un proceso que realiza tareas de tiempo crítico que se deben ejecutar inmediatamente para ejecutarse correctamente. Los subprocesos de un proceso de clase de prioridad alta adelantan los subprocesos de los procesos de clase de prioridad normal o de prioridad inactiva. Un ejemplo es Windows Lista de tareas, que debe responder rápidamente cuando lo llama el usuario, independientemente de la carga en el sistema operativo. Debe tener mucho cuidado al usar la clase de prioridad alta, ya que una aplicación enlazada a la CPU de clase de alta prioridad puede usar casi todos los ciclos disponibles. Solo una prioridad en tiempo real adelanta los subprocesos establecidos en este nivel.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tiempo real** (256)


</dt> <dd>

Indica un proceso que tiene la prioridad más alta posible. Los subprocesos de un proceso de clase de prioridad en tiempo real adelantan los subprocesos de todos los demás procesos, incluidos los subprocesos de alta prioridad y los procesos del sistema operativo que realizan tareas importantes. Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un intervalo muy breve puede hacer que las cachés de disco no se vaciarán o que un mouse deje de responder.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**A continuación se muestra \_ Normal** (16384)


</dt> <dd>

Indica un proceso que tiene una prioridad mayor que Idle pero menor que Normal.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Anterior \_ Normal** (32768)


</dt> <dd>

Indica un proceso que tiene una prioridad mayor que Normal pero menor que Alta.

</dd> </dl>

</dd> <dt>

**ShowWindow**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")
</dt> </dl>

Cómo se muestra la ventana al usuario. Puede ser cualquiera de los valores que se pueden especificar en el parámetro *nCmdShow* para la [función ShowWindow.](/windows/desktop/api/winuser/nf-winuser-showwindow)

</dd> <dt>

**Título**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")
</dt> </dl>

Texto que se muestra en la barra de título cuando se crea una nueva ventana de consola; se usa para los procesos de consola. Si **es NULL,** el nombre del archivo ejecutable se usa como título de la ventana. Esta propiedad debe ser **NULL para los** procesos de la gui o la consola que no crean una nueva ventana de consola.

</dd> <dt>

**WinstationDesktop**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")
</dt> </dl>

El nombre del escritorio o el nombre de la estación de escritorio y ventana para el proceso. Una barra diagonal inversa en la cadena indica que la cadena incluye nombres de estación de escritorio y de ventana. Si **WinstationDesktop** es **NULL,** el nuevo proceso hereda la estación de escritorio y ventana de su proceso primario. Si **WinstationDesktop** es una cadena vacía, el proceso no hereda la estación de escritorio y ventana de su proceso primario. El sistema determina si se debe crear una nueva estación de escritorio y ventana. Una estación de ventana es un objeto seguro que contiene un Portapapeles, un conjunto de átomos globales y un grupo de objetos de escritorio. La estación de ventana interactiva que se asigna a la sesión de inicio de sesión del usuario interactivo también contiene el teclado, el mouse y el dispositivo para mostrar. Un escritorio es un objeto seguro contenido dentro de una estación de ventana. Un escritorio tiene una superficie de presentación lógica y contiene ventanas, menús y enlaces. Una estación de ventana puede tener varios escritorios. Solo los escritorios de la estación de ventana interactiva pueden ser visibles y recibir la entrada del usuario.

</dd> <dt>

**X**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX")
</dt> </dl>

Desplazamiento X de la esquina superior izquierda de una ventana si se crea una nueva ventana, en píxeles. Los desplazamientos se encuentran en la esquina superior izquierda de la pantalla. Para los procesos de GUI, la posición especificada se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *X* de **CreateWindow** es **CW \_ USEDEFAULT.**

> \[! Nota X\]  
> y **Y** no se pueden especificar de forma independiente.

 

</dd> <dt>

**XCountChars**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")
</dt> </dl>

Ancho del búfer de pantalla en columnas de caracteres. Esta propiedad se usa para los procesos que crean una ventana de consola y se omite en los procesos de gui.

> [!Note]  
> **XCountChars** y **YCountChars** no se pueden especificar de forma independiente.

 

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")
</dt> </dl>

Ancho de píxel de una ventana si se crea una nueva ventana. Para los procesos de GUI, solo se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro nWidth de **CreateWindow** es **CW \_ USEDEFAULT.**

> [!Note]  
> **XSize** y **YSize** no se pueden especificar de forma independiente.

 

</dd> <dt>

**S**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Proceso win32API y estructuras de subproceso \| \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwY")
</dt> </dl>

Desplazamiento en píxeles de la esquina superior izquierda de una ventana si se crea una nueva ventana. Los desplazamientos se encuentran en la esquina superior izquierda de la pantalla. Para los procesos de GUI, la posición especificada se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *y* de **CreateWindow** es **CW \_ USEDEFAULT.**

> \[! Nota X\]  
> y **Y** no se pueden especificar de forma independiente.

 

</dd> <dt>

**YCountChars**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")
</dt> </dl>

Alto del búfer de pantalla en filas de caracteres. Esta propiedad se usa para los procesos que crean una ventana de consola, pero se omite en los procesos de GUI.

> [!Note]  
> **XCountChars** y **YCountChars** no se pueden especificar de forma independiente.

 

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")
</dt> </dl>

Alto de píxel de una ventana si se crea una nueva ventana. Para los procesos de GUI, solo se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *nWidth* de **CreateWindow** es **CW \_ USEDEFAULT.**

> [!Note]  
> **XSize** y **YSize** no se pueden especificar de forma independiente.

 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta clase se deriva de [**\_ MethodParameterClass de Win32.**](win32-methodparameterclass.md)

Información general

El [**método Win32 \_ Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) permite configurar opciones de inicio para cualquier proceso nuevo que se ejecute en un equipo. Por ejemplo, puede configurar un proceso para que se inicie en una ventana "oculta", lo que impide que un usuario lo vea y, posiblemente, lo interrumpa. Si el proceso se ejecuta en una ventana de comandos, puede configurar el tamaño, el título y los colores de primer plano y fondo de la ventana.

Las opciones de inicio se configuran mediante la **clase \_ ProcessStartup de Win32.** **Win32 \_ ProcessStartup es** una clase de tipo de método; La clase Method Type solo existe para pasar información a un método. En este caso, todas las propiedades de una instancia de **\_ ProcessStartup de Win32** se pasan a una instancia de [**Proceso de Win32. \_**](win32-process.md)

**Uso de \_ ProcessStartup de Win32**

1.  Cree una instancia de **\_ ProcessStartup de Win32.**
2.  Configure las propiedades de la nueva instancia.
3.  Incluya la instancia como parte del método Process Create de [**Win32. \_**](win32-process.md)

Por ejemplo, si ha creado una instancia de **\_ ProcessStartup de Win32** denominada objConfig, debe pasar el nombre del objeto en el método Create como se muestra a continuación:

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a>Ejemplos

Puede usar la clase **\_ ProcessStartup de Win32** para configurar varias opciones de inicio para un proceso. Estas opciones incluyen, entre otras cosas, la creación de un proceso en una ventana oculta y la creación de un proceso de mayor prioridad. El siguiente VBScript crea un proceso en una ventana oculta.


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



El siguiente VBScript crea un proceso de prioridad más alta.


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



En el siguiente ejemplo de código vbscript se crea Bloc de notas proceso en el equipo local. **Win32 \_ ProcessStartup** se usa para configurar los valores del proceso.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**Proceso \_ win32**](win32-process.md)
</dt> <dt>

[**\_\_ProviderHostQuotaConfiguration**](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[Tareas wmi: procesos](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
