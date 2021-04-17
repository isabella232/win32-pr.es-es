---
description: Después de crear un archivo INF, normalmente escribirá el código fuente de la aplicación de instalación. Llame a las funciones de configuración desde la aplicación de instalación para realizar muchas operaciones de instalación.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Crear aplicaciones de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667884"
---
# <a name="creating-setup-applications"></a>Crear aplicaciones de instalación

Después de crear un archivo INF, normalmente escribirá el código fuente de la aplicación de instalación. Llame a las funciones de configuración desde la aplicación de instalación para realizar muchas operaciones de instalación.

En los pasos siguientes se describe una manera de usar las funciones de configuración de para crear una aplicación de instalación. Puede usar este ejemplo como punto de partida o desarrollar su propio algoritmo de instalación.

**Inicialización**

-   [Abra el archivo INF y, si procede, anexe otros archivos INF.](opening-the-inf-file.md)
-   [Extraiga la información del archivo INF.](extracting-file-information-from-the-inf-file.md)
-   [Recopile información de configuración del usuario.](gathering-setup-information-from-the-user.md)
-   [Cree una cola.](creating-a-queue-and-queuing-file-operations.md)

**Archivos de instalación**

-   [Confirme la cola y especifique una rutina de devolución de llamada.](committing-the-queue.md)
-   [Actualice la información del registro.](updating-registry-information.md)

**Limpieza**

-   [Cierre la cola de archivos y el archivo INF.](closing-the-file-queue-and-inf-file.md)
-   [Libere cualquier otro recurso del sistema y finalice el programa.](releasing-other-system-resources.md)

 

 



