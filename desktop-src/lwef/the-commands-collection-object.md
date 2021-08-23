---
title: El objeto de colección Commands
description: El objeto de colección Commands
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f7933bd973ae500b75abb51c47899fa60322444d49fe0835f6bfa3efab97f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975665"
---
# <a name="the-commands-collection-object"></a>El objeto de colección Commands

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El servidor de Microsoft Agent mantiene una lista de comandos que están disponibles actualmente para el usuario. Esta lista incluye comandos que el servidor define para la interacción general (como Ocultar y abrir la ventana Comandos de voz), la lista de clientes disponibles (pero no activos de entrada) y los comandos definidos por el cliente activo actual. Los dos primeros conjuntos de comandos son comandos globales; es decir, están disponibles en cualquier momento, independientemente del cliente activo de entrada. Los comandos definidos por el cliente solo están disponibles cuando ese cliente está activo en la entrada y el carácter está visible.

Cada aplicación cliente puede definir una colección de comandos denominada colección [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) Para agregar un comando a la colección, use el [**método Add**](add-method.md) [**o Insert.**](insert-method.md) Aunque puede especificar las propiedades de un comando con instrucciones independientes, para obtener un rendimiento óptimo del código, especifique todas las propiedades de un comando en la instrucción del método **Add** o **Insert.** Para cada comando de la colección, puede determinar si el acceso del usuario al comando aparece en el menú emergente del carácter, en la ventana Comandos de voz, en ambos o en ninguno de ellos. Por ejemplo, si desea que un comando aparezca en el menú emergente del carácter, establezca las propiedades [**Título**](caption-property.md) y [**Visible del**](visible-property.md) comando. Para mostrar el comando en la ventana Comandos de voz, establezca las propiedades [**VoiceCaption**](voicecaption-property.md) y [**Voice del**](voice-property.md) comando.

Un usuario puede acceder a los comandos comm [**individuales**](/windows/desktop/lwef/the-commands-collection-object)y de la colección solo cuando la aplicación cliente está activa en la entrada. Por lo tanto, cuando pueda compartir el carácter con otras aplicaciones cliente, normalmente querrá establecer las propiedades [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)y [**Voice**](voice-property.md) para el objeto de colección **Commands,** así como para los comandos de la colección. Esto coloca una entrada para la **colección Comandos** en el menú emergente de un carácter y en la ventana Comandos de voz.

Cuando el usuario cambia al cliente [](/windows/desktop/lwef/the-commands-collection-object) eligiendo su entrada Comandos, el servidor activa automáticamente la entrada del cliente, notificando a la aplicación cliente mediante el evento [**ActivateInput**](activateinput-event.md) y hace que los comandos de su colección estén disponibles. El servidor también notifica al cliente que ya no está activo de entrada con el [**evento DeActivateInput.**](deactivateinput-event.md) Esto permite que el servidor presente y acepte solo los comandos que se aplican al contexto del cliente activo de entrada actual. También sirve para evitar conflictos de nombre de comando entre clientes.

Un cliente también puede solicitar explícitamente que se haga el cliente activo de entrada mediante [**el método Activate.**](activate-method.md) Este método también admite la configuración de la aplicación para que no sea el cliente activo de entrada. Es posible que quiera usar este método al compartir un carácter con otra aplicación, estableciendo la aplicación en input-active cuando la ventana de la aplicación obtiene el foco y no input-active cuando pierde el foco.

De forma similar, puede usar el [**método Activate**](activate-method.md) para establecer que la aplicación sea (o no) el cliente activo del carácter. El cliente activo es el cliente que recibe la entrada cuando su carácter es el carácter superior. Cuando este estado cambia, el servidor notifica a la aplicación con el [**evento ActiveClientChange.**](activeclientchange-event.md)

Cuando se muestra el menú emergente de un carácter, los cambios en las propiedades de una colección Comandos o los comandos de su colección no aparecen hasta que el usuario vuelve [**a**](/windows/desktop/lwef/the-commands-collection-object) mostrar el menú. Sin embargo, la ventana Comandos muestra los cambios a medida que se hacen.

-   [Métodos de objeto Commands](commands-object-methods.md)
-   [Propiedades del objeto Commands](commands-object-properties.md)

 

 