---
description: Funciones de salida de depuración
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Funciones de salida de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee1bdbc9cce98ce1704b62a8354b81951df33c4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884234"
---
# <a name="debug-output-functions"></a>Funciones de salida de depuración

Las [DirectShow base proporcionan](directshow-base-classes.md) varias macros para mostrar información de depuración.



| Función                                               | Descripción                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DbgCheckModuleLevel**](dbgcheckmodulelevel.md)     | Comprueba si el registro está habilitado para los tipos de mensaje y el nivel dados.                             |
| [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) | Muestra información sobre los objetos activos.                                                           |
| [**DbgInitialise**](dbginitialise.md)                 | Inicializa la biblioteca de depuración.                                                                       |
| [**DbgLog**](dbglog.md)                               | Envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados. |
| [**DbgOutString**](dbgoutstring.md)                   | Envía una cadena a la ubicación de salida de depuración.                                                         |
| [**DbgSetModuleLevel**](dbgsetmodulelevel.md)         | Establece el nivel de registro para uno o varios tipos de mensaje.                                                |
| [**DbgTerminate**](dbgterminate.md)                   | Limpia la biblioteca de depuración.                                                                         |
| [**Displaytype**](displaytype.md)                     | Envía información sobre un tipo de medio a la ubicación de salida de depuración.                                   |
| [**DumpGraph**](dumpgraph.md)                         | Envía información sobre un gráfico de filtros a la ubicación de salida de depuración.                                 |
| [**GuidNames**](guidnames.md)                         | Matriz global que contiene cadenas que representan los GUID definidos en Uuids.h.                        |
| [**NOMBRE**](name.md)                                   | Genera una cadena de solo depuración.                                                                       |
| [**NOTA**](note.md)                                   | Envía una cadena a la ubicación de salida de depuración.                                                         |
| [**RECORDAR**](remind.md)                               | Genera un recordatorio en tiempo de compilación.                                                                |



 

**Claves del Registro**

La función de salida de depuración DirectShow usar un conjunto de claves del Registro. La ubicación de estas claves del Registro depende de la versión de Windows.

*Antes de Windows Vista*, las claves de depuración se encuentran en la ruta de acceso siguiente:

**HKEY \_ DEPURACIÓN \_ DE** \\ **SOFTWARE DE MÁQUINA** \\ **LOCAL**

En Windows Vista o versiones posteriores, se encuentran en la ruta de acceso siguiente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectShow** \\ **Debug**

En el caso de los filtros de terceros, la ubicación depende de la versión del DirectShow [base que](directshow-base-classes.md) se usó para compilar el filtro. La versión incluida en el SDK Windows para Windows Vista usa la ruta de acceso más reciente. Las versiones anteriores usaban la ruta de acceso anterior.

En los comentarios siguientes, se usa la etiqueta *&lt; DebugRoot &gt;* para indicar estas dos rutas de acceso. Sustituya la ruta de acceso correcta, según la versión de Windows o la versión de las clases base.

**Registro de depuración**

DirectShow define varios tipos de mensaje, que se muestran en la tabla siguiente.



| Valor                   | Descripción                                             |
|-------------------------|---------------------------------------------------------|
| ERROR \_ DE REGISTRO              | Notificación de error.                                     |
| BLOQUEO DE \_ REGISTROS            | Bloqueo y desbloqueo de secciones críticas.             |
| MEMORIA DE \_ REGISTRO             | Asignación de memoria y creación y destrucción de objetos. |
| TIEMPO DE \_ REGISTRO             | Medidas de tiempo y rendimiento.                    |
| SEGUIMIENTO DEL \_ REGISTRO              | Seguimiento de llamadas generales.                                   |
| CUSTOM1 a CUSTOM5 | Disponible para mensajes de depuración personalizados                     |



 

Cada una de las DirectShow de registro de depuración especifica un tipo de mensaje y un nivel de registro. El mensaje de depuración solo se muestra cuando el nivel de depuración actual para ese tipo de mensaje es igual o mayor que el nivel especificado en la función de registro. De lo contrario, se omite el mensaje.

Por ejemplo, el código siguiente genera la cadena "This is a debug message" (Este es un mensaje de depuración) si el nivel DE SEGUIMIENTO DE REGISTRO \_ es 3 o superior:

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Cada módulo puede establecer su propio nivel de depuración para cada tipo de mensaje. (Un *módulo* es un archivo DLL o ejecutable que se puede cargar mediante la **función LoadLibrary).** Los niveles de depuración de un módulo aparecen en el Registro con la siguiente clave:

**HKEY \_ LOCAL \_ MACHINE** \\ **&lt; DebugRoot &gt;** \\ **&lt; ModuleName &gt;** \\ **&lt; MessageType &gt;**

donde *<Message Type>* es el tipo de mensaje menos el inicial "LOG"; por \_ ejemplo, **LOCKING** para los mensajes LOG \_ LOCKING. Cuando se carga un módulo, la biblioteca de depuración encuentra los niveles de registro del módulo en el Registro. Si las claves del Registro no existen, la biblioteca de depuración las crea.

Un módulo también puede establecer sus propios niveles en tiempo de ejecución mediante la [**función DbgSetModuleLevel.**](dbgsetmodulelevel.md) Para enviar un mensaje a la salida de depuración, llame a la [**macro DbgLog.**](dbglog.md) En el ejemplo siguiente se crea un mensaje de nivel 3 de tipo LOG \_ TRACE:

También puede especificar niveles de registro globales con la siguiente clave del Registro:


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



La biblioteca de depuración usa el nivel que sea mayor, el nivel global o el nivel de módulo.

**Ubicación de salida de depuración**

La ubicación de salida de depuración viene determinada por otra clave del Registro:

**HKEY \_ LOCAL \_ MACHINE** \\ **&lt; DebugRoot &gt;** \\ **<Modile Name>** \\ **LogToFile**

Si el valor de esta clave es `Console` , la salida va a la ventana de consola. Si el valor es `Deb` , , o una cadena `Debug` `Debugger` vacía, la salida va a la ventana del depurador. De lo contrario, la salida se escribe en un archivo especificado por la clave del Registro.

Antes de que un ejecutable DirectShow biblioteca de depuración, debe llamar a la [**función DbgInitialise.**](dbginitialise.md) Después, debe llamar a la [**función DbgTerminate.**](dbgterminate.md) Los archivos DLL no necesitan llamar a estas funciones, ya que el punto de entrada dll (definido en la biblioteca de clases base) las llama automáticamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilidades de depuración](debugging-utilities.md)
</dt> </dl>

 

 



