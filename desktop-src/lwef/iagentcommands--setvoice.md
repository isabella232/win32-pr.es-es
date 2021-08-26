---
title: IAgentCommands SetVoice
description: IAgentCommands SetVoice
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02fb124b51a3be1796258fdcb8ffa31d8b81b59636027f3d99497b27cd2bd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961905"
---
# <a name="iagentcommandssetvoice"></a>IAgentCommands::SetVoice

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

Establece la [**propiedad Texto**](voice-property.md) de voz para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el valor de la propiedad [**Texto**](voice-property.md) de voz de una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

Una [**colección Commands**](/windows/desktop/lwef/the-commands-collection-object) debe tener su [**propiedad Voice**](voice-property.md) text establecida para que sea accesible por voz. También debe tener su propiedad [**VoiceCaption**](voicecaption-property.md) o [**Caption**](caption-property.md) establecida para que aparezca en la ventana Comandos de voz y su propiedad [**Visible**](visible-property.md) establecida en **True** para que aparezca en el menú emergente del carácter.

La expresión BSTR que proporcione puede incluir caracteres de corchetes ( ) para indicar palabras opcionales y caracteres de barra \[ \] vertical ( ) para \| indicar cadenas alternativas. Las alternativas deben ir entre paréntesis. Por ejemplo, "(hello there hi)" indica al motor de voz que acepte \[ \] \| "hello", "hello there" o "hi" para el comando. No olvide incluir espacios adecuados entre palabras que incluya entre corchetes o paréntesis, así como otro texto. No olvide incluir espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes ni paréntesis.

Puede usar el operador star ( ) para especificar cero o más instancias de las palabras incluidas en el grupo o el operador más (+) para especificar una o varias \* instancias. Por ejemplo, el siguiente resultado es una gramática que admite "try this", "please try this" y "please please try this", con iteraciones ilimitadas de "please":

``` syntax
   "please* try this"
```

El siguiente formato de gramática excluye "try this" porque el operador + define al menos una instancia de "please":

``` syntax
   "please+ try this"
```

Los operadores de repetición siguen las reglas normales de precedencia y se aplican al elemento de texto inmediatamente anterior. Por ejemplo, la siguiente gramática da como resultado "Nueva York" y "Nueva York", pero no "Nueva York Nueva York":

``` syntax
   "New York+"
```

Por lo tanto, normalmente desea usar estos operadores con los caracteres de agrupación. Por ejemplo, la gramática siguiente incluye "Nueva York" y "Nueva York Nueva York":

``` syntax
   "(New York)+"
```

Los operadores de repetición son útiles cuando se quiere crear una gramática que incluya una secuencia repetida, como un número de teléfono o la especificación de una lista de elementos:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Aunque los operadores también se pueden usar con corchetes (un carácter de agrupación opcional), esto puede reducir la eficacia del procesamiento del Agente de la gramática.

También puede usar puntos suspensivos (...) para admitir la detención de *palabras,* es decir, decir al  motor de reconocimiento de voz que ignore las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras no utilizados). Cuando se usan puntos suspensivos, el motor de voz solo reconoce palabras específicas en la cadena, independientemente de si se habla con palabras o frases adyacentes. Por ejemplo, si establece esta propiedad en " \[ ... \] check mail \[ ... " the speech recognition engine will match \] phrases like "please check mail" or "check mail please" to this command. Los puntos suspensivos se pueden usar en cualquier lugar dentro de una cadena. Sin embargo, tenga cuidado al usar esta técnica, ya que la configuración de voz con puntos suspensivos puede aumentar el potencial de coincidencias no deseadas.

Al definir las palabras y la gramática del comando, incluya al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales. Además, asegúrese de que la palabra incluye solo palabras y letras pronunciables. En el caso de los números, es mejor escribir la palabra en lugar de usar una representación ambigua. Por ejemplo, "345" no es una buena forma gramatical. De forma similar, en lugar de "IEEE", use "I triple E". Además, omita los signos de puntuación o símbolos. Por ejemplo, en lugar de \# "the 1 $10 pizza!", use "the number one ten dollar pizza". Incluir caracteres no pronunciables o símbolos para un comando puede hacer que el motor de voz no compile la gramática de todos los comandos. Por último, haga que el parámetro de voz sea lo más distinto posible de otros comandos de voz que defina. Cuanto mayor sea la similitud entre la gramática de voz de los comandos, más probable es que el motor de voz realice un error de reconocimiento. También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.

Puede incluir en las palabras gramaticales en forma de "*\\ pronunciación* de texto ", donde "text" es el texto que se muestra y "pronunciación" es texto que aclara la pronunciación. Por ejemplo, la gramática , "1st first", se reconocería cuando el usuario dice "first", pero el evento Command devolverá el texto \\ "1st [](/windows/desktop/lwef/the-command-object) \\ first". También puede usar IPA (Alfabeto fonético internacional) para especificar una pronunciación empezando la pronunciación con un carácter de signo de signo de perdigón (""), y luego el texto que representa la \# pronunciación IPA.

Para los motores de reconocimiento de voz japonés, puede definir la gramática con el formato *"kana \\ kanji",* lo que reduce las pronunciaciones alternativas y aumenta la precisión. (La ordenación se invierte por compatibilidad con versiones anteriores). Esto es especialmente importante para la pronunciación de nombres adecuados en Kanji. Sin embargo, solo puede pasar "kanji", sin kana, en cuyo caso el motor debe escuchar todas las pronunciaciones aceptables para el kanji. También puede pasar solo Kana.

A excepción de los errores que usan los caracteres de formato de agrupación o repetición, Microsoft Agent no notifica errores en la gramática, a menos que el propio motor informe del error. Si pasa texto en la gramática que el motor no puede compilar, pero el motor no controla y devuelve como un error, el Agente no puede notificar el error. Por lo tanto, la aplicación cliente debe tener cuidado al definir la gramática de la [**propiedad**](voice-property.md) Voice.

> [!Note]  
> Las características gramaticales disponibles pueden depender del motor de reconocimiento de voz. Es posible que quiera consultar con el proveedor del motor para determinar qué opciones de gramática se admiten. Use [**SRModeID para**](srmodeid-property.md) usar un motor específico.

 

El funcionamiento de esta propiedad depende del estado del estado de reconocimiento de voz del servidor de Microsoft Agent. Por ejemplo, si el reconocimiento de voz está deshabilitado o no está instalado, esta función no tiene ningún efecto inmediato. Sin embargo, si el reconocimiento de voz está habilitado durante una sesión, el comando estará accesible cuando su aplicación cliente esté activa en la entrada.

## <a name="see-also"></a>Consulte también

[**IAgentCommands::GetVoice**](iagentcommands--getvoice.md), [**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md)


 

 