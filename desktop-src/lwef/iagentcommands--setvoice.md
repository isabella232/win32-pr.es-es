---
title: IAgentCommands SetVoice
description: IAgentCommands SetVoice
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a8e29936dbca65ffded5f8a5e5ea5297b28362e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487594"
---
# <a name="iagentcommandssetvoice"></a>IAgentCommands::SetVoice

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

Establece la propiedad texto de [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el valor de la propiedad de texto de [**voz**](voice-property.md) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

Una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) debe tener la propiedad texto de [**voz**](voice-property.md) establecida en accesible desde voz. También debe tener la propiedad [**VoiceCaption**](voicecaption-property.md) o [**Caption**](caption-property.md) establecida en aparecer en la ventana comandos de voz y su propiedad [**visible**](visible-property.md) establecida en **true** para que aparezca en el menú emergente del carácter.

La expresión BSTR que proporcione puede incluir caracteres corchetes ( \[ \] ) para indicar que las palabras opcionales y los caracteres de barra vertical ( \| ) indican cadenas alternativas. Las alternativas deben ir entre paréntesis. Por ejemplo, "(Hello \[ ahí \] \| HI)" indica al motor de voz que acepte "Hello", "Hello There" o "HI" para el comando. No olvide incluir los espacios adecuados entre las palabras que incluya entre corchetes o paréntesis, así como otro texto. No olvide incluir los espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes o paréntesis.

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

Por lo tanto, normalmente deseará usar estos operadores con los caracteres de agrupación. Por ejemplo, la siguiente gramática incluye "Nueva York" y "Nueva York Nueva York":

``` syntax
   "(New York)+"
```

Los operadores de repetición son útiles cuando se desea crear una gramática que incluya una secuencia repetida como un número de teléfono o una especificación de una lista de elementos:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Aunque los operadores también se pueden usar con corchetes (un carácter de agrupación opcional), esto puede reducir la eficacia del procesamiento de la gramática del agente.

También puede usar puntos suspensivos (...) para admitir la detección de *palabras*, es decir, indicar al motor de reconocimiento de voz que omita las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras *basura* ). Al usar puntos suspensivos, el motor de voz solo reconoce palabras específicas de la cadena, con independencia de que se digan con palabras o frases adyacentes. Por ejemplo, si establece esta propiedad en " \[ ... \] Comprobar correo electrónico \[ ... \] "el motor de reconocimiento de voz coincidirá con frases como" Revise el correo "o" consulte correo electrónico "para este comando. Los puntos suspensivos se pueden usar en cualquier parte de una cadena. Sin embargo, tenga cuidado con esta técnica, ya que la configuración de voz con puntos suspensivos puede aumentar el potencial de las coincidencias no deseadas.

Al definir las palabras y la gramática del comando, incluya al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales. Además, asegúrese de que la palabra solo incluye palabras y letras pronunciables. En el caso de los números, es mejor deletrear la palabra en lugar de usar una representación ambigua. Por ejemplo, "345" no es un buen formulario de gramática. Del mismo modo, en lugar de "IEEE", use "I triple E". También puede omitir cualquier signo de puntuación o símbolos. Por ejemplo, en lugar de " \# $1 10 pizza!", use el número 1 10 de la pizza de dólares. La inclusión de símbolos o caracteres no pronunciables para un comando puede hacer que el motor de voz no pueda compilar la gramática de todos los comandos. Por último, haga que el parámetro de voz sea lo bastante distinto posible desde otros comandos de voz que defina. Cuanto mayor sea la similitud entre la gramática de voz de los comandos, más probable será que el motor de voz haga un error de reconocimiento. También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.

Puede incluir en las palabras gramaticales en forma de "*\\ Pronunciación de texto*", donde "texto" es el texto que se muestra y "Pronunciación" es el texto que clarifica la pronunciación. Por ejemplo, la gramática, "1º \\ primero", se reconocería cuando el usuario dice "primero", pero el evento de [**comando**](/windows/desktop/lwef/the-command-object) devolverá el texto "1º \\ primero". También puede usar IPA (alfabeto fonético internacional) para especificar una pronunciación iniciando la pronunciación con un carácter de signo de almohadilla (" \# ") y, después, el texto que representa la pronunciación del IPA.

En el caso de los motores de reconocimiento de voz en japonés, puede definir la gramática con el formato "*Kana \\ kanji*", lo que reduce las pronunciaciones alternativas y aumenta la precisión. (La ordenación se invierte por compatibilidad con versiones anteriores). Esto es especialmente importante para la Pronunciación de nombres adecuados en kanji. Sin embargo, puede pasar "kanji" sin Kana, en cuyo caso el motor debe escuchar todas las pronunciaciones aceptadas para el kanji. También puede pasar Kana.

A excepción de los errores que usan los caracteres de formato de agrupación o repetición, el agente de Microsoft no notificará los errores en la gramática, a menos que el propio motor notifique el error. Si pasa texto en la gramática de que el motor no se puede compilar, pero el motor no controla y devuelve como un error, el agente no puede informar del error. Por lo tanto, la aplicación cliente debe tener cuidado al definir la gramática de la propiedad [**Voice**](voice-property.md) .

> [!Note]  
> Las características de gramática disponibles pueden depender del motor de reconocimiento de voz. Puede que desee consultar con el proveedor del motor para determinar qué opciones de gramática se admiten. Use [**SRModeID**](srmodeid-property.md) para usar un motor específico.

 

El funcionamiento de esta propiedad depende del estado del reconocimiento de voz de Microsoft Agent Server. Por ejemplo, si el reconocimiento de voz está deshabilitado o no está instalado, esta función no tiene ningún efecto inmediato. Sin embargo, si el reconocimiento de voz está habilitado durante una sesión, el comando pasará a ser accesible cuando la aplicación cliente sea de entrada.

## <a name="see-also"></a>Consulte también

[**IAgentCommands:: GetVoice**](iagentcommands--getvoice.md), [**IAgentCommands:: SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands:: setVisible**](iagentcommands--setvisible.md)


 

 