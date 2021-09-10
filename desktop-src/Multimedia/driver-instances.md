---
title: Instancias de controlador
description: Instancias de controlador
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- controladores instalables, instancias
- controladores instalables, varias instancias
- varias instancias de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37148dcb12fbfa2984d4e55424102b5985165d9d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372200"
---
# <a name="driver-instances"></a>Instancias de controlador

Windows permite varias instancias de un controlador instalable. El sistema crea una instancia del controlador cada vez que se abre el controlador y destruye la instancia cuando se cierra el controlador. Las instancias de controlador son especialmente útiles para controladores instalables que admiten varios dispositivos o que se abren varias veces por varias aplicaciones o por la misma aplicación.

Para ayudar al controlador a realizar un seguimiento de las instancias, el sistema envía un identificador de instancia de controlador con cada mensaje de controlador una vez creada la instancia. Dado que este identificador identifica de forma única la instancia, los controladores instalables suelen asociar el identificador con la memoria y otros recursos que han asignado específicamente para la instancia.

Cuando se abre la primera instancia, el sistema envía los mensajes [**DRV \_ LOAD,**](drv-load.md) [**DRV \_ ENABLE**](drv-enable.md)y [**DRV \_ OPEN**](drv-open.md) al controlador en ese orden. Los mensajes DRV LOAD y DRV ENABLE notifican al controlador que ahora está en memoria \_ y está habilitado para su \_ funcionamiento. El mensaje DRV \_ OPEN identifica el identificador de instancia y puede incluir información de configuración para la instancia. En cada apertura posterior de una instancia del mismo controlador, el sistema envía solo un mensaje DRV \_ OPEN.

Al procesar un mensaje LOAD de DRV, un controlador normalmente lee las opciones de configuración del Registro, configura el controlador y cualquier hardware asociado, y asigna memoria para que la usen todas las instancias \_ del controlador. Si un controlador no puede completar la configuración o asignar memoria, devuelve cero para dirigir al sistema a quitar inmediatamente el controlador de la memoria e impedir que se envíen mensajes posteriores. Al procesar el mensaje DRV ENABLE, el controlador prepara el hardware para recibir y procesar las solicitudes de entrada y salida \_ (E/S). La preparación puede incluir la instalación de controladores de interrupción.

Al procesar el mensaje DRV OPEN, el controlador asigna la memoria o los recursos requeridos por la instancia determinada del controlador y, a continuación, devuelve \_ un valor distinto de cero. El sistema usa este valor distinto de cero como identificador *del controlador* en los mensajes de controlador posteriores de la instancia. El controlador puede usar este identificador para cualquier propósito. Por ejemplo, algunos controladores usan un identificador de memoria para que el identificador obtenga acceso rápido a la memoria que contiene información sobre la instancia determinada.

Muchos controladores instalables procesan el segundo parámetro del mensaje DRV OPEN, lo que proporciona al sistema y a las aplicaciones los medios para enviar información adicional al controlador al \_ abrir una instancia. El parámetro puede ser un valor único o una dirección de una estructura que contiene un conjunto de valores. Al procesar DRV OPEN, el controlador comprueba el parámetro para determinar si es un valor y usa los valores especificados, si los hay, para completar la creación \_ de la instancia.

El sistema envía un [**mensaje DRV \_ CLOSE**](drv-close.md) cada vez que se cierra una instancia. El identificador de instancia enviado con el mensaje identifica la instancia que se va a cerrar. Cuando se cierra la última instancia restante, el sistema envía los mensajes DRV \_ CLOSE, [**DRV \_ DISABLE**](drv-disable.md)y [**DRV \_ FREE**](drv-free.md) en ese orden. El mensaje DRV CLOSE indica al controlador que cierre la instancia y los mensajes DRV DISABLE y DRV FREE notifican al controlador que ahora está deshabilitado y se liberará inmediatamente de \_ \_ la \_ memoria.

Al procesar el mensaje DRV CLOSE, el controlador normalmente libera la memoria o los recursos \_ asignados para la instancia. Al procesar el mensaje DISABLE de DRV, el controlador coloca cualquier hardware en un estado inactivo, lo que puede incluir la eliminación \_ de controladores de interrupción. Al procesar el mensaje DRV FREE, el controlador libera la memoria o los recursos \_ que todavía están asignados.

Los controladores instalables no son necesarios para admitir varias instancias. Un controlador puede evitar que se cree cualquier instancia devolviendo cero para el [**mensaje DRV \_ OPEN.**](drv-open.md)

 

 




