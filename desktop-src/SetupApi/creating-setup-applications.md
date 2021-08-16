---
description: Después de crear un archivo INF, normalmente escribirá el código fuente de la aplicación de instalación. Llame a las funciones de instalación desde la aplicación de instalación para realizar muchas operaciones de instalación.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Creación de aplicaciones de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77f920a024a4414690baad7684af90a30ee4ca3c9f96a2c6f61b1b84430c072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887451"
---
# <a name="creating-setup-applications"></a>Creación de aplicaciones de instalación

Después de crear un archivo INF, normalmente escribirá el código fuente de la aplicación de instalación. Llame a las funciones de instalación desde la aplicación de instalación para realizar muchas operaciones de instalación.

Los pasos siguientes abarcan una manera de usar las funciones de instalación para crear una aplicación de instalación. Puede usar este ejemplo como punto de partida o desarrollar su propio algoritmo de instalación.

**Inicialización**

-   [Abra inf y, si procede, anexe otros archivos INF.](opening-the-inf-file.md)
-   [Extraiga información de archivo del archivo INF.](extracting-file-information-from-the-inf-file.md)
-   [Recopila la información de configuración del usuario.](gathering-setup-information-from-the-user.md)
-   [Cree una cola.](creating-a-queue-and-queuing-file-operations.md)

**Instalación de archivos**

-   [Confirme la cola, especificando una rutina de devolución de llamada.](committing-the-queue.md)
-   [Actualice la información del Registro.](updating-registry-information.md)

**Limpieza**

-   [Cierre la cola de archivos e INF.](closing-the-file-queue-and-inf-file.md)
-   [Libere cualquier otro recurso del sistema y finalice el programa.](releasing-other-system-resources.md)

 

 



