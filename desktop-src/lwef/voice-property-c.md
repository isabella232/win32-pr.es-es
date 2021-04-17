---
title: Propiedad Voice (objeto Command)
description: Propiedad Voice
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a8f9003b5200882fc01ee37edb868a261c68c7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695843"
---
# <a name="voice-property-command-object"></a><span data-ttu-id="36e5c-103">Propiedad Voice (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="36e5c-103">Voice Property (Command Object)</span></span>

<span data-ttu-id="36e5c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36e5c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="36e5c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="36e5c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="36e5c-106">Devuelve o establece el texto que se pasa a la gramática del motor de voz (para reconocimiento) para que coincida con este [**comando**](/windows/desktop/lwef/the-command-object) para el carácter.</span><span class="sxs-lookup"><span data-stu-id="36e5c-106">Returns or sets the text that is passed to the speech engine grammar (for recognition) for matching this [**Command**](/windows/desktop/lwef/the-command-object) for the character.</span></span>

</dd> <dt>

<span data-ttu-id="36e5c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="36e5c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="36e5c-108">\*agente \***. Caracteres ("**_CharacterID_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Cadena* de voz\]</span><span class="sxs-lookup"><span data-stu-id="36e5c-108">*agent\***.Characters ("**_CharacterID_*_").Commands ("_*_name_*_").Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="36e5c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="36e5c-109">Part</span></span>     | <span data-ttu-id="36e5c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="36e5c-110">Description</span></span>                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36e5c-111">*string*</span><span class="sxs-lookup"><span data-stu-id="36e5c-111">*string*</span></span> | <span data-ttu-id="36e5c-112">Expresión de cadena correspondiente a las palabras o la frase que va a usar el motor de voz para reconocer este [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="36e5c-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36e5c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36e5c-113">Remarks</span></span>

<span data-ttu-id="36e5c-114">Si no proporciona este parámetro, el [**VoiceCaption**](voicecaption-property.md) del objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) no aparecerá en la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="36e5c-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span> <span data-ttu-id="36e5c-115">Si especifica un parámetro de [**voz**](voice-property.md) pero no un **VoiceCaption** (o un [**título**](https://www.bing.com/search?q=**Caption**)), el comando no aparecerá en la ventana comandos de voz, pero será accesible desde un momento en el que la aplicación cliente se convierta en una entrada activa.</span><span class="sxs-lookup"><span data-stu-id="36e5c-115">If you specify a [**Voice**](voice-property.md) parameter but not a **VoiceCaption** (or [**Caption**](https://www.bing.com/search?q=**Caption**)), the command will not appear in the Voice Commands Window, but it will be voice-accessible when the client application becomes input-active.</span></span>

<span data-ttu-id="36e5c-116">La expresión de cadena puede incluir caracteres corchetes ( \[ \] ) para indicar que las palabras opcionales y los caracteres de barra vertical ( \| ) indican cadenas alternativas.</span><span class="sxs-lookup"><span data-stu-id="36e5c-116">Your string expression can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="36e5c-117">Las alternativas deben ir entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="36e5c-117">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="36e5c-118">Por ejemplo, "(Hello \[ ahí \] \| HI)" indica al motor de voz que acepte "Hello", "Hello There" o "HI" para el comando.</span><span class="sxs-lookup"><span data-stu-id="36e5c-118">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="36e5c-119">No olvide incluir los espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes o paréntesis.</span><span class="sxs-lookup"><span data-stu-id="36e5c-119">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="36e5c-120">Puede usar el operador Star ( \* ) para especificar cero o más instancias de las palabras incluidas en el grupo o el operador más (+) para especificar una o más instancias.</span><span class="sxs-lookup"><span data-stu-id="36e5c-120">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="36e5c-121">Por ejemplo, el siguiente resultado es una gramática que admite "pruebe esto", "pruébelo", "pruébelo", con iteraciones ilimitadas de ":</span><span class="sxs-lookup"><span data-stu-id="36e5c-121">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="36e5c-122">El siguiente formato de gramática excluye "pruebe esto" porque el operador + define al menos una instancia de "":</span><span class="sxs-lookup"><span data-stu-id="36e5c-122">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="36e5c-123">Los operadores de repetición siguen las reglas normales de precedencia y se aplican al elemento de texto inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="36e5c-123">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="36e5c-124">Por ejemplo, la siguiente gramática da como resultado "Nueva York" y "Nueva York York", pero no "Nueva York Nueva York":</span><span class="sxs-lookup"><span data-stu-id="36e5c-124">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="36e5c-125">Por lo tanto, normalmente deseará usar estos operadores con los caracteres de agrupación.</span><span class="sxs-lookup"><span data-stu-id="36e5c-125">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="36e5c-126">Por ejemplo, la siguiente gramática incluye "Nueva York" y "Nueva York Nueva York":</span><span class="sxs-lookup"><span data-stu-id="36e5c-126">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="36e5c-127">Los operadores de repetición son útiles cuando se desea crear una gramática que incluya una secuencia repetida como un número de teléfono o una especificación de una lista de elementos.</span><span class="sxs-lookup"><span data-stu-id="36e5c-127">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="36e5c-128">Aunque los operadores también se pueden usar con el carácter opcional de agrupación de corchetes, esto puede reducir la eficacia del procesamiento del agente de la gramática.</span><span class="sxs-lookup"><span data-stu-id="36e5c-128">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="36e5c-129">También puede usar puntos suspensivos (...) para admitir la detección de *palabras*, es decir, indicar al motor de reconocimiento de voz que omita las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras *basura* ).</span><span class="sxs-lookup"><span data-stu-id="36e5c-129">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="36e5c-130">Por lo tanto, el motor de voz solo reconoce palabras específicas de la cadena, con independencia de que se digan con palabras o frases adyacentes.</span><span class="sxs-lookup"><span data-stu-id="36e5c-130">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="36e5c-131">Por ejemplo, si establece esta propiedad en " \[ ... \] Comprobar correo electrónico \[ ... \] ", el motor de reconocimiento de voz coincidirá con frases como" comprobar correo "o" consultar correo electrónico "a este comando.</span><span class="sxs-lookup"><span data-stu-id="36e5c-131">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="36e5c-132">Los puntos suspensivos se pueden usar en cualquier parte de una cadena.</span><span class="sxs-lookup"><span data-stu-id="36e5c-132">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="36e5c-133">Sin embargo, tenga cuidado al usar esta técnica, ya que puede aumentar el potencial de las coincidencias no deseadas.</span><span class="sxs-lookup"><span data-stu-id="36e5c-133">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="36e5c-134">Al definir la gramática de palabras para el comando, incluya al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales.</span><span class="sxs-lookup"><span data-stu-id="36e5c-134">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="36e5c-135">Además, asegúrese de que la palabra solo incluye palabras y letras pronunciables.</span><span class="sxs-lookup"><span data-stu-id="36e5c-135">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="36e5c-136">En el caso de los números, es mejor deletrear la palabra en lugar de usar una representación ambigua.</span><span class="sxs-lookup"><span data-stu-id="36e5c-136">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="36e5c-137">Por ejemplo, "345" no es un buen formulario de gramática.</span><span class="sxs-lookup"><span data-stu-id="36e5c-137">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="36e5c-138">Del mismo modo, en lugar de "IEEE", use "I triple E".</span><span class="sxs-lookup"><span data-stu-id="36e5c-138">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="36e5c-139">También puede omitir cualquier signo de puntuación o símbolos.</span><span class="sxs-lookup"><span data-stu-id="36e5c-139">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="36e5c-140">Por ejemplo, en lugar de " \# $1 10 pizza!", use el número 1 10 de la pizza de dólares.</span><span class="sxs-lookup"><span data-stu-id="36e5c-140">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="36e5c-141">La inclusión de símbolos o caracteres no pronunciables para un comando puede hacer que el motor de voz no pueda compilar la gramática de todos los comandos.</span><span class="sxs-lookup"><span data-stu-id="36e5c-141">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="36e5c-142">Por último, haga que el parámetro de voz sea lo bastante distinto posible desde otros comandos de voz que defina.</span><span class="sxs-lookup"><span data-stu-id="36e5c-142">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="36e5c-143">Cuanto mayor sea la similitud entre la gramática de voz de los comandos, más probable será que el motor de voz haga un error de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="36e5c-143">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="36e5c-144">También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.</span><span class="sxs-lookup"><span data-stu-id="36e5c-144">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="36e5c-145">Puede incluir en las palabras gramaticales en forma de "*\\ Pronunciación de texto*", donde *texto* es el texto que se muestra y la *Pronunciación* es texto que clarifica la pronunciación.</span><span class="sxs-lookup"><span data-stu-id="36e5c-145">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="36e5c-146">Por ejemplo, la gramática, "1º \\ primero", se reconocería cuando el usuario dice "primero", pero el evento de [**comando**](/windows/desktop/lwef/the-command-object) devolverá el texto "1º \\ primero".</span><span class="sxs-lookup"><span data-stu-id="36e5c-146">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](/windows/desktop/lwef/the-command-object) event will return the text, "1st\\first".</span></span> <span data-ttu-id="36e5c-147">También puede usar IPA (alfabeto fonético internacional) para especificar una pronunciación iniciando la pronunciación con un signo de almohadilla (" \# ") y, a continuación, incluye el texto que representa la pronunciación del IPA.</span><span class="sxs-lookup"><span data-stu-id="36e5c-147">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="36e5c-148">En el caso de los motores de reconocimiento de voz en japonés, puede definir la gramática con el formato "*Kana \\ kanji*", lo que reduce las pronunciaciones alternativas y aumenta la precisión.</span><span class="sxs-lookup"><span data-stu-id="36e5c-148">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="36e5c-149">(La ordenación se invierte por compatibilidad con versiones anteriores). Esto es especialmente importante para la Pronunciación de nombres adecuados en kanji.</span><span class="sxs-lookup"><span data-stu-id="36e5c-149">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="36e5c-150">Sin embargo, puede pasar kanji sin Kana, en cuyo caso el motor debe escuchar todas las pronunciaciones aceptadas para el kanji.</span><span class="sxs-lookup"><span data-stu-id="36e5c-150">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="36e5c-151">También puede pasar Kana.</span><span class="sxs-lookup"><span data-stu-id="36e5c-151">You can also pass in just Kana.</span></span>

<span data-ttu-id="36e5c-152">Tenga en cuenta también que para idiomas como el japonés, el chino y el tailandés, que no usan caracteres de espacio para designar saltos de palabra, inserte un carácter de espacio de ancho cero de Unicode (0x200B) para indicar los saltos de palabra lógicos.</span><span class="sxs-lookup"><span data-stu-id="36e5c-152">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="36e5c-153">Salvo que se produzcan errores con los caracteres de formato de agrupación o repetición, el agente no notificará los errores en la gramática, a menos que el propio motor informe del error.</span><span class="sxs-lookup"><span data-stu-id="36e5c-153">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="36e5c-154">Si pasa texto en la gramática de que el motor no se puede compilar, pero el motor no controla y devuelve como un error, el agente no puede informar del error.</span><span class="sxs-lookup"><span data-stu-id="36e5c-154">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="36e5c-155">Por lo tanto, la aplicación cliente debe definir cuidadosamente la gramática de la propiedad [**Voice**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="36e5c-155">Therefore, the client application must be carefully define grammar for the [**Voice**](voice-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="36e5c-156">Las características de gramática disponibles pueden depender del motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="36e5c-156">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="36e5c-157">Puede que desee consultar con el proveedor del motor para determinar qué opciones de gramática se admiten.</span><span class="sxs-lookup"><span data-stu-id="36e5c-157">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="36e5c-158">Use [**SRModeID**](srmodeid-property.md) para usar un motor específico.</span><span class="sxs-lookup"><span data-stu-id="36e5c-158">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="36e5c-159">La operación de esta propiedad depende del estado de la propiedad reconocimiento de voz del servidor.</span><span class="sxs-lookup"><span data-stu-id="36e5c-159">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="36e5c-160">Por ejemplo, si el reconocimiento de voz está deshabilitado o no está instalado, esta propiedad no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="36e5c-160">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
