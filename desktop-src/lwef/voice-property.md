---
title: Propiedad Voice (objeto Commands)
description: Obtenga información sobre la propiedad Voice del objeto Commands, que devuelve o establece el texto que se pasa a la gramática del motor de voz (para el reconocimiento).
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7403075d8ec0b2d16c66130fc9534edf4fc391df
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396160"
---
# <a name="voice-property-commands-object"></a><span data-ttu-id="c933b-103">Propiedad Voice (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="c933b-103">Voice Property (Commands Object)</span></span>

<span data-ttu-id="c933b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c933b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c933b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c933b-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c933b-106">Devuelve o establece el texto que se pasa a la gramática del motor de voz (para el reconocimiento).</span><span class="sxs-lookup"><span data-stu-id="c933b-106">Returns or sets the text that is passed to the speech engine grammar (for recognition).</span></span>

</dd> <dt>

<span data-ttu-id="c933b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="c933b-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c933b-108">*agent\***. Caracteres ("**_CharacterID_*_"). Commands.Voice_ \*  \[  =  *string*\]</span><span class="sxs-lookup"><span data-stu-id="c933b-108">*agent\***.Characters ("**_CharacterID_*_").Commands.Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="c933b-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c933b-109">Part</span></span>     | <span data-ttu-id="c933b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c933b-110">Description</span></span>                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c933b-111">*string*</span><span class="sxs-lookup"><span data-stu-id="c933b-111">*string*</span></span> | <span data-ttu-id="c933b-112">Expresión de cadena correspondiente a las palabras o frases que va a usar el motor de voz para reconocer este comando.</span><span class="sxs-lookup"><span data-stu-id="c933b-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c933b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c933b-113">Remarks</span></span>

<span data-ttu-id="c933b-114">Si no proporciona este parámetro, [**voiceCaption**](voicecaption-property.md) del objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) no aparecerá en la ventana Comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="c933b-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span>

<span data-ttu-id="c933b-115">La expresión de cadena que proporcione puede incluir caracteres de corchetes ( ) para indicar palabras opcionales y caracteres de barra \[ \] vertical ( ) para \| indicar cadenas alternativas.</span><span class="sxs-lookup"><span data-stu-id="c933b-115">The string expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="c933b-116">Las alternativas deben ir entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="c933b-116">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="c933b-117">Por ejemplo, "(hello there hi)" indica al motor de voz que acepte \[ \] \| "hello", "hello there" o "hi" para el comando.</span><span class="sxs-lookup"><span data-stu-id="c933b-117">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="c933b-118">No olvide incluir espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes ni paréntesis.</span><span class="sxs-lookup"><span data-stu-id="c933b-118">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span> <span data-ttu-id="c933b-119">Puede usar el operador star ( ) para especificar cero o más instancias de las palabras incluidas en el grupo o el operador más (+) para especificar una o varias \* instancias.</span><span class="sxs-lookup"><span data-stu-id="c933b-119">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="c933b-120">Por ejemplo, el siguiente resultado es una gramática que admite "try this", "please try this", "please please try this", with unlimited iterations of "please":</span><span class="sxs-lookup"><span data-stu-id="c933b-120">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="c933b-121">El siguiente formato de gramática excluye "try this" porque el operador + define al menos una instancia de "please":</span><span class="sxs-lookup"><span data-stu-id="c933b-121">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="c933b-122">Los operadores de repetición siguen las reglas normales de precedencia y se aplican al elemento de texto inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="c933b-122">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="c933b-123">Por ejemplo, la siguiente gramática da como resultado "Nueva York" y "Nueva York", pero no "Nueva York Nueva York":</span><span class="sxs-lookup"><span data-stu-id="c933b-123">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="c933b-124">Por lo tanto, normalmente desea usar estos operadores con los caracteres de agrupación.</span><span class="sxs-lookup"><span data-stu-id="c933b-124">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="c933b-125">Por ejemplo, la gramática siguiente incluye "Nueva York" y "Nueva York Nueva York":</span><span class="sxs-lookup"><span data-stu-id="c933b-125">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="c933b-126">Los operadores de repetición son útiles cuando se quiere crear una gramática que incluya una secuencia repetida, como un número de teléfono o la especificación de una lista de elementos.</span><span class="sxs-lookup"><span data-stu-id="c933b-126">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="c933b-127">Aunque los operadores también se pueden usar con el carácter de agrupación de corchetes opcional, hacerlo puede reducir la eficacia del procesamiento del Agente de la gramática.</span><span class="sxs-lookup"><span data-stu-id="c933b-127">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="c933b-128">También puede usar puntos suspensivos (...) para admitir la detención de *palabras,* es decir, para decir  al motor de reconocimiento de voz que ignore las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras no utilizados).</span><span class="sxs-lookup"><span data-stu-id="c933b-128">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="c933b-129">Por lo tanto, el motor de voz reconoce solo palabras específicas en la cadena, independientemente de cuando se habla con palabras o frases adyacentes.</span><span class="sxs-lookup"><span data-stu-id="c933b-129">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="c933b-130">Por ejemplo, si establece esta propiedad en " \[ ... \] check mail ... ", el motor de reconocimiento de voz coincidirá con frases como \[ \] "please check mail" o "check mail please" con este comando.</span><span class="sxs-lookup"><span data-stu-id="c933b-130">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="c933b-131">Los puntos suspensivos se pueden usar en cualquier lugar dentro de una cadena.</span><span class="sxs-lookup"><span data-stu-id="c933b-131">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="c933b-132">Sin embargo, tenga cuidado al usar esta técnica, ya que puede aumentar el potencial de coincidencias no deseadas.</span><span class="sxs-lookup"><span data-stu-id="c933b-132">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="c933b-133">Al definir la gramática de palabras para el comando, incluya al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales.</span><span class="sxs-lookup"><span data-stu-id="c933b-133">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="c933b-134">Además, asegúrese de que la palabra incluye solo palabras y letras pronunciables.</span><span class="sxs-lookup"><span data-stu-id="c933b-134">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="c933b-135">En el caso de los números, es mejor escribir la palabra en lugar de usar una representación ambigua.</span><span class="sxs-lookup"><span data-stu-id="c933b-135">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="c933b-136">Por ejemplo, "345" no es una buena forma gramatical.</span><span class="sxs-lookup"><span data-stu-id="c933b-136">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="c933b-137">De forma similar, en lugar de "IEEE", use "I triple E".</span><span class="sxs-lookup"><span data-stu-id="c933b-137">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="c933b-138">Además, omita los signos de puntuación o símbolos.</span><span class="sxs-lookup"><span data-stu-id="c933b-138">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="c933b-139">Por ejemplo, en lugar de \# "the 1 $10 pizza!", use "the number one ten dollar pizza".</span><span class="sxs-lookup"><span data-stu-id="c933b-139">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="c933b-140">Incluir caracteres no pronunciables o símbolos para un comando puede hacer que el motor de voz no compile la gramática de todos los comandos.</span><span class="sxs-lookup"><span data-stu-id="c933b-140">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="c933b-141">Por último, haga que el parámetro de voz sea lo más distinto posible de otros comandos de voz que defina.</span><span class="sxs-lookup"><span data-stu-id="c933b-141">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="c933b-142">Cuanto mayor sea la similitud entre la gramática de voz de los comandos, más probable es que el motor de voz realice un error de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="c933b-142">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="c933b-143">También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.</span><span class="sxs-lookup"><span data-stu-id="c933b-143">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="c933b-144">Puede incluir en las palabras gramaticales en forma de  *\\ "pronunciación* de texto", donde el texto es el texto que se muestra y *la pronunciación* es texto que aclara la pronunciación.</span><span class="sxs-lookup"><span data-stu-id="c933b-144">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="c933b-145">Por ejemplo, la gramática , "1st first", se reconocería cuando el usuario dice "first", pero el evento Command devolverá el texto \\ "1st [](command-event.md) \\ first".</span><span class="sxs-lookup"><span data-stu-id="c933b-145">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](command-event.md) event will return the text, "1st\\first".</span></span> <span data-ttu-id="c933b-146">También puede usar IPA (alfabeto fonético internacional) para especificar una pronunciación empezando la pronunciación con un carácter de signo de perdigón (""), y luego incluir el texto que representa la \# pronunciación IPA.</span><span class="sxs-lookup"><span data-stu-id="c933b-146">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="c933b-147">En el caso de los motores de reconocimiento de voz en japonés, puede definir la gramática con el formato *"kana \\ kanji",* lo que reduce las pronunciaciones alternativas y aumenta la precisión.</span><span class="sxs-lookup"><span data-stu-id="c933b-147">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="c933b-148">(La ordenación se invierte por compatibilidad con versiones anteriores). Esto es especialmente importante para la pronunciación de nombres adecuados en Kanji.</span><span class="sxs-lookup"><span data-stu-id="c933b-148">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="c933b-149">Sin embargo, solo puede pasar kanji sin kana, en cuyo caso el motor debe escuchar todas las pronunciaciones aceptables para el kanji.</span><span class="sxs-lookup"><span data-stu-id="c933b-149">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="c933b-150">También puede pasar solo Kana.</span><span class="sxs-lookup"><span data-stu-id="c933b-150">You can also pass in just Kana.</span></span>

