---
description: COMREPL realiza su trabajo en tres fases.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Fases de replicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466607"
---
# <a name="replication-phases"></a>Fases de replicación

COMREPL realiza su trabajo en tres fases. El proceso de replicación se divide en fases distintas por las dos razones siguientes:

-   Para separar el trabajo realizado para preparar el origen del trabajo que se realiza en cada destino
-   Para retrasar la modificación del destino hasta que se hayan adquirido todos los datos del origen

Las fases de replicación son las siguientes.



| Fase         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fase de preparación | Exporta todas las aplicaciones instaladas localmente en el equipo de origen. Esta fase no afecta a la configuración de ningún destino.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Fase de copia    | Copia los datos en un equipo de destino. Todas las aplicaciones exportadas en el origen se copian en el destino. Se trata de una operación de copia de archivos. (Vea [Administración de archivos).](file-management.md) Este paso también adquiere algunos datos del equipo de origen que no están encapsulados en archivos de aplicación exportados (por ejemplo, identidades de aplicación). Estos datos se mantienen en memoria dentro de COMREPL. Esta fase no afecta a la configuración de ningún equipo de destino.                                                                               |
| Fase de instalación | Instala el catálogo de origen en un equipo de destino. Cuando se inicia este paso, todos los datos necesarios para volver a configurar el destino se encuentran dentro de los archivos de aplicación del sistema de archivos del destino o se mantienen como datos de instancia en COMREPL. Esta fase eliminará todas las aplicaciones instaladas en el destino (excepto las aplicaciones descritas en [Qué](what-gets-replicated.md)se replica) antes de instalar las aplicaciones copiadas del origen. COMREPL se instala en varios destinos simultáneamente mediante un subproceso de instalación por destino. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de archivos](file-management.md)
</dt> <dt>

[Registro e informes de errores](logging-and-error-reporting.md)
</dt> <dt>

[Uso de COMREPL](using-comrepl.md)
</dt> <dt>

[Qué se replica](what-gets-replicated.md)
</dt> </dl>

 

 



