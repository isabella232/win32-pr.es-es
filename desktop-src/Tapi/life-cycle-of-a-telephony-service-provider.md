---
description: En este tema se proporciona una revisión de alto nivel de las operaciones de TSP.
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: Ciclo de vida de un proveedor de servicios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830bc16ca606bb5bd38c4bce7c1e6e39dadb65a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568636"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>Ciclo de vida de un proveedor de servicios de telefonía

En este tema se proporciona una revisión de alto nivel de las operaciones de TSP.

Una sesión es el tiempo durante el cual una determinada configuración sigue siendo válida y las operaciones de telefonía se llevan a cabo. Un proveedor de servicios puede admitir muchas sesiones entre el momento en que se carga por primera vez y el momento en que se libera. En cada sesión, TAPI negocia la versión de la interfaz, inicia la sesión, lleva a cabo las operaciones y finalmente cierra la sesión. El proveedor de servicios no debe conservar la información de una sesión a la siguiente.

Una vez conocida la versión de la interfaz, TAPI llama a la función [**\_ ProviderInit de TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) para establecer todos los parámetros operativos. Se garantiza que toda la información de configuración del registro es estable cuando se llama a la función providerInit de **TSPI \_** . La mayoría de los proveedores de servicios leen toda la información de configuración en ese momento.

Las operaciones normales pueden continuar en cualquier orden, una vez inicializado el proveedor de servicios.

TAPI negocia información específica del dispositivo en cada dispositivo. TAPI y el proveedor de servicios se confirman en una versión cuando se abre un dispositivo.

El proveedor de servicios puede recibir solicitudes para seleccionar y cancelar versiones de extensión. Mientras se selecciona una versión de la extensión, el dispositivo funciona estrictamente según la versión de la extensión específica del dispositivo.

La negociación de una versión de extensión específica del dispositivo puede producirse varias veces, tanto antes como después de que se abra el dispositivo. TAPI pasa un intervalo de versiones, y el proveedor de servicios elige y devuelve un valor de este intervalo. Normalmente, el proveedor de servicios tiene deshabilitadas las extensiones específicas del dispositivo.

Esto confirma que TAPI y el proveedor de servicios operan en ese nivel de versión de la extensión hasta que se cancele la selección. Durante el tiempo que una extensión específica del dispositivo está en vigor, un intento de negociar un nivel de versión de la extensión debería permitir solo el nivel de versión que está actualmente en vigor. Una vez cancelada la extensión específica del dispositivo, se puede negociar y seleccionar una versión diferente.

Las operaciones telefónicas dentro del par **abrir/cerrar** se muestran en la siguiente ilustración. Algunas de estas operaciones son sincrónicas, otras son asincrónicas. Si una operación se completa de forma asincrónica, se puede solicitar otra operación antes de que se complete el primer informe. Por lo tanto, las operaciones se pueden superponer de cualquier manera. Finalmente, el proveedor de servicios debe notificar la finalización de cualquier operación asincrónica solicitada. Cerrar un teléfono fuerza la finalización de las operaciones asincrónicas pendientes (posiblemente con una indicación de "error").

El ciclo de vida de los dispositivos de línea es similar al del ciclo de vida de los teléfonos, salvo que las líneas tienen sus propios procedimientos de negociación, inicialización, apertura y cierre. Las operaciones en líneas abiertas están entre corchetes por su propio par de **apertura y cierre** . Este par está entre corchetes entre el mismo par de **inicialización y cierre** que el teléfono **abierto/cierre**.

Los ciclos de vida de las llamadas se **encierran estrictamente entre el abrir o cerrar** la línea que los contiene. La duración de las llamadas puede comenzar de varias maneras:

-   Solicitado desde TAPI a través de funciones como [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)o [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference).
-   Se originó espontáneamente en el proveedor de servicios como nuevas llamadas entrantes, llamadas iniciadas por el usuario en un auricular telefónico conectado o llamadas generadas como un efecto secundario de otras operaciones, como poner en espera una llamada existente.

Las duraciones de las distintas llamadas dentro de la misma línea pueden superponerse entre sí de cualquier manera. Todas las llamadas finalizan su duración en el momento en que se invoca la función TSPI [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) . En la ilustración siguiente se muestra el ciclo de vida de varias llamadas.

![ciclos de vida de las llamadas superpuestas](images/modell.png)

