---
description: Una aplicación puede usar trabajos anidados para administrar subconjuntos de procesos. Los trabajos anidados también habilitan una aplicación que usa trabajos para hospedar otras aplicaciones que también usan trabajos.
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: Trabajos anidados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf105c70ec8e83b395fcce56c6274d4838358bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375022"
---
# <a name="nested-jobs"></a>Trabajos anidados

Una aplicación puede usar trabajos anidados para administrar subconjuntos de procesos. Los trabajos anidados también habilitan una aplicación que usa trabajos para hospedar otras aplicaciones que también usan trabajos.

**Windows 7, Windows Server 2008 R2, Windows XP con SP3, Windows Server 2008, Windows Vista y Windows Server 2003:** Un proceso solo se puede asociar a un único trabajo. Los trabajos anidados se introdujeron en Windows 8 y Windows Server 2012.

En este tema se proporciona información general sobre el anidamiento de trabajos y el comportamiento de los trabajos anidados:

-   [Jerarquías de trabajos anidados](#nested-job-hierarchies)
-   [Crear una jerarquía de trabajos anidados](#creating-a-nested-job-hierarchy)
-   [Límites y notificaciones de trabajos para trabajos anidados](#job-limits-and-notifications-for-nested-jobs)
-   [Contabilidad de recursos para trabajos anidados](#resource-accounting-for-nested-jobs)
-   [Finalización de trabajos anidados](#termination-of-nested-jobs)

Para obtener información general sobre los trabajos y los objetos de trabajo, vea [Objetos de trabajo](job-objects.md).

## <a name="nested-job-hierarchies"></a>Jerarquías de trabajos anidados

Los trabajos anidados tienen una relación de elementos primarios y secundarios en la que cada trabajo secundario contiene un subconjunto de los procesos de su trabajo primario. Si se agrega un proceso que ya está en un trabajo a otro trabajo, los trabajos se anidan de forma predeterminada si el sistema puede formar una jerarquía de trabajos válida y ninguno de ellos establece límites de interfaz de usuario [**(SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) **con JobObjectBasicUIRestrictions).**

En la figura 1 se muestra una jerarquía de trabajos que contiene un árbol de procesos etiquetados de P0 a P7. El trabajo 1 es *el trabajo primario* del trabajo 2 y el trabajo 4, y es un *antecesor* del trabajo 3. El trabajo 2 es *el elemento primario inmediato* del trabajo 3; El trabajo 3 es *el elemento secundario inmediato* del trabajo 2. Los trabajos 1, 2 y  3 forman una cadena de trabajos en la que los trabajos 1 y 2 son la cadena de trabajos primaria *del* trabajo 3. El trabajo final de una cadena de trabajos es *el trabajo inmediato* de los procesos de ese trabajo. En la figura 1, el trabajo 3 es el trabajo inmediato de los procesos P2, P3 y P4.

![Figura 1. una jerarquía de trabajos anidados que contiene un árbol de procesos](images/nested-jobs-a.png)

Los trabajos anidados también se pueden usar para administrar grupos de procesos del mismo nivel. En la jerarquía de trabajos que se muestra en la figura 2, el trabajo 1 es el trabajo primario del trabajo 2. Tenga en cuenta que una jerarquía de trabajos puede contener solo una parte de un árbol de procesos. En la figura 2, P0 no está en la jerarquía, pero sus procesos secundarios son de P1 a P5.

![Figura 2. una jerarquía de trabajos anidados que contiene procesos del mismo nivel](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>Crear una jerarquía de trabajos anidados

Los procesos de una jerarquía de trabajos se asocian explícitamente a un objeto de trabajo mediante la función [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) o se asocian implícitamente durante la creación del proceso, igual que para los trabajos independientes. El orden en que se crean los trabajos y se asignan los procesos determina si se puede crear una jerarquía.

Para compilar una jerarquía de trabajos mediante una asociación explícita, todos los objetos de trabajo deben crearse mediante [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)y, a continuación, se debe llamar a [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) varias veces para que cada proceso asocie el proceso a cada trabajo al que debe pertenecer. Para asegurarse de que la jerarquía de trabajos es válida, asigne primero todos los procesos al trabajo en la raíz de la jerarquía y, a continuación, asigne un subconjunto de procesos al objeto de trabajo secundario inmediato, y así sucesivamente. Si los procesos se asignan a trabajos en este orden, un trabajo secundario siempre tendrá un subconjunto de procesos en su trabajo primario mientras se crea la jerarquía, que es necesaria para el anidamiento. Si los procesos se asignan a trabajos en orden aleatorio, en algún momento un trabajo secundario tendrá procesos que no están en su trabajo primario. Esto no se permite mediante el anidamiento y provocará un error **en AssignProcessToJobObject.**

Cuando los procesos se asocian implícitamente a un trabajo durante la creación del proceso, se asocia un proceso secundario a cada trabajo de la cadena de trabajos de su proceso primario. Si el objeto de trabajo inmediato permite la interrupción, el proceso secundario se separa del objeto de trabajo inmediato y de cada trabajo de la cadena de trabajos primarios, moviendo hacia arriba la jerarquía hasta llegar a un trabajo que no permite la interrupción. Si el objeto de trabajo inmediato no permite la interrupción, el proceso secundario no se interrumpirá incluso si los trabajos de su cadena de trabajos primario lo permiten.

## <a name="job-limits-and-notifications-for-nested-jobs"></a>Límites y notificaciones de trabajos para trabajos anidados

Para determinados límites de recursos, el límite  establecido para los trabajos de una cadena de trabajos primaria determina el límite efectivo que se aplica a un trabajo secundario. El límite efectivo del trabajo secundario puede ser más restrictivo que el límite de su elemento primario, pero no puede ser menos restrictivo. Por ejemplo, si la clase de prioridad de un trabajo secundario es ABOVE NORMAL PRIORITY CLASS y la clase de prioridad de su trabajo primario es NORMAL PRIORITY CLASS, el límite efectivo para los procesos del trabajo secundario es \_ \_ NORMAL PRIORITY \_ \_ \_ \_ \_ CLASS. Sin embargo, si la clase de prioridad del trabajo secundario es BELOW NORMAL PRIORITY CLASS, el límite efectivo para los procesos del trabajo secundario \_ es BELOW NORMAL PRIORITY \_ \_ \_ \_ \_ CLASS. Se aplican límites efectivos para la clase de prioridad, afinidad, cargo de confirmación, límite de tiempo de ejecución por proceso, límite de clase de programación y mínimo y máximo del espacio de trabajo. Para obtener más información sobre los límites de recursos específicos, [ **vea SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

Cuando se producen determinados eventos, como la creación de un nuevo proceso o la infracción del límite de recursos, se envía un mensaje al puerto de finalización de E/S asociado a un trabajo. Un trabajo también se puede registrar para recibir notificaciones cuando se superan ciertos límites. Para un trabajo no anidado, el mensaje se envía al puerto de finalización de E/S asociado al trabajo. Para un trabajo anidado, el mensaje se envía a cada puerto de finalización de E/S asociado a cualquier trabajo de la cadena de trabajo primaria del trabajo que desencadenó el mensaje. Un trabajo secundario no necesita tener un puerto de finalización de E/S asociado para los mensajes que desencadena que se envíen a los puertos de finalización de E/S de trabajos primarios superiores en la cadena de trabajos. Para obtener más información sobre mensajes específicos, [**vea JOBOBJECT \_ ASSOCIATE COMPLETION \_ \_ PORT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-nested-jobs"></a>Contabilidad de recursos para trabajos anidados

La información de contabilidad de recursos de un trabajo anidado describe el uso de todos los procesos asociados a ese trabajo, incluidos los procesos de los trabajos secundarios. Por lo tanto, cada trabajo de una cadena de trabajos representa los recursos agregados utilizados por sus propios procesos y los procesos de cada trabajo secundario debajo de él en la cadena de trabajos.

## <a name="termination-of-nested-jobs"></a>Finalización de trabajos anidados

Cuando se termina un trabajo en una jerarquía de trabajos, el sistema finaliza los procesos de ese trabajo y todos sus trabajos secundarios, empezando por el trabajo secundario en la parte inferior de la jerarquía. Los recursos pendientes usados por cada proceso finalizado se cobran al trabajo primario.

El identificador de trabajo debe tener el derecho de acceso JOB \_ OBJECT \_ TERMINATE, igual que para los trabajos independientes.

 

 
