---
description: COMREPL es una utilidad que replicará el catálogo de COM+ desde un equipo de origen determinado a uno o varios equipos de destino.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: Utilidad de replicación COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446cfc0e627463e8c142ccab624c3773123034c2becebc402a6069f74d30ccd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305300"
---
# <a name="the-comrepl-replication-utility"></a>Utilidad de replicación COMREPL

COMREPL es una utilidad que replicará el catálogo de COM+ desde un equipo de origen determinado a uno o varios equipos de destino. Piense en el equipo de origen que representa una "configuración maestra". COMREPL se usa para replicar esta configuración maestra para mantener un conjunto de equipos configurados de forma idéntica.

La unidad de replicación es toda la configuración de COM+ en el equipo maestro. Todas las aplicaciones COM+ del servidor maestro se replican en los equipos de destino. es todo o nada. Además, todas las aplicaciones COM+ instaladas previamente en los equipos de destino, a excepción de las aplicaciones preinstaladas de COM+, se eliminarán como parte del proceso de replicación.

COMREPL solo replica los datos de configuración de COM+. Esto incluye las aplicaciones COM+ y la configuración de equipo específica de COM+. Microsoft Internet Information Services (IIS) tiene una utilidad similar (IISSync), que usa COMREPL para replicar la configuración de IIS y COM+.

Para obtener información detallada sobre el inicio y el uso de COMREPL, consulte los temas siguientes en esta sección:

-   [Uso de COMREPL](using-comrepl.md)
-   [Qué se replica](what-gets-replicated.md)
-   [Fases de replicación](replication-phases.md)
-   [Administración de archivos](file-management.md)
-   [Registro e informes de errores](logging-and-error-reporting.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear paquetes de instalación para aplicaciones COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Implementación de servidores proxy de aplicación](deploying-application-proxies.md)
</dt> <dt>

[El catálogo de COM+](the-com--catalog.md)
</dt> </dl>

 

 



