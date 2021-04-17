---
description: Para que una aplicación use cualquiera de las funciones de teléfono complementarias de TAPI 30, necesita una conexión a TAPI, a través de la cual puede recibir mensajes.
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: Inicialización y apagado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6831b8cfda84ac564450caec554191198fd4c21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677507"
---
# <a name="initialization-and-shutdown"></a>Inicialización y apagado

Para que una aplicación use cualquiera de las 30 funciones de teléfono complementarias de TAPI, necesita una conexión a TAPI, a través de la cual puede recibir mensajes. La aplicación establece esta conexión mediante la función [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) . En esta función, la aplicación especifica el mecanismo de notificación mediante el cual TAPI informa a la aplicación de los cambios en el estado del teléfono y de la finalización asincrónica de las funciones de teléfono.

La función [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) devuelve dos fragmentos de información a la aplicación: un *identificador* de la aplicación y el número de dispositivos telefónicos. El identificador de la aplicación representa el uso de TAPI de la aplicación. Las funciones TAPI que usan identificadores de teléfono no requieren el identificador de la aplicación, ya que este identificador se deriva del identificador de teléfono especificado.

La segunda parte de la información devuelta por [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) es el número de dispositivos telefónicos disponibles para TAPI. Los dispositivos telefónicos se identifican por su identificador de dispositivo (ID. de *dispositivo*). Los identificadores de dispositivo válidos van desde cero hasta el número de dispositivos de teléfono menos uno. Por ejemplo, si **phoneInitializeEx** informa de que hay dos dispositivos telefónicos en un sistema, los identificadores de dispositivos telefónicos válidos son 0 y 1. Una vez que una aplicación ha terminado de usar las funciones de teléfono de TAPI, invoca a [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown), pasando su identificador de aplicación para cerrar el uso de TAPI. Esto permite a TAPI liberar los recursos asignados a la aplicación.

Las aplicaciones no deben invocar [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) sin abrir posteriormente un teléfono (al menos para la supervisión). Si la aplicación no supervisa y no usa ningún dispositivo, debe llamar a [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) para que los recursos de memoria asignados por la biblioteca de vínculos dinámicos de TAPI se puedan liberar si no se necesitan y la propia biblioteca se puede descargar de la memoria mientras no se necesite.

Tanto [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) como [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) funcionan sincrónicamente. Es decir, estas funciones devuelven una indicación de éxito o error y nunca devuelven un identificador de solicitud asincrónica.

 

 



