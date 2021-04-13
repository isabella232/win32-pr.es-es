---
description: Al procesar una copia de seguridad, un solicitante y una coordenada de escritores para proporcionar una imagen de sistema estable desde la que realizar copias de seguridad de los datos (el volumen de copia sombra), agrupar los archivos en función de su uso y almacenar información sobre los datos guardados.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Información general sobre el procesamiento de una copia de seguridad en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360603"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Información general sobre el procesamiento de una copia de seguridad en VSS

Al procesar una copia de seguridad, un solicitante y una coordenada de escritores para proporcionar una imagen de sistema estable desde la que realizar copias de seguridad de los datos (el volumen de copia sombra), agrupar los archivos en función de su uso y almacenar información sobre los datos guardados. Todo esto debe realizarse al crear solo una interrupción mínima en el flujo de trabajo normal del escritor.

Un solicitante consulta a los escritores sus metadatos, procesa estos datos, notifica a los escritores antes del inicio de la instantánea y de las operaciones de copia de seguridad y, a continuación, notifica a los escritores de nuevo después de que finalicen las operaciones de instantáneas y de copia de seguridad.

En respuesta a estas notificaciones, el escritor proporciona información acerca de los archivos de los que se va a hacer una copia de seguridad, incluida la especificación de grupos de archivos para coordinar ([*componentes*](vssgloss-c.md)), las pausas en sus operaciones de e/s antes de una instantánea y, a continuación, vuelve al funcionamiento normal después de la finalización de una instantánea o al final de la copia de seguridad

Durante el procesamiento de la copia de seguridad, un escritor especifica los archivos de los que es responsable a través de sus metadatos de solo lectura, el documento de metadatos de escritor (consulte [metadatos de VSS: trabajar con el documento de metadatos del escritor](working-with-the-writer-metadata-document.md)). A continuación, el solicitante interpreta estos metadatos, elige qué hacer para realizar la copia de seguridad y almacena estas decisiones en su propio objeto de metadatos, en el documento componentes de copia de seguridad (vea [metadatos de VSS: trabajar con el documento componentes de copia de seguridad](working-with-the-backup-components-document.md)). Este documento de componentes de copia de seguridad está disponible para la inspección y modificación del escritor durante las operaciones de copia de seguridad y restauración.

En este diagrama se muestran las interacciones entre el solicitante, el servicio VSS, la compatibilidad con el kernel de VSS, cualquier Escritor VSS implicado y cualquier proveedor de hardware VSS.

![interacciones entre el solicitante, los componentes de copia de seguridad, los escritores y los proveedores](images/vssimpl.png)

Para comprender con más detalle las tareas básicas relacionadas con la realización de una copia de seguridad, resulta útil dividir esta información general en los temas siguientes:

-   [Información general sobre la inicialización de copias de seguridad](overview-of-backup-initialization.md)
-   [Información general de la fase de detección de copias de seguridad](overview-of-the-backup-discovery-phase.md)
-   [Información general de las tareas anteriores a la copia de seguridad](overview-of-pre-backup-tasks.md)
-   [Información general sobre la copia de seguridad real de archivos](overview-of-actual-backup-of-files.md)
-   [Información general sobre la terminación de copia de seguridad](overview-of-backup-termination.md)

 

 



