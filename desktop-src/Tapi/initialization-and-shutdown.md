---
description: Para que una aplicación use cualquiera de las funciones de teléfono 30 adicionales de TAPIs, necesita una conexión a TAPI, a través de la cual puede recibir mensajes.
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: Inicialización y apagado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7414b78636a7ce7bf93e297b0cbef4d9dc7d6482191c1b1948235d1dc117423
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867295"
---
# <a name="initialization-and-shutdown"></a>Inicialización y apagado

Para que una aplicación use cualquiera de las 30 funciones telefónicas adicionales de TAPI, necesita una conexión a TAPI, a través de la cual puede recibir mensajes. La aplicación establece esta conexión mediante la [**función phoneInitializeEx.**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) En esta función, la aplicación especifica el mecanismo de notificación por el que TAPI informa a la aplicación de los cambios en el estado del teléfono y de la finalización asincrónica de funciones telefónicas.

La [**función phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) devuelve dos fragmentos de información *a* la aplicación: un identificador de aplicación y el número de dispositivos de teléfono. El identificador de la aplicación representa el uso de TAPI de la aplicación. Las funciones TAPI que usan identificadores de teléfono no requieren el identificador de la aplicación, ya que este identificador se deriva del identificador de teléfono especificado.

El segundo fragmento de información devuelto por [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) es el número de dispositivos de teléfono disponibles para TAPI. Teléfono dispositivos se identifican por su identificador de dispositivo *(id. de dispositivo).* Los identificadores de dispositivo válidos van desde cero hasta el número de dispositivos de teléfono menos uno. Por ejemplo, si **phoneInitializeEx** informa de que hay dos dispositivos de teléfono en un sistema, los identificadores de dispositivos telefónicos válidos son 0 y 1. Una vez que una aplicación termina de usar las funciones telefónicas de TAPI, invoca [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)y pasa su identificador de aplicación para apagar su uso de TAPI. Esto permite a TAPI liberar los recursos asignados a la aplicación.

Las aplicaciones no deben [**invocar phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) sin abrir posteriormente un teléfono (al menos para la supervisión). Si la aplicación no está supervisando y no usa ningún dispositivo, debe llamar a [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) para que los recursos de memoria asignados por la biblioteca de vínculos dinámicos TAPI se puedan liberar si no son necesarios y la propia biblioteca se puede descargar de la memoria mientras no sea necesario.

Tanto [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) como [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) funcionan sincrónicamente. Es decir, estas funciones devuelven una indicación de éxito o error y nunca devuelven un identificador de solicitud asincrónico.

 

 



