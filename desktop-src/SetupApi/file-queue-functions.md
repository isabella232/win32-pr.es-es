---
description: Las siguientes funciones se usan con colas de archivos.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Funciones de cola de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70087bfcc00f2c3d86c93cc62081adc9aa50705d248d79a524435c95f480562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887084"
---
# <a name="file-queue-functions"></a>Funciones de cola de archivos

Las siguientes funciones se usan con colas de archivos.



| Función                                                             | Descripción                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | Finaliza la cola. Las transacciones restantes no se confirman.                                   |
| [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | Confirma todas las transacciones en cola.                                                                      |
| [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | Inicializa y devuelve un identificador a la cola de archivos.                                                   |
| [**SetupPromptReboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | Solicita al usuario que reinicie su equipo, si es necesario.                                         |
| [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | Pone en cola una copia de archivo.                                                                                   |
| [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | Pone en cola los archivos en una sección Archivos de copia inf.                                                        |
| [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | Pone en cola los archivos de una sección Archivos de copia inf con la información predeterminada especificada en un archivo INF. |
| [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | Pone en cola una eliminación de archivos.                                                                               |
| [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | Pone en cola los archivos en una sección Inf Delete Files (Eliminar archivos INF).                                                      |
| [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | Pone en cola el nombre de un archivo.                                                                                 |
| [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | Pone en cola los archivos en una sección INF Rename Files (Archivos de cambio de nombre de INF).                                                      |
| [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | Examina la cola de archivos.                                                                                 |
| [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | Establece la invalidación de la ruta de acceso de la plataforma.                                                                      |



 

 

 



