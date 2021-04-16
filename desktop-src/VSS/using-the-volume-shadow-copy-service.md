---
description: Las operaciones de copia de seguridad y restauración de VSS usan un protocolo para la interacción de los sistemas que utilizan almacenamiento masivo (escritores) y los que lo respaldan (solicitantes).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Usar el Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541763"
---
# <a name="using-the-volume-shadow-copy-service"></a>Usar el Servicio de instantáneas de volumen

Las operaciones de copia de seguridad y restauración de VSS usan un protocolo para la interacción de los sistemas que utilizan almacenamiento masivo (escritores) y los que lo respaldan (solicitantes).

Las operaciones de copia de seguridad y restauración están dirigidas principalmente por el solicitante, que controla el comportamiento del escritor y del proveedor mediante la generación de eventos COM en todo el sistema para que los procese el escritor. Dado que los métodos de generación de eventos son asincrónicos, los escritores tienen un control limitado en el estado del solicitante a través de los controladores asincrónicos disponibles para VSS (vea [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).

Esta interacción requiere estructuras de datos básicas que describen archivos y grupos de archivos ([*componentes*](vssgloss-c.md)), así como un modelo de metadatos para permitir el almacenamiento de la información de copia de seguridad y permitir la comunicación entre el autor y el solicitante.

-   [Compatibilidad de aplicaciones de VSS](usage-conventions.md)
-   [Configuración de VSS](configuring-vss.md)
-   [Metadatos de VSS](vss-metadata.md)
-   [Trabajar con la selección y las rutas de acceso lógicas](working-with-selectability-and-logical-paths.md)
-   [Información general sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md)
-   [Información general sobre el procesamiento de una restauración en VSS](overview-of-processing-a-restore-under-vss.md)

 

 



