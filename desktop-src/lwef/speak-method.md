---
title: Método Speak
description: Método Speak
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88792a53fac80c68154f938e91fb9bfe63b2b8e3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487623"
---
# <a name="speak-method"></a><span data-ttu-id="51f8a-103">Método Speak</span><span class="sxs-lookup"><span data-stu-id="51f8a-103">Speak Method</span></span>

<span data-ttu-id="51f8a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="51f8a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="51f8a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="51f8a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="51f8a-106">Habla el archivo de texto o de sonido especificado para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="51f8a-106">Speaks the specified text or sound file for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="51f8a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="51f8a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="51f8a-108">\*agente ***. Caracteres ("*** CharacterID \* *").* \*  \[ *Texto* \] de voz, \[ *URL*\]</span><span class="sxs-lookup"><span data-stu-id="51f8a-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speak*\* \[*Text*\], \[*Url*\]</span></span>



| <span data-ttu-id="51f8a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="51f8a-109">Part</span></span>   | <span data-ttu-id="51f8a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="51f8a-110">Description</span></span>                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f8a-111">*Texto*</span><span class="sxs-lookup"><span data-stu-id="51f8a-111">*Text*</span></span> | <span data-ttu-id="51f8a-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="51f8a-112">Optional.</span></span> <span data-ttu-id="51f8a-113">Cadena que especifica lo que dice el carácter.</span><span class="sxs-lookup"><span data-stu-id="51f8a-113">A string that specifies what the character says.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="51f8a-114">*Url*</span><span class="sxs-lookup"><span data-stu-id="51f8a-114">*Url*</span></span>  | <span data-ttu-id="51f8a-115">Opcional.</span><span class="sxs-lookup"><span data-stu-id="51f8a-115">Optional.</span></span> <span data-ttu-id="51f8a-116">Expresión de cadena que especifica la ubicación de un archivo de audio (. WAV o. Formato LWV).</span><span class="sxs-lookup"><span data-stu-id="51f8a-116">A string expression specifying the location of an audio file (.WAV or .LWV format).</span></span> <span data-ttu-id="51f8a-117">La ubicación puede especificarse como un archivo (incluida una especificación de ruta de acceso UNC) o una dirección URL (cuando también se recuperan datos de animación de caracteres a través del protocolo HTTP).</span><span class="sxs-lookup"><span data-stu-id="51f8a-117">The location can be specified as a file (including a UNC path specification) or URL (when character animation data is also being retrieved via HTTP protocol).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51f8a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51f8a-118">Remarks</span></span>

<span data-ttu-id="51f8a-119">Aunque los parámetros *Text* y *URL* son opcionales, se debe proporcionar uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="51f8a-119">Although the *Text* and *Url* parameters are optional, one of them must be supplied.</span></span> <span data-ttu-id="51f8a-120">Para usar este método con un carácter configurado para hablar solo en su globo de palabras o mediante un motor de conversión de texto a voz (TTS), basta con proporcionar el parámetro de *texto* .</span><span class="sxs-lookup"><span data-stu-id="51f8a-120">To use this method with a character configured to speak only in its word balloon or using a text-to-speech (TTS) engine, simply provide the *Text* parameter.</span></span> <span data-ttu-id="51f8a-121">Incluya un espacio entre palabras para definir los saltos de palabra adecuados en el globo de palabras, incluso para los idiomas que tradicionalmente no incluyen espacios.</span><span class="sxs-lookup"><span data-stu-id="51f8a-121">Include a space between words to define appropriate word breaks in the word balloon, even for languages that do not traditionally include spaces.</span></span>

<span data-ttu-id="51f8a-122">También puede incluir caracteres de barra vertical ( \| ) en el parámetro *Text* para designar cadenas alternativas, de modo que el servidor elija aleatoriamente una cadena diferente cada vez que procese el método.</span><span class="sxs-lookup"><span data-stu-id="51f8a-122">You can also include vertical bar characters (\|) in the *Text* parameter to designate alternative strings, so that the server randomly chooses a different string each time it processes the method.</span></span>

<span data-ttu-id="51f8a-123">La compatibilidad con caracteres de la salida de TTS se define cuando el carácter se compila mediante el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="51f8a-123">Character support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="51f8a-124">Para generar la salida de TTS, un motor TTS compatible ya debe estar instalado antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="51f8a-124">To generate TTS output, a compatible TTS engine must already be installed before calling this method.</span></span> <span data-ttu-id="51f8a-125">Para obtener más información, consulte [acceso a servicios de voz](accessing-speech-services.md).</span><span class="sxs-lookup"><span data-stu-id="51f8a-125">For further information, see [Accessing Speech Services](accessing-speech-services.md).</span></span>

