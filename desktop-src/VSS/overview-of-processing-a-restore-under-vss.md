---
description: En el procesamiento de una copia de seguridad en VSS, los solicitantes y escritores trabajaron juntos para generar una imagen de sistema estable desde la que realizar la copia de seguridad de los datos, lo que requería coordinación y la creación de una instantánea del sistema actual.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Información general sobre el procesamiento de una restauración en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696986"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>Información general sobre el procesamiento de una restauración en VSS

En el procesamiento de una copia de seguridad en VSS, los solicitantes y escritores trabajaron juntos para generar una imagen de sistema estable desde la que realizar la copia de seguridad de los datos, lo que requería coordinación y la creación de una instantánea del sistema actual.

A diferencia de una copia de seguridad de VSS, en la que el propósito de la coordinación de solicitante y escritores es generar una imagen de sistema estable desde la que copiar los datos, el objetivo de una restauración basada en VSS es devolver los archivos al disco de forma más útil para las aplicaciones (escritores) que se ejecutan actualmente en el sistema. Esto no requiere una imagen de sistema estable, por lo que no es necesaria ninguna instantánea.

En su lugar, la atención se centra en evitar la interrupción de la actividad del escritor, lo que impide la creación de conjuntos de datos incoherentes en el disco y permite a los escritores el ámbito necesario para evaluar y combinar datos cuando sea necesario.

Al igual que una operación de copia de seguridad, una restauración de VSS requiere acceso a un documento de componentes de copia de seguridad y a documentos de metadatos de escritura. Normalmente, estos documentos no se obtienen mediante la consulta de las aplicaciones en ejecución, sino que se recuperan de las versiones almacenadas como documentos XML en los medios de copia de seguridad.

Como es el caso de las operaciones de copia de seguridad, los documentos de metadatos del escritor siguen siendo objetos de solo lectura y, una vez recuperados, el documento componentes de copia de seguridad todavía se puede modificar. Las modificaciones del documento componentes de copia de seguridad permiten que los escritores y el solicitante se comuniquen sobre lo siguiente:

-   Reemplazar [*métodos de restauración*](vssgloss-r.md) con [*destinos de restauración*](vssgloss-r.md)
-   Usar [ *asignaciones de ubicación alternativas*](vssgloss-a.md)
-   Restaurar archivos en nuevas ubicaciones en disco
-   Usar diferentes reglas de selección de las utilizadas durante la copia de seguridad

Para comprender con más detalle las tareas básicas relacionadas con la realización de una restauración, resulta útil dividir esta información general en los siguientes temas:

-   [Información general de la inicialización de restauración](overview-of-restore-initialization.md)
-   [Información general de la preparación para la restauración](overview-of-preparing-for-restore.md)
-   [Información general de la restauración de archivos real](overview-of-actual-file-restoration.md)
-   [Información general sobre la limpieza y la finalización de la restauración](overview-of-restore-clean-up-and-termination.md)

 

 



