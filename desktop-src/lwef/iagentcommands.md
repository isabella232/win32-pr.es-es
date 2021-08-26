---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1bcc40f80e9a10301ec305fdc3e8f3e83984ceb0de5d36121e13c3d823b8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961895"
---
# <a name="iagentcommands"></a>IAgentCommands

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El servidor de Microsoft Agent mantiene una lista de comandos que están disponibles actualmente para el usuario. Esta lista incluye comandos que el servidor define para la interacción general, como Ocultar y Propiedades del agente de Microsoft, la lista de clientes disponibles (pero no activos de entrada) y los comandos definidos por el cliente activo actual. Los dos primeros conjuntos de comandos son comandos globales; es decir, están disponibles en cualquier momento, independientemente del cliente activo de entrada. Los comandos definidos por el cliente solo están disponibles cuando ese cliente está activo en la entrada.

Recupere una **interfaz IAgentCommands** consultando la [**interfaz IAgentCharacter**](https://www.bing.com/search?q=**IAgentCharacter**) para **IAgentCommands**. Cada aplicación cliente de Microsoft Agent puede definir una colección de comandos denominada colección [**de**](/windows/desktop/lwef/the-commands-collection-object) comandos. Para agregar un [**comando**](/windows/desktop/lwef/the-command-object) a la colección, use el [**método Add**](add-method.md) [**o Insert.**](insert-method.md) Aunque puede especificar  las propiedades de un comando mediante métodos [**IAgentCommand,**](iagentcommand.md) para un rendimiento óptimo del código, especifique todas las propiedades de un comando en los [**métodos IAgentCommands::Add**](iagentcommands--add.md) o [**IAgentCommands::Insert**](iagentcommands--insert.md) al establecer inicialmente las propiedades de un **nuevo comando**.  Puede usar los métodos **IAgentCommand** para consultar o cambiar la configuración de la propiedad.

Para cada [**comando**](/windows/desktop/lwef/the-command-object) de la colección Comandos, puede determinar si el comando aparece en el menú emergente del carácter, en la ventana Comandos de voz, en ambos o en ninguno de ellos. [](/windows/desktop/lwef/the-commands-collection-object) Por ejemplo, si desea que un comando aparezca en el menú emergente del carácter, establezca las propiedades [**Título**](caption-property.md) y [**Visible del**](visible-property.md) comando. Para mostrar el comando en la **ventana Comandos de** voz , establezca las propiedades **Título** y Voz [**del**](voice-property.md) comando.

Un usuario puede acceder a los comandos individuales de la colección comandos solo cuando la aplicación cliente está activa en la entrada y el carácter está visible. Por lo tanto, normalmente querrá establecer las propiedades [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)y [**Voice**](voice-property.md) para el objeto de colección [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) así como para los comandos de la colección, ya que esto coloca una entrada para la colección **Commands** en el menú emergente de un carácter y en la ventana Comandos de voz. Cuando el usuario cambia al cliente eligiendo su entrada **Comandos,** el servidor activa automáticamente la entrada del cliente, notificando a la aplicación  cliente mediante [**IAgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) y hace que los comandos de su colección estén disponibles. El servidor también notifica al cliente que ya no está activo de entrada con el evento **IAgentNotifySink::ActivateInputState.** Esto permite que el servidor presente y acepte solo los **comandos** que se aplican al contexto del cliente activo de entrada actual. También sirve para evitar conflictos [**de**](/windows/desktop/lwef/the-command-object)nombre de comando entre clientes.

Un cliente también puede solicitar explícitamente que se haga el cliente activo de entrada mediante el [**método IAgentCharacter::Activate.**](iagentcharacter--activate.md) Este método también admite la configuración de la aplicación para que no sea el cliente activo de entrada. Es posible que quiera usar este método al compartir un carácter con otra aplicación, estableciendo la aplicación en input-active cuando la ventana de la aplicación obtiene el foco y no input-active cuando pierde el foco.

De forma similar, puede usar [**IAgentCharacter::Activate**](iagentcharacter--activate.md) para establecer que la aplicación sea (o no) el cliente activo del carácter. El cliente activo es el cliente que recibe la entrada cuando su carácter es el carácter superior. Cuando este estado cambia, el servidor notifica a la aplicación con el evento [**IAgentNotifySinkEx::ActiveClientChange.**](iagentnotifysinkex--activeclientchange.md)

Cuando se muestra el menú emergente de un carácter, los cambios en las propiedades de una colección Comandos o los comandos de su colección no aparecen hasta que el usuario vuelve [**a**](/windows/desktop/lwef/the-commands-collection-object) mostrar el menú. Sin embargo, cuando se abre, la ventana Comandos de voz muestra los cambios a medida que se hacen.

**IAgentCommands** define una interfaz que permite a las aplicaciones agregar, quitar, establecer y consultar propiedades para una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) Estas funciones también están disponibles en [**IAgentCommandsEx**](iagentcommandsex.md).

