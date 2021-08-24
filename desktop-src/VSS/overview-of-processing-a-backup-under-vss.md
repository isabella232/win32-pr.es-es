---
description: Al procesar una copia de seguridad, el solicitante y los escritores se coordinan para proporcionar una imagen estable del sistema desde la que realizar copias de seguridad de los datos (el volumen de instantáneas), agrupar los archivos en función de su uso y almacenar información sobre los datos guardados.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Información general sobre el procesamiento de una copia de seguridad en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60874b1c66bcc75788912f54e5b3ffc8314f1bc0d0ad6d92b815725af727936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510015"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Información general sobre el procesamiento de una copia de seguridad en VSS

Al procesar una copia de seguridad, el solicitante y los escritores se coordinan para proporcionar una imagen estable del sistema desde la que realizar copias de seguridad de los datos (el volumen de instantáneas), agrupar los archivos en función de su uso y almacenar información sobre los datos guardados. Todo esto debe hacerse mientras se crea solo una interrupción mínima en el flujo de trabajo normal del escritor.

Un solicitante consulta a los escritores sus metadatos, procesa estos datos, notifica a los escritores antes del inicio de la instantánea y de las operaciones de copia de seguridad y, a continuación, notifica de nuevo a los escritores una vez que finalizan las operaciones de instantánea y copia de seguridad.

En respuesta a estas notificaciones, el sistema de escritura proporciona información sobre los archivos de los que se va a realizar una copia de seguridad, incluida la especificación de grupos de archivos para coordinar [*(componentes*](vssgloss-c.md)) , se pausa en sus operaciones de E/S antes de una instantánea y, a continuación, vuelve al funcionamiento normal después de la finalización de una instantánea o al final de la copia de seguridad.

Durante el procesamiento de la copia de seguridad, un escritor especifica los archivos de los que es responsable a través de sus metadatos de solo lectura: el documento de metadatos del escritor (vea [VsS Metadata: Working with](working-with-the-writer-metadata-document.md)the Writer Metadata Document ). A continuación, el solicitante interpreta estos metadatos, elige de qué hacer una copia de seguridad y almacena estas decisiones en su propio objeto de metadatos, el documento componentes de copia de seguridad (vea [VSS Metadata: Working with](working-with-the-backup-components-document.md)the Backup Components Document ). Este documento de componentes de copia de seguridad está disponible para la inspección y modificación del escritor durante las operaciones de copia de seguridad y restauración.

En este diagrama se muestran las interacciones entre el solicitante, el servicio VSS, la compatibilidad del kernel de VSS, los escritores de VSS implicados y los proveedores de hardware de VSS.

![interacciones entre solicitantes, componentes de copia de seguridad, escritores y proveedores](images/vssimpl.png)

Para comprender mejor las tareas básicas implicadas en la realización de una copia de seguridad, es útil dividir esta información general en los temas siguientes:

-   [Información general sobre la inicialización de copia de seguridad](overview-of-backup-initialization.md)
-   [Información general de la fase de detección de copia de seguridad](overview-of-the-backup-discovery-phase.md)
-   [Información general de las tareas previas a la copia de seguridad](overview-of-pre-backup-tasks.md)
-   [Información general sobre la copia de seguridad real de archivos](overview-of-actual-backup-of-files.md)
-   [Información general sobre la terminación de copia de seguridad](overview-of-backup-termination.md)

 

 



