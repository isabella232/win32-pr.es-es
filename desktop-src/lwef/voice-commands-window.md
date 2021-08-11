---
title: Ventana Comandos de voz
description: Ventana Comandos de voz
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f4e5ce02ea9a964663efacbc19a3b302d6e58f0364d705491be26229b15f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245108"
---
# <a name="voice-commands-window"></a>Ventana Comandos de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

La ventana Comandos de voz muestra los comandos de voz activos actuales disponibles para el carácter. La ventana aparece cuando se elige el comando Abrir ventana comandos o la propiedad [**Visible**](visible-property.md) del objeto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) se establece en **True.** Si el motor de voz aún no se ha cargado, al consultar o establecer esta propiedad, Microsoft Agent intentará inicializar el motor. Si el usuario deshabilita la voz, la ventana todavía se puede mostrar; sin embargo, incluirá un mensaje de texto que informa al usuario de que la voz está deshabilitada actualmente.

Los comandos del cliente activo de entrada aparecen en la [](voice-property.md)ventana Comandos de voz en función de la configuración de las propiedades Voice [**Caption**](caption-property.md) y **Voice** enumeradas en [**VoiceCaption**](voicecaption-property.md) de su [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

**Figura 1. Ventana Comandos de voz**

La ventana Comandos de voz aparece cuando se elige el comando Abrir ventana comandos. Los comandos del cliente activo de entrada aparecen en la [](voice-property.md)[](caption-property.md) ventana  Comandos de voz en función de la configuración de las propiedades Título de voz y Voz que aparecen en **Voz** de la [**colección**](/windows/desktop/lwef/the-commands-collection-object) Comandos.

En la ventana Comandos de voz también se muestra [**voiceCaption**](voicecaption-property.md) de la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) para otros clientes del carácter y los siguientes comandos de voz generados por el servidor para la interacción general en la entrada Comandos globales:



| Título de voz                       | Gramática de voz                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abrir \| la ventana Cerrar comandos de voz | (abrir \| la ventana de \[ \] comandos) \[ \] \| ¿Qué puedo \[ decir ahora?\] <br/> alterna con: <br/> Cerrar \[ la ventana de \] \[ comandos\] <br/> |
| Ocultar                                | Ocultar \*                                                                                                                                                  |
| *CharacterName*                     | *CharacterName*\*\*                                                                                                                                      |
| Comandos globales                     | \[mostrarme \] \[ \] comandos globales                                                                                                                          |



 

\* Un carácter se muestra aquí solo si está visible actualmente.

\*\* Se muestran todos los caracteres cargados.

Al hablar el comando de voz de la colección [**Comandos**](/windows/desktop/lwef/the-commands-collection-object) de otro cliente, se cambia a ese cliente y la ventana Comandos de voz muestra los comandos de ese cliente. No se expande ninguna otra entrada. De forma similar, si el usuario cambia los caracteres, la ventana Comandos de voz cambia para mostrar los comandos de su cliente activo de entrada. Si el cliente ya está activo de entrada, hablar uno de sus comandos de voz no tiene ningún efecto. (Sin embargo, si el usuario contrae el subárbol del cliente activo con el mouse, al hablar el nombre del cliente se vuelve a mostrar el subárbol del cliente).

Si un cliente tiene comandos de voz, pero no hay ninguna configuración de voz para su objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) (o ningún título de [**voz),**](caption-property.md)el árbol muestra "(command undefined)" como la entrada primaria, pero solo cuando ese cliente está activo para la entrada y el cliente tiene comandos en su colección que tienen configuración de título y **voz.** [](voice-property.md) 

El servidor muestra automáticamente los comandos del cliente activo de entrada actual y, si es necesario, desplaza la ventana para mostrar tantos comandos del cliente como sea posible, en función del tamaño de la ventana. Si el carácter no tiene entradas de cliente, se expande la entrada Comandos globales.

Si el usuario habla "Comandos globales", la ventana Comandos de voz siempre muestra sus entradas de subárbol asociadas. Si ya se muestran, el comando no tiene ningún efecto.

Aunque también puede mostrar u ocultar la ventana Comandos de voz del código de la aplicación mediante la [**propiedad Visible,**](visible-property.md) no puede cambiar el tamaño o la ubicación de la ventana Comandos de voz. El servidor mantiene las propiedades de la ventana Comandos de voz en función de la interacción del usuario con la ventana. Su ubicación inicial es inmediatamente adyacente al icono de la barra de tareas del carácter.

La ventana Comandos de voz se incluye en el orden de la ventana ALT+TAB. Esto permite al usuario cambiar a la ventana para desplazarse, cambiar el tamaño o cambiar la posición de la ventana con el teclado.

-   [Sugerencia de escucha](the-listening-tip.md)
-   [Ventana Opciones avanzadas de caracteres](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