<span data-ttu-id="51f8a-126">Si utiliza el archivo de sonido grabado (. WAV o. Solo formato de LWV) para el carácter, especifique la ubicación del archivo en el parámetro *URL* .</span><span class="sxs-lookup"><span data-stu-id="51f8a-126">If you use recorded sound-file (.WAV or .LWV format only) output for the character, specify the file's location in the *Url* parameter.</span></span> <span data-ttu-id="51f8a-127">Esta especificación de archivo puede incluir una ruta de acceso UNC (Convención de nomenclatura universal) o local (absoluta o relativa).</span><span class="sxs-lookup"><span data-stu-id="51f8a-127">This file specification can include a local (absolute or relative) or universal naming convention (UNC) path.</span></span> <span data-ttu-id="51f8a-128">El nombre de archivo no puede incluir caracteres no incluidos en la página de códigos de EE. UU. 1252.</span><span class="sxs-lookup"><span data-stu-id="51f8a-128">The filename cannot include any characters not included in the US code page 1252.</span></span> <span data-ttu-id="51f8a-129">Sin embargo, si usa el protocolo HTTP para tener acceso a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar la animación antes de llamar al método **Speak** .</span><span class="sxs-lookup"><span data-stu-id="51f8a-129">However, if you are using the HTTP protocol to access the character animation data, use the [**Get**](get-method.md) method to load the animation before calling the **Speak** method.</span></span> <span data-ttu-id="51f8a-130">Consulte [uso de la herramienta de edición de sonido lingüístico de Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) para obtener información sobre Creative. Archivos LWV.</span><span class="sxs-lookup"><span data-stu-id="51f8a-130">See [Using the Microsoft Linguistic Information Sound Editing Tool](using-the-microsoft-linguistic-information-sound-editing-tool.md) for information about creative .LWV files.</span></span>

