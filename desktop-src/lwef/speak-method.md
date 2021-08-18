---
title: Método Speak
description: Método Speak
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8798809dc4cdfa38438bee2fa9449f879871e4018b0e6b046d95a73583b03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475347"
---
# <a name="speak-method"></a>Método Speak

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Habla el archivo de texto o sonido especificado para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Speak_ *  \[ *Text* \] , \[ *Url*\]



| Parte   | Descripción                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Texto* | Opcional. Cadena que especifica lo que dice el carácter.                                                                                                                                                                                                   |
| *Url*  | Opcional. Expresión de cadena que especifica la ubicación de un archivo de audio (. WAV o . FORMATO LWV). La ubicación se puede especificar como un archivo (incluida una especificación de ruta de acceso UNC) o una dirección URL (cuando los datos de animación de caracteres también se recuperan a través del protocolo HTTP). |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Aunque los *parámetros Text* *y Url* son opcionales, se debe proporcionar uno de ellos. Para usar este método con un carácter configurado para hablar solo en su globo de palabras o mediante un motor de texto a voz (TTS), basta con proporcionar el *parámetro Text.* Incluya un espacio entre palabras para definir los saltos de palabras adecuados en el globo de palabras, incluso para los idiomas que tradicionalmente no incluyen espacios.

También puede incluir caracteres de barra vertical ( ) en el parámetro Text para designar cadenas alternativas, de modo que el servidor elija aleatoriamente una cadena diferente cada vez que \| procese  el método.

La compatibilidad con caracteres de la salida de TTS se define cuando el carácter se compila mediante el Editor de caracteres del Agente de Microsoft. Para generar la salida de TTS, ya debe instalarse un motor de TTS compatible antes de llamar a este método. Para más información, consulte [Acceso a servicios de Voz.](accessing-speech-services.md)

Si usa un archivo de sonido grabado (. WAV o . Solo formato LWV) para el carácter, especifique la ubicación del archivo en el *parámetro Url.* Esta especificación de archivo puede incluir una ruta de acceso local (absoluta o relativa) o una convención de nomenclatura universal (UNC). El nombre de archivo no puede incluir ningún carácter que no se incluya en la página de códigos de EE. UU. 1252. Sin embargo, si usa el protocolo HTTP para acceder a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar la animación antes de llamar al **método Speak.** Consulte Using the Microsoft Linguistic Information Sound Editing Tool (Uso de la herramienta de edición de sonido de información [lingüística de Microsoft)](using-the-microsoft-linguistic-information-sound-editing-tool.md) para obtener información sobre la creación. Archivos LWV.

Al usar la salida del archivo de sonido grabado, todavía puede usar el parámetro *Text* para especificar las palabras que aparecen en el globo de palabras del carácter. Sin embargo, si especifica un archivo de sonido mejorado lingüísticamente (. LWV) para el parámetro *Url* y no especifica texto para la palabra globo, el *parámetro Text* usa el texto almacenado en el archivo.

También puede variar los parámetros de la salida de voz con etiquetas especiales que incluya en el *parámetro Text.* Para obtener más información, vea [Etiquetas de salida de voz de Microsoft Agent](microsoft-agent-speech-output-tags.md).

Si declara una referencia de objeto y la establece en este método, devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object) Puede usarlo para sincronizar otras partes del código con la salida hablada del carácter, como en el ejemplo siguiente:


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



También puede usar un objeto [**Request**](/windows/desktop/lwef/the-request-object) para comprobar si hay determinadas condiciones de error. Por ejemplo, si usa el método **Speak** para hablar y no tiene instalado  un motor [](status-property.md) TTS compatible, el servidor establece la propiedad Status del objeto Request en "failed" con su propiedad [**Description**](description-property.md) en "Class not registered" o "Unknown or object returned error". Para determinar si tiene un motor de TTS instalado, use la [**propiedad TTSModeID.**](ttsmodeid-property.md)

Del mismo modo, si el carácter intenta hablar un archivo de sonido y si el archivo no se ha [](/windows/desktop/lwef/the-request-object) cargado o [](status-property.md) hay un problema con el dispositivo de audio, el servidor también establece la propiedad Estado del objeto Solicitud en "error" con un número de código de error adecuado.

También puede incluir etiquetas de voz de marcador en el texto de voz para sincronizar el código:


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



Para obtener más información sobre la etiqueta de voz de marcador, vea [Etiquetas de salida de voz.](mrk-tag.md)

El **método Speak** usa la última acción que se reproduce para determinar qué animación de habla se va a reproducir. Por ejemplo, si antecedió el comando **Speak** con un objeto [**Play**](play-method.md) "**GestureRight",** el servidor reproducirá **GestureRight** y, a continuación, la animación de habla **GestureRight.** Si la última animación reproducido no tiene animación de habla, el Agente reproduce la animación asignada al estado **De habla del** carácter.

Si llama a **Speak** y el canal de audio está ocupado, la salida de audio del carácter no se escuchará, pero el texto se mostrará en el globo de palabras.

La separación automática de palabras del agente en el globo de palabras interrumpe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio o tabulación). Sin embargo, si no es posible, puede interrumpir una palabra para ajustarse al globo. En idiomas como japonés, chino y tailandés, donde los espacios no se usan para interrumpir palabras, inserte un carácter de espacio de ancho cero Unicode (0x200B) entre caracteres para definir saltos de palabras lógicos.

> [!Note]  
> La propiedad Enabled del [**globo de**](enabled-property.md) palabras también debe ser **True para** que se muestre el texto.

 

> [!Note]  
> Establezca el identificador de idioma del carácter (estableciendo el **LanguageID** del carácter antes de usar el método **Speak** para garantizar la presentación adecuada del texto en el globo de palabras.

 

## <a name="see-also"></a>Consulte también

[**Bookmark event**](bookmark-event.md), [**RequestStart event**](requeststart-event.md), [**RequestComplete event**](requestcomplete-event.md)


 

 