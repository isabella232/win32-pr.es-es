---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fc57b7e2e5f628708f46ace98700605f1eb5d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533148"
---
# <a name="iagentcommands"></a>IAgentCommands

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El servidor de agente de Microsoft mantiene una lista de comandos que están disponibles actualmente para el usuario. Esta lista incluye los comandos que define el servidor para la interacción general, como las propiedades de ocultar y del agente de Microsoft, la lista de clientes disponibles (pero no de entrada-activo) y los comandos definidos por el cliente activo actual. Los dos primeros conjuntos de comandos son comandos globales; es decir, están disponibles en cualquier momento, independientemente del cliente de entrada-activo. Los comandos definidos por el cliente solo están disponibles cuando el cliente es de entrada.

Recupere una interfaz **IAgentCommands** consultando la interfaz [**IAgentCharacter**](https://www.bing.com/search?q=**IAgentCharacter**) para **IAgentCommands**. Cada aplicación cliente de agente de Microsoft puede definir una colección de comandos denominada colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Para agregar un [**comando**](/windows/desktop/lwef/the-command-object) a la colección, use el método [**Add**](add-method.md) o [**Insert**](insert-method.md) . Aunque puede especificar las propiedades **de un comando** mediante [**métodos IAgentCommand**](iagentcommand.md) , para un rendimiento óptimo del código, especifique todas las propiedades de un **comando** en los métodos [**IAgentCommands:: Add**](iagentcommands--add.md) o [**IAgentCommands:: Insert**](iagentcommands--insert.md) cuando establezca inicialmente las propiedades para un nuevo **comando**. Puede usar los métodos **IAgentCommand** para consultar o cambiar la configuración de propiedades.

Para cada [**comando**](/windows/desktop/lwef/the-command-object) de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , puede determinar si el comando aparece en el menú emergente del carácter, en la ventana comandos de voz, en ambos o en ninguno. Por ejemplo, si desea que aparezca un comando en el menú emergente del carácter, establezca la [**leyenda**](caption-property.md) del comando y las propiedades [**visibles**](visible-property.md) . Para mostrar el comando en la **ventana comandos de voz**, establezca las propiedades **Caption** y [**Voice**](voice-property.md) del comando.

Un usuario puede tener acceso a los comandos individuales de la colección de comandos solo cuando la aplicación cliente es de entrada activa y el carácter está visible. Por lo tanto, normalmente querrá establecer las propiedades [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)y [**Voice**](voice-property.md) para el objeto de colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , así como para los comandos de la colección, ya que coloca una entrada para la colección **Commands** en el menú emergente de un carácter y en la ventana comandos de voz. Cuando el usuario cambia a su cliente mediante la selección de su entrada de **comandos** , el servidor convierte automáticamente la entrada de cliente en activa, notifica a la aplicación cliente mediante [**IAgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) y pone a disposición los **comandos** de su colección. El servidor también notifica al cliente que ya no es de entrada-activa con el evento **IAgentNotifySink:: ActivateInputState** . Esto permite que el servidor presente y acepte solo los **comandos** que se aplican al contexto actual de entrada-activo del cliente. También sirve para evitar conflictos de nombres de [**comando**](/windows/desktop/lwef/the-command-object)entre clientes.

Un cliente también puede solicitar explícitamente que se convierta en el cliente de entrada y activo mediante el método [**IAgentCharacter:: Activate**](iagentcharacter--activate.md) . Este método también admite la configuración de la aplicación para que no sea el cliente de entrada-activo. Puede usar este método al compartir un carácter con otra aplicación, configurando la aplicación para que sea de entrada-activa cuando la ventana de la aplicación recibe el foco y no es una entrada activa cuando pierde el foco.

Del mismo modo, puede usar [**IAgentCharacter:: Activate**](iagentcharacter--activate.md) para establecer que la aplicación sea (o no) el cliente activo del carácter. El cliente activo es el cliente que recibe la entrada cuando su carácter es el carácter más alto. Cuando este estado cambia, el servidor notifica a la aplicación con el evento [**IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md) .

Cuando se muestra el menú emergente de un carácter, los cambios en las propiedades de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) o los comandos de su colección no aparecen hasta que el usuario vuelve a mostrar el menú. Sin embargo, cuando se abre, la ventana comandos de voz muestra los cambios a medida que se producen.