Una [**colección Comandos**](/windows/desktop/lwef/the-commands-collection-object) puede aparecer como un comando en el menú emergente y en la ventana Comandos de voz de un carácter. Para que aparezca **la colección Commands,** debe establecer su [**propiedad Caption.**](caption-property.md) En la tabla siguiente se resume cómo las propiedades de una **colección Commands** afectan a su presentación.



| Propiedad Caption | Voice-Caption propiedad | Propiedad Voice | Propiedad Visible | Aparece en el menú emergente del carácter             | Aparece en la ventana Comandos de voz                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Sí              | Sí                    | Sí            | Verdadero             | Sí, mediante [ **título**](caption-property.md) | Sí, con [ **VoiceCaption**](voicecaption-property.md) |
| Sí              | Sí                    | No¹            | Verdadero             | Sí, mediante [ **título**](caption-property.md) | No                                                       |
| Sí              | Sí                    | Sí            | False            | No                                             | Sí, con [ **VoiceCaption**](voicecaption-property.md) |
| Sí              | Sí                    | No¹            | False            | No                                             | No                                                       |
| No¹              | Sí                    | Sí            | True             | No                                             | Sí, con [ **VoiceCaption**](voicecaption-property.md) |
| No¹              | Sí                    | Sí            | False            | No                                             | Sí, con [ **VoiceCaption**](voicecaption-property.md) |
| No¹              | Sí                    | No¹            | True             | No                                             | No                                                       |
| No¹              | Sí                    | No¹            | False            | No                                             | No                                                       |
| Sí              | No¹                    | Sí            | Verdadero             | Sí, mediante [ **título**](caption-property.md) | Sí, mediante [ **título**](caption-property.md)           |
| Sí              | No¹                    | No¹            | True             | Sí                                            | No                                                       |
| Sí              | No¹                    | Sí            | False            | No                                             | Sí, mediante [ **título**](caption-property.md)           |
| Sí              | No¹                    | No¹            | False            | No                                             | No                                                       |
| No¹              | No¹                    | Sí            | True             | No                                             | No²                                                      |
| No¹              | No¹                    | Sí            | False            | No                                             | No²                                                      |
| No¹              | No¹                    | No¹            | True             | No                                             | No                                                       |
| No¹              | No¹                    | No¹            | False            | No                                             | No                                                       |



 

¹Si el valor de la propiedad es NULL. En algunos lenguajes de programación, es posible que una cadena vacía no se interprete igual que una cadena null.

²El comando sigue siendo accesible por voz.

**Métodos en orden de Vtable**



| Métodos IAgentCommands                           | Descripción                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Recupera un objeto [**Command**](/windows/desktop/lwef/the-command-object) de la [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)              |
| [**GetCount**](iagentcommands--getcount.md)     | Devuelve el valor del número de [**comandos de**](/windows/desktop/lwef/the-command-object) una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) |
| [**SetCaption**](iagentcommands--setcaption.md) | Establece el valor de la [**propiedad Caption**](caption-property.md) para una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)    |
| [**GetCaption**](iagentcommands--getcaption.md) | Devuelve el valor de la [**propiedad Caption**](caption-property.md) de una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)  |
| [**SetVoice**](iagentcommands--setvoice.md)     | Establece el valor de la [**propiedad Voice**](voice-property.md) para una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)        |
| [**GetVoice**](iagentcommands--getvoice.md)     | Devuelve el valor de la [**propiedad Voice**](voice-property.md) de una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)      |
| [**SetVisible**](iagentcommands--setvisible.md) | Establece el valor de la [**propiedad Visible**](visible-property.md) para una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)    |
| [**GetVisible**](iagentcommands--getvisible.md) | Devuelve el valor de la [**propiedad Visible**](visible-property.md) de una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)  |
| [**Añadir**](iagentcommands--add.md)               | Agrega un [**objeto Command**](/windows/desktop/lwef/the-command-object) a una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)                       |
| [**insertar**](iagentcommands--insert.md)         | Inserta un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)                    |
| [**Quitar**](iagentcommands--remove.md)         | Quita un objeto [**Command**](/windows/desktop/lwef/the-command-object) de una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)                    |
| [**Removeall**](iagentcommands--removeall.md)   | Quita todos los [**objetos Command**](/windows/desktop/lwef/the-command-object) de una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)               |



 

 

 