---
title: Instancias de controlador
description: Instancias de controlador
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- Controladores instalables, instancias
- Controladores instalables, varias instancias
- varias instancias de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37148dcb12fbfa2984d4e55424102b5985165d9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775126"
---
# <a name="driver-instances"></a>Instancias de controlador

Windows permite varias instancias de un controlador instalable. El sistema crea una instancia del controlador cada vez que se abre el controlador y destruye la instancia cuando se cierra el controlador. Las instancias de controlador son especialmente útiles para los controladores instalables que admiten varios dispositivos o que se abren en varias aplicaciones o en la misma aplicación varias veces.

Para ayudar al controlador a realizar un seguimiento de las instancias, el sistema envía un identificador de instancia de controlador con cada mensaje de controlador una vez creada la instancia. Dado que este identificador identifica de forma única la instancia, los controladores instalables a menudo asocian el identificador con la memoria y otros recursos que se han asignado específicamente para la instancia.

Cuando se abre la primera instancia, el sistema envía los mensajes de [**\_ carga DRV**](drv-load.md), [**DRV \_ enable**](drv-enable.md)y [**DRV \_ Open**](drv-open.md) al controlador en ese orden. Los \_ mensajes DRV Load y DRV \_ enable notifican al controlador que ahora está en la memoria y están habilitados para su funcionamiento. El \_ mensaje abierto DRV identifica el identificador de instancia y puede incluir información de configuración de la instancia. En cada apertura subsiguiente de una instancia del mismo controlador, el sistema solo envía un \_ mensaje abierto DRV.

Al procesar un \_ mensaje de carga drv, un controlador normalmente Lee las opciones de configuración del registro, configura el controlador y cualquier hardware asociado y asigna memoria para el uso de todas las instancias del controlador. Si un controlador no puede completar la configuración o asignar memoria, devuelve cero para indicar al sistema que quite inmediatamente el controlador de la memoria y que no se envíen los mensajes posteriores. Al procesar el \_ mensaje de habilitación drv, el controlador prepara el hardware para recibir y procesar solicitudes de entrada y salida (e/s). La preparación puede incluir la instalación de controladores de interrupción.

Al procesar el \_ mensaje abierto drv, el controlador asigna la memoria o los recursos requeridos por la instancia determinada del controlador y, a continuación, devuelve un valor distinto de cero. El sistema utiliza este valor distinto de cero como *identificador de controlador* en los mensajes de controlador posteriores para la instancia. El controlador puede usar este identificador para cualquier propósito. Por ejemplo, algunos controladores utilizan un identificador de memoria para el identificador con el fin de obtener un acceso rápido a la memoria que contiene información sobre la instancia determinada.

Muchos controladores instalables procesan el segundo parámetro del mensaje Open de DRV, lo que \_ permite al sistema y a las aplicaciones enviar información adicional al controlador al abrir una instancia de. El parámetro puede ser un valor único o una dirección de una estructura que contenga un conjunto de valores. Al procesar DRV \_ Open, el controlador comprueba el parámetro para determinar si es un valor y usa los valores especificados, si los hay, para completar la creación de la instancia.

El sistema envía un mensaje [**DRV \_ Close**](drv-close.md) cada vez que se cierra una instancia. El identificador de instancia enviado con el mensaje identifica la instancia que se va a cerrar. Cuando se cierra la última instancia restante, el sistema envía los \_ mensajes DRV Close, [**DRV \_ Disable**](drv-disable.md)y [**DRV \_ Free**](drv-free.md) en ese orden. El \_ mensaje de cierre DRV dirige el controlador para cerrar la instancia, y los \_ mensajes DRV Disable y DRV \_ Free notifican al controlador que ahora está deshabilitado y se liberarán inmediatamente de la memoria.

Al procesar el \_ mensaje de cierre drv, el controlador libera normalmente cualquier memoria o recursos asignados a la instancia. Al procesar el \_ mensaje DRV disable, el controlador coloca cualquier hardware en un estado inactivo, lo que puede incluir la eliminación de controladores de interrupción. Al procesar el mensaje de disponibilidad de DRV \_ , el controlador libera cualquier memoria o recursos que todavía estén asignados.

No es necesario que los controladores instalables admitan varias instancias. Un controlador puede impedir que se cree cualquier instancia devolviendo cero para el [**mensaje \_ abierto DRV**](drv-open.md) .

 

 




