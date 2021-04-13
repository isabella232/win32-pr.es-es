---
title: Compatibilidad con menús emergentes
description: Compatibilidad con menús emergentes
ms.assetid: a8a1cf91-c18a-497f-89a7-b47536eaca0a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890d7eab6595200cb00e8422644b10f39807bab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358941"
---
# <a name="pop-up-menu-support"></a>Compatibilidad con menús emergentes

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El agente de Microsoft incluye un menú emergente (también conocido como menú contextual) para cada carácter. El servidor muestra este menú emergente automáticamente cuando un usuario hace clic con el botón secundario en el carácter. Puede Agregar comandos para la aplicación cliente al menú mediante la definición de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Para cada comando de la colección que defina, puede especificar el [**título**](caption-property.md) y las propiedades [**visibles**](visible-property.md) . El **título** es el texto que aparece en el menú cuando la propiedad **visible** está establecida en **true**. También puede usar la propiedad [**Enabled**](enabled-property.md) para mostrar el comando en el menú como Disabled y el [**HelpContextID**](helpcontextid-property.md) para admitir la compatibilidad con la propiedad. Defina la tecla de acceso para el texto del menú incluyendo una y comercial (&) antes del carácter de texto de la configuración del texto del **título** .

El servidor agrega automáticamente los comandos de menú para abrir la ventana comandos de voz y oculta el carácter, así como los títulos de los [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de otros clientes del carácter, a fin de permitir que los usuarios cambien de un cliente a otro. El servidor agrega automáticamente un separador al menú entre sus entradas de menú y las definidas por el cliente. Los separadores solo aparecen cuando hay elementos en el menú para separar.

Para quitar comandos de un menú, use el método [**Remove**](remove-method.md) . Tenga en cuenta que las entradas de menú no cambian mientras se muestra el menú. Si agrega o quita comandos o cambia sus propiedades, el menú muestra los cambios cuando el usuario vuelve a mostrar el menú.

Si prefiere proporcionar sus propios servicios de menú emergente para un carácter, puede usar la propiedad [**AutoPopupMenu**](autopopupmenu-property.md) para desactivar el control de servidor de la acción de clic con el botón secundario. Después, puede usar la notificación de eventos [**click**](click-event.md) para crear su propio comportamiento de control de menús.

Cuando el usuario selecciona un comando en el menú emergente de un carácter o en la ventana comandos de voz, el servidor desencadena el evento de [**comando**](command-event.md) del cliente asociado y devuelve los parámetros de la entrada mediante el objeto [**UserInput**](/windows/desktop/lwef/iagentuserinput) .

El servidor también proporciona un menú emergente para el icono de la barra de tareas del carácter. Cuando el carácter esté visible, haga clic con el botón secundario en este menú para mostrar los mismos comandos que los que se muestran al hacer clic con el botón secundario en el carácter. Sin embargo, cuando el carácter está oculto, solo se incluyen los comandos proporcionados por el servidor.

 

 