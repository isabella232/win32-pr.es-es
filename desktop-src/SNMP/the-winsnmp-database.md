---
title: La base de datos WinSNMP
description: La implementación de Microsoft WinSNMP mantiene un almacén de información administrativa en una base de datos.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2f478c9bb1c05d3a094e2a15fac0a9cef5968f245257a0702d045eb90bd2fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886005"
---
# <a name="the-winsnmp-database"></a>La base de datos WinSNMP

La implementación de Microsoft WinSNMP mantiene un almacén de información administrativa en una base de datos. La base de datos incluye la siguiente información:

-   Propiedades de red y versión.

    La implementación usa estas propiedades para determinar qué protocolo de transporte de red y el marco de versión de SNMP se usarán para completar las solicitudes de transmisión. Para obtener más información, vea [Acerca de las versiones de SNMP.](about-snmp-versions.md)

-   Modo de traducción de entidades y contexto.

    La implementación usa este modo para interpretar nombres descriptivos para entidades y contextos SNMP. Para obtener más información, vea [Establecer el modo de traducción de entidades y contexto.](setting-the-entity-and-context-translation-mode.md)

-   Configuración de directiva de retransmisión.

    La implementación usa esta configuración para determinar si debe ejecutar o no la directiva de retransmisión de la aplicación. La implementación almacena un valor de tiempo de espera y un recuento de reintentos para cada entidad de destino. Para obtener más información, vea [Acerca de la retransmisión](about-retransmission.md) y [Administración de la directiva de retransmisión.](managing-the-retransmission-policy.md)

 

 




