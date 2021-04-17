---
description: Una operación que se completa de forma asincrónica realiza parte de su procesamiento en la llamada de función realizada por la aplicación y el resto de la misma en un subproceso de ejecución independiente después de que TAPI 2. x se haya devuelto desde la llamada de función.
ms.assetid: 37b544e4-6413-4741-b8b6-ec676ce4ca97
title: Funciones asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e792a4b1d6a25a4f49fbb2abe2c19ce3071ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678123"
---
# <a name="asynchronous-functions"></a>Funciones asincrónicas

Una operación que se completa de forma asincrónica realiza parte de su procesamiento en la llamada de función realizada por la aplicación y el resto de la misma en un subproceso de ejecución independiente después de que TAPI 2. x se haya devuelto desde la llamada de función. Para garantizar la finalización del procesamiento de la llamada, el proveedor de servicios vectore la solicitud a otra entidad activa del sistema (por ejemplo, un servidor LAN, hardware de complemento, conmutador o red) y, a continuación, vuelve a la aplicación. En este momento, se devuelve un resultado de error negativo o un identificador de solicitud positivo a la aplicación.

En el momento de la finalización asincrónica (el proveedor de servicios ha recibido una interrupción del hardware, lo que significa que se debe entregar un mensaje), el proveedor de servicios llama a TAPISRV e informa de que "el evento *X* se acaba de realizar. Entregue un mensaje apropiado a todas las aplicaciones afectadas ". Cuando TAPISRV recibe este mensaje, reenvía el mensaje a la biblioteca de vínculos dinámicos TAPI, en el proceso de la aplicación, que, a su vez, envía un mensaje de ventana, señala un identificador de evento o se envía a un puerto de finalización de e/s, de acuerdo con el esquema de notificación de mensajes seleccionado por la aplicación en [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) o [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa).

Cuando se completa la parte asincrónica de la operación, se envía un mensaje de [**\_ respuesta de línea**](./line-reply.md) (o [**\_ respuesta de teléfono**](./phone-reply.md)) a la aplicación. Este mensaje contiene, como uno de sus parámetros, el identificador de solicitud devuelto por la llamada de función. Este identificador de solicitud permite a la aplicación determinar qué solicitud original se ha completado. (Las aplicaciones deben recordar los identificadores de solicitud de todas sus solicitudes en curso para que los mensajes de respuesta se puedan controlar correctamente). Un segundo parámetro para el mensaje de respuesta de línea \_ (o respuesta de teléfono \_ ) es el valor devuelto asincrónico. Puede ser un valor negativo (para un error) o cero si la operación se completó correctamente. En el caso de las operaciones asincrónicas, se puede devolver cualquiera de los valores devueltos como parte de la función Return o como el parámetro *dwParam2* en el mensaje de respuesta de línea \_ o de respuesta de teléfono \_ . El valor 0, que indica que se ha realizado correctamente, solo se devolverá en el mensaje de respuesta de línea \_ y nunca como el valor devuelto de la función.

Las funciones Initialize ( [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) y [**phoneInitializeEx**](/windows/win32/api/tapi/nf-tapi-phoneinitializeexa)) indican a TAPI cómo enviar estos mensajes a la aplicación.

> [!Note]  
> En algunos casos, si una aplicación multiproceso llama a una función asincrónica desde un subproceso distinto del subproceso desde el que la aplicación inicializó el dispositivo de línea o teléfono, la aplicación puede recibir el mensaje de respuesta de [**línea \_**](./line-reply.md) o de [**\_ respuesta de teléfono**](./phone-reply.md) antes de que se devuelva la función asincrónica. En tales casos, la aplicación debe guardar los parámetros del mensaje y esperar hasta que se devuelva la función asincrónica y se conozca el identificador de la solicitud antes de procesar el mensaje.

 

 

 