Una llamada puede originarse en TAPI, tal y como se muestra en el par **MakeCall/CloseCall** . También se puede originar una llamada en el proveedor de servicios. El proveedor de servicios anuncia esto con un mensaje de [**línea \_ NEWCALL**](line-newcall.md) a un procedimiento de devolución de llamada proporcionado por TAPI. En tal caso, TAPI devuelve su identificador para la llamada, que se incluye en las devoluciones de llamada subsiguientes que se producen en la llamada. En el caso de las llamadas cuya duración se origina en TAPI, este identificador se incluye en la operación TSPI que crea la llamada.

Todas las operaciones que inician la duración de una llamada provocan que TAPI y el proveedor de servicios intercambien identificadores para la nueva llamada. En el caso de las llamadas originadas por TAPI, TAPI pasa su identificador y recibe el identificador del proveedor de servicios como parámetro de devolución. En el caso de que la llamada se origine en el proveedor de servicios, el proveedor de servicios pasa su identificador a TAPI y recibe el identificador de TAPI como parámetro de devolución.

En la ilustración siguiente se ofrece una vista de alto nivel de la instalación, configuración y eliminación de un proveedor de servicios. secuencias del ciclo de vida que abarcan muchas sesiones. El ciclo de vida típico para estas operaciones se puede mostrar con la siguiente línea de tiempo.

![instalación, configuración y eliminación de proveedores de servicios](images/model2.png)

Se muestra el ciclo de vida de instalación y eliminación típico, que abarca varias sesiones. Las llamadas a los procedimientos **install** y [**Remove**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) se emparejan estrictamente y no se superponen. Las llamadas al procedimiento de **configuración** pueden ocurrir varias veces dentro de este par. Normalmente, el proveedor de servicios realiza una como efecto secundario del procedimiento de **instalación** para crear entradas de línea y de teléfono. Se puede llamar al procedimiento de **configuración** en otros momentos para modificar una configuración existente. El procedimiento de **instalación** debe realizarse antes de que se permita cualquier otra función TSPI. En el escenario ideal, todas las sesiones están estrictamente anidadas dentro del par de procedimientos de **instalación o eliminación** .

Las funciones [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall), [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)y [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) interactúan con el propio proveedor de servicios en lugar de con cualquier dispositivo específico. Afectan a la información de configuración estática que sobrevive en varias sesiones y deben estar presentes para que cualquier otra operación pueda continuar. Por lo tanto, todas las demás operaciones se anidan entre la invocación de **TSPI \_ providerInstall** y la finalización de su **\_ providerRemove TSPI** correspondiente. Normalmente, estas dos operaciones se realizan muy lejos, lo que es más probable en una carga diferente del proveedor de servicios o un arranque diferente del equipo. Llamar a la función de **configuración** externamente es opcional, porque el procedimiento de **instalación** es necesario para incluir el comportamiento de **configuración** además de los suyos propios. La razón habitual para llamarla externamente es modificar una configuración existente.

En el concepto de la finalización de una operación de [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) , se inserta un detalle. Es conveniente permitir que el usuario ejecute la utilidad del panel de control de telefonía suministrada con el servicio de telefonía para modificar las configuraciones del proveedor de servicios, incluso cuando las operaciones de telefonía (sesiones) están en curso. Por consiguiente, las especificaciones [**TSPI \_ ProviderConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) y **TSPI \_ providerRemove** permiten la invocación mientras hay una sesión pendiente. Sin embargo, es necesario retrasar cualquier cambio en la configuración hasta que las operaciones de telefonía se cierren y se reinicien. Por lo tanto, la finalización de cualquier operación **TSPI \_ ProviderConfig** o **TSPI \_ providerRemove** se produce fuera de cualquier sesión. El anidamiento de acciones es como se muestra en la ilustración, aunque las llamadas a procedimientos pueden aparecer en un orden ligeramente diferente. Se permite a un proveedor de servicios simplemente deshabilitar la **configuración** o [**quitar**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) mientras se están realizando las operaciones, aunque se debe notificar al usuario con un cuadro de diálogo. Se prefiere una implementación más fácil de usar que permita al menos un subconjunto de operaciones.

Estas operaciones de **instalación**, **configuración** y [**eliminación**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) tienen el efecto secundario de señalar cualquier aplicación de telefonía en ejecución, lo que finalmente da lugar a que se cierre el uso del servicio de telefonía. Juntos, finaliza todas las sesiones pendientes para los proveedores de servicios. Esto significa que los proveedores de servicios deben leer la nueva configuración del registro cuando se inician las nuevas sesiones. Todos los cambios pendientes debidos a una **configuración** o una [**eliminación**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) mientras se estaban realizando las operaciones en curso se aplican.

 

 
