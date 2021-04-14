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
# <a name="speak-method"></a>Método Speak

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Habla el archivo de texto o de sonido especificado para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *").* *  \[ *Texto* \] de voz, \[ *URL*\]



| Parte   | Descripción                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Texto* | Opcional. Cadena que especifica lo que dice el carácter.                                                                                                                                                                                                   |
| *Url*  | Opcional. Expresión de cadena que especifica la ubicación de un archivo de audio (. WAV o. Formato LWV). La ubicación puede especificarse como un archivo (incluida una especificación de ruta de acceso UNC) o una dirección URL (cuando también se recuperan datos de animación de caracteres a través del protocolo HTTP). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Aunque los parámetros *Text* y *URL* son opcionales, se debe proporcionar uno de ellos. Para usar este método con un carácter configurado para hablar solo en su globo de palabras o mediante un motor de conversión de texto a voz (TTS), basta con proporcionar el parámetro de *texto* . Incluya un espacio entre palabras para definir los saltos de palabra adecuados en el globo de palabras, incluso para los idiomas que tradicionalmente no incluyen espacios.

También puede incluir caracteres de barra vertical ( \| ) en el parámetro *Text* para designar cadenas alternativas, de modo que el servidor elija aleatoriamente una cadena diferente cada vez que procese el método.

La compatibilidad con caracteres de la salida de TTS se define cuando el carácter se compila mediante el editor de caracteres del agente de Microsoft. Para generar la salida de TTS, un motor TTS compatible ya debe estar instalado antes de llamar a este método. Para obtener más información, consulte [acceso a servicios de voz](accessing-speech-services.md).

Si utiliza el archivo de sonido grabado (. WAV o. Solo formato de LWV) para el carácter, especifique la ubicación del archivo en el parámetro *URL* . Esta especificación de archivo puede incluir una ruta de acceso UNC (Convención de nomenclatura universal) o local (absoluta o relativa). El nombre de archivo no puede incluir caracteres no incluidos en la página de códigos de EE. UU. 1252. Sin embargo, si usa el protocolo HTTP para tener acceso a los datos de animación de caracteres, use el método [**Get**](get-method.md) para cargar la animación antes de llamar al método **Speak** . Consulte [uso de la herramienta de edición de sonido lingüístico de Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) para obtener información sobre Creative. Archivos LWV.

Al utilizar la salida de archivo de sonido grabada, todavía puede usar el parámetro de *texto* para especificar las palabras que aparecen en el globo de palabras del carácter. Sin embargo, si especifica un archivo de sonido lingüísticamente mejorado (. LWV) para el parámetro *URL* y no especifica texto para el globo de palabras, el parámetro de *texto* usa el texto almacenado en el archivo.

También puede modificar los parámetros de la salida de voz con etiquetas especiales que incluya en el parámetro de *texto* . Para obtener más información, consulte [etiquetas de salida de voz del agente de Microsoft](microsoft-agent-speech-output-tags.md).

Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . Puede utilizar esto para sincronizar otras partes del código con la salida de voz del carácter, como en el ejemplo siguiente:


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



También puede usar un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) para comprobar ciertas condiciones de error. Por ejemplo, si usa el método **Speak** para hablar y no tiene instalado un motor TTS compatible, el servidor establece la propiedad [**status**](status-property.md) del objeto **request** en "Failed" con su propiedad [**Description**](description-property.md) en "clase no registrada" o "desconocido o el objeto devolvió un error". Para determinar si tiene un motor de TTS instalado, utilice la propiedad [**TTSModeID**](ttsmodeid-property.md) .

Del mismo modo, si tiene el carácter intentando hablar de un archivo de sonido, y si el archivo no se ha cargado o hay un problema con el dispositivo de audio, el servidor también establece la propiedad [**status**](status-property.md) del objeto [**request**](/windows/desktop/lwef/the-request-object) en "Failed" con un número de código de error adecuado.

También puede incluir etiquetas de voz de marcador en el texto de habla para sincronizar el código:


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



Para obtener más información sobre la etiqueta de voz de marcador, consulte [etiquetas de salida de voz](mrk-tag.md).

El método **Speak** usa la última acción reproducida para determinar qué animación de habla reproducir. Por ejemplo, si precedía el comando **Speak** con una [**reproducción**](play-method.md) "**GestureRight**", el servidor reproducirá **GestureRight** y, a continuación, la animación **GestureRight** Speaking. Si la última animación reproducida no tiene ninguna animación en voz, el agente reproduce la animación asignada al estado **hablando** del carácter.

Si llama a **Speak** y el canal de audio está ocupado, no se escuchará la salida de audio del carácter, pero el texto se mostrará en el globo de palabras.

La separación de palabras automática del agente en el globo de palabras rompe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio o tabulación). Sin embargo, si no es posible, puede romper una palabra para ajustarse al globo. En idiomas como el japonés, el chino y el tailandés, donde los espacios no se usan para romper palabras, inserte un carácter de espacio de cero (0x200B) de Unicode entre caracteres para definir los saltos de palabra lógicos.

> [!Note]  
> La propiedad [**Enabled**](enabled-property.md) del globo de palabra también debe ser **true** para que el texto se muestre.

 

> [!Note]  
> Establezca el identificador de idioma del carácter (estableciendo el valor de la función **LanguageID** del carácter antes de usar el método **Speak** para garantizar la presentación de texto adecuada en el globo de palabras.

 

## <a name="see-also"></a>Consulte también

[**Evento Bookmark**](bookmark-event.md), [**evento RequestStart**](requeststart-event.md), [**evento RequestComplete**](requestcomplete-event.md)


 

 