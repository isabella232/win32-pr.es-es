---
title: Funciones de devolución de llamada de estado
description: Funciones de devolución de llamada de estado
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funciones de devolución de llamada de AVICap, estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07539b016ea344f2a38d54a7274d01006532ed040ea3fa96990bff09e22d470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037165"
---
# <a name="status-callback-functions"></a>Funciones de devolución de llamada de estado

Una ventana de captura puede enviar mensajes a la función de devolución de llamada de estado al capturar vídeo en el disco o durante otras operaciones largas para notificar a la aplicación el progreso de una operación. La información de estado incluye un identificador de mensaje y una cadena de texto con formato lista para mostrarse. La aplicación puede usar el identificador de mensaje para filtrar las notificaciones y limitar los mensajes que se presentarán al usuario. Durante las operaciones de captura, el primer mensaje enviado a la función de devolución de llamada es siempre IDS CAP BEGIN y el último \_ \_ es siempre IDS CAP \_ \_ END. Un identificador de mensaje de cero indica que se está iniciando una nueva operación y que la función de devolución de llamada debe borrar el estado actual.

 

 




