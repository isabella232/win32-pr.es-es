---
title: El objeto Command
description: El objeto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714369"
---
# <a name="the-command-object"></a>El objeto Command

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Un objeto [**Command**](/windows/desktop/lwef/the-command-object) es un elemento de una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . El servidor proporciona al usuario acceso a los objetos de **comando** cuando la aplicación cliente pasa a ser de entrada activa.

-   [Propiedades del objeto de comando](command-object-properties.md)

Para tener acceso a la propiedad de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) , se hace referencia a él en su colección mediante su propiedad [**Name**](name-property.md) . En VBScript y Visual Basic puede usar la propiedad **nombre** directamente:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Para los lenguajes de programación que no admiten colecciones, use el método de [**comando**](command-method.md) :


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



También puede hacer referencia a un objeto de comando mediante la creación de una referencia a él. En Visual Basic, declare una variable de objeto y use la instrucción SET para crear la referencia:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



En Visual Basic 5,0, también puede declarar el objeto como de tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) y crear la referencia. Esta Convención permite el enlace anticipado, lo que da como resultado un mejor rendimiento:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



En VBScript, puede declarar una referencia como un tipo determinado, pero todavía puede declarar la variable y establecerla en el [**comando**](/windows/desktop/lwef/the-command-object) de la colección:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Puede aparecer un comando en el menú emergente del carácter y en la ventana comandos, o bien en ambos. Para que aparezca en el menú emergente, debe tener un título y tener la propiedad [**visible**](visible-property.md) establecida en **true**. Además, la propiedad **visible** del objeto de colección Commands también debe establecerse en **true**. Para que aparezca en la ventana comandos, un [**comando**](/windows/desktop/lwef/the-command-object) debe tener establecidas las propiedades [**Caption**](caption-property.md) y [**Voice**](voice-property.md) . Tenga en cuenta que las entradas del menú emergente de un carácter no cambian mientras se muestra el menú. Si agrega o quita comandos o cambia sus propiedades mientras se muestra el menú emergente del carácter, el menú muestra esos cambios cada vez que el usuario lo muestra. Sin embargo, la ventana comandos refleja dinámicamente los cambios que realice.

En la tabla siguiente se resume el modo en que las propiedades de un [**comando**](/windows/desktop/lwef/the-command-object) afectan a su presentación:



Propiedad Caption

Propiedad Voice-Caption

Propiedad Voice

Propiedad visible

Propiedad Enabled

Aparece en el menú emergente del carácter

Aparece en la ventana comandos

Sí

Sí

Sí

True

True

Normal, con [ **título**](caption-property.md)

Sí, uso de [ **VoiceCaption**](voicecaption-property.md)

Sí

Sí

Sí

True

False

Deshabilitado, con [ **título**](caption-property.md)

No

Sí

Sí

Sí

False

True

No aparece

Sí, uso de [ **VoiceCaption**](voicecaption-property.md)

Sí

Sí

Sí

False

False

No aparece

No

Sí

Sí

No 

True

True

Normal, con [ **título**](caption-property.md)

No

Sí

Sí

No 

True

False

Deshabilitado, con [ **título**](caption-property.md)

No

Sí

Sí

No 

False

True

No aparece

No

Sí

Sí

No 

False

False

No aparece

No

No 

Sí

Sí

True

True

No aparece

Sí, uso de [ **VoiceCaption**](voicecaption-property.md)

No 

Sí

Sí

True

False

No aparece

No

No 

Sí

Sí

False

True

No aparece

Sí, uso de [ **VoiceCaption**](voicecaption-property.md)

No 

Sí

Sí

False

False

No aparece

No

No 

Sí

No 

True

True

No aparece

No

No 

Sí

No 

True

False

No aparece

No

No 

Sí

No 

False

True

No aparece

No

No 

Sí

No 

False

False

No aparece

No

Sí

No 

Sí

True

True

Normal, con [ **título**](caption-property.md)

Sí, usar [ **título**](caption-property.md)

Sí

No 

Sí

True

False

Deshabilitado, con [ **título**](caption-property.md)

No

Sí

No 

Sí

False

True

No aparece

Sí, usar [ **título**](caption-property.md)

Sí

No 

Sí

False

False

No aparece

No

Sí

No 

No 

True

True

Normal, con [ **título**](caption-property.md)

No

Sí

No 

No 

True

False

Deshabilitado, con [ **título**](caption-property.md)

No

Sí

No 

No 

False

True

No aparece

No

Sí

No 

No 

False

False

No aparece

No

No 

No 

Sí

True

True

No aparece

No 

No 

No 

Sí

True

False

No aparece

No

No 

No 

Sí

False

True

No aparece

No 

No 

No 

Sí

False

False

No aparece

No

No 

No 

No 

True

True

No aparece

No

No 

No 

No 

True

False

No aparece

No

No 

No 

No 

False

True

No aparece

No

No 

No 

No 

False

False

No aparece

No

 Si el valor de la propiedad es NULL. En algunos lenguajes de programación, una cadena vacía no puede interpretarse igual que una cadena nula.  El comando sigue siendo accesible mediante voz.<br/>



 

Cuando el servidor recibe la entrada para uno de los comandos, envía un evento de [**comando**](/windows/desktop/lwef/the-command-object) y devuelve el nombre del **comando** como un atributo del objeto [**UserInput**](/windows/desktop/lwef/iagentuserinput) . Después, puede usar las instrucciones condicionales para buscar coincidencias y procesar el **comando**.

 

