---
description: VSS está diseñado para solucionar los problemas descritos en los problemas comunes de copia de seguridad de volumen.
ms.assetid: f9a3efea-d6e8-40df-92ac-f6faaa4fca60
title: El modelo VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e65061b9496fe04769a9b2429f7e05a2064de63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696492"
---
# <a name="the-vss-model"></a>El modelo VSS

VSS está diseñado para solucionar los problemas descritos en los [problemas comunes de copia de seguridad de volumen](common-volume-backup-issues.md).

El modelo de VSS incluye lo siguiente:

-   Mecanismo de instantáneas. VSS proporciona una captura de volumen rápida del estado de un disco en un instante en el tiempo, una [*instantánea*](vssgloss-s.md) del volumen. Esta copia de volumen existe en paralelo con el volumen activo y contiene copias de todos los archivos del disco que se guardan de forma eficaz y están disponibles como un dispositivo independiente.
-   Estado de archivo coherente mediante la coordinación de aplicaciones. VSS proporciona un mecanismo de comunicación entre procesos basado en COM y orientado a eventos que los procesos participantes pueden utilizar para determinar el estado del sistema con respecto a las operaciones de copia de seguridad, restauración y instantáneas (captura de volumen). Estos eventos definen las fases por las que las aplicaciones que modifican los datos en disco ([*escritores*](vssgloss-w.md)) pueden poner todos sus archivos en un estado coherente antes de la creación de la instantánea.
-   Minimizar el tiempo de inactividad de la aplicación. La instantánea de VSS existe en paralelo con una copia en directo del volumen del que se va a hacer una copia de seguridad, por lo que, salvo el breve período de preparación y creación de la instantánea, una aplicación puede continuar su trabajo. El tiempo necesario para crear realmente una instantánea, que se produce entre los eventos [*Freeze*](vssgloss-f.md) y [*reanudar*](vssgloss-t.md) , normalmente tarda aproximadamente un minuto.

    Aunque la preparación de un escritor para una instantánea, incluido el estado de almacenamiento e/s y guardado (consulte [información general de las tareas anteriores a la copia de seguridad](overview-of-pre-backup-tasks.md)), puede no ser trivial, es mucho menor que el tiempo necesario para realizar realmente una copia de seguridad de un volumen, lo que puede tardar horas.

-   Interfaz unificada para VSS. VSS abstrae los mecanismos de instantáneas dentro de una interfaz común y permite a un proveedor de hardware agregar y administrar las características únicas de sus propios proveedores. Cualquier aplicación de copia de seguridad ([*solicitante*](vssgloss-r.md)) y cualquier escritor debe poder ejecutarse en cualquier sistema de almacenamiento en disco que admita la interfaz de VSS.
-   Copia de seguridad multivolumen. VSS admite [*conjuntos de instantáneas*](vssgloss-s.md), que son colecciones de instantáneas, en varios tipos de volúmenes de disco de varios proveedores. Todas las instantáneas de un conjunto de instantáneas se crearán con la misma marca de tiempo y presentarán el mismo estado de disco para un estado de disco multivolumen.
-   Compatibilidad con instantáneas nativas. A partir de Windows XP, la compatibilidad con la instantánea está disponible a través de VSS como parte nativa del sistema operativo Windows. Siempre que haya al menos un disco NTFS presente en un sistema, estos sistemas se pueden configurar para admitir instantáneas de todos los sistemas de disco montados en ellos.

 

 



