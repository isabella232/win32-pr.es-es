---
title: Propiedad Voice (objeto Commands)
description: Obtenga información sobre la propiedad Voice del objeto Commands, que devuelve o establece el texto que se pasa a la gramática del motor de voz (para el reconocimiento).
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af651532894537f58d35f860b781d3be42bfacf89b9be01d7caa26aa40102ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715815"
---
# <a name="voice-property-commands-object"></a>Propiedad Voice (objeto Commands)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el texto que se pasa a la gramática del motor de voz (para el reconocimiento).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands.Voice_ *  \[  =  *string*\]



| Parte     | Descripción                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| *string* | Expresión de cadena que corresponde a las palabras o frases que va a usar el motor de voz para reconocer este comando. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si no proporciona este parámetro, [**VoiceCaption**](voicecaption-property.md) del objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) no aparecerá en la ventana Comandos de voz.

La expresión de cadena que proporcione puede incluir caracteres de corchete ( ) para indicar palabras opcionales y caracteres de barra \[ \] vertical ( ) para \| indicar cadenas alternativas. Las alternativas deben incluirse entre paréntesis. Por ejemplo, "(hello there hi)" indica al motor de voz que acepte \[ \] \| "hello", "hello there" o "hi" para el comando. No olvide incluir espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes ni paréntesis. Puede usar el operador star ( ) para especificar cero o más instancias de las palabras incluidas en el grupo o el operador más (+) para especificar una o varias \* instancias. Por ejemplo, el siguiente resultado es una gramática que admite "try this", "please try this", "please please try this", with unlimited iterations of "please":


```
   "please* try this"
```



El siguiente formato de gramática excluye "try this" porque el operador + define al menos una instancia de "please":


```
   "please+ try this"
```



Los operadores de repetición siguen las reglas normales de precedencia y se aplican al elemento de texto inmediatamente anterior. Por ejemplo, la siguiente gramática da como resultado "Nueva York" y "Nueva York", pero no "Nueva York Nueva York":


```
   "New York+"
```



Por lo tanto, normalmente desea utilizar estos operadores con los caracteres de agrupación. Por ejemplo, la siguiente gramática incluye "Nueva York" y "Nueva York Nueva York":


```
   "(New York)+"
```



Los operadores de repetición son útiles cuando se desea crear una gramática que incluya una secuencia repetida, como un número de teléfono o la especificación de una lista de elementos.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Aunque los operadores también se pueden usar con el carácter de agrupación de corchetes opcional, esto puede reducir la eficacia del procesamiento del Agente de la gramática.

También puede usar puntos suspensivos (...) para admitir la detención de *palabras,* es decir, decir al  motor de reconocimiento de voz que ignore las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras no utilizados). Por lo tanto, el motor de voz solo reconoce palabras específicas en la cadena, independientemente de cuando se habla con palabras o frases adyacentes. Por ejemplo, si establece esta propiedad en " \[ ... \] check mail ... ", el motor de reconocimiento de voz coincidirá con frases como \[ \] "please check mail" o "check mail please" con este comando. Los puntos suspensivos se pueden usar en cualquier lugar dentro de una cadena. Sin embargo, tenga cuidado al usar esta técnica, ya que puede aumentar el potencial de coincidencias no deseadas.

Al definir la gramática de palabras para el comando, incluya al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales. Además, asegúrese de que la palabra solo incluye palabras y letras pronunciables. En el caso de los números, es mejor escribir la palabra en lugar de usar una representación ambigua. Por ejemplo, "345" no es una buena forma gramatical. De forma similar, en lugar de "IEEE", use "I triple E". Además, omita los signos de puntuación o símbolos. Por ejemplo, en lugar de \# "the 1 $10 pizza!", use "the number one ten dollar pizza". Incluir caracteres no pronunciables o símbolos para un comando puede hacer que el motor de voz no pueda compilar la gramática de todos los comandos. Por último, haga que el parámetro de voz sea lo más distinto posible de otros comandos de voz que defina. Cuanto mayor sea la similitud entre la gramática de voz para los comandos, más probable es que el motor de voz realice un error de reconocimiento. También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.

Puede incluir en las palabras gramaticales en forma de  *\\ "pronunciación* de texto", donde el texto es el texto mostrado y *la pronunciación* es el texto que aclara la pronunciación. Por ejemplo, la gramática , "1st first", se reconocería cuando el usuario dice "first", pero el evento Command devolverá el texto \\ "1st [](command-event.md) \\ first". También puede usar IPA (alfabeto fonético internacional) para especificar una pronunciación empezando la pronunciación con un carácter de signo de kilo (" ") y, a continuación, incluir el texto que representa la \# pronunciación IPA.

En el caso de los motores de reconocimiento de voz en japonés, puede definir la gramática con el formato *"kana \\ kanji",* lo que reduce las pronunciaciones alternativas y aumenta la precisión. (La ordenación se invierte por compatibilidad con versiones anteriores). Esto es especialmente importante para la pronunciación de nombres adecuados en Kanji. Sin embargo, solo puede pasar kanji sin el kana, en cuyo caso el motor debe escuchar todas las pronunciaciones aceptables para el kanji. También puede pasar solo Kana.

Tenga en cuenta también que para idiomas como japonés, chino y tailandés, que no usan caracteres de espacio para designar saltos de palabras, inserte un carácter de espacio de ancho cero Unicode (0x200B) para indicar saltos de palabras lógicos.

A excepción de los errores que usan los caracteres de formato de agrupación o repetición, el Agente no notifica errores en la gramática, a menos que el propio motor informe del error. Si pasa texto en la gramática que el motor no puede compilar, pero el motor no controla y devuelve como un error, el Agente no puede notificar el error. Por lo tanto, la aplicación cliente debe definir cuidadosamente la gramática para la **propiedad** Voice.

> [!Note]  
> Las características gramaticales disponibles pueden depender del motor de reconocimiento de voz. Es posible que quiera consultar con el proveedor del motor para determinar qué opciones de gramática se admiten. Use [**SRModeID para**](srmodeid-property.md) usar un motor específico.

 

El funcionamiento de esta propiedad depende del estado de la propiedad de reconocimiento de voz del servidor. Por ejemplo, si el reconocimiento de voz está deshabilitado o no está instalado, esta propiedad no tiene ningún efecto.

 

 
