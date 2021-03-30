---
description: Las siguientes notificaciones se usan con las colas de archivos. Para obtener más información sobre el formato y el uso de las notificaciones, vea notificaciones.
ms.assetid: 4a171b4a-8623-4be3-81ee-99081fe23034
title: Notificaciones de cola de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b674dee015c4c9408ff5dc853d5d3b2412e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082986"
---
# <a name="file-queue-notifications"></a>Notificaciones de cola de archivos

Las siguientes notificaciones se usan con las colas de archivos. Para obtener más información sobre el formato y el uso de las notificaciones, vea [notificaciones](notifications.md).



| notificación                                                      | Descripción                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)         | Se produjo un error durante una operación de copia de archivos.                                                  |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)     | Se produjo un error durante una operación de eliminación de archivos.                                                 |
| [**SPFILENOTIFY \_ ENDCOPY**](spfilenotify-endcopy.md)             | Ha finalizado una operación de copia de archivos.                                                                 |
| [**SPFILENOTIFY \_ ENDDELETE**](spfilenotify-enddelete.md)         | Ha finalizado una operación de eliminación de archivos.                                                                |
| [**SPFILENOTIFY \_ ENDQUEUE**](spfilenotify-endqueue.md)           | La cola ha terminado de confirmarse.                                                                  |
| [**SPFILENOTIFY \_ ENDRENAME**](spfilenotify-endrename.md)         | Ha finalizado una operación de cambio de nombre de archivo.                                                                  |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)     | Ha finalizado una subcola (copia, cambio de nombre o eliminación).                                               |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md) | El archivo estaba en uso y la operación actual se ha retrasado hasta que se reinicia el sistema.       |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)   | El idioma de la operación actual no coincide con el idioma del sistema.                           |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)         | Se necesitan nuevos medios de origen.                                                                         |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)         | Se ha analizado un nodo en la cola de archivos. (Solo [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) ) |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)     | Se produjo un error durante una operación de cambio de nombre de archivo.                                                 |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)         | Se ha iniciado una operación de copia de archivos.                                                                  |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)     | Se ha iniciado una operación de eliminación de archivos.                                                                |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)       | La cola ha empezado a confirmarse.                                                                    |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)     | Se ha iniciado una operación de cambio de nombre de archivo.                                                                |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md) | Se ha iniciado una subcola (copia, cambio de nombre o eliminación).                                             |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)   | Ya existe una copia del archivo especificado en el destino.                                          |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)     | Existe una versión más reciente del archivo especificado en el destino.                                         |



 

 

 



