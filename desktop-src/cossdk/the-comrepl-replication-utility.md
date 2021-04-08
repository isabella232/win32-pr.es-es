---
description: COMREPL es una utilidad que replicará el catálogo de COM+ de un equipo de origen determinado en uno o varios equipos de destino.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: La utilidad de replicación COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000745"
---
# <a name="the-comrepl-replication-utility"></a>La utilidad de replicación COMREPL

COMREPL es una utilidad que replicará el catálogo de COM+ de un equipo de origen determinado en uno o varios equipos de destino. Piense en el equipo de origen que representa una "configuración maestra". COMREPL se usa para replicar esta configuración maestra con el fin de mantener un conjunto de equipos configurados de forma idéntica.

La unidad de replicación es toda la configuración de COM+ en el equipo maestro. Todas las aplicaciones COM+ del servidor principal se replican en los equipos de destino; es todo o nada. Además, todas las aplicaciones COM+ instaladas anteriormente en los equipos de destino, con la excepción de las aplicaciones COM+ preinstaladas, se eliminarán como parte del proceso de replicación.

COMREPL solo replica los datos de configuración de COM+. Esto incluye las aplicaciones COM+ y la configuración del equipo específico de COM+. Microsoft Internet Information Services (IIS) tiene una utilidad similar (IISSync) que hace uso de COMREPL para replicar la configuración de IIS y COM+.

Para obtener información detallada sobre cómo iniciar y usar COMREPL, vea los temas siguientes en esta sección:

-   [Usar COMREPL](using-comrepl.md)
-   [Lo que se replica](what-gets-replicated.md)
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

 

 



