---
title: Ventana comandos de voz
description: Ventana comandos de voz
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4ad0a1521e8dacc941ba5b2ce5f6c264c65a31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704951"
---
# <a name="voice-commands-window"></a>Ventana comandos de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

La ventana comandos de voz muestra los comandos de voz activos actuales disponibles para el carácter. La ventana aparece cuando se elige el comando Abrir ventana comandos o la propiedad [**visible**](visible-property.md) del objeto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) se establece en **true**. Si el motor de voz aún no se ha cargado, la consulta o el establecimiento de esta propiedad hará que el agente de Microsoft intente inicializar el motor. Si el usuario deshabilita la voz, la ventana puede seguir apareciendo; sin embargo, incluirá un mensaje de texto que informa al usuario de que la voz está deshabilitada actualmente.

Los comandos de entrada-activo del cliente aparecen en la ventana comandos de voz en [**función de los valores**](voice-property.md)de propiedad [**leyenda**](caption-property.md) y **voz** de voz que aparecen en el [**VoiceCaption**](voicecaption-property.md) de su colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

**Figura 1. Ventana comandos de voz**

La ventana comandos de voz aparece cuando se elige el comando Abrir ventana comandos. Los comandos de entrada-activo del cliente aparecen en la ventana comandos de voz en [**función de los valores**](voice-property.md)de propiedad [**leyenda**](caption-property.md) y **voz** de voz que aparecen en **voz** de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

La ventana comandos de voz también muestra el [**VoiceCaption**](voicecaption-property.md) de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) para otros clientes del carácter y los siguientes comandos de voz generados por el servidor para la interacción general en la entrada comandos globales:



| Leyenda de voz                       | Gramática de voz                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abrir la \| ventana comandos de voz de cierre | (abrir \| Mostrar) \[ la \] \[ ventana comandos \] \| ¿Qué puedo decir \[ ahora?\] <br/> alterna con: <br/> cerrar \[ la \] \[ ventana comandos\] <br/> |
| Ocultar                                | u \*                                                                                                                                                  |
| *Nombredecarácter*                     | *Nombredecarácter*\*\*                                                                                                                                      |
| Comandos globales                     | \[mostrarme \] \[ \] comandos globales                                                                                                                          |



 

\* Aquí solo se muestra un carácter si está visible actualmente.

\*\* Se enumeran todos los caracteres cargados.

Al hablar del comando de voz de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de otro cliente, se cambia a ese cliente y la ventana comandos de voz muestra los comandos de ese cliente. No se expanden otras entradas. Del mismo modo, si el usuario cambia los caracteres, la ventana comandos de voz cambia para mostrar los comandos de su cliente de entrada-activo. Si el cliente ya es de entrada-activo, hablar de uno de sus comandos de voz no tiene ningún efecto. (Sin embargo, si el usuario contrae el subárbol del cliente activo con el mouse, al hablar del nombre del cliente se vuelve a mostrar el subárbol del cliente).

Si un cliente tiene comandos de voz, pero no tiene ningún valor de [**voz**](voice-property.md) para el objeto de [**comando**](/windows/desktop/lwef/the-commands-collection-object) (o no tiene [**título**](caption-property.md)de **voz**), el árbol muestra "(comando sin definir)" como entrada primaria, pero solo cuando ese cliente es de entrada-activo y el cliente tiene comandos en su colección que tienen una configuración de **leyenda** y de **voz** .

El servidor muestra automáticamente los comandos del cliente actual de entrada-activo y, si es necesario, desplaza la ventana para mostrar tantos comandos del cliente como sea posible, en función del tamaño de la ventana. Si el carácter no tiene entradas de cliente, se expandirá la entrada comandos globales.

Si el usuario habla de "comandos globales", la ventana comandos de voz muestra siempre las entradas de subárbol asociadas. Si ya se muestran, el comando no tiene ningún efecto.

Aunque también puede mostrar u ocultar la ventana comandos de voz del código de la aplicación mediante la propiedad [**visible**](visible-property.md) , no puede cambiar el tamaño o la ubicación de la ventana comandos de voz. El servidor mantiene las propiedades de la ventana comandos de voz en función de la interacción del usuario con la ventana. Su ubicación inicial es inmediatamente adyacente al icono de la barra de tareas del carácter.

La ventana comandos de voz se incluye en el orden de las ventanas ALT + TAB. Esto permite a un usuario cambiar a la ventana para desplazarse, cambiar el tamaño o cambiar la posición de la ventana con el teclado.

-   [La sugerencia de escucha](the-listening-tip.md)
-   [La ventana Opciones de carácter avanzadas](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