<span data-ttu-id="51f8a-131">Al utilizar la salida de archivo de sonido grabada, todavía puede usar el parámetro de *texto* para especificar las palabras que aparecen en el globo de palabras del carácter.</span><span class="sxs-lookup"><span data-stu-id="51f8a-131">When using recorded sound-file output, you can still use the *Text* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="51f8a-132">Sin embargo, si especifica un archivo de sonido lingüísticamente mejorado (. LWV) para el parámetro *URL* y no especifica texto para el globo de palabras, el parámetro de *texto* usa el texto almacenado en el archivo.</span><span class="sxs-lookup"><span data-stu-id="51f8a-132">However, if you specify a linguistically enhanced sound file (.LWV) for the *Url* parameter and do not specify text for the word balloon, the *Text* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="51f8a-133">También puede modificar los parámetros de la salida de voz con etiquetas especiales que incluya en el parámetro de *texto* .</span><span class="sxs-lookup"><span data-stu-id="51f8a-133">You can also vary parameters of the speech output with special tags that you include in the *Text* parameter.</span></span> <span data-ttu-id="51f8a-134">Para obtener más información, consulte [etiquetas de salida de voz del agente de Microsoft](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="51f8a-134">For more information, see [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

<span data-ttu-id="51f8a-135">Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="51f8a-135">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="51f8a-136">Puede utilizar esto para sincronizar otras partes del código con la salida de voz del carácter, como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="51f8a-136">You can use this to synchronize other parts of your code with the character's spoken output, as in the following example:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



<span data-ttu-id="51f8a-137">También puede usar un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) para comprobar ciertas condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="51f8a-137">You can also use a [**Request**](/windows/desktop/lwef/the-request-object) object to check for certain error conditions.</span></span> <span data-ttu-id="51f8a-138">Por ejemplo, si usa el método **Speak** para hablar y no tiene instalado un motor TTS compatible, el servidor establece la propiedad [**status**](status-property.md) del objeto **request** en "Failed" con su propiedad [**Description**](description-property.md) en "clase no registrada" o "desconocido o el objeto devolvió un error".</span><span class="sxs-lookup"><span data-stu-id="51f8a-138">For example, if you use the **Speak** method to speak and do not have a compatible TTS engine installed, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with its [**Description**](description-property.md) property to "Class not registered" or "Unknown or object returned error".</span></span> <span data-ttu-id="51f8a-139">Para determinar si tiene un motor de TTS instalado, utilice la propiedad [**TTSModeID**](ttsmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="51f8a-139">To determine if you have a TTS engine installed, use the [**TTSModeID**](ttsmodeid-property.md) property.</span></span>

<span data-ttu-id="51f8a-140">Del mismo modo, si tiene el carácter intentando hablar de un archivo de sonido, y si el archivo no se ha cargado o hay un problema con el dispositivo de audio, el servidor también establece la propiedad [**status**](status-property.md) del objeto [**request**](/windows/desktop/lwef/the-request-object) en "Failed" con un número de código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="51f8a-140">Similarly, if you have the character attempt to speak a sound file, and if the file has not been loaded or there is a problem with the audio device, the server also sets the [**Request**](/windows/desktop/lwef/the-request-object) object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="51f8a-141">También puede incluir etiquetas de voz de marcador en el texto de habla para sincronizar el código:</span><span class="sxs-lookup"><span data-stu-id="51f8a-141">You can also include bookmark speech tags in your Speak text to synchronize your code:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



<span data-ttu-id="51f8a-142">Para obtener más información sobre la etiqueta de voz de marcador, consulte [etiquetas de salida de voz](mrk-tag.md).</span><span class="sxs-lookup"><span data-stu-id="51f8a-142">For more information on the bookmark speech tag, see [Speech Output Tags](mrk-tag.md).</span></span>

<span data-ttu-id="51f8a-143">El método **Speak** usa la última acción reproducida para determinar qué animación de habla reproducir.</span><span class="sxs-lookup"><span data-stu-id="51f8a-143">The **Speak** method uses the last action played to determine which speaking animation to play.</span></span> <span data-ttu-id="51f8a-144">Por ejemplo, si precedía el comando **Speak** con una [**reproducción**](play-method.md) "**GestureRight**", el servidor reproducirá **GestureRight** y, a continuación, la animación **GestureRight** Speaking.</span><span class="sxs-lookup"><span data-stu-id="51f8a-144">For example, if you preceded the **Speak** command with a [**Play**](play-method.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="51f8a-145">Si la última animación reproducida no tiene ninguna animación en voz, el agente reproduce la animación asignada al estado **hablando** del carácter.</span><span class="sxs-lookup"><span data-stu-id="51f8a-145">If the last animation played has no speaking animation, Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="51f8a-146">Si llama a **Speak** y el canal de audio está ocupado, no se escuchará la salida de audio del carácter, pero el texto se mostrará en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="51f8a-146">If you call **Speak** and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span>

<span data-ttu-id="51f8a-147">La separación de palabras automática del agente en el globo de palabras rompe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio o tabulación).</span><span class="sxs-lookup"><span data-stu-id="51f8a-147">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="51f8a-148">Sin embargo, si no es posible, puede romper una palabra para ajustarse al globo.</span><span class="sxs-lookup"><span data-stu-id="51f8a-148">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="51f8a-149">En idiomas como el japonés, el chino y el tailandés, donde los espacios no se usan para romper palabras, inserte un carácter de espacio de cero (0x200B) de Unicode entre caracteres para definir los saltos de palabra lógicos.</span><span class="sxs-lookup"><span data-stu-id="51f8a-149">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="51f8a-150">La propiedad [**Enabled**](enabled-property.md) del globo de palabra también debe ser **true** para que el texto se muestre.</span><span class="sxs-lookup"><span data-stu-id="51f8a-150">The word balloon's [**Enabled**](enabled-property.md) property must also be **True** for text to display.</span></span>

 

> [!Note]  
> <span data-ttu-id="51f8a-151">Establezca el identificador de idioma del carácter (estableciendo el valor de la función **LanguageID** del carácter antes de usar el método **Speak** para garantizar la presentación de texto adecuada en el globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="51f8a-151">Set the character's language ID (by setting the character's **LanguageID** before using the **Speak** method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="51f8a-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="51f8a-152">See Also</span></span>

<span data-ttu-id="51f8a-153">[**Evento Bookmark**](bookmark-event.md), [**evento RequestStart**](requeststart-event.md), [**evento RequestComplete**](requestcomplete-event.md)</span><span class="sxs-lookup"><span data-stu-id="51f8a-153">[**Bookmark event**](bookmark-event.md), [**RequestStart event**](requeststart-event.md), [**RequestComplete event**](requestcomplete-event.md)</span></span>


 

 