---
title: Propiedad Voice (objeto Commands)
description: Propiedad Voice
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0207fb4fb6f09d460496b6886354bc17738def17
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533657"
---
# <a name="voice-property-commands-object"></a>Propiedad Voice (objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el texto que se pasa a la gramática del motor de voz (para reconocimiento).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_"). Cadena Commands. Voice_ *  \[  =  \]



| Parte     | Descripción                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| *string* | Expresión de cadena correspondiente a las palabras o la frase que va a usar el motor de voz para reconocer este comando. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si no proporciona este parámetro, el [**VoiceCaption**](voicecaption-property.md) del objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) no aparecerá en la ventana comandos de voz.

La expresión de cadena proporcionada puede incluir caracteres corchetes ( \[ \] ) para indicar que las palabras opcionales y los caracteres de barra vertical ( \| ) indican cadenas alternativas. Las alternativas deben ir entre paréntesis. Por ejemplo, "(Hello \[ ahí \] \| HI)" indica al motor de voz que acepte "Hello", "Hello There" o "HI" para el comando. No olvide incluir los espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes o paréntesis. Puede usar el operador Star ( \* ) para especificar cero o más instancias de las palabras incluidas en el grupo o el operador más (+) para especificar una o más instancias. Por ejemplo, el siguiente resultado es una gramática que admite "pruebe esto", "pruébelo", "pruébelo", con iteraciones ilimitadas de ":


```
   "please* try this"
```



El siguiente formato de gramática excluye "pruebe esto" porque el operador + define al menos una instancia de "":


```
   "please+ try this"
```



Los operadores de repetición siguen las reglas normales de precedencia y se aplican al elemento de texto inmediatamente anterior. Por ejemplo, la siguiente gramática da como resultado "Nueva York" y "Nueva York York", pero no "Nueva York Nueva York":


```
   "New York+"
```



Por lo tanto, normalmente deseará usar estos operadores con los caracteres de agrupación. Por ejemplo, la siguiente gramática incluye "Nueva York" y "Nueva York Nueva York":


```
   "(New York)+"
```



Los operadores de repetición son útiles cuando se desea crear una gramática que incluya una secuencia repetida como un número de teléfono o una especificación de una lista de elementos.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Aunque los operadores también se pueden usar con el carácter opcional de agrupación de corchetes, esto puede reducir la eficacia del procesamiento del agente de la gramática.

También puede usar puntos suspensivos (...) para admitir la detección de *palabras*, es decir, indicar al motor de reconocimiento de voz que omita las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras *basura* ). Por lo tanto, el motor de voz solo reconoce palabras específicas de la cadena, con independencia de que se digan con palabras o frases adyacentes. Por ejemplo, si establece esta propiedad en " \[ ... \] Comprobar correo electrónico \[ ... \] ", el motor de reconocimiento de voz coincidirá con frases como" comprobar correo "o" consultar correo electrónico "a este comando. Los puntos suspensivos se pueden usar en cualquier parte de una cadena. Sin embargo, tenga cuidado al usar esta técnica, ya que puede aumentar el potencial de las coincidencias no deseadas.

Al definir la gramática de palabras para el comando, incluya al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales. Además, asegúrese de que la palabra solo incluye palabras y letras pronunciables. En el caso de los números, es mejor deletrear la palabra en lugar de usar una representación ambigua. Por ejemplo, "345" no es un buen formulario de gramática. Del mismo modo, en lugar de "IEEE", use "I triple E". También puede omitir cualquier signo de puntuación o símbolos. Por ejemplo, en lugar de " \# $1 10 pizza!", use el número 1 10 de la pizza de dólares. La inclusión de símbolos o caracteres no pronunciables para un comando puede hacer que el motor de voz no pueda compilar la gramática de todos los comandos. Por último, haga que el parámetro de voz sea lo bastante distinto posible desde otros comandos de voz que defina. Cuanto mayor sea la similitud entre la gramática de voz de los comandos, más probable será que el motor de voz haga un error de reconocimiento. También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.

Puede incluir en las palabras gramaticales en forma de "*\\ Pronunciación de texto*", donde *texto* es el texto que se muestra y la *Pronunciación* es texto que clarifica la pronunciación. Por ejemplo, la gramática, "1º \\ primero", se reconocería cuando el usuario dice "primero", pero el evento de [**comando**](command-event.md) devolverá el texto "1º \\ primero". También puede usar IPA (alfabeto fonético internacional) para especificar una pronunciación iniciando la pronunciación con un signo de almohadilla (" \# ") y, a continuación, incluye el texto que representa la pronunciación del IPA.

En el caso de los motores de reconocimiento de voz en japonés, puede definir la gramática con el formato "*Kana \\ kanji*", lo que reduce las pronunciaciones alternativas y aumenta la precisión. (La ordenación se invierte por compatibilidad con versiones anteriores). Esto es especialmente importante para la Pronunciación de nombres adecuados en kanji. Sin embargo, puede pasar kanji sin Kana, en cuyo caso el motor debe escuchar todas las pronunciaciones aceptadas para el kanji. También puede pasar Kana.

Tenga en cuenta también que para idiomas como el japonés, el chino y el tailandés, que no usan caracteres de espacio para designar saltos de palabra, inserte un carácter de espacio de ancho cero de Unicode (0x200B) para indicar los saltos de palabra lógicos.

Salvo que se produzcan errores con los caracteres de formato de agrupación o repetición, el agente no notificará los errores en la gramática, a menos que el propio motor informe del error. Si pasa texto en la gramática de que el motor no se puede compilar, pero el motor no controla y devuelve como un error, el agente no puede informar del error. Por lo tanto, la aplicación cliente debe definir cuidadosamente la gramática de la propiedad **Voice** .

> [!Note]  
> Las características de gramática disponibles pueden depender del motor de reconocimiento de voz. Puede que desee consultar con el proveedor del motor para determinar qué opciones de gramática se admiten. Use [**SRModeID**](srmodeid-property.md) para usar un motor específico.

 

La operación de esta propiedad depende del estado de la propiedad reconocimiento de voz del servidor. Por ejemplo, si el reconocimiento de voz está deshabilitado o no está instalado, esta propiedad no tiene ningún efecto.

 

 
