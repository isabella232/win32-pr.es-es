---
description: La rutina de devolución de llamada de cola predeterminada controla las notificaciones enviadas por SetupCommitFileQueue de forma genérica.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: Acerca de la rutina de devolución de llamada de cola predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907855"
---
# <a name="about-the-default-queue-callback-routine"></a>Acerca de la rutina de devolución de llamada de cola predeterminada

La rutina de devolución de llamada de cola predeterminada controla las notificaciones enviadas por [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) de forma genérica. Mediante el uso de la rutina predeterminada, obtiene una interfaz de usuario preparada para crear cuadros de diálogo de instalación comunes. Se recomienda usar la rutina de devolución de llamada de cola predeterminada, tanto para facilitar el uso como para garantizar una apariencia y un comportamiento coherentes de los cuadros de diálogo generados durante la instalación.

La rutina de devolución de llamada predeterminada requiere una estructura de contexto para mantener el registro interno. Además, la cola pasa información adicional relevante a la notificación actual en un conjunto de parámetros, *Param1* y *Param2*.

Por ejemplo, si la cola envía una notificación de SPFILENOTIFY \_ NEEDMEDIA a la rutina de devolución de llamada predeterminada, *Param1* apunta a una estructura de [**\_ medios de origen**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) que contiene información sobre los medios necesarios y *Param2* apunta a una matriz de caracteres que puede recibir información de la ruta de acceso del usuario.

La rutina de devolución de llamada predeterminada usa esta información para pedir al usuario que inserte los medios de origen necesarios, especifique una nueva ruta de acceso, omita la copia del archivo actual o cancele la operación actual. La rutina de devolución de llamada de cola predeterminada devuelve FILEOP \_ NEWPATH, FILEOP \_ doit, FILEOP \_ SKIP o FILEOP \_ Abort a la cola, dependiendo de la acción realizada por el usuario.

Para obtener información sobre cómo la rutina de devolución de llamada de cola predeterminada controla cada notificación de cola, vea [notificaciones de cola de archivos](file-queue-notifications.md).

Para obtener información sobre las rutinas de devolución de llamada de cola personalizadas, vea [crear una rutina de devolución de llamada de cola personalizada](creating-a-custom-queue-callback-routine.md).

 

 



