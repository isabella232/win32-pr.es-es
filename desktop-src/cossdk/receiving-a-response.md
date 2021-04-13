---
description: Recibir una respuesta
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Recibir una respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539286"
---
# <a name="receiving-a-response"></a>Recibir una respuesta

Dado que los componentes en cola están diseñados para funcionar de forma asincrónica, las aplicaciones cliente no deben bloquearse mientras se espera una respuesta de una solicitud en cola. No obstante, a menudo resulta útil para la aplicación cliente o una aplicación relacionada en el equipo cliente para recibir una respuesta a la larga. Por ejemplo, es posible que un cliente desee recibir una notificación cuando se haya completado correctamente una transacción solicitada.

Hay varias maneras de que un componente en cola envíe una respuesta de vuelta a su llamador de forma asincrónica. Por ejemplo, podría enviar un correo electrónico. Como alternativa, el servidor podría publicar eventos débilmente acoplados a los que el cliente podría suscribirse.

Otra forma de que un cliente obtenga una respuesta de un componente en cola que se ejecuta en un servidor es para que el cliente pase el método llamado a un objeto de notificación. Un objeto de notificación es una instancia de un componente en cola que se ejecuta en el cliente. Este tipo de objeto de notificación podría ser bastante sencillo, que solo contiene un entero que se usa para representar un valor de error, o podría ser bastante complejo, con toda la información necesaria para revertir una transacción en el cliente. En cualquier caso, el cliente que realiza la llamada pasa un objeto de notificación como parámetro de entrada siempre que se espera una respuesta de un componente en cola que se ejecuta en un servidor. Dado que el objeto de notificación está en cola, el servidor puede llamar a en sus métodos para modificar su estado, que el cliente puede leer posteriormente. En este escenario, el servicio de componentes en cola de COM+ se utiliza tanto en el cliente como en el servidor para permitir la comunicación asincrónica en ambas direcciones.

 

 