**IAgentCommands** define una interfaz que permite a las aplicaciones agregar, quitar, establecer y consultar las propiedades de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Estas funciones también están disponibles en [**IAgentCommandsEx**](iagentcommandsex.md).

Una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) puede aparecer como un comando en el menú emergente y en la ventana comandos de voz para un carácter. Para que aparezca la colección de **comandos** , debe establecer su propiedad [**Caption**](caption-property.md) . En la tabla siguiente se resume el modo en que las propiedades de una colección **Commands** afectan a su presentación.



| Propiedad Caption | Propiedad Voice-Caption | Propiedad Voice | Propiedad visible | Aparece en el menú emergente del carácter             | Aparece en la ventana comandos de voz                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Sí              | Sí                    | Sí            | True             | Sí, usar [ **título**](caption-property.md) | Sí, uso de [ **VoiceCaption**](voicecaption-property.md) |
| Sí              | Sí                    | No ¹            | True             | Sí, usar [ **título**](caption-property.md) | No                                                       |
| Sí              | Sí                    | Sí            | False            | No                                             | Sí, uso de [ **VoiceCaption**](voicecaption-property.md) |
| Sí              | Sí                    | No ¹            | False            | No                                             | No                                                       |
| No ¹              | Sí                    | Sí            | True             | No                                             | Sí, uso de [ **VoiceCaption**](voicecaption-property.md) |
| No ¹              | Sí                    | Sí            | False            | No                                             | Sí, uso de [ **VoiceCaption**](voicecaption-property.md) |
| No ¹              | Sí                    | No ¹            | True             | No                                             | No                                                       |
| No ¹              | Sí                    | No ¹            | False            | No                                             | No                                                       |
| Sí              | No ¹                    | Sí            | True             | Sí, usar [ **título**](caption-property.md) | Sí, usar [ **título**](caption-property.md)           |
| Sí              | No ¹                    | No ¹            | True             | Sí                                            | No                                                       |
| Sí              | No ¹                    | Sí            | False            | No                                             | Sí, usar [ **título**](caption-property.md)           |
| Sí              | No ¹                    | No ¹            | False            | No                                             | No                                                       |
| No ¹              | No ¹                    | Sí            | True             | No                                             | No²                                                      |
| No ¹              | No ¹                    | Sí            | False            | No                                             | No²                                                      |
| No ¹              | No ¹                    | No ¹            | True             | No                                             | No                                                       |
| No ¹              | No ¹                    | No ¹            | False            | No                                             | No                                                       |



 

¹ si el valor de la propiedad es NULL. En algunos lenguajes de programación, una cadena vacía no puede interpretarse igual que una cadena nula.

² el comando sigue siendo accesible mediante voz.

**Métodos en orden de Vtable**



| Métodos IAgentCommands                           | Descripción                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Recupera un objeto [**Command**](/windows/desktop/lwef/the-command-object) de la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .              |
| [**GetCount**](iagentcommands--getcount.md)     | Devuelve el valor del número de [**comandos**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . |
| [**SetCaption**](iagentcommands--setcaption.md) | Establece el valor de la propiedad [**Caption**](caption-property.md) de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**GetCaption**](iagentcommands--getcaption.md) | Devuelve el valor de la propiedad [**Caption**](caption-property.md) de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**SetVoice**](iagentcommands--setvoice.md)     | Establece el valor de la propiedad [**Voice**](voice-property.md) para una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .        |
| [**GetVoice**](iagentcommands--getvoice.md)     | Devuelve el valor de la propiedad [**Voice**](voice-property.md) de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .      |
| [**SetVisible**](iagentcommands--setvisible.md) | Establece el valor de la propiedad [**visible**](visible-property.md) para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**GetVisible**](iagentcommands--getvisible.md) | Devuelve el valor de la propiedad [**visible**](visible-property.md) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**Agréguela**](iagentcommands--add.md)               | Agrega un objeto [**Command**](/windows/desktop/lwef/the-command-object) a una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .                       |
| [**Introducir**](iagentcommands--insert.md)         | Inserta un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**Retirar**](iagentcommands--remove.md)         | Quita un objeto [**Command**](/windows/desktop/lwef/the-command-object) de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**RemoveAll**](iagentcommands--removeall.md)   | Quita todos los objetos de [**comando**](/windows/desktop/lwef/the-command-object) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .               |



 

 

 