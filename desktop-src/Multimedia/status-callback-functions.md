---
title: Funciones de devolución de llamada de estado
description: Funciones de devolución de llamada de estado
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funciones de devolución de llamada AVICap, estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418702"
---
# <a name="status-callback-functions"></a>Funciones de devolución de llamada de estado

Una ventana de captura puede enviar mensajes a la función de devolución de llamada de estado durante la captura de vídeo en disco o durante otras operaciones largas para notificar a la aplicación el progreso de una operación. La información de estado incluye un identificador de mensaje y una cadena de texto con formato lista para su presentación. La aplicación puede usar el identificador de mensaje para filtrar las notificaciones y limitar los mensajes que se van a presentar al usuario. Durante las operaciones de captura, el primer mensaje enviado a la función de devolución de llamada es siempre ID \_ Cap \_ Begin y el último es el extremo de los identificadores \_ \_ . Un identificador de mensaje de cero indica que se está iniciando una nueva operación y que la función de devolución de llamada debe borrar el estado actual.

 

 




