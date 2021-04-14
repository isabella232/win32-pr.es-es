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
# <a name="iagentcharacterspeak"></a>IAgentCharacter:: Speak

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Habla el archivo de texto o de sonido.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Texto que el carácter va a hablar.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

Dirección URL (o especificación de archivo) de un archivo de sonido que se va a utilizar para la salida de voz. Puede tratarse de un archivo de sonido estándar (. WAV) o un archivo de sonido mejorado lingüísticamente (. LWV).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud de [**voz**](/windows/desktop/lwef/iagentcharacter--speak) .

</dd> </dl>

Para usar este método con un carácter configurado para hablar con un motor de conversión de texto a voz (TTS); simplemente proporcione el parámetro *bszText* . Puede incluir caracteres de barra vertical ( \| ) en el parámetro *bszText* para designar cadenas alternativas, de modo que cada vez que el servidor procese el método, elija aleatoriamente una cadena diferente. La compatibilidad con la salida de TTS se define cuando el carácter se compila mediante el editor de caracteres del agente de Microsoft.

Si desea utilizar la salida de archivo de sonido para el carácter, especifique la ubicación del archivo en el parámetro *bszURL* . Al utilizar el protocolo HTTP para descargar un archivo de sonido, use el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad del archivo antes de usar este método. Puede usar el parámetro *bszText* para especificar las palabras que aparecen en el globo de palabras del carácter. Si especifica un archivo de sonido lingüísticamente mejorado (. LWV) para el parámetro *bszURL* y no especifica texto, el parámetro *bszText* usa el texto almacenado en el archivo.

El método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa la última animación reproducida para determinar qué animación de habla reproducir. Por ejemplo, si antepone el comando **Speak** con un [**IAgentCharacter::P**](iagentcharacter--play.md) "**GestureRight**", el servidor reproducirá **GestureRight** y, a continuación, la animación **GestureRight** Speaking. Si la última animación reproducida no tiene ninguna animación en voz, el agente de Microsoft reproduce la animación asignada al estado **hablando** del carácter.

Si llama a [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) y el canal de audio está ocupado, no se escuchará la salida de audio del carácter, pero el texto se mostrará en el globo de palabras. La propiedad [Enabled](enabled-property.md) del globo de palabra también debe ser **true** para que el texto se muestre.

La separación de palabras automáticas de Microsoft Agent en el globo de palabras, divide las palabras con caracteres de espacio en blanco (por ejemplo, espacio y tabulación). Sin embargo, puede dividir una palabra en el globo también. En idiomas como el japonés, el chino y el tailandés, donde no se usan espacios para romper palabras, inserte un carácter de espacio de ancho cero de Unicode (0x200B) entre los caracteres para definir los saltos de palabra lógicos.

> [!Note]  
> Establezca el identificador de idioma del carácter (mediante [**IAgentCharacterEx:: SetLanguageID**](iagentcharacterex--setlanguageid.md) antes de usar el método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) para garantizar la presentación de texto adecuada en el globo de palabras.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::P establecer**](iagentcharacter--play.md), [**IAgentBalloon:: GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::P**](iagentcharacter--prepare.md) redondear


 

 