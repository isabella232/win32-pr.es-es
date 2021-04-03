---
title: Error
description: Error
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- Funciones de devolución de llamada AVICap, mensajes de notificación de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076141"
---
# <a name="error"></a>Error

Una ventana de captura utiliza mensajes de notificación de errores para notificar a la aplicación de errores de AVICap, como la falta de espacio en disco, el intento de escribir en un archivo de solo lectura, no tener acceso al hardware o quitar demasiados fotogramas. El contenido de una notificación de error incluye un identificador de mensaje y una cadena de texto con formato lista para su presentación. La aplicación puede usar el identificador de mensaje para filtrar las notificaciones y limitar los mensajes que se van a presentar al usuario. Un identificador de mensaje de cero indica que se está iniciando una nueva operación y que la función de devolución de llamada debe borrar cualquier mensaje de error mostrado.

 

 