<span data-ttu-id="c933b-151">Tenga en cuenta también que para idiomas como japonés, chino y tailandés, que no usan caracteres de espacio para designar saltos de palabras, inserte un carácter de espacio de ancho cero Unicode (0x200B) para indicar saltos de palabras lógicos.</span><span class="sxs-lookup"><span data-stu-id="c933b-151">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="c933b-152">A excepción de los errores que usan los caracteres de formato de agrupación o repetición, el Agente no notifica errores en la gramática, a menos que el propio motor informe del error.</span><span class="sxs-lookup"><span data-stu-id="c933b-152">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="c933b-153">Si pasa texto en la gramática que el motor no puede compilar, pero el motor no controla y devuelve como un error, el Agente no puede notificar el error.</span><span class="sxs-lookup"><span data-stu-id="c933b-153">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="c933b-154">Por lo tanto, la aplicación cliente debe definir cuidadosamente la gramática para la **propiedad** Voice.</span><span class="sxs-lookup"><span data-stu-id="c933b-154">Therefore, the client application must be carefully define grammar for the **Voice** property.</span></span>

> [!Note]  
> <span data-ttu-id="c933b-155">Las características gramaticales disponibles pueden depender del motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="c933b-155">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="c933b-156">Es posible que quiera consultar con el proveedor del motor para determinar qué opciones de gramática se admiten.</span><span class="sxs-lookup"><span data-stu-id="c933b-156">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="c933b-157">Use [**SRModeID para**](srmodeid-property.md) usar un motor específico.</span><span class="sxs-lookup"><span data-stu-id="c933b-157">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="c933b-158">El funcionamiento de esta propiedad depende del estado de la propiedad de reconocimiento de voz del servidor.</span><span class="sxs-lookup"><span data-stu-id="c933b-158">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="c933b-159">Por ejemplo, si el reconocimiento de voz está deshabilitado o no está instalado, esta propiedad no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="c933b-159">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
