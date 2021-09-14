---
title: Funciones de devolución de llamada de estado
description: Funciones de devolución de llamada de estado
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funciones de devolución de llamada de AVICap, estado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161373"
---
# <a name="status-callback-functions"></a>Funciones de devolución de llamada de estado

Una ventana de captura puede enviar mensajes a la función de devolución de llamada de estado al capturar vídeo en el disco o durante otras operaciones largas para notificar a la aplicación el progreso de una operación. La información de estado incluye un identificador de mensaje y una cadena de texto con formato lista para mostrarse. La aplicación puede usar el identificador de mensaje para filtrar las notificaciones y limitar los mensajes que se presentarán al usuario. Durante las operaciones de captura, el primer mensaje enviado a la función de devolución de llamada es siempre IDS CAP BEGIN y el último \_ \_ es siempre IDS CAP \_ \_ END. Un identificador de mensaje de cero indica que se está iniciando una nueva operación y que la función de devolución de llamada debe borrar el estado actual.

 

 




