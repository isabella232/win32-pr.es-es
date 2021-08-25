---
description: Cada una de las operaciones de copia de seguridad y restauración de VSS usa un protocolo para la interacción de los sistemas que usan almacenamiento masivo (escritores) y los que lo copian de seguridad (solicitantes).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Uso del Servicio de instantáneas de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ad0f07cc20da83f9401ff5194776300c5aad23a950b2fbc7f14f787fe22f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866255"
---
# <a name="using-the-volume-shadow-copy-service"></a>Uso del Servicio de instantáneas de volumen

Cada una de las operaciones de copia de seguridad y restauración de VSS usa un protocolo para la interacción de los sistemas que usan almacenamiento masivo (escritores) y los que lo copian de seguridad (solicitantes).

Las operaciones de copia de seguridad y restauración están controladas principalmente por el solicitante, que controla el comportamiento del escritor y del proveedor mediante la generación de eventos COM en todo el sistema para que el escritor lo procese. Dado que los métodos de generación de eventos son asincrónicos, los escritores tienen un control limitado en el estado del solicitante a través de los controladores asincrónicos disponibles para VSS (vea [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).

Esta interacción requiere estructuras de datos básicas que describan archivos y grupos de archivos [*(componentes*](vssgloss-c.md)), así como un modelo de metadatos para permitir el almacenamiento de información de copia de seguridad y permitir la comunicación entre escritor y solicitante.

-   [Compatibilidad de aplicaciones de VSS](usage-conventions.md)
-   [Configuración de VSS](configuring-vss.md)
-   [Metadatos de VSS](vss-metadata.md)
-   [Trabajar con la capacidad de selección y las rutas de acceso lógicas](working-with-selectability-and-logical-paths.md)
-   [Información general sobre el procesamiento de una copia de seguridad en VSS](overview-of-processing-a-backup-under-vss.md)
-   [Información general sobre el procesamiento de una restauración en VSS](overview-of-processing-a-restore-under-vss.md)

 

 



