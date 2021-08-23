---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e2288a7b913becc54e2c0baa43eb14903e65fb7eddf6620d5cefbd78968026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665485"
---
# <a name="iagentcommand"></a>IAgentCommand

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Un [**objeto Command**](/windows/desktop/lwef/the-command-object) es un elemento de una colección [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) El servidor proporciona al usuario acceso a los comandos que la aplicación cliente pasa a estar activa en la entrada. Para recuperar un **comando**, llame a [**IAgentCommands::GetCommand**](iagentcommands--getcommand.md).

**IAgentCommand define** una interfaz que permite a las aplicaciones establecer y consultar propiedades para objetos [**Command**](/windows/desktop/lwef/the-command-object) que pueden aparecer en el menú emergente de un carácter y en la ventana Comandos de voz. Estas funciones también están disponibles en [**IAgentCommandEx**](iagentcommandex.md). Un **objeto Command** es un elemento de una colección [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) El servidor proporciona al usuario acceso a los comandos cuando la aplicación cliente pasa a estar activa en la entrada.

Un [**comando**](/windows/desktop/lwef/the-command-object) puede aparecer en el menú emergente del carácter y en la ventana Comandos de voz o en ambos. Para que aparezca en el menú emergente, debe tener un título y tener la [**propiedad Visible**](visible-property.md) establecida en **True.** [](caption-property.md) La **propiedad Visible** para su objeto de colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) también debe establecerse en **True** para que el comando aparezca en el menú emergente cuando la aplicación cliente esté activa en la entrada. Para que aparezca en la ventana Comandos de voz, un **comando** debe tener establecidas sus propiedades [**VoiceCaption**](voicecaption-property.md) y [**Voice.**](voice-property.md) (Por compatibilidad con versiones anteriores, si no hay **VoiceCaption**, se usa la **configuración de** título).

Las entradas del menú emergente de un carácter no cambian mientras se muestra el menú. Si agrega o quita Comandos o cambia sus propiedades mientras se muestra el menú emergente del carácter, el menú muestra esos cambios cuando se vuelve a mostrar. Sin embargo, la ventana Comandos de voz muestra los cambios a medida que se hacen.

En la tabla siguiente se resume cómo afectan las propiedades de un comando a su presentación.



| Propiedad Caption | Voice-Caption propiedad | Propiedad Voice | Propiedad Visible | Aparece en el menú emergente del carácter             | Aparece en la ventana Comandos de voz                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Sí              | Sí                    | Sí            | Verdadero             | Sí, con [ **Título**](caption-property.md) | Sí, con [ **VoiceCaption**](voicecaption-property.md) |
| Sí              | Sí                    | No¹            | Verdadero             | Sí, con [ **Título**](caption-property.md) | No                                                       |
| Sí              | Sí                    | Sí            | False            | No                                             | Sí, con [ **VoiceCaption**](voicecaption-property.md) |
| Sí              | Sí                    | No¹            | False            | No                                             | No                                                       |
| No¹              | Sí                    | Sí            | True             | No                                             | Sí, con [ **VoiceCaption**](voicecaption-property.md) |
| No¹              | Sí                    | Sí            | False            | No                                             | Sí, con [ **VoiceCaption**](voicecaption-property.md) |
| No¹              | Sí                    | No¹            | True             | No                                             | No                                                       |
| No¹              | Sí                    | No¹            | False            | No                                             | No                                                       |
| Sí              | No¹                    | Sí            | Verdadero             | Sí, con [ **Título**](caption-property.md) | Sí, con [ **Título**](caption-property.md)           |
| Sí              | No¹                    | No¹            | True             | Sí                                            | No                                                       |
| Sí              | No¹                    | Sí            | False            | No                                             | Sí, con [ **Título**](caption-property.md)           |
| Sí              | No¹                    | No¹            | False            | No                                             | No                                                       |
| No¹              | No¹                    | Sí            | True             | No                                             | No²                                                      |
| No¹              | No¹                    | Sí            | False            | No                                             | No²                                                      |
| No¹              | No¹                    | No¹            | True             | No                                             | No                                                       |
| No¹              | No¹                    | No¹            | False            | No                                             | No                                                       |



 

