---
title: Uso del Windows de eventos
description: En esta sección se enumeran los temas que explican las tareas que se pueden realizar mediante el SDK Windows Recopilador de eventos. En cada uno de los temas siguientes se incluyen ejemplos de código y explicaciones de todas las tareas.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b928dddcd3e70848d510a8986962d478bedbe6f2f8bffcbec19c276983328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006015"
---
# <a name="using-windows-event-collector"></a>Uso del Windows de eventos

En esta sección se enumeran los temas que explican las tareas que se pueden realizar mediante el SDK Windows Recopilador de eventos. En cada uno de los temas siguientes se incluyen ejemplos de código y explicaciones de todas las tareas.

## <a name="in-this-section"></a>En esta sección

-   [Creación de una suscripción iniciada por el recopilador](creating-an-event-collector-subscription.md)

    Proporciona información y un ejemplo de código de C++ para crear una suscripción iniciada por el recopilador. Una suscripción iniciada por el recopilador le permite recibir eventos en un equipo local (el recopilador de eventos) que se reenvían desde un equipo remoto (un origen de eventos).

-   [Configuración de una suscripción iniciada por origen](setting-up-a-source-initiated-subscription.md)

    Proporciona información y un ejemplo de código de C++ para crear una suscripción iniciada por el origen. Una suscripción iniciada por el origen le permite recibir eventos en un equipo local (el recopilador de eventos) que se reenvían desde un equipo remoto (un origen de eventos) sin especificar los orígenes de eventos en la suscripción.

-   [Agregar un origen de eventos a una suscripción iniciada por el recopilador](adding-an-event-source-to-an-event-collector-subscription.md)

    Proporciona información y un ejemplo de código de C++ para agregar un origen de eventos (equipo local o equipo remoto) a una suscripción iniciada por el recopilador. Una suscripción iniciada por el recopilador no puede empezar a recopilar eventos hasta que se agrega un origen de eventos a la suscripción.

-   [Creación de suscripciones de eventos de hardware](creating-hardware-event-subscriptions.md)

    Proporciona información sobre cómo crear una suscripción de eventos para recibir eventos de hardware desde un equipo que tenga instalado un controlador de administración de placa base (BMC).

-   [Eliminación de una suscripción del recopilador de eventos](deleting-an-event-collector-subscription.md)

    Proporciona información y un ejemplo de código de C++ para eliminar una suscripción del recopilador de eventos de un equipo local.

-   [Mostrar las propiedades de una suscripción del recopilador de eventos](displaying-the-properties-of-an-event-collector-subscription.md)

    Proporciona información y un ejemplo de código de C++ para mostrar los valores de propiedad de una suscripción del recopilador de eventos. Los valores de propiedad pueden proporcionar información útil, como las direcciones de los orígenes de eventos, el estado de la suscripción y los orígenes de eventos, e información sobre cómo se entregan los eventos.

-   [Mostrar el estado de una suscripción del recopilador de eventos](displaying-the-status-of-an-event-collector-subscription.md)

    Proporciona información y un ejemplo de código de C++ para mostrar el estado en tiempo de ejecución de los orígenes de eventos asociados a una suscripción del Recopilador de eventos. Esto le permite ver mensajes de error que pueden ayudar a resolver problemas, lo que impide que un origen de eventos reenvía eventos.

-   [Enumerar suscripciones del recopilador de eventos](listing-event-collector-subscriptions.md)

    Proporciona información y un ejemplo de código de C++ para enumerar las suscripciones que existen en un equipo local. Puede usar los nombres de suscripción que se obtienen con este ejemplo para eliminar una suscripción, agregar un origen de eventos a una suscripción, recuperar las propiedades de una suscripción o ver el estado de una suscripción.

-   [Quitar un origen de eventos de una suscripción iniciada por el recopilador](removing-an-event-source-from-an-event-collector-subscription.md)

    Proporciona información y un ejemplo de código de C++ para quitar un origen de eventos de una suscripción iniciada por el recopilador. Puede quitar un origen de eventos de una suscripción iniciada por el recopilador sin deshabilitar la suscripción.

-   [Reintentar una suscripción del recopilador de eventos](retrying-an-event-collector-subscription.md)

    Proporciona información y un ejemplo de código de C++ para reintentar una suscripción del recopilador de eventos cuando se produce un error en uno o varios orígenes de eventos. Puede reintentar un único origen de eventos o puede volver a intentar toda la suscripción.

 

 




