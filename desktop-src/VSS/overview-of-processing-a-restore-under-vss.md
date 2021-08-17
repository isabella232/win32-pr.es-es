---
description: Al procesar una copia de seguridad en VSS, los solicitantes y escritores trabajaron juntos para generar una imagen estable del sistema a partir de la cual realizar copias de seguridad de los datos, lo que requería coordinación y creación de una instantánea del sistema actual.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Información general sobre el procesamiento de una restauración en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b01094a02b823f372271f14c04801820407573b9351bfe7e2fc2ad9dc74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937963"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>Información general sobre el procesamiento de una restauración en VSS

Al procesar una copia de seguridad en VSS, los solicitantes y escritores trabajaron juntos para generar una imagen estable del sistema a partir de la cual realizar copias de seguridad de los datos, lo que requería coordinación y creación de una instantánea del sistema actual.

A diferencia de una copia de seguridad de VSS, donde el propósito de la coordinación entre solicitantes y escritores es generar una imagen de sistema estable desde la que copiar datos, el objetivo de una restauración basada en VSS es devolver los archivos al disco de la manera más útil para las aplicaciones (escritores) que se ejecutan actualmente en el sistema. Esto no requiere una imagen estable del sistema, por lo que no es necesaria ninguna instantánea.

En su lugar, la atención se centra en evitar la interrupción de la actividad del escritor, evitar la creación de conjuntos de datos incoherentes en el disco y permitir a los escritores el ámbito necesario para evaluar y combinar datos cuando sea necesario.

Al igual que una operación de copia de seguridad, una restauración de VSS requiere acceso tanto a un documento de componentes de copia de seguridad como a los documentos de metadatos del escritor. Normalmente, estos documentos no se obtienen consultando las aplicaciones en ejecución, sino que se recuperan de versiones almacenadas como documentos XML en medios de copia de seguridad.

Como es el caso durante las operaciones de copia de seguridad, los documentos de metadatos del escritor siguen siendo objetos de solo lectura y, una vez recuperados, el documento de componentes de copia de seguridad todavía se puede modificar. Las modificaciones del documento componentes de copia de seguridad permiten a los escritores y solicitantes comunicarse sobre lo siguiente:

-   Invalidar métodos [*de restauración con*](vssgloss-r.md) [*destinos de restauración*](vssgloss-r.md)
-   Uso de [ *asignaciones de ubicación alternativas*](vssgloss-a.md)
-   Restauración de archivos en nuevas ubicaciones en el disco
-   Usar reglas de selección diferentes de las usadas durante la copia de seguridad

Para comprender con más detalle las tareas básicas relacionadas con la realización de una restauración, resulta útil dividir esta información general en los siguientes temas:

-   [Información general sobre la inicialización de restauración](overview-of-restore-initialization.md)
-   [Información general sobre la preparación para la restauración](overview-of-preparing-for-restore.md)
-   [Información general sobre la restauración real de archivos](overview-of-actual-file-restoration.md)
-   [Introducción a la limpieza y terminación de restauración](overview-of-restore-clean-up-and-termination.md)

 

 



