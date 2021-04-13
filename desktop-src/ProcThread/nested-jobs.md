---
description: Una aplicación puede usar trabajos anidados para administrar subconjuntos de procesos. Los trabajos anidados también habilitan una aplicación que usa trabajos para hospedar otras aplicaciones que también usan trabajos.
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: Trabajos anidados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf105c70ec8e83b395fcce56c6274d4838358bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552009"
---
# <a name="nested-jobs"></a>Trabajos anidados

Una aplicación puede usar trabajos anidados para administrar subconjuntos de procesos. Los trabajos anidados también habilitan una aplicación que usa trabajos para hospedar otras aplicaciones que también usan trabajos.

**Windows 7, Windows server 2008 R2, Windows XP con SP3, Windows server 2008, Windows Vista y Windows server 2003:** Un proceso solo se puede asociar a un único trabajo. Los trabajos anidados se introdujeron en Windows 8 y Windows Server 2012.

En este tema se proporciona información general sobre el anidamiento de trabajos y el comportamiento de los trabajos anidados:

-   [Jerarquías de trabajos anidados](#nested-job-hierarchies)
-   [Crear una jerarquía de trabajos anidada](#creating-a-nested-job-hierarchy)
-   [Límites de trabajo y notificaciones para trabajos anidados](#job-limits-and-notifications-for-nested-jobs)
-   [Contabilidad de recursos para trabajos anidados](#resource-accounting-for-nested-jobs)
-   [Finalización de trabajos anidados](#termination-of-nested-jobs)

Para obtener información general sobre los trabajos y los objetos de trabajo, vea [objetos de trabajo](job-objects.md).

## <a name="nested-job-hierarchies"></a>Jerarquías de trabajos anidados

Los trabajos anidados tienen una relación de elementos primarios y secundarios en la que cada trabajo secundario contiene un subconjunto de los procesos en su trabajo primario. Si un proceso que ya se encuentra en un trabajo se agrega a otro trabajo, los trabajos se anidan de forma predeterminada si el sistema puede formar una jerarquía de trabajos válida y ninguno de los conjuntos de trabajos limita la interfaz de usuario ([**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) con **JobObjectBasicUIRestrictions**).

En la figura 1 se muestra una jerarquía de trabajos que contiene un árbol de procesos con la etiqueta P0 a través de P7. El trabajo 1 es el trabajo *primario* del trabajo 2 y el trabajo 4, y es un *antecesor* del trabajo 3. El trabajo 2 es el *elemento primario inmediato* del trabajo 3; El trabajo 3 es el *elemento secundario inmediato* del trabajo 2. Los trabajos 1, 2 y 3 forman una *cadena de trabajos* en la que los trabajos 1 y 2 son la *cadena de trabajos primaria* del trabajo 3. El trabajo final de una cadena de trabajos es el *trabajo inmediato* de los procesos de ese trabajo. En la figura 1, el trabajo 3 es el trabajo inmediato de los procesos P2, P3 y P4.

![Figura 1. una jerarquía de trabajos anidada que contiene un árbol de procesos](images/nested-jobs-a.png)

Los trabajos anidados también se pueden usar para administrar grupos de procesos del mismo nivel. En la jerarquía de trabajos que se muestra en la figura 2, el trabajo 1 es el trabajo primario del trabajo 2. Tenga en cuenta que una jerarquía de trabajos podría contener solo parte de un árbol de procesos. En la figura 2, P0 no se encuentra en la jerarquía de, pero sus procesos secundarios son.

![Figura 2. una jerarquía de trabajos anidada que contiene procesos del mismo nivel](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>Crear una jerarquía de trabajos anidada

Los procesos de una jerarquía de trabajos se asocian explícitamente a un objeto de trabajo mediante la función [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) o se asocian implícitamente durante la creación del proceso, igual que para los trabajos independientes. El orden en que se crean los trabajos y los procesos se asignan determina si se puede crear una jerarquía.

Para compilar una jerarquía de trabajos mediante la asociación explícita, todos los objetos de trabajo se deben crear con [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)y, a continuación, se debe llamar a [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) varias veces para que cada proceso asocie el proceso a cada trabajo al que debe pertenecer. Para asegurarse de que la jerarquía de trabajos es válida, primero asigne todos los procesos al trabajo en la raíz de la jerarquía y, a continuación, asigne un subconjunto de procesos al objeto de trabajo secundario inmediato, y así sucesivamente. Si los procesos se asignan a los trabajos en este orden, un trabajo secundario siempre tendrá un subconjunto de procesos en su trabajo primario mientras se crea la jerarquía, lo que es necesario para el anidamiento. Si los procesos se asignan a los trabajos en orden aleatorio, en algún momento un trabajo secundario tendrá procesos que no están en su trabajo primario. Esto no se permite mediante el anidamiento y se producirá un error en **AssignProcessToJobObject** .

Cuando los procesos están asociados implícitamente a un trabajo durante la creación del proceso, un proceso secundario se asocia a cada trabajo de la cadena de trabajos de su proceso primario. Si el objeto de trabajo inmediato permite la separación, el proceso secundario se rompe del objeto de trabajo inmediato y de cada trabajo de la cadena de trabajo primaria, moviendo la jerarquía hasta que llega a un trabajo que no permite la separación. Si el objeto de trabajo inmediato no permite la separación, el proceso secundario no se interrumpe aunque los trabajos de su cadena de trabajo principal lo permitan.

## <a name="job-limits-and-notifications-for-nested-jobs"></a>Límites de trabajo y notificaciones para trabajos anidados

En el caso de ciertos límites de recursos, el límite establecido para los trabajos de una cadena de trabajo primaria determina el *límite efectivo* que se aplica a un trabajo secundario. El límite efectivo del trabajo secundario puede ser más restrictivo que el límite de su elemento primario, pero no puede ser menos restrictivo. Por ejemplo, si la clase de prioridad de un trabajo secundario está por encima de \_ la clase de prioridad normal \_ \_ y su clase de prioridad del trabajo principal es la clase de prioridad normal \_ \_ , el límite efectivo para los procesos en el trabajo secundario es \_ clase de prioridad normal \_ . Sin embargo, si la clase de prioridad del trabajo secundario está por debajo de la \_ \_ clase de prioridad normal \_ , el límite efectivo para los procesos en el trabajo secundario está por debajo de la \_ clase de prioridad normal \_ \_ . Los límites efectivos se aplican para la clase de prioridad, la afinidad, el cargo de confirmación, el límite de tiempo de ejecución por proceso, el límite de clase de programación y el espacio de trabajo mínimo y máximo. Para obtener más información sobre los límites de recursos específicos, vea [ **SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

Cuando se producen determinados eventos, como la creación de un nuevo proceso o la infracción del límite de recursos, se envía un mensaje al puerto de finalización de e/s asociado a un trabajo. Un trabajo también puede registrarse para recibir notificaciones cuando se superan determinados límites. Para un trabajo no anidado, el mensaje se envía al puerto de finalización de e/s asociado al trabajo. Para un trabajo anidado, el mensaje se envía a todos los puertos de finalización de e/s asociados a cualquier trabajo en la cadena de trabajos primaria del trabajo que desencadenó el mensaje. No es necesario que un trabajo secundario tenga un puerto de finalización de e/s asociado para los mensajes que desencadena que se envíen a los puertos de finalización de e/s de los trabajos primarios situados más arriba en la cadena de trabajos. Para obtener más información sobre mensajes específicos, vea [**JOBOBJECT \_ Associate \_ Complete \_ Port**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-nested-jobs"></a>Contabilidad de recursos para trabajos anidados

La información de cuentas de recursos para un trabajo anidado describe el uso de cada proceso asociado a ese trabajo, incluidos los procesos de los trabajos secundarios. Por lo tanto, cada trabajo de una cadena de trabajo representa los recursos agregados usados por sus propios procesos y los procesos de cada trabajo secundario por debajo de él en la cadena de trabajos.

## <a name="termination-of-nested-jobs"></a>Finalización de trabajos anidados

Cuando finaliza un trabajo en una jerarquía de trabajos, el sistema termina los procesos en ese trabajo y todos sus trabajos secundarios, empezando por el trabajo secundario en la parte inferior de la jerarquía. Los recursos pendientes utilizados por cada proceso terminado se cobran al trabajo primario.

El identificador de trabajo debe tener el \_ objeto de trabajo \_ terminar el acceso a la derecha, igual que para los trabajos independientes.

 

 
