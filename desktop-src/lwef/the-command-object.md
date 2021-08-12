---
title: El objeto Command
description: El objeto Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242a90022431b826cf877edd862cd89a39d193865ed31afc1e4ff911f4189756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245621"
---
# <a name="the-command-object"></a>El objeto Command

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Un [**objeto Command**](/windows/desktop/lwef/the-command-object) es un elemento de una colección [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) El servidor proporciona al usuario acceso a los **objetos Command** cuando la aplicación cliente se convierte en input-active.

-   [Propiedades del objeto Command](command-object-properties.md)

Para tener acceso a la propiedad de un [**objeto Command,**](/windows/desktop/lwef/the-command-object) se hace referencia a él en su colección mediante su [**propiedad Name.**](name-property.md) En VBScript y Visual Basic puede usar la **propiedad Name** directamente:


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



Para los lenguajes de programación que no admiten colecciones, use el [**método Command:**](command-method.md)


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



También puede hacer referencia a un objeto Command creando una referencia a él. En Visual Basic, declare una variable de objeto y use la instrucción Set para crear la referencia:


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



En Visual Basic 5.0, también puede declarar el objeto como tipo [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) y crear la referencia. Esta convención permite el enlace temprano, lo que da como resultado un mejor rendimiento:


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



En VBScript, puede declarar una referencia como un tipo determinado, pero todavía puede declarar la variable y establecerla en [**el comando**](/windows/desktop/lwef/the-command-object) de la colección:


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



Un comando puede aparecer en el menú emergente del carácter y en la ventana Comandos, o en ambos. Para aparecer en el menú emergente, debe tener un título y tener la [**propiedad Visible**](visible-property.md) establecida en **True.** Además, su propiedad Visible del objeto **de** colección Commands también debe establecerse en **True.** Para que aparezca en la ventana Comandos, un [**comando**](/windows/desktop/lwef/the-command-object) debe tener establecidas sus propiedades [**Caption**](caption-property.md) [**y**](voice-property.md) Voice. Tenga en cuenta que las entradas del menú emergente de un carácter no cambian mientras se muestra el menú. Si agrega o quita comandos o cambia sus propiedades mientras se muestra el menú emergente del carácter, el menú muestra esos cambios cada vez que el usuario lo muestra a continuación. Sin embargo, la ventana Comandos refleja dinámicamente los cambios que realice.

En la tabla siguiente se resume cómo afectan las propiedades de un [**comando**](/windows/desktop/lwef/the-command-object) a su presentación:



Propiedad Caption

Voice-Caption propiedad

Propiedad Voice

Propiedad Visible

Propiedad Enabled

Aparece en el menú emergente del carácter

Aparece en la ventana Comandos

Sí

Sí

Sí

True

True

Normal, con [ **título**](caption-property.md)

Sí, con [ **VoiceCaption**](voicecaption-property.md)

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

Sí, con [ **VoiceCaption**](voicecaption-property.md)

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

Sí, con [ **VoiceCaption**](voicecaption-property.md)

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

Sí, con [ **VoiceCaption**](voicecaption-property.md)

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

Sí, con [ **Título**](caption-property.md)

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

Sí, con [ **Título**](caption-property.md)

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

 Si el valor de la propiedad es NULL. En algunos lenguajes de programación, es posible que una cadena vacía no se interprete igual que una cadena nula.  El comando sigue siendo accesible por voz.<br/>



 

Cuando el servidor recibe la entrada de uno de los comandos, envía un evento [**Command**](/windows/desktop/lwef/the-command-object) y devuelve el nombre del **comando** como atributo del [**objeto UserInput.**](/windows/desktop/lwef/iagentuserinput) A continuación, puede usar instrucciones condicionales para hacer coincidir y procesar el **comando**.

 

