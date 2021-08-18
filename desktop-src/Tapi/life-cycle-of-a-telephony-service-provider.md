---
description: En este tema se proporciona una revisión de alto nivel de las operaciones de TSP.
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: Ciclo de vida de un proveedor de servicios de telefonía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6282f4e7b946ffb79bd6233688869616cc0b0259a1d491834452290474c552a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012714"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>Ciclo de vida de un proveedor de servicios de telefonía

En este tema se proporciona una revisión de alto nivel de las operaciones de TSP.

Una sesión es el tiempo durante el que una configuración determinada sigue siendo válida y se realizan operaciones de telefonía. Un proveedor de servicios puede admitir muchas sesiones entre el momento en que se carga por primera vez y cuando finalmente se libera. Para cada sesión, TAPI negocia la versión de la interfaz, inicia la sesión, realiza operaciones y, finalmente, cierra la sesión. El proveedor de servicios no debe conservar la información de una sesión a la siguiente.

Una vez conocida la versión de la interfaz, TAPI llama a la [**función \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) de TSPI para establecer todos los parámetros operativos. El proveedor de servicios se asegura de que toda la información de configuración del Registro es estable cuando se llama a la función **\_ providerInit de TSPI.** La mayoría de los proveedores de servicios leen toda la información de configuración en ese momento.

Las operaciones normales pueden continuar en cualquier orden, después de inicializar el proveedor de servicios.

TAPI negocia la información específica del dispositivo por dispositivo. TAPI y el proveedor de servicios se confirman en una versión cuando se abre un dispositivo.

El proveedor de servicios puede recibir solicitudes para seleccionar y cancelar versiones de extensión. Mientras se selecciona una versión de extensión, el dispositivo funciona estrictamente según esa versión de extensión específica del dispositivo.

La negociación de una versión de extensión específica del dispositivo puede producirse varias veces, tanto antes como después de abrir el dispositivo. TAPI pasa un intervalo de versiones y el proveedor de servicios elige y devuelve un valor de este intervalo. Normalmente, el proveedor de servicios tiene deshabilitadas las extensiones específicas del dispositivo.

Esto confirma que TAPI y el proveedor de servicios funcionan en ese nivel de versión de extensión hasta que se cancela la selección. Durante el tiempo en que una extensión específica del dispositivo está en vigor, un intento de negociar un nivel de versión de extensión solo debe permitir el nivel de versión que está actualmente en vigor. Una vez cancelada la extensión específica del dispositivo, se puede negociar y seleccionar una versión diferente.

Teléfono operaciones dentro del par **Abrir/Cerrar** se muestran en la ilustración siguiente. Algunas de estas operaciones son sincrónicas y otras son asincrónicas. Si una operación se completa de forma asincrónica, se puede solicitar otra operación antes de que la primera informe de la finalización. Por lo tanto, las operaciones se pueden superponer de cualquier manera. El proveedor de servicios debe notificar finalmente la finalización de cualquier operación asincrónica solicitada. El cierre de un teléfono obliga a que se completen las operaciones asincrónicas pendientes (posiblemente con una indicación de "error").

El ciclo de vida de los dispositivos de línea es similar al ciclo de vida de los teléfonos, salvo que las líneas tienen sus propios procedimientos de negociación, inicialización, apertura y cierre. Las operaciones en líneas abiertas están entre corchetes por su propio par **Abrir/Cerrar.** Este par está entre corchetes entre el mismo par **inicialización/apagado** que el teléfono **Abrir/Cerrar.**

Los ciclos de vida de las llamadas están entre corchetes estrictamente entre la apertura **y cierre** de la línea que las contiene. Las duraciones de las llamadas pueden comenzar de varias maneras:

-   Se solicita desde TAPI a través de funciones como [**lineMakeCall,**](/windows/win32/api/tapi/nf-tapi-linemakecall) [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)o [**lineSetupConference.**](/windows/win32/api/tapi/nf-tapi-linesetupconference)
-   Se originó en el proveedor de servicios como nuevas llamadas entrantes, llamadas iniciadas por el usuario en un teléfono conectado o llamadas generadas como efecto secundario de otras operaciones, como poner en espera una llamada existente.

Las duraciones de llamadas distintas dentro de la misma línea pueden superponerse entre sí de cualquier manera. Todas las llamadas finalizan su duración en el momento en que se invoca la función [**TSPI \_ lineCloseCall de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) El ciclo de vida de varias llamadas se muestra en la ilustración siguiente.

![ciclos de vida de llamadas superpuestas](images/modell.png)

