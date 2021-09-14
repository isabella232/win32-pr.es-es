---
description: Un objeto de trabajo permite administrar grupos de procesos como una unidad. Los objetos de trabajo son objetos intercambiables, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos.
ms.assetid: 59296384-5e78-44dd-8019-f1df6668928b
title: Objetos de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d9758faf2b66f047ca60dbba91601b202b4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375055"
---
# <a name="job-objects"></a>Objetos de trabajo

Un *objeto de trabajo* permite administrar grupos de procesos como una unidad. Los objetos de trabajo son objetos intercambiables, protegibles y compartibles que controlan los atributos de los procesos asociados a ellos. Las operaciones realizadas en un objeto de trabajo afectan a todos los procesos asociados con el objeto de trabajo. Entre los ejemplos se incluyen la aplicación de límites, como el tamaño del conjunto de trabajo y la prioridad del proceso, o la terminación de todos los procesos asociados a un trabajo.

-   [Creación de trabajos](#creating-jobs)
-   [Administración de procesos en trabajos](#managing-processes-in-jobs)
-   [Límites y notificaciones de trabajos](#job-limits-and-notifications)
-   [Contabilidad de recursos para trabajos](#resource-accounting-for-jobs)
-   [Administración de objetos de trabajo](#managing-job-objects)
-   [Administrar un árbol de procesos que usa objetos de trabajo](#managing-a-process-tree-that-uses-job-objects)

## <a name="creating-jobs"></a>Crear trabajos

Para crear un objeto de trabajo, use la [**función CreateJobObject.**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) Cuando se crea el trabajo, no hay ningún proceso asociado al trabajo.

Para asociar un proceso a un trabajo, use la [**función AssignProcessToJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) Después de asociar un proceso a un trabajo, no se puede dividir la asociación. Un proceso se puede asociar a más de un trabajo en una jerarquía de trabajos anidados. Para obtener más información, vea [Trabajos anidados.](nested-jobs.md)

**Windows 7, Windows Server 2008 R2, Windows XP con SP3, Windows Server 2008, Windows Vista y Windows Server 2003:** Un proceso solo se puede asociar a un trabajo. Los trabajos no se pueden anidar. La capacidad de anidar trabajos se agregó en Windows 8 y Windows Server 2012.

Puede especificar un descriptor de seguridad para un objeto de trabajo al llamar a la [**función CreateJobObject.**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) Para obtener más información, vea [Derechos de acceso y seguridad de objetos de trabajo.](job-object-security-and-access-rights.md)

## <a name="managing-processes-in-jobs"></a>Administración de procesos en trabajos

Una vez que un proceso está asociado a un trabajo, de forma predeterminada, los procesos secundarios que crea mediante [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) también se asocian al trabajo. (Los procesos secundarios creados [**con \_ Process.Create de Win32**](../cimwin32prov/create-method-in-class-win32-process.md) no están asociados al trabajo). Este comportamiento predeterminado se puede cambiar estableciendo el límite extendido JOB OBJECT LIMIT BREAKAWAY OK o \_ JOB OBJECT LIMIT SILENT \_ \_ \_ \_ \_ \_ \_ BREAKAWAY OK para el \_ trabajo.

-   Si el trabajo tiene el límite extendido JOB OBJECT LIMIT BREAKAWAY OK y el proceso primario se creó con la marca \_ \_ CREATE \_ \_ \_ BREAKAWAY FROM JOB, \_ \_ los procesos secundarios del proceso primario no se asocian al trabajo.
-   Si el trabajo tiene el límite extendido JOB OBJECT LIMIT SILENT BREAKAWAY OK, los procesos secundarios de cualquier proceso primario asociado al trabajo no se \_ \_ \_ \_ \_ asocian al trabajo. No es necesario que los procesos primarios se creen con la marca CREATE \_ BREAKAWAY \_ FROM \_ JOB.

Si el trabajo está anidado, la configuración de interrupción de los trabajos primarios de la jerarquía afecta a si los procesos secundarios están asociados a otro trabajo de la jerarquía. Para obtener más información, vea [Trabajos anidados.](nested-jobs.md)

Para determinar si un proceso se está ejecutando en un trabajo, use la [**función IsProcessInJob.**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)

Para finalizar todos los procesos asociados actualmente a un objeto de trabajo, use la [**función TerminateJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)

## <a name="job-limits-and-notifications"></a>Límites y notificaciones de trabajos

Un trabajo puede aplicar límites como el tamaño del conjunto de trabajo, la prioridad del proceso y el límite de tiempo de finalización del trabajo en cada proceso asociado al trabajo. Si un proceso asociado a un trabajo intenta aumentar el tamaño del conjunto de trabajo o la prioridad del proceso desde el límite establecido por el trabajo, las llamadas a la función se realizarán correctamente, pero se omitirán en modo silencioso. Un trabajo también puede establecer límites que desencadenan una notificación cuando se superan, pero permiten que el trabajo continúe en ejecución.

Para establecer los límites de un trabajo, use la [**función SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) Para obtener una lista de posibles límites que se pueden establecer para un trabajo, vea los temas siguientes:

-   [**INFORMACIÓN DE LÍMITE \_ BÁSICO \_ DE \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**RESTRICCIONES \_ \_ BÁSICAS DE LA INTERFAZ \_ DE USUARIO DE JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**INFORMACIÓN DE CONTROL DE \_ FRECUENCIA DE CPU DE \_ \_ \_ JOBOBJECT**](/windows/desktop/api/Winnt/ns-winnt-jobobject_cpu_rate_control_information)
-   [**INFORMACIÓN DE LÍMITE \_ EXTENDIDO \_ DE \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**INFORMACIÓN DEL LÍMITE \_ DE NOTIFICACIONES \_ DE \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_notification_limit_information)

Los límites de seguridad se deben establecer individualmente para cada proceso asociado a un objeto de trabajo. Para obtener más información, vea [Derechos de acceso y seguridad de procesos.](process-security-and-access-rights.md)

**Windows XP con SP3 y Windows Server 2003:** La [**función SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) se puede usar para establecer limitaciones de seguridad para todos los procesos asociados a un objeto de trabajo. A partir Windows Vista, los límites de seguridad deben establecerse individualmente para cada proceso asociado a un objeto de trabajo.

Si el trabajo está anidado, los trabajos primarios de la jerarquía influyen en el límite que se aplica para el trabajo. Para obtener más información, vea [Trabajos anidados.](nested-jobs.md)

Si el trabajo tiene un puerto de finalización de E/S asociado, puede recibir notificaciones cuando se superan determinados límites de trabajo. El sistema envía mensajes al puerto de finalización cuando se supera un límite o se producen otros eventos. Para asociar un puerto de finalización a un trabajo, use la función [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con la clase de información de objeto de trabajo **JobObjectAssociateCompletionPortInformation** y un puntero a una estructura [**JOBOBJECT \_ ASSOCIATE COMPLETION \_ \_ PORT.**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port) Es mejor hacerlo cuando el trabajo está inactivo, para reducir la posibilidad de que falten notificaciones para los procesos cuyos estados cambian durante la asociación del puerto de finalización.

Todos los mensajes se envían directamente desde el trabajo como si el trabajo hubiera llamado a la [**función PostQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-postqueuedcompletionstatus) Un subproceso debe supervisar el puerto de finalización mediante [**la función GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para recoger los mensajes. Tenga en cuenta que, a excepción de los límites establecidos con la clase de información **JobObjectNotificationLimitInformation,** no se garantiza la entrega de mensajes al puerto de finalización; El error de que llegue un mensaje no significa necesariamente que no se produzca el evento. Se garantiza que las notificaciones de los límites **establecidos con JobObjectNotificationLimitInformation** lleguen al puerto de finalización. Para obtener una lista de posibles mensajes, [**vea JOBOBJECT \_ ASSOCIATE COMPLETION \_ \_ PORT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-jobs"></a>Contabilidad de recursos para trabajos

El objeto de trabajo registra información de contabilidad básica para todos sus procesos asociados, incluidos los que han finalizado. Para recuperar esta información de contabilidad, use la [**función QueryInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) Para obtener una lista de la información de contabilidad que se mantiene para un trabajo, vea los temas siguientes:

-   [**INFORMACIÓN DE CONTABILIDAD BÁSICA DE JOBOBJECT \_ \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**INFORMACIÓN BÁSICA Y \_ \_ DE CONTABILIDAD DE \_ E/S \_ DE \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)

Si el objeto de trabajo está anidado, la información de contabilidad de cada trabajo secundario se agrega en su trabajo primario. Para obtener más información, vea [Trabajos anidados.](nested-jobs.md)

## <a name="managing-job-objects"></a>Administración de objetos de trabajo

El estado de un objeto de trabajo se establece en señalado cuando se finalizan todos sus procesos porque se ha superado el límite de tiempo de finalización del trabajo especificado. Use [**WaitForSingleObject o**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) para supervisar el objeto de trabajo para este evento.

Para obtener un identificador para un objeto de trabajo existente, use la función [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) y especifique el nombre dado al objeto cuando se creó. Solo se pueden abrir objetos de trabajo con nombre.

Para cerrar un identificador de objeto de trabajo, use la [**función CloseHandle.**](/windows/win32/api/handleapi/nf-handleapi-closehandle) El trabajo se destruye cuando se ha cerrado su último identificador y se han terminado todos los procesos asociados. Sin embargo, si el trabajo tiene especificada la marca JOB OBJECT LIMIT KILL ON JOB CLOSE, al cerrar el último identificador de objeto de trabajo se finalizan todos los procesos asociados y, a continuación, se destruye el propio objeto de \_ \_ \_ \_ \_ \_ trabajo. Si un trabajo anidado tiene especificada la marca JOB OBJECT LIMIT KILL ON JOB CLOSE, al cerrar el último identificador de objeto de trabajo se finalizan todos los procesos asociados al trabajo y sus trabajos secundarios en la \_ \_ \_ \_ \_ \_ jerarquía.

## <a name="managing-a-process-tree-that-uses-job-objects"></a>Administrar un árbol de procesos que usa objetos de trabajo

A partir Windows 8 y Windows Server 2012, una aplicación [](nested-jobs.md) puede usar trabajos anidados para administrar un árbol de procesos que usa más de un objeto de trabajo. Sin embargo, una aplicación que se debe ejecutar en Windows 7, Windows Server 2008 R2 o versiones anteriores de Windows que no admiten trabajos anidados debe administrar el árbol de procesos de otras maneras.

Si una herramienta debe administrar un árbol de procesos que usa objetos de trabajo y no es posible usar trabajos anidados, tanto la herramienta como los miembros del árbol de procesos deben colaborar. Use una de las siguientes opciones:

-   Use el límite JOB \_ OBJECT \_ LIMIT SILENT \_ \_ BREAKAWAY \_ OK. Si la herramienta usa este límite, no puede supervisar un árbol de procesos completo. La herramienta solo puede supervisar los procesos que agrega al trabajo. Si estos procesos crean procesos secundarios, no están asociados al trabajo. En esta opción, los procesos secundarios se pueden asociar a otros objetos de trabajo.
-   Use el límite JOB \_ OBJECT \_ LIMIT \_ BREAKAWAY \_ OK. Si la herramienta usa este límite, puede supervisar todo el árbol de procesos, excepto aquellos procesos que cualquier miembro del árbol se interrumpe explícitamente del árbol. Un miembro del árbol puede crear un proceso secundario en un nuevo objeto de trabajo llamando a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) con la marca CREATE BREAKAWAY FROM JOB y, a continuación, llamando a \_ la función \_ \_ [**AssignProcessToJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) De lo contrario, el miembro debe controlar los casos en los que Se produce un error **en AssignProcessToJobObject.**

    La marca CREATE BREAKAWAY FROM JOB no tiene ningún efecto si la herramienta no \_ \_ supervisa el \_ árbol. Por lo tanto, esta es la opción preferida, pero requiere conocimientos avanzados de los procesos que se supervisan.

-   Para evitar las interrupciones de cualquier tipo, no se establece el límite DE INTERRUPCIÓN DE JOB OBJECT LIMIT OK ni el límite JOB \_ \_ OBJECT LIMIT SILENT \_ \_ \_ \_ \_ \_ BREAKAWAY \_ OK. En esta opción, la herramienta puede supervisar todo el árbol de procesos. Sin embargo, si un proceso secundario intenta asociarse a sí mismo o a otro proceso secundario con un trabajo mediante una llamada a [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject), se producirá un error en la llamada. Si el proceso se diseñó para asociarse a un trabajo específico, este error puede impedir que el proceso funcione correctamente.

 

 
