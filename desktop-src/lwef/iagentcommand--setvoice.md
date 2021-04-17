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
# <a name="iagentcommandsetvoice"></a><span data-ttu-id="17742-103">IAgentCommand::SetVoice</span><span class="sxs-lookup"><span data-stu-id="17742-103">IAgentCommand::SetVoice</span></span>

<span data-ttu-id="17742-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17742-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

<span data-ttu-id="17742-105">Establece la propiedad [**Voice**](voice-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="17742-105">Sets the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="17742-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="17742-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="17742-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="17742-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="17742-108">BSTR que especifica el texto de la propiedad [**Voice**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="17742-108">A BSTR that specifies the text for the [**Voice**](voice-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="17742-109">Un [**comando**](/windows/desktop/lwef/the-command-object) debe tener la propiedad de [**voz**](voice-property.md) y la propiedad [**habilitada**](enabled-property.md) establecida en accesible para voz.</span><span class="sxs-lookup"><span data-stu-id="17742-109">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Voice**](voice-property.md) property and [**Enabled**](enabled-property.md) property set to be voice-accessible.</span></span> <span data-ttu-id="17742-110">También debe tener su propiedad [**VoiceCaption**](voicecaption-property.md) establecida en aparecer en la **ventana comandos de voz**.</span><span class="sxs-lookup"><span data-stu-id="17742-110">It also must have its [**VoiceCaption**](voicecaption-property.md) property set to appear in the **Voice Commands Window**.</span></span> <span data-ttu-id="17742-111">(Para mantener la compatibilidad con versiones anteriores, si no hay ningún **VoiceCaption**, se usa la configuración del [**título**](caption-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="17742-111">(For backward compatibility, if there is no **VoiceCaption**, the [**Caption**](caption-property.md) setting is used.)</span></span>

<span data-ttu-id="17742-112">La expresión BSTR que proporcione puede incluir caracteres corchetes ( \[ \] ) para indicar que las palabras opcionales y los caracteres de barra vertical ( \| ) indican cadenas alternativas.</span><span class="sxs-lookup"><span data-stu-id="17742-112">The BSTR expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="17742-113">Las alternativas deben ir entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="17742-113">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="17742-114">Por ejemplo, "(Hello \[ ahí \] \| HI)" indica al motor de voz que acepte "Hello", "Hello There" o "HI" para el comando.</span><span class="sxs-lookup"><span data-stu-id="17742-114">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="17742-115">No olvide incluir los espacios adecuados entre el texto entre corchetes o paréntesis y el texto que no está entre corchetes o paréntesis.</span><span class="sxs-lookup"><span data-stu-id="17742-115">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="17742-116">Puede usar el operador Star ( \* ) para especificar cero o más instancias de las palabras incluidas en el grupo o el operador más (+) para especificar una o más instancias.</span><span class="sxs-lookup"><span data-stu-id="17742-116">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="17742-117">Por ejemplo, el siguiente resultado es una gramática que admite "pruebe esto", "pruebe esto" y "pruébelo", con iteraciones ilimitadas de ",":</span><span class="sxs-lookup"><span data-stu-id="17742-117">For example, the following results in a grammar that supports "try this", "please try this", and "please please try this", with unlimited iterations of "please":</span></span>

``` syntax
   "please* try this"
```

<span data-ttu-id="17742-118">El siguiente formato de gramática excluye "pruebe esto" porque el operador + define al menos una instancia de "":</span><span class="sxs-lookup"><span data-stu-id="17742-118">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>

``` syntax
   "please+ try this"
```

<span data-ttu-id="17742-119">Los operadores de repetición siguen las reglas normales de precedencia y se aplican al elemento de texto inmediatamente anterior.</span><span class="sxs-lookup"><span data-stu-id="17742-119">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="17742-120">Por ejemplo, la siguiente gramática da como resultado "Nueva York" y "Nueva York York", pero no "Nueva York Nueva York":</span><span class="sxs-lookup"><span data-stu-id="17742-120">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>

``` syntax
   "New York+"
```

<span data-ttu-id="17742-121">Por lo tanto, normalmente querrá usar estos operadores con los caracteres de agrupación.</span><span class="sxs-lookup"><span data-stu-id="17742-121">Therefore, you will typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="17742-122">Por ejemplo, la siguiente gramática incluye "Nueva York" y "Nueva York Nueva York":</span><span class="sxs-lookup"><span data-stu-id="17742-122">For example, the following grammar includes both "New York" and "New York New York":</span></span>

``` syntax
   "(New York)+"
```

<span data-ttu-id="17742-123">Los operadores de repetición son útiles cuando se desea crear una gramática que incluya una secuencia repetida como un número de teléfono o una especificación de una lista de elementos:</span><span class="sxs-lookup"><span data-stu-id="17742-123">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items:</span></span>

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

<span data-ttu-id="17742-124">Aunque los operadores también se pueden usar con los corchetes (un carácter de agrupación opcional), esto puede reducir la eficacia del procesamiento de la gramática del agente.</span><span class="sxs-lookup"><span data-stu-id="17742-124">Although the operators can also be used with the square brackets (an optional grouping character), doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="17742-125">También puede usar puntos suspensivos (...) para admitir la detección de *palabras*, es decir, indicar al motor de reconocimiento de voz que omita las palabras que se pronuncian en esta posición en la frase (a veces denominadas palabras *basura* ).</span><span class="sxs-lookup"><span data-stu-id="17742-125">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="17742-126">Por lo tanto, el motor de voz solo reconoce palabras específicas de la cadena, con independencia de que se digan con palabras o frases adyacentes.</span><span class="sxs-lookup"><span data-stu-id="17742-126">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="17742-127">Por ejemplo, si establece esta propiedad en " \[ ... \] Comprobar correo electrónico \[ ... \] "el motor de reconocimiento de voz coincidirá con frases como" Revise el correo "o" consulte correo electrónico "para este comando.</span><span class="sxs-lookup"><span data-stu-id="17742-127">For example, if you set this property to "\[...\] check mail \[...\]" the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="17742-128">Los puntos suspensivos se pueden usar en cualquier parte de una cadena.</span><span class="sxs-lookup"><span data-stu-id="17742-128">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="17742-129">Sin embargo, tenga cuidado al usar esta técnica, ya que la configuración de voz con puntos suspensivos puede aumentar el potencial de las coincidencias no deseadas.</span><span class="sxs-lookup"><span data-stu-id="17742-129">However, be careful using this technique, because voice settings with ellipses may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="17742-130">Al definir las palabras y la gramática del comando, asegúrese siempre de incluir al menos una palabra necesaria; es decir, evite proporcionar solo palabras opcionales.</span><span class="sxs-lookup"><span data-stu-id="17742-130">When defining the words and grammar for your command, always make sure that you include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="17742-131">Además, asegúrese de que la palabra solo incluye palabras y letras pronunciables.</span><span class="sxs-lookup"><span data-stu-id="17742-131">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="17742-132">En el caso de los números, es mejor deletrear la palabra en lugar de usar la representación numérica.</span><span class="sxs-lookup"><span data-stu-id="17742-132">For numbers, it is better to spell out the word rather than using the numeric representation.</span></span> <span data-ttu-id="17742-133">También puede omitir cualquier signo de puntuación o símbolos.</span><span class="sxs-lookup"><span data-stu-id="17742-133">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="17742-134">Por ejemplo, en lugar de " \# $1 10 pizza!", use el número 1 10 de la pizza de dólares.</span><span class="sxs-lookup"><span data-stu-id="17742-134">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="17742-135">La inclusión de símbolos o caracteres no pronunciables para un comando puede hacer que el motor de voz no pueda compilar la gramática de todos los comandos.</span><span class="sxs-lookup"><span data-stu-id="17742-135">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="17742-136">Por último, haga que el parámetro de voz sea lo bastante distinto posible desde otros comandos de voz que defina.</span><span class="sxs-lookup"><span data-stu-id="17742-136">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="17742-137">Cuanto mayor sea la similitud entre la gramática de voz de los comandos, más probable será que el motor de voz haga un error de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="17742-137">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="17742-138">También puede usar las puntuaciones de confianza para distinguir mejor entre dos comandos que pueden tener una gramática de voz similar o similar.</span><span class="sxs-lookup"><span data-stu-id="17742-138">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="17742-139">La configuración de la propiedad [**Voice**](voice-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object) habilita automáticamente Speech Services del agente, lo que hace que la clave de escucha y la sugerencia de escucha estén disponibles.</span><span class="sxs-lookup"><span data-stu-id="17742-139">Setting the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) automatically enables Agent's speech services, making the Listening key and Listening Tip available.</span></span> <span data-ttu-id="17742-140">Sin embargo, no carga el motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="17742-140">However, it does not load the speech recognition engine.</span></span>

> [!Note]  
> <span data-ttu-id="17742-141">Las características de gramática disponibles pueden depender del motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="17742-141">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="17742-142">Puede que desee consultar con el proveedor del motor para determinar qué opciones de gramática se admiten.</span><span class="sxs-lookup"><span data-stu-id="17742-142">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="17742-143">Use [**IAgentCharacterEx:: SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) para especificar un motor.</span><span class="sxs-lookup"><span data-stu-id="17742-143">Use [**IAgentCharacterEx::SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) to specify an engine.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="17742-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="17742-144">See Also</span></span>

<span data-ttu-id="17742-145">[**IAgentCommand:: GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setEnabled**](iagentcommand--setenabled.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="17742-145">[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 