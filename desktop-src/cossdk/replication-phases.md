---
description: COMREPL realiza su trabajo en tres fases.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fases de replicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714885"
---
# <a name="replication-phases"></a>Fases de replicación

COMREPL realiza su trabajo en tres fases. El proceso de replicación se divide en distintas fases por los dos motivos siguientes:

-   Para separar el trabajo realizado para preparar el origen a partir del trabajo que se realiza en cada destino
-   Para retrasar la modificación del destino hasta que se hayan adquirido todos los datos desde el origen

Las fases de replicación son las siguientes.



| Fase         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fase de preparación | Exporta todas las aplicaciones instaladas localmente en el equipo de origen. Esta fase no toca la configuración de ningún destino.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Fase de copia    | Copia datos en un equipo de destino. Todas las aplicaciones exportadas en el origen se copian en el destino. Se trata de una operación de copia de archivos. (Consulte [Administración de archivos](file-management.md)). Este paso también adquiere algunos datos del equipo de origen que no se encapsulan en los archivos de aplicación exportados (por ejemplo, las identidades de aplicación). Estos datos se almacenan en la memoria de COMREPL. Esta fase no toca la configuración de ningún equipo de destino.                                                                               |
| Fase de instalación | Instala el catálogo de origen en un equipo de destino. Cuando se inicia este paso, todos los datos necesarios para volver a configurar el destino se encuentran en los archivos de aplicación del sistema de archivos del destino o se almacenan como datos de instancia en COMREPL. En esta fase se eliminarán todas las aplicaciones instaladas en el destino (excepto las aplicaciones descritas en [lo que se replica](what-gets-replicated.md)) antes de instalar las aplicaciones copiadas desde el origen. COMREPL se instala en varios destinos simultáneamente mediante el uso de un subproceso de instalación por destino. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de archivos](file-management.md)
</dt> <dt>

[Registro e informes de errores](logging-and-error-reporting.md)
</dt> <dt>

[Usar COMREPL](using-comrepl.md)
</dt> <dt>

[Lo que se replica](what-gets-replicated.md)
</dt> </dl>

 

 



