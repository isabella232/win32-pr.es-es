---
description: Las funciones de configuración incluyen la funcionalidad de cola de archivos.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Colas de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002325"
---
# <a name="file-queues"></a>Colas de archivos

Las funciones de configuración incluyen la funcionalidad de cola de archivos. Una cola de archivos es una lista de operaciones de copia, cambio de nombre y eliminación de archivos. Estas operaciones se pueden enviar a la cola en cualquier orden. Cuando se confirma la cola, estas operaciones se procesan como un lote, en orden del tipo de operación.

En las secciones siguientes se explica qué es una cola y cómo utilizarla al crear una aplicación de instalación. También se describe el orden en el que se procesan las operaciones de archivo en cola a medida que se confirman las colas y las notificaciones que la cola envía a una rutina de devolución de llamada en cada fase.

-   [Acerca de las colas de archivos](about-file-queues.md)
-   [Usar colas de archivos](using-file-queues.md)
-   [Referencia de cola de archivos](file-queue-reference.md)

 

 



