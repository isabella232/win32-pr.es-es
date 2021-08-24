---
title: IAgentCommand SetVoice
description: IAgentCommand SetVoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45af753dea18e9fda7b613e3b800ac886d949eb6494fd969cd8b7ceb488dfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477246"
---
# <a name="iagentcommandsetvoice"></a>IAgentCommand::SetVoice

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

Establece la [**propiedad Voice**](voice-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el texto de la propiedad [**Voice**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) debe tener su [**propiedad Voice y**](voice-property.md) la propiedad [**Enabled**](enabled-property.md) establecidas para que sean accesibles por voz. También debe tener su propiedad [**VoiceCaption**](voicecaption-property.md) establecida para que aparezca en la ventana **Comandos de voz**. (Para la compatibilidad con versiones anteriores, si no hay **VoiceCaption,** se usa la opción [**Título).**](caption-property.md)

La expresión BSTR que proporcione puede incluir caracteres de corchete ( ) para indicar palabras opcionales y caracteres de barra \[ \] vertical ( ) para \| indicar cadenas alternativas. Las alternativas deben incluirse entre paréntesis. Por ejemplo, "(hello there hi)" indica al motor de voz que acepte \[ \] \| "hello", "hello there" o "hi" para el comando. No olvide incluir los espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes ni paréntesis.

Puede usar el operador star ( ) para especificar cero o más instancias de las palabras incluidas en el grupo o el operador más (+) para especificar una o varias \* instancias. Por ejemplo, el siguiente resultado es una gramática que admite "try this", "please try this" y "please please try this", with unlimited iterations of "please":

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

Por lo tanto, normalmente querrá usar estos operadores con los caracteres de agrupación. Por ejemplo, la siguiente gramática incluye "Nueva York" y "Nueva York Nueva York":

``` syntax
   "(New York)+"
```

Los operadores de repetición son útiles cuando se desea crear una gramática que incluya una secuencia repetida, como un número de teléfono o una especificación de una lista de elementos:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Aunque los operadores también se pueden usar con los corchetes (un carácter de agrupación opcional), esto puede reducir la eficacia del procesamiento del Agente de la gramática.

También puede usar puntos suspensivos (...) para admitir la detención de *palabras,* es decir, decir al  motor de reconocimiento de voz que ignore las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras no utilizados). Por lo tanto, el motor de voz solo reconoce palabras específicas en la cadena, independientemente de cuando se habla con palabras o frases adyacentes. Por ejemplo, si establece esta propiedad en " \[ ... \] check mail ... " el motor de reconocimiento de voz coincidirá con frases como \[ \] "please check mail" o "check mail please" con este comando. Los puntos suspensivos se pueden usar en cualquier lugar dentro de una cadena. Sin embargo, tenga cuidado con esta técnica, ya que la configuración de voz con puntos suspensivos puede aumentar el potencial de coincidencias no deseadas.

Al definir las palabras y la gramática del comando, asegúrese siempre de incluir al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales. Además, asegúrese de que la palabra solo incluye palabras y letras pronunciables. En el caso de los números, es mejor escribir la palabra en lugar de usar la representación numérica. Además, omita los signos de puntuación o símbolos. Por ejemplo, en lugar de \# "1 pizza de 1 USD", use "la pizza número uno diez dólares". Incluir caracteres no pronunciables o símbolos para un comando puede hacer que el motor de voz no pueda compilar la gramática de todos los comandos. Por último, haga que el parámetro de voz sea lo más distinto posible de otros comandos de voz que defina. Cuanto mayor sea la similitud entre la gramática de voz para los comandos, más probable es que el motor de voz realice un error de reconocimiento. También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.

Al establecer [**la propiedad**](voice-property.md) Voz de un [**comando,**](/windows/desktop/lwef/the-command-object) se habilitan automáticamente los servicios de voz del Agente, lo que hace que la clave de escucha y la sugerencia de escucha estén disponibles. Sin embargo, no carga el motor de reconocimiento de voz.

> [!Note]  
> Las características gramaticales disponibles pueden depender del motor de reconocimiento de voz. Es posible que quiera consultar con el proveedor del motor para determinar qué opciones de gramática se admiten. Use [**IAgentCharacterEx::SRModeID para**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) especificar un motor.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 