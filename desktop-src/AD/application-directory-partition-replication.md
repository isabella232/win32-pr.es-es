---
title: Replicación de partición de directorio de aplicaciones
description: Las particiones de directorio de aplicaciones se utilizan con más frecuencia para almacenar datos dinámicos.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- AD de replicación de partición de directorio de aplicaciones
- Particiones de directorio de aplicaciones AD, replicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41523b86ae8d3a744d4eb288c5b240a60222aa21
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077568"
---
# <a name="application-directory-partition-replication"></a>Replicación de partición de directorio de aplicaciones

Las particiones de directorio de aplicaciones se utilizan con más frecuencia para almacenar datos dinámicos. Dado que los datos cambian con más frecuencia que los datos de configuración de un bosque, se pueden establecer el ámbito de replicación y la frecuencia de una partición de directorio de aplicaciones para cada partición. Se pueden utilizar las características de replicación de Active Directory Domain Services, pero los datos de replicación se pueden optimizar para adaptarse al tipo de datos almacenado en la partición.

El sistema operativo no exige un número máximo de réplicas, pero el número de réplicas debe mantenerse al mínimo para reducir el impacto en el rendimiento de la replicación de los datos dinámicos de la partición de directorio de aplicaciones.

El KCC genera y mantiene la topología de replicación para una partición de directorio de aplicaciones.

## <a name="application-directory-partition-replication-within-a-site"></a>Replicación de particiones de directorio de aplicaciones dentro de un sitio

Se pueden configurar los intervalos de replicación que controlan la replicación dentro de un sitio de una partición de directorio de aplicaciones. Esto permite que los datos dinámicos de una partición de directorio de aplicaciones se sincronicen más rápidamente que los datos más estáticos en una partición de dominio. Para obtener más información sobre la configuración mediante programación de una partición de directorio de aplicaciones, vea modificar la configuración de la [partición de directorio de aplicaciones](modifying-application-directory-partition-configuration.md).

Dos atributos en el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) de la partición de directorio de aplicación y dos valores de registro en cada controlador de dominio de Windows 2000 y versiones posteriores controlan la latencia de iniciar una notificación de cambio de origen en los asociados de replicación de un sitio.

-   El atributo [**MSDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) de un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) especifica el retraso, en segundos, después de que un objeto de origen cambie antes de que se notifique al primer asociado de replicación. Un valor del registro en cada controlador de dominio puede especificar un valor similar. En un bosque de Windows Server 2003, el primer retardo predeterminado es 15 segundos. En un bosque de modo mixto, el primer retardo predeterminado es de cinco minutos.
-   El atributo [**MSDS-Replication-Notify--DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) de un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) especifica el retraso, en segundos, entre las notificaciones posteriores al segundo, tercer y así sucesivamente los asociados de replicación. Un valor del registro en cada controlador de dominio puede especificar un valor similar. En un bosque de Windows Server 2003, el retraso subsiguiente predeterminado es de 3 segundos. En un bosque de modo mixto, el retraso subsiguiente predeterminado es de 30 segundos.

Los atributos de [**crossRef**](/windows/desktop/ADSchema/c-crossref) se aplican a todos los controladores de dominio que hospedan una réplica de la partición de directorio de aplicaciones y solo afectan a la replicación de la partición de directorio de aplicaciones identificada por el objeto **crossRef** . Los valores del registro solo se aplican al controlador de dominio en el que se establecen y afectan a la replicación dentro de un sitio para todas las particiones que hospeda el controlador de dominio. Si no se establece ningún atributo **crossRef** ni sus valores de registro, un controlador de dominio utiliza los valores predeterminados. Si se establecen los valores del registro, invalidan los valores establecidos en el objeto **crossRef** . De forma predeterminada, no se establecen los valores del registro y de **crossRef** , por lo que se utilizan los valores predeterminados. Esto permite a un administrador acelerar la replicación de todas las réplicas de una partición de directorio de aplicaciones mediante el establecimiento de los valores de **crossRef** , a la vez que permite un ajuste más preciso de la configuración del registro en cada controlador de dominio.

A partir de Windows Server 2003, las particiones de dominio también usan estos atributos del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para controlar la latencia de replicación dentro del sitio. Se trata de un cambio respecto a las versiones anteriores del servidor en las que los intervalos de retraso se controlaban mediante valores del registro en cada controlador de dominio. Cuando el bosque se actualiza a Windows Server 2003, los valores del registro existentes se conservan solo si se han modificado con los valores predeterminados. Los intervalos de notificación de los controladores de dominio del registro invalidan los intervalos de notificación almacenados en el objeto **crossRef** de la partición.

## <a name="application-directory-partition-replication-across-sites"></a>Replicación de particiones de directorio de aplicaciones entre sitios

Las réplicas de una partición de directorio de aplicaciones que se encuentran entre sitios respetan la programación de la replicación entre sitios como se hace para la replicación de catálogo global y la partición de dominio. Sin embargo, las réplicas de una partición de directorio de aplicaciones suelen encontrarse en un sitio cuando se hospedan datos realmente volátiles, ya que es posible que la latencia de replicación entre sitios no sea aceptable para que las réplicas sean coherentes entre sí.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>Las particiones de directorio de aplicaciones no se replican en catálogos globales

Los objetos de una partición de directorio de aplicaciones no se replican en el catálogo global. La partición del directorio de aplicaciones se ha aprovisionado como hospedaje de datos dinámicos y objetos para los que no es razonable, ni es factible replicar los objetos ampliamente. Por esta razón, la partición del directorio de aplicaciones ofrece el ámbito controlado y la frecuencia de replicación. Por este motivo, no hay ninguna razón para permitir que estos objetos se repliquen en el catálogo global y, por tanto, se distribuyan en todo el bosque en el que exista un servidor de catálogo global. Esto no impide que los objetos de una partición de directorio de aplicaciones usen atributos en el esquema marcado como [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset). Al igual que con cualquier controlador de dominio, se puede configurar un servidor de catálogo global para que sea una réplica completa de una partición de directorio de aplicaciones.

 

 