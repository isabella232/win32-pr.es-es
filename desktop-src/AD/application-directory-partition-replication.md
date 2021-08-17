---
title: Replicación de particiones de directorio de aplicación
description: Las particiones de directorio de aplicación se usan con más frecuencia para almacenar datos dinámicos.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- AD de replicación de particiones de directorio de aplicación
- Particiones de directorio de aplicación ad , replicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7df6c50653fe1660bbf95f0f6ca580404d38c366c1045bc3d1b712ca771d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024415"
---
# <a name="application-directory-partition-replication"></a>Replicación de particiones de directorio de aplicación

Las particiones de directorio de aplicación se usan con más frecuencia para almacenar datos dinámicos. Dado que los datos cambian con más frecuencia que los datos de configuración de un bosque, se pueden establecer el ámbito de replicación y la frecuencia de una partición de directorio de aplicación para cada partición. Las características de replicación Active Directory Domain Services se pueden usar, pero los datos de replicación se pueden ajustar para adaptarse al tipo de datos almacenados en la partición.

El sistema operativo no aplica un número máximo de réplicas, pero el número de réplicas se debe mantener al mínimo para reducir el impacto en el rendimiento de la replicación de los datos dinámicos de partición del directorio de la aplicación.

El KCC genera y mantiene la topología de replicación para una partición de directorio de aplicación.

## <a name="application-directory-partition-replication-within-a-site"></a>Replicación de particiones de directorio de aplicación dentro de un sitio

Se pueden configurar los intervalos de replicación que controlan la replicación dentro del sitio de una partición de directorio de aplicación. Esto permite que los datos dinámicos de una partición de directorio de aplicación se sincronicen más rápidamente que los datos más estáticos de una partición de dominio. Para obtener más información sobre cómo configurar mediante programación una partición de directorio de aplicación, vea Modificación de la configuración de partición de [directorio de aplicación.](modifying-application-directory-partition-configuration.md)

Dos atributos en el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) de la partición de directorio de la aplicación y dos valores del Registro en cada controlador de dominio de Windows 2000 y versiones posteriores controlan la latencia de iniciar una notificación de cambio de origen a los asociados de replicación dentro de un sitio.

-   El atributo [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) de un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) especifica el retraso, en segundos, después de un cambio de objeto de origen antes de que se notifique al primer asociado de replicación. Un valor del Registro en cada controlador de dominio puede especificar un valor similar. En un Windows Server 2003, el primer retraso predeterminado es de 15 segundos. En un bosque en modo mixto, el primer retraso predeterminado es de cinco minutos.
-   El atributo [**msDS-Replication-Notify-Subsequent-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) de un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) especifica el retraso, en segundos, entre las notificaciones posteriores al segundo, tercer, y así sucesivamente en los asociados de replicación. Un valor del Registro en cada controlador de dominio puede especificar un valor similar. En un Windows Server 2003, el retraso posterior predeterminado es de 3 segundos. En un bosque en modo mixto, el retraso posterior predeterminado es de 30 segundos.

Los [**atributos crossRef se**](/windows/desktop/ADSchema/c-crossref) aplican a todos los controladores de dominio que hospedan una réplica de la partición del directorio de la aplicación y afectan solo a la replicación de la partición de directorio de aplicación identificada por el objeto **crossRef.** Los valores del Registro solo se aplican al controlador de dominio en el que se establecen y afectan a la replicación dentro del sitio para todas las particiones que hospeda el controlador de dominio. Si no se **establecen los atributos crossRef** ni sus valores del Registro, un controlador de dominio usa los valores predeterminados. Si se establecen los valores del Registro, invalidan los valores establecidos en el **objeto crossRef.** De forma predeterminada, no se establecen los valores de registro y **crossRef,** por lo que se usan los valores predeterminados. Esto permite a un administrador acelerar la replicación de todas las réplicas de una partición de directorio de aplicación estableciendo los valores **crossRef,** al tiempo que permite un ajuste más preciso con la configuración del Registro en cada controlador de dominio.

A partir de Windows Server 2003, las particiones de dominio también usan estos atributos del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para controlar la latencia de replicación dentro del sitio. Se trata de un cambio con respecto a versiones anteriores del servidor en las que los intervalos de retraso se controlaban mediante valores del Registro en cada controlador de dominio. Cuando el bosque se actualiza a Windows Server 2003, los valores del Registro existentes solo se conservan si se han modificado a partir de los valores predeterminados. Los intervalos de notificación de controladores de dominio del Registro invalidan los intervalos de notificación almacenados en el **objeto crossRef de partición.**

## <a name="application-directory-partition-replication-across-sites"></a>Replicación de particiones de directorio de aplicación entre sitios

Las réplicas de una partición de directorio de aplicación que se encuentran entre sitios observan la programación de replicación entre sitios como se hace para la partición de dominio y la replicación del catálogo global. Sin embargo, las réplicas de una partición de directorio de aplicación se encuentran más a menudo dentro de un sitio cuando se hospedan datos realmente volátiles porque es posible que la latencia de replicación entre sitios no sea aceptable para que las réplicas sean coherentes entre sí.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>Las particiones de directorio de aplicación no se replican en catálogos globales

Los objetos de una partición de directorio de aplicación no se replican en el catálogo global. La partición del directorio de la aplicación se prevé como el hospedaje de datos dinámicos y objetos para los que no puede ser razonable ni factible replicar los objetos ampliamente. Por este motivo, la partición del directorio de la aplicación ofrece un ámbito controlado y una frecuencia de replicación. Por este motivo, no hay ninguna razón para permitir que estos objetos se repliquen en el catálogo global y, por tanto, se distribuyen por todo el bosque donde existe un servidor de catálogo global. Esto no impide que los objetos de una partición de directorio de aplicación utilicen atributos en el esquema marcado como [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset). Al igual que con cualquier controlador de dominio, se puede configurar un servidor de catálogo global para que sea una réplica completa de una partición de directorio de aplicación.

 

 