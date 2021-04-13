---
description: Un objeto de trabajo permite administrar grupos de procesos como una unidad. Los objetos de trabajo son objetos Namable, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos.
ms.assetid: 59296384-5e78-44dd-8019-f1df6668928b
title: Objetos de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d9758faf2b66f047ca60dbba91601b202b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360693"
---
# <a name="job-objects"></a>Objetos de trabajo

Un *objeto de trabajo* permite administrar grupos de procesos como una unidad. Los objetos de trabajo son objetos Namable, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos. Las operaciones realizadas en un objeto de trabajo afectan a todos los procesos asociados con el objeto de trabajo. Entre los ejemplos se incluyen la aplicación de límites, como el tamaño del espacio de trabajo y la prioridad del proceso, o la finalización de todos los procesos asociados a un trabajo.

-   [Crear trabajos](#creating-jobs)
-   [Administrar procesos en trabajos](#managing-processes-in-jobs)
-   [Límites del trabajo y notificaciones](#job-limits-and-notifications)
-   [Contabilidad de recursos para trabajos](#resource-accounting-for-jobs)
-   [Administrar objetos de trabajo](#managing-job-objects)
-   [Administrar un árbol de procesos que usa objetos de trabajo](#managing-a-process-tree-that-uses-job-objects)

## <a name="creating-jobs"></a>Crear trabajos

Para crear un objeto de trabajo, utilice la función [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Cuando se crea el trabajo, no se asocia ningún proceso con el trabajo.

Para asociar un proceso a un trabajo, use la función [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) . Una vez que un proceso está asociado a un trabajo, no se puede interrumpir la asociación. Un proceso se puede asociar a más de un trabajo en una jerarquía de trabajos anidados. Para obtener más información, vea [trabajos anidados](nested-jobs.md).

**Windows 7, Windows server 2008 R2, Windows XP con SP3, Windows server 2008, Windows Vista y Windows server 2003:** Un proceso solo se puede asociar a un trabajo. Los trabajos no se pueden anidar. La capacidad de anidar trabajos se agregó en Windows 8 y Windows Server 2012.

Puede especificar un descriptor de seguridad para un objeto de trabajo cuando llame a la función [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Para obtener más información, vea [seguridad de objetos de trabajo y derechos de acceso](job-object-security-and-access-rights.md).

## <a name="managing-processes-in-jobs"></a>Administrar procesos en trabajos

Una vez que un proceso está asociado a un trabajo, de forma predeterminada, todos los procesos secundarios que crea mediante [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) también se asocian con el trabajo. (Los procesos secundarios creados mediante el [**proceso de Win32 \_ . Create**](../cimwin32prov/create-method-in-class-win32-process.md) no están asociados con el trabajo). Este comportamiento predeterminado se puede cambiar estableciendo el límite de objetos de trabajo de límite extendido \_ \_ \_ \_ Aceptar o \_ el \_ límite \_ de objetos de trabajo separación silenciosa \_ \_ correcto para el trabajo.

-   Si el trabajo tiene la separación del límite de objetos de trabajo de límite extendido \_ \_ \_ \_ correcto y el proceso primario se creó con la \_ marca crear separación \_ de \_ trabajo, los procesos secundarios del proceso primario no están asociados con el trabajo.
-   Si el trabajo tiene la \_ \_ \_ separación silenciosa límite de objetos \_ de trabajo de límite extendido \_ correcto, los procesos secundarios de cualquier proceso primario asociado con el trabajo no están asociados con el trabajo. No es necesario crear procesos primarios con la \_ marca crear separación desde el \_ \_ trabajo.

Si el trabajo está anidado, la configuración de separación de los trabajos primarios de la jerarquía afecta a si los procesos secundarios están asociados a otro trabajo en la jerarquía. Para obtener más información, vea [trabajos anidados](nested-jobs.md).

Para determinar si un proceso se está ejecutando en un trabajo, utilice la función [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob) .

Para finalizar todos los procesos asociados actualmente a un objeto de trabajo, utilice la función [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) .

## <a name="job-limits-and-notifications"></a>Límites del trabajo y notificaciones

Un trabajo puede exigir límites, como el tamaño del espacio de trabajo, la prioridad del proceso y el límite de tiempo del trabajo final de cada proceso asociado con el trabajo. Si un proceso asociado a un trabajo intenta aumentar su tamaño de espacio de trabajo o la prioridad del proceso desde el límite establecido por el trabajo, las llamadas de función se realizan correctamente pero se omiten de forma silenciosa. Un trabajo también puede establecer los límites que desencadenan una notificación cuando se superan, pero permiten que el trabajo continúe ejecutándose.

Para establecer los límites de un trabajo, use la función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) . Para obtener una lista de posibles límites que se pueden establecer para un trabajo, vea los temas siguientes:

-   [**\_información de \_ límite \_ básico de JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**restricciones de la \_ \_ interfaz de usuario básica de JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**\_información de \_ control de velocidad de CPU de JOBOBJECT \_ \_**](/windows/desktop/api/Winnt/ns-winnt-jobobject_cpu_rate_control_information)
-   [**JOBOBJECT \_ \_ información de límite extendido \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_información de \_ límite de notificación de JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_notification_limit_information)

Los límites de seguridad deben establecerse individualmente para cada proceso asociado a un objeto de trabajo. Para obtener más información, consulte [seguridad de procesos y derechos de acceso](process-security-and-access-rights.md).

**Windows XP con SP3 y Windows Server 2003:** La función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) se puede usar para establecer limitaciones de seguridad para todos los procesos asociados a un objeto de trabajo. A partir de Windows Vista, los límites de seguridad se deben establecer individualmente para cada proceso asociado a un objeto de trabajo.

Si el trabajo está anidado, los trabajos primarios de la jerarquía influyen en el límite que se aplica para el trabajo. Para obtener más información, vea [trabajos anidados](nested-jobs.md).

Si el trabajo tiene un puerto de finalización de e/s asociado, puede recibir notificaciones cuando se superan determinados límites de trabajo. El sistema envía mensajes al puerto de finalización cuando se supera un límite o cuando se producen otros eventos. Para asociar un puerto de finalización a un trabajo, use la función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la clase de información de objeto de trabajo **JobObjectAssociateCompletionPortInformation** y un puntero a una estructura de [**\_ \_ \_ Puerto de finalización de JOBOBJECT asociada**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port) . Es mejor hacerlo cuando el trabajo está inactivo, para reducir la posibilidad de que falten notificaciones para los procesos cuyos Estados cambian durante la Asociación del puerto de finalización.

Todos los mensajes se envían directamente desde el trabajo como si el trabajo hubiera llamado a la función [**PostQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-postqueuedcompletionstatus) . Un subproceso debe supervisar el puerto de finalización mediante la función [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para recoger los mensajes. Tenga en cuenta que, con la excepción de los límites establecidos con la clase de información **JobObjectNotificationLimitInformation** , no se garantiza la entrega de mensajes al puerto de finalización. el hecho de que llegue un mensaje no implica necesariamente que no se haya producido el evento. Se garantiza que las notificaciones de los límites establecidos con **JobObjectNotificationLimitInformation** llegan al puerto de finalización. Para obtener una lista de los posibles mensajes, consulte [**JOBOBJECT \_ Associate \_ Complete \_ Port**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-jobs"></a>Contabilidad de recursos para trabajos

El objeto de trabajo registra información básica de cuentas de todos sus procesos asociados, incluidos los que han terminado. Para recuperar esta información de cuentas, utilice la función [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) . Para obtener una lista de la información de cuentas que se mantiene para un trabajo, vea los temas siguientes:

-   [**\_información básica de \_ cuentas \_ de JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**\_ \_ información de cuentas básica y de \_ e/s de \_ JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)

Si el objeto de trabajo está anidado, la información de cuentas de cada trabajo secundario se agrega en su trabajo primario. Para obtener más información, vea [trabajos anidados](nested-jobs.md).

## <a name="managing-job-objects"></a>Administrar objetos de trabajo

El estado de un objeto de trabajo se establece en señalizado cuando todos sus procesos finalizan porque se ha superado el límite de tiempo de final de trabajo especificado. Use [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) o [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) para supervisar el objeto de trabajo para este evento.

Para obtener un identificador para un objeto de trabajo existente, use la función [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) y especifique el nombre asignado al objeto cuando se creó. Solo se pueden abrir objetos de trabajo con nombre.

Para cerrar un identificador de objeto de trabajo, utilice la función [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) . El trabajo se destruye cuando se ha cerrado su último identificador y se han finalizado todos los procesos asociados. Sin embargo, si el trabajo tiene la \_ \_ marca de límite \_ de objetos de trabajo para el \_ \_ cierre del trabajo \_ especificado, al cerrar el último identificador de objeto de trabajo se finalizan todos los procesos asociados y, a continuación, se destruye el propio objeto de trabajo. Si un trabajo anidado tiene la \_ marca de \_ límite \_ de objetos de trabajo limitado en el cierre del \_ \_ trabajo \_ especificada, al cerrar el último identificador de objeto de trabajo se finalizan todos los procesos asociados con el trabajo y sus trabajos secundarios en la jerarquía.

## <a name="managing-a-process-tree-that-uses-job-objects"></a>Administrar un árbol de procesos que usa objetos de trabajo

A partir de Windows 8 y Windows Server 2012, una aplicación puede usar [trabajos anidados](nested-jobs.md) para administrar un árbol de procesos que usa más de un objeto de trabajo. Sin embargo, una aplicación que se debe ejecutar en Windows 7, Windows Server 2008 R2 o versiones anteriores de Windows que no admiten trabajos anidados debe administrar el árbol de procesos de otras maneras.

Si una herramienta debe administrar un árbol de procesos que usa objetos de trabajo y no es posible utilizar trabajos anidados, la herramienta y los miembros del árbol de procesos deben cooperar. Use una de las siguientes opciones:

-   Use el \_ límite de \_ \_ separación silenciosa del límite de objetos \_ de trabajo \_ . Si la herramienta utiliza este límite, no puede supervisar un árbol de procesos completo. La herramienta solo puede supervisar los procesos que agrega al trabajo. Si estos procesos crean procesos secundarios, no se asocian con el trabajo. En esta opción, los procesos secundarios pueden asociarse a otros objetos de trabajo.
-   Use el límite de separación de límite de objetos de trabajo \_ \_ \_ \_ correcto. Si la herramienta utiliza este límite, puede supervisar el árbol de procesos completo, excepto aquellos procesos que cualquier miembro del árbol interrumpa explícitamente en el árbol. Un miembro del árbol puede crear un proceso secundario en un nuevo objeto de trabajo mediante una llamada a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) con la \_ marca crear separación desde el \_ \_ trabajo y, a continuación, llamar a la función [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) . De lo contrario, el miembro debe controlar los casos en los que **AssignProcessToJobObject** produce un error.

    La \_ marca crear separación \_ de \_ trabajo no tiene ningún efecto si la herramienta no está supervisando el árbol. Por lo tanto, esta es la opción preferida, pero requiere un conocimiento avanzado de los procesos que se están supervisando.

-   Evite las escisión de cualquier tipo si no establece la \_ separación de límite de objetos de trabajo \_ \_ \_ correcta ni el límite de objetos de trabajo \_ límite de \_ \_ separación silenciosa \_ \_ . En esta opción, la herramienta puede supervisar todo el árbol de procesos. Sin embargo, si un proceso secundario intenta asociarse a sí mismo o a otro proceso secundario con un trabajo mediante una llamada a [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject), se producirá un error en la llamada. Si el proceso se ha diseñado para asociarse a un trabajo específico, este error puede impedir que el proceso funcione correctamente.

 

 
