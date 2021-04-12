---
title: Objeto de colección Commands
description: Objeto de colección Commands
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2367035d86f92d57dc459564943b9e7797ecb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420551"
---
# <a name="the-commands-collection-object"></a>Objeto de colección Commands

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El servidor de agente de Microsoft mantiene una lista de comandos que están disponibles actualmente para el usuario. Esta lista incluye los comandos que define el servidor para la interacción general (por ejemplo, para ocultar y abrir la ventana comandos de voz), la lista de clientes disponibles (pero no de entrada-activo) y los comandos definidos por el cliente activo actual. Los dos primeros conjuntos de comandos son comandos globales; es decir, están disponibles en cualquier momento, independientemente del cliente de entrada-activo. Los comandos definidos por el cliente solo están disponibles cuando el cliente es de entrada y el carácter está visible.

Cada aplicación cliente puede definir una colección de comandos denominada colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Para agregar un comando a la colección, use el método [**Add**](add-method.md) o [**Insert**](insert-method.md) . Aunque puede especificar las propiedades de un comando con instrucciones independientes, para obtener un rendimiento óptimo del código, especifique todas las propiedades de un comando en la instrucción **Add** o **Insert** Method. Para cada comando de la colección, puede determinar si el acceso de usuario al comando aparece en el menú emergente del carácter, en la ventana comandos de voz, en ambos o en ninguno. Por ejemplo, si desea que aparezca un comando en el menú emergente del carácter, establezca la [**leyenda**](caption-property.md) del comando y las propiedades [**visibles**](visible-property.md) . Para mostrar el comando en la ventana comandos de voz, establezca las propiedades [**VoiceCaption**](voicecaption-property.md) y [**Voice**](voice-property.md) del comando.

Un usuario puede tener acceso a los [**comandos**](/windows/desktop/lwef/the-commands-collection-object)COMM individuales and en la colección solo cuando la aplicación cliente es de entrada-activa. Por lo tanto, cuando pueda compartir el carácter con otras aplicaciones cliente, normalmente querrá establecer las propiedades [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)y [**Voice**](voice-property.md) para el objeto de colección **Commands** , así como para los comandos de la colección. Esto coloca una entrada para la colección de **comandos** en el menú emergente de un carácter y en la ventana comandos de voz.

Cuando el usuario cambia a su cliente mediante la selección de la entrada [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , el servidor hace que la entrada del cliente se active automáticamente, se notifica a la aplicación cliente mediante el evento [**ActivateInput**](activateinput-event.md) y pone a disposición los comandos de su colección. El servidor también notifica al cliente que ya no es de entrada-activa con el evento [**DeActivateInput**](deactivateinput-event.md) . Esto permite que el servidor presente y acepte solo los comandos que se aplican al contexto actual de entrada-activo del cliente. También sirve para evitar conflictos de nombres de comando entre clientes.

Un cliente también puede solicitar explícitamente que se convierta en el cliente de entrada y activo mediante el método [**Activate**](activate-method.md) . Este método también admite la configuración de la aplicación para que no sea el cliente de entrada-activo. Es posible que desee usar este método cuando comparta un carácter con otra aplicación, estableciendo que la aplicación sea de entrada-activa cuando la ventana de la aplicación recibe el foco y no es una entrada activa cuando pierde el foco.

Del mismo modo, puede utilizar el método [**Activate**](activate-method.md) para establecer que la aplicación sea (o no) el cliente activo del carácter. El cliente activo es el cliente que recibe la entrada cuando su carácter es el carácter más alto. Cuando este estado cambia, el servidor notifica a la aplicación con el evento [**ActiveClientChange**](activeclientchange-event.md) .

Cuando se muestra el menú emergente de un carácter, los cambios en las propiedades de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) o los comandos de su colección no aparecen hasta que el usuario vuelve a mostrar el menú. Sin embargo, la ventana comandos muestra los cambios a medida que se producen.

-   [Commands (métodos del objeto)](commands-object-methods.md)
-   [Propiedades del objeto Commands](commands-object-properties.md)

 

 