---
title: La base de datos WinSNMP
description: La implementación de Microsoft WinSNMP mantiene un almacén de información administrativa en una base de datos.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486710"
---
# <a name="the-winsnmp-database"></a>La base de datos WinSNMP

La implementación de Microsoft WinSNMP mantiene un almacén de información administrativa en una base de datos. La base de datos incluye la siguiente información:

-   Propiedades de red y de versión.

    La implementación de utiliza estas propiedades para determinar qué protocolo de transporte de red y versión de SNMP Framework se utiliza para completar las solicitudes de transmisión. Para obtener más información, consulte [acerca de las versiones de SNMP](about-snmp-versions.md).

-   Modo de traducción de entidades y contextos.

    La implementación utiliza este modo para interpretar los nombres descriptivos de las entidades y contextos SNMP. Para obtener más información, vea [establecer el modo de traducción de entidades y contextos](setting-the-entity-and-context-translation-mode.md).

-   Configuración de la Directiva de retransmisión.

    La implementación usa esta opción para determinar si debe ejecutar o no la Directiva de retransmisión de la aplicación. La implementación almacena un valor de tiempo de espera y un número de reintentos para cada entidad de destino. Para obtener más información, vea [acerca de la retransmisión](about-retransmission.md) y [Administración de la Directiva de retransmisión](managing-the-retransmission-policy.md).

 

 




