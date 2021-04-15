---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c4ba90f7d355a0baa088a78aa05b7a91e14112
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695592"
---
# <a name="iagentcommand"></a>IAgentCommand

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Un objeto [**Command**](/windows/desktop/lwef/the-command-object) es un elemento de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . El servidor proporciona al usuario acceso a los comandos que la aplicación cliente entra en activo. Para recuperar un **comando**, llame a [**IAgentCommands:: GetCommand**](iagentcommands--getcommand.md).

**IAgentCommand** define una interfaz que permite a las aplicaciones establecer y consultar las propiedades de los objetos de [**comando**](/windows/desktop/lwef/the-command-object) que pueden aparecer en el menú emergente de un carácter y en la ventana comandos de voz. Estas funciones también están disponibles en [**IAgentCommandEx**](iagentcommandex.md). Un objeto **Command** es un elemento de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . El servidor proporciona al usuario acceso a los comandos cuando la aplicación cliente se convierte en una entrada activa.

Puede aparecer un [**comando**](/windows/desktop/lwef/the-command-object) en el menú emergente del carácter y en la ventana comandos de voz. Para que aparezca en el menú emergente, debe tener un [**título**](caption-property.md) y tener la propiedad [**visible**](visible-property.md) establecida en **true**. La propiedad **visible** para su objeto de colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) también debe establecerse en **true** para que el comando aparezca en el menú emergente cuando la aplicación cliente sea de entrada-activa. Para que aparezca en la ventana comandos de voz, un **comando** debe tener su conjunto de propiedades [**VoiceCaption**](voicecaption-property.md) y [**Voice**](voice-property.md) . (Para mantener la compatibilidad con versiones anteriores, si no hay ningún **VoiceCaption**, se usa la configuración del **título** ).

Las entradas del menú emergente de un carácter no cambian mientras se muestra el menú. Si agrega o quita comandos o cambia sus propiedades mientras se muestra el menú emergente del carácter, el menú muestra esos cambios cuando se vuelve a mostrar. Sin embargo, la ventana comandos de voz muestra los cambios a medida que se realizan.

En la tabla siguiente se resume el modo en que las propiedades de un comando afectan a su presentación.



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

Por lo general, si define un [**comando**](/windows/desktop/lwef/the-command-object) con un valor de [**voz**](voice-property.md) , también debe definir la configuración de [**leyenda**](caption-property.md) y **voz** para la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) asociada. Si la colección de **comandos** de un conjunto de comandos no tiene ningún valor de **voz** o de **leyenda** y actualmente es de entrada, pero los **comandos** tienen la configuración de **leyenda** y **voz** , los **comandos** aparecen en la vista de árbol de la ventana comandos de voz en "(comando no definido)" cuando la aplicación cliente pasa a ser de entrada activa.

Cuando el servidor recibe una entrada que coincide con uno de los objetos de [**comando**](/windows/desktop/lwef/the-command-object) definidos para la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , envía un evento [**IAgentNotifySink:: Command**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) y devuelve el identificador del comando como un atributo del objeto [**IAgentUserInput**](https://www.bing.com/search?q=**IAgentUserInput**) . Después, puede usar las instrucciones condicionales para buscar coincidencias y procesar el comando.

**Métodos en orden de Vtable**



| Métodos IAgentCommand                                                   | Descripción                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**SetCaption**](https://www.bing.com/search?q=**SetCaption**)                             | Establece el valor para el [**título**](caption-property.md) de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                         |
| [**GetCaption**](https://www.bing.com/search?q=**GetCaption**)                             | Devuelve el valor de la propiedad [**Caption**](caption-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetVoice**](iagentcommand--setvoice.md)                             | Establece el valor para el texto de la [**voz**](voice-property.md) de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                        |
| [**GetVoice**](iagentcommand--getvoice.md)                             | Devuelve el valor de la propiedad [**Voice**](voice-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) .                   |
| [**SetEnabled**](iagentcommand--setenabled.md)                         | Establece el valor de la propiedad [**Enabled**](enabled-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetEnabled**](iagentcommand--getenabled.md)                         | Devuelve el valor de la propiedad [**Enabled**](enabled-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetVisible**](iagentcommand--setvisible.md)                         | Establece el valor de la propiedad [**visible**](visible-property.md) para un objeto [**Command**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetVisible**](iagentcommand--getvisible.md)                         | Devuelve el valor de la propiedad [**visible**](visible-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md) | Establece el valor de la propiedad [**Confidence**](confidence-property.md) para un objeto [**Command**](/windows/desktop/lwef/the-command-object) .           |
| [**GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md) | Devuelve el valor de la propiedad [**Confidence**](confidence-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) .         |
| [**SetConfidenceText**](iagentcommand--setconfidencetext.md)           | Establece el valor de la propiedad [**ConfidenceText**](confidencetext-property.md) para un objeto [**Command**](/windows/desktop/lwef/the-command-object) .   |
| [**getConfidenceText**](iagentcommand--getconfidencetext.md)           | Devuelve el valor de la propiedad [**ConfidenceText**](confidencetext-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) . |
| [**getID**](iagentcommand--getid.md)                                   | Devuelve el identificador de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                                                                      |



 

 

 