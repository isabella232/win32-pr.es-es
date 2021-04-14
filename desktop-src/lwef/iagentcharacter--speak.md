---
title: IAgentCharacter Speak
description: IAgentCharacter Speak
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e290ab9037ee6f261445d4dfd00a206213cd26
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533154"
---
# <a name="iagentcharacterspeak"></a><span data-ttu-id="5a562-103">IAgentCharacter:: Speak</span><span class="sxs-lookup"><span data-stu-id="5a562-103">IAgentCharacter::Speak</span></span>

<span data-ttu-id="5a562-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a562-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="5a562-105">Habla el archivo de texto o de sonido.</span><span class="sxs-lookup"><span data-stu-id="5a562-105">Speaks the text or sound file.</span></span>

-   <span data-ttu-id="5a562-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5a562-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5a562-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="5a562-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="5a562-108">Texto que el carácter va a hablar.</span><span class="sxs-lookup"><span data-stu-id="5a562-108">The text the character is to speak.</span></span>

</dd> <dt>

<span data-ttu-id="5a562-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span><span class="sxs-lookup"><span data-stu-id="5a562-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span></span>
</dt> <dd>

<span data-ttu-id="5a562-110">Dirección URL (o especificación de archivo) de un archivo de sonido que se va a utilizar para la salida de voz.</span><span class="sxs-lookup"><span data-stu-id="5a562-110">The URL (or file specification) of a sound file to use for spoken output.</span></span> <span data-ttu-id="5a562-111">Puede tratarse de un archivo de sonido estándar (. WAV) o un archivo de sonido mejorado lingüísticamente (. LWV).</span><span class="sxs-lookup"><span data-stu-id="5a562-111">This can be a standard sound file (.WAV) or linguistically enhanced sound file (.LWV).</span></span>

</dd> <dt>

<span data-ttu-id="5a562-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="5a562-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="5a562-113">Dirección de una variable que recibe el identificador de solicitud de [**voz**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="5a562-113">Address of a variable that receives the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="5a562-114">Para usar este método con un carácter configurado para hablar con un motor de conversión de texto a voz (TTS); simplemente proporcione el parámetro *bszText* .</span><span class="sxs-lookup"><span data-stu-id="5a562-114">To use this method with a character configured to speak using a text-to-speech (TTS) engine; simply provide the *bszText* parameter.</span></span> <span data-ttu-id="5a562-115">Puede incluir caracteres de barra vertical ( \| ) en el parámetro *bszText* para designar cadenas alternativas, de modo que cada vez que el servidor procese el método, elija aleatoriamente una cadena diferente.</span><span class="sxs-lookup"><span data-stu-id="5a562-115">You can include vertical bar characters (\|) in the *bszText* parameter to designate alternative strings, so that each time the server processes the method, it randomly choose a different string.</span></span> <span data-ttu-id="5a562-116">La compatibilidad con la salida de TTS se define cuando el carácter se compila mediante el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a562-116">Support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="5a562-117">Si desea utilizar la salida de archivo de sonido para el carácter, especifique la ubicación del archivo en el parámetro *bszURL* .</span><span class="sxs-lookup"><span data-stu-id="5a562-117">If you want to use sound file output for the character, specify the location for the file in the *bszURL* parameter.</span></span> <span data-ttu-id="5a562-118">Al utilizar el protocolo HTTP para descargar un archivo de sonido, use el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad del archivo antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="5a562-118">When using the HTTP protocol to download a sound file, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the file before using this method.</span></span> <span data-ttu-id="5a562-119">Puede usar el parámetro *bszText* para especificar las palabras que aparecen en el globo de palabras del carácter.</span><span class="sxs-lookup"><span data-stu-id="5a562-119">You can use the *bszText* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="5a562-120">Si especifica un archivo de sonido lingüísticamente mejorado (. LWV) para el parámetro *bszURL* y no especifica texto, el parámetro *bszText* usa el texto almacenado en el archivo.</span><span class="sxs-lookup"><span data-stu-id="5a562-120">If you specify a linguistically enhanced sound file (.LWV) for the *bszURL* parameter and do not specify text, the *bszText* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="5a562-121">El método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa la última animación reproducida para determinar qué animación de habla reproducir.</span><span class="sxs-lookup"><span data-stu-id="5a562-121">The [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method uses the last animation played to determine which speaking animation to play.</span></span> <span data-ttu-id="5a562-122">Por ejemplo, si antepone el comando **Speak** con un [**IAgentCharacter::P**](iagentcharacter--play.md) "**GestureRight**", el servidor reproducirá **GestureRight** y, a continuación, la animación **GestureRight** Speaking.</span><span class="sxs-lookup"><span data-stu-id="5a562-122">For example, if you precede the **Speak** command with an [**IAgentCharacter::Play**](iagentcharacter--play.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="5a562-123">Si la última animación reproducida no tiene ninguna animación en voz, el agente de Microsoft reproduce la animación asignada al estado **hablando** del carácter.</span><span class="sxs-lookup"><span data-stu-id="5a562-123">If the last animation played has no speaking animation, then Microsoft Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="5a562-124">Si llama a [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) y el canal de audio está ocupado, no se escuchará la salida de audio del carácter, pero el texto se mostrará en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="5a562-124">If you call [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span> <span data-ttu-id="5a562-125">La propiedad [Enabled](enabled-property.md) del globo de palabra también debe ser **true** para que el texto se muestre.</span><span class="sxs-lookup"><span data-stu-id="5a562-125">The word balloon's [Enabled](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="5a562-126">La separación de palabras automáticas de Microsoft Agent en el globo de palabras, divide las palabras con caracteres de espacio en blanco (por ejemplo, espacio y tabulación).</span><span class="sxs-lookup"><span data-stu-id="5a562-126">Microsoft Agent's automatic word breaking in the word balloon, breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="5a562-127">Sin embargo, puede dividir una palabra en el globo también.</span><span class="sxs-lookup"><span data-stu-id="5a562-127">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="5a562-128">En idiomas como el japonés, el chino y el tailandés, donde no se usan espacios para romper palabras, inserte un carácter de espacio de ancho cero de Unicode (0x200B) entre los caracteres para definir los saltos de palabra lógicos.</span><span class="sxs-lookup"><span data-stu-id="5a562-128">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="5a562-129">Establezca el identificador de idioma del carácter (mediante [**IAgentCharacterEx:: SetLanguageID**](iagentcharacterex--setlanguageid.md) antes de usar el método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) para garantizar la presentación de texto adecuada en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="5a562-129">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5a562-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5a562-130">See Also</span></span>

<span data-ttu-id="5a562-131">[**IAgentCharacter::P establecer**](iagentcharacter--play.md), [**IAgentBalloon:: GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::P**](iagentcharacter--prepare.md) redondear</span><span class="sxs-lookup"><span data-stu-id="5a562-131">[**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md)</span></span>


 

 