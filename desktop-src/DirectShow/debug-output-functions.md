---
description: Funciones de salida de depuración
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Funciones de salida de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659299"
---
# <a name="debug-output-functions"></a>Funciones de salida de depuración

Las [clases base de DirectShow](directshow-base-classes.md) proporcionan varias macros para mostrar información de depuración.



| Función                                               | Descripción                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DbgCheckModuleLevel**](dbgcheckmodulelevel.md)     | Comprueba si el registro está habilitado para los tipos de mensaje y el nivel especificados.                             |
| [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) | Muestra información acerca de los objetos activos.                                                           |
| [**DbgInitialise**](dbginitialise.md)                 | Inicializa la biblioteca de depuración.                                                                       |
| [**DbgLog**](dbglog.md)                               | Envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados. |
| [**DbgOutString**](dbgoutstring.md)                   | Envía una cadena a la ubicación de salida de depuración.                                                         |
| [**DbgSetModuleLevel**](dbgsetmodulelevel.md)         | Establece el nivel de registro para uno o más tipos de mensaje.                                                |
| [**DbgTerminate**](dbgterminate.md)                   | Limpia la biblioteca de depuración.                                                                         |
| [**TipoDePresentación**](displaytype.md)                     | Envía información sobre un tipo de medio a la ubicación de salida de depuración.                                   |
| [**DumpGraph**](dumpgraph.md)                         | Envía información sobre un gráfico de filtro a la ubicación de salida de depuración.                                 |
| [**GuidNames**](guidnames.md)                         | Matriz global que contiene cadenas que representan los GUID definidos en UUID. h.                        |
| [**NAME**](name.md)                                   | Genera una cadena de solo depuración.                                                                       |
| [**Tenga en cuenta**](note.md)                                   | Envía una cadena a la ubicación de salida de depuración.                                                         |
| [**TE**](remind.md)                               | Genera un recordatorio en tiempo de compilación.                                                                |



 

**Claves del registro**

La función de salida de depuración de DirectShow usa un conjunto de claves del registro. La ubicación de estas claves del registro depende de la versión de Windows.

*Antes de Windows Vista*, las claves de depuración se encuentran en la siguiente ruta de acceso:

**HKEY \_ \_** Depuración de \\ **software** \\  de máquina local

En Windows Vista o posterior, se encuentran en la siguiente ruta de acceso:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **DirectShow** \\ **Debug**

En el caso de los filtros de terceros, la ubicación depende de la versión de las [clases base de DirectShow](directshow-base-classes.md) que se usó para generar el filtro. La versión incluida en el Windows SDK para Windows Vista utiliza la ruta de acceso más reciente. Las versiones anteriores usaban la ruta de acceso anterior.

En las notas siguientes, la etiqueta *<DebugRoot>* se usa para indicar estas dos rutas de acceso. Reemplace la ruta de acceso correcta, dependiendo de la versión de Windows o de la versión de las clases base.

**Depurar registro**

DirectShow define varios tipos de mensajes, que se muestran en la tabla siguiente.



| Value                   | Descripción                                             |
|-------------------------|---------------------------------------------------------|
| ERROR de registro \_              | Notificación de error.                                     |
| bloqueo de registro \_            | Bloqueo y desbloqueo de secciones críticas.             |
| memoria de registro \_             | Asignación de memoria y creación y destrucción de objetos. |
| tiempo de registro \_             | Medidas de tiempo y rendimiento.                    |
| seguimiento de registro \_              | Seguimiento de llamadas general.                                   |
| CUSTOM1 a través de CUSTOM5 | Disponible para mensajes de depuración personalizados                     |



 

Cada una de las funciones de registro de depuración de DirectShow especifica un tipo de mensaje y un nivel de registro. El mensaje de depuración solo se muestra cuando el nivel de depuración actual para ese tipo de mensaje es igual o mayor que el nivel especificado en la función de registro. De lo contrario, se omite el mensaje.

Por ejemplo, el código siguiente genera la cadena "This is a Debug Message" si el nivel de seguimiento del registro \_ es 3 o superior:

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Cada módulo puede establecer su propio nivel de depuración para cada tipo de mensaje. (Un *módulo* es un archivo dll o ejecutable que se puede cargar mediante la función **LoadLibrary** ). Los niveles de depuración de un módulo aparecen en el registro con la siguiente clave:

**HKEY \_ local \_ Machine**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**

donde *<Message Type>* es el tipo de mensaje menos el "Registro \_ " inicial; por ejemplo, el **bloqueo** de mensajes de bloqueo de registro \_ . Cuando se carga un módulo, la biblioteca de depuración encuentra los niveles de registro del módulo en el registro. Si las claves del registro no existen, la biblioteca de depuración las crea.

Un módulo también puede establecer sus propios niveles en tiempo de ejecución mediante la función [**DbgSetModuleLevel**](dbgsetmodulelevel.md) . Para enviar un mensaje a la salida de depuración, llame a la macro [**DbgLog**](dbglog.md) . En el ejemplo siguiente se crea un mensaje de nivel 3 de tipo \_ Trace log:

También puede especificar niveles de registro globales, con la siguiente clave del registro:


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



La biblioteca de depuración utiliza cualquier nivel mayor, el nivel global o el nivel de módulo.

**Ubicación de salida de depuración**

La ubicación de salida de depuración viene determinada por otra clave del registro:

**HKEY \_ \_Máquina local** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile**

Si el valor de esta clave es `Console` , el resultado se dirige a la ventana de la consola. Si el valor es `Deb` , `Debug` , `Debugger` o una cadena vacía, la salida va a la ventana del depurador. De lo contrario, la salida se escribe en un archivo especificado por la clave del registro.

Antes de que un ejecutable use la biblioteca de depuración de DirectShow, debe llamar a la función [**DbgInitialise**](dbginitialise.md) . Después, debe llamar a la función [**DbgTerminate**](dbgterminate.md) . No es necesario que las DLL llamen a estas funciones, ya que el punto de entrada de DLL (definido en la biblioteca de clases base) las llama automáticamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de depuración](debugging-utilities.md)
</dt> </dl>

 

 