Una llamada se puede originar en TAPI como se muestra con el **par MakeCall/CloseCall.** Una llamada también se puede originar en el proveedor de servicios. El proveedor de servicios lo anuncia con un [**mensaje \_ LINE NEWCALL**](line-newcall.md) a un procedimiento de devolución de llamada proporcionado por TAPI. En tal caso, TAPI devuelve su identificador para la llamada, que se incluye en las devoluciones de llamada posteriores que informan de los eventos que se producen en la llamada. En el caso de las llamadas cuya duración se origina en TAPI, este identificador se incluye en la operación TSPI que crea la llamada.

Todas las operaciones que inician la duración de una llamada tienen como resultado que TAPI y el proveedor de servicios intercambian identificadores para la nueva llamada. En el caso de las llamadas originadas por TAPI, TAPI pasa su identificador y recibe el identificador del proveedor de servicios como parámetro de devolución. En el caso de que la llamada se origine en el proveedor de servicios, el proveedor de servicios pasa su identificador a TAPI y recibe el identificador TAPI como parámetro de retorno.

En la ilustración siguiente se ofrece una vista muy general de la instalación, configuración y eliminación del proveedor de servicios. secuencias de ciclo de vida que abarcan muchas sesiones. El ciclo de vida típico de estas operaciones se puede mostrar con la siguiente línea de tiempo.

![instalación, configuración y eliminación del proveedor de servicios](images/model2.png)

Se muestra el ciclo de vida de instalación y eliminación típico, que abarca varias sesiones. Las llamadas a **los procedimientos Install** [**y Remove**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) están emparejadas estrictamente y no se superponen. Las llamadas al **procedimiento Config** pueden producirse varias veces dentro de este par. Normalmente, el proveedor de servicios realiza una operación como efecto secundario interno del procedimiento **de** instalación para crear entradas de línea y teléfono. Se **puede** llamar al procedimiento Config en otras ocasiones para modificar una instalación existente. El **procedimiento de** instalación debe realizarse antes de permitir cualquier otra función TSPI. En el escenario ideal, todas las sesiones se anidan estrictamente dentro del par **de procedimientos Install/Remove.**

Las funciones [**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall), [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)y [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) interactúan con el propio proveedor de servicios en lugar de con cualquier dispositivo específico. Afectan a la información de configuración estática que sobrevive en varias sesiones y debe estar presente para que cualquier otra operación continúe. Por lo tanto, todas las demás operaciones se anidan entre la invocación del proveedor **\_ TSPIInstall** y la finalización de su proveedor **de TSPI \_ correspondienteRemove**. Estas dos operaciones suelen producirse muy separadas, lo más probable es que se deba a una carga diferente del proveedor de servicios o a un arranque diferente de la máquina. Llamar **externamente a** la función Config es opcional, ya que el procedimiento **de** instalación es necesario para incluir el comportamiento **Config** además del suyo propio. El motivo habitual para llamarlo externamente es modificar una configuración existente.

Hay una sutilidad incrustada en el concepto de la finalización de una operación [**\_ providerRemove de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) Es conveniente permitir que el usuario ejecute la utilidad De telefonía Panel de control suministrada con el servicio de telefonía para modificar las configuraciones del proveedor de servicios, incluso cuando las operaciones de telefonía (sesiones) están en curso. Por lo tanto, las especificaciones providerConfig y **TSPI \_ providerRemove** permiten la invocación mientras hay una sesión pendiente. [**\_**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) Sin embargo, los cambios en la configuración deben retrasarse hasta que se apaguen y reinicien las operaciones de telefonía. Por lo tanto, estrictamente hablando, la finalización de cualquier operación **\_ providerConfig** o **TSPI \_ providerRemove** de TSPI se produce fuera de cualquier sesión. El anidamiento de acciones es como se muestra en la ilustración, aunque las llamadas a procedimientos pueden aparecer en un orden ligeramente diferente. Se permite que un proveedor de servicios [](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) simplemente no permita **la** configuración o la eliminación mientras las operaciones están en curso, aunque el usuario debe recibir una notificación con un cuadro de diálogo. Se prefiere una implementación más fácil de usar que permita al menos un subconjunto de operaciones.

Estas **operaciones de** [](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) instalación, **configuración** y eliminación tienen el efecto secundario de señalizar las aplicaciones de telefonía en ejecución, lo que finalmente provoca que cierren su uso del servicio de telefonía. Juntos, finalizan todas las sesiones pendientes para los proveedores de servicios. Esto significa a los proveedores de servicios que deben leer la nueva configuración del Registro cuando se inician nuevas sesiones. Los cambios que estaban pendientes debido a una **configuración o** a [**la**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) eliminación mientras las operaciones estaban en curso se acomete.

 

 
