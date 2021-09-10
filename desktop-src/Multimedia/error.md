---
title: Error
description: Error
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- Funciones de devolución de llamada de AVICap, mensajes de notificación de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371977"
---
# <a name="error"></a>Error

Una ventana de captura usa mensajes de notificación de error para notificar a la aplicación errores de AVICap, como que se queda sin espacio en disco, intenta escribir en un archivo de solo lectura, no tiene acceso al hardware o quita demasiados fotogramas. El contenido de una notificación de error incluye un identificador de mensaje y una cadena de texto con formato lista para mostrarse. La aplicación puede usar el identificador de mensaje para filtrar las notificaciones y limitar los mensajes que se presentarán al usuario. Un identificador de mensaje de cero indica que se está iniciando una nueva operación y que la función de devolución de llamada debe borrar cualquier mensaje de error mostrado.

 

 