¹Si el valor de la propiedad es NULL. En algunos lenguajes de programación, es posible que una cadena vacía no se interprete como la misma que una cadena null.

²El comando sigue siendo accesible por voz.

Por lo general, si define [](voice-property.md) un comando con [](caption-property.md) [](/windows/desktop/lwef/the-command-object) una  configuración de voz, también definirá la configuración de título y voz para su colección de comandos [**asociada.**](/windows/desktop/lwef/the-commands-collection-object) Si  la colección Comandos de un conjunto de  comandos **no** tiene ninguna configuración de  voz o  título y actualmente está activa en la entrada, pero los comandos tienen la configuración de título y voz, los comandos aparecen en la vista de árbol de la ventana Comandos de voz en "(comando indefinido)" cuando la aplicación cliente se convierte en entrada-activa.  

Cuando el servidor recibe una entrada que coincide con uno de los objetos [**Command**](/windows/desktop/lwef/the-command-object) definidos para la colección [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) envía un evento [**IAgentNotifySink::Command**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) y devuelve el identificador del comando como atributo del objeto [**IAgentUserInput.**](https://www.bing.com/search?q=**IAgentUserInput**) A continuación, puede usar instrucciones condicionales para hacer coincidir y procesar el comando.

**Métodos en orden de Vtable**



| Métodos IAgentCommand                                                   | Descripción                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**SetCaption**](https://www.bing.com/search?q=**SetCaption**)                             | Establece el valor del título [**de**](caption-property.md) un [**objeto**](/windows/desktop/lwef/the-command-object) Command.                         |
| [**GetCaption**](https://www.bing.com/search?q=**GetCaption**)                             | Devuelve el valor de la [**propiedad Caption**](caption-property.md) de un [**objeto Command.**](/windows/desktop/lwef/the-command-object)               |
| [**SetVoice**](iagentcommand--setvoice.md)                             | Establece el valor del texto [**de voz**](voice-property.md) para un [**objeto**](/windows/desktop/lwef/the-command-object) Command.                        |
| [**GetVoice**](iagentcommand--getvoice.md)                             | Devuelve el valor de la [**propiedad Voice**](voice-property.md) de un [**objeto Command.**](/windows/desktop/lwef/the-command-object)                   |
| [**SetEnabled**](iagentcommand--setenabled.md)                         | Establece el valor de la [**propiedad Enabled**](enabled-property.md) para un [**objeto Command.**](/windows/desktop/lwef/the-command-object)                 |
| [**GetEnabled**](iagentcommand--getenabled.md)                         | Devuelve el valor de la [**propiedad Enabled**](enabled-property.md) de un [**objeto Command.**](/windows/desktop/lwef/the-command-object)               |
| [**SetVisible**](iagentcommand--setvisible.md)                         | Establece el valor de la [**propiedad Visible**](visible-property.md) para un [**objeto Command.**](/windows/desktop/lwef/the-command-object)                 |
| [**GetVisible**](iagentcommand--getvisible.md)                         | Devuelve el valor de la [**propiedad Visible**](visible-property.md) de un [**objeto**](/windows/desktop/lwef/the-command-object) Command.               |
| [**SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md) | Establece el valor de la [**propiedad Confidence**](confidence-property.md) para un [**objeto Command.**](/windows/desktop/lwef/the-command-object)           |
| [**GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md) | Devuelve el valor de la [**propiedad Confidence**](confidence-property.md) de un [**objeto Command.**](/windows/desktop/lwef/the-command-object)         |
| [**SetConfidenceText**](iagentcommand--setconfidencetext.md)           | Establece el valor de la [**propiedad ConfidenceText**](confidencetext-property.md) para un [**objeto Command.**](/windows/desktop/lwef/the-command-object)   |
| [**getConfidenceText**](iagentcommand--getconfidencetext.md)           | Devuelve el valor de la [**propiedad ConfidenceText**](confidencetext-property.md) de un [**objeto Command.**](/windows/desktop/lwef/the-command-object) |
| [**getID**](iagentcommand--getid.md)                                   | Devuelve el identificador de un [**objeto**](/windows/desktop/lwef/the-command-object) Command.                                                                      |



 

 

 