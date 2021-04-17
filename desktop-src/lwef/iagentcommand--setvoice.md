---
title: IAgentCommand SetVoice
description: IAgentCommand SetVoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704953"
---
# <a name="iagentcommandsetvoice"></a>IAgentCommand::SetVoice

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

Establece la propiedad [**Voice**](voice-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el texto de la propiedad [**Voice**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) debe tener la propiedad de [**voz**](voice-property.md) y la propiedad [**habilitada**](enabled-property.md) establecida en accesible para voz. También debe tener su propiedad [**VoiceCaption**](voicecaption-property.md) establecida en aparecer en la **ventana comandos de voz**. (Para mantener la compatibilidad con versiones anteriores, si no hay ningún **VoiceCaption**, se usa la configuración del [**título**](caption-property.md) ).

La expresión BSTR que proporcione puede incluir caracteres corchetes ( \[ \] ) para indicar que las palabras opcionales y los caracteres de barra vertical ( \| ) indican cadenas alternativas. Las alternativas deben ir entre paréntesis. Por ejemplo, "(Hello \[ ahí \] \| HI)" indica al motor de voz que acepte "Hello", "Hello There" o "HI" para el comando. No olvide incluir los espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes o paréntesis.

Puede usar el operador Star ( \* ) para especificar cero o más instancias de las palabras incluidas en el grupo o el operador más (+) para especificar una o más instancias. Por ejemplo, el siguiente resultado es una gramática que admite "pruebe esto", "pruebe esto" y "pruébelo", con iteraciones ilimitadas de ",":

``` syntax
   "please* try this"
```

El siguiente formato de gramática excluye "pruebe esto" porque el operador + define al menos una instancia de "":

``` syntax
   "please+ try this"
```

Los operadores de repetición siguen las reglas normales de precedencia y se aplican al elemento de texto inmediatamente anterior. Por ejemplo, la siguiente gramática da como resultado "Nueva York" y "Nueva York York", pero no "Nueva York Nueva York":

``` syntax
   "New York+"
```

Por lo tanto, normalmente querrá usar estos operadores con los caracteres de agrupación. Por ejemplo, la siguiente gramática incluye "Nueva York" y "Nueva York Nueva York":

``` syntax
   "(New York)+"
```

Los operadores de repetición son útiles cuando se desea crear una gramática que incluya una secuencia repetida como un número de teléfono o una especificación de una lista de elementos:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Aunque los operadores también se pueden usar con los corchetes (un carácter de agrupación opcional), esto puede reducir la eficacia del procesamiento de la gramática del agente.

También puede usar puntos suspensivos (...) para admitir la detección de *palabras*, es decir, indicar al motor de reconocimiento de voz que omita las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras *basura* ). Por lo tanto, el motor de voz solo reconoce palabras específicas de la cadena, con independencia de que se digan con palabras o frases adyacentes. Por ejemplo, si establece esta propiedad en " \[ ... \] Comprobar correo electrónico \[ ... \] "el motor de reconocimiento de voz coincidirá con frases como" Revise el correo "o" consulte correo electrónico "para este comando. Los puntos suspensivos se pueden usar en cualquier parte de una cadena. Sin embargo, tenga cuidado al usar esta técnica, ya que la configuración de voz con puntos suspensivos puede aumentar el potencial de las coincidencias no deseadas.

Al definir las palabras y la gramática del comando, asegúrese siempre de incluir al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales. Además, asegúrese de que la palabra solo incluye palabras y letras pronunciables. En el caso de los números, es mejor deletrear la palabra en lugar de usar la representación numérica. También puede omitir cualquier signo de puntuación o símbolos. Por ejemplo, en lugar de " \# $1 10 pizza!", use el número 1 10 de la pizza de dólares. La inclusión de símbolos o caracteres no pronunciables para un comando puede hacer que el motor de voz no pueda compilar la gramática de todos los comandos. Por último, haga que el parámetro de voz sea lo bastante distinto posible desde otros comandos de voz que defina. Cuanto mayor sea la similitud entre la gramática de voz de los comandos, más probable será que el motor de voz haga un error de reconocimiento. También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.

La configuración de la propiedad [**Voice**](voice-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object) habilita automáticamente Speech Services del agente, lo que hace que la clave de escucha y la sugerencia de escucha estén disponibles. Sin embargo, no carga el motor de reconocimiento de voz.

> [!Note]  
> Las características de gramática disponibles pueden depender del motor de reconocimiento de voz. Puede que desee consultar con el proveedor del motor para determinar qué opciones de gramática se admiten. Use [**IAgentCharacterEx:: SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) para especificar un motor.

 

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setEnabled**](iagentcommand--setenabled.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 