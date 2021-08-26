---
title: IAgentCharacter Speak
description: IAgentCharacter Speak
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693b40a00b34173976410391249d3fac1a7f0684e34a6e2ae82afbd8b8169ce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014218"
---
# <a name="iagentcharacterspeak"></a>IAgentCharacter::Speak

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Habla el archivo de texto o sonido.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Texto que el carácter va a hablar.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

Dirección URL (o especificación de archivo) de un archivo de sonido que se usará para la salida hablada. Puede ser un archivo de sonido estándar (. WAV) o archivo de sonido mejorado lingüísticamente (. LWV).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador [**de solicitud speak.**](/windows/desktop/lwef/iagentcharacter--speak)

</dd> </dl>

Para usar este método con un carácter configurado para hablar mediante un motor de texto a voz (TTS); simplemente proporcione el *parámetro bszText.* Puede incluir caracteres de barra vertical ( ) en el parámetro \| *bszText* para designar cadenas alternativas, de modo que cada vez que el servidor procese el método, elija aleatoriamente una cadena diferente. La compatibilidad con la salida de TTS se define cuando el carácter se compila mediante el Editor de caracteres de Microsoft Agent.

Si desea usar la salida de archivo de sonido para el carácter, especifique la ubicación del archivo en el *parámetro bszURL.* Cuando use el protocolo HTTP para descargar un archivo de sonido, use el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad del archivo antes de usar este método. Puede usar el *parámetro bszText para* especificar las palabras que aparecen en el globo de palabras del carácter. Si especifica un archivo de sonido mejorado lingüísticamente (. LWV) para el *parámetro bszURL* y no especifica texto, el *parámetro bszText* usa el texto almacenado en el archivo.

El [**método Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa la última animación que se reproduce para determinar qué animación de habla se va a reproducir. Por ejemplo, si precede el comando **Speak** con un [**IAgentCharacter::P lay**](iagentcharacter--play.md) "**GestureRight",** el servidor reproducirá **GestureRight** y, a continuación, la animación de habla **GestureRight.** Si la última animación reproducido no tiene animación de habla, Microsoft Agent reproduce la animación asignada al estado **De habla del** carácter.

Si llama a [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) y el canal de audio está ocupado, la salida de audio del carácter no se escuchará, pero el texto se mostrará en el globo de palabras. La propiedad Enabled del [globo de](enabled-property.md) palabras también debe ser **True** para que se muestre el texto.

La separación automática de palabras de Microsoft Agent en el globo de palabras interrumpe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio y tabulación). Sin embargo, también puede interrumpir una palabra para ajustarse al globo. En idiomas como japonés, chino y tailandés, donde los espacios no se usan para interrumpir palabras, inserte un carácter de espacio de ancho cero Unicode (0x200B) entre caracteres para definir saltos de palabras lógicos.

> [!Note]  
> Establezca el identificador de idioma del carácter (mediante [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) antes de usar el método [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) para garantizar la presentación adecuada del texto dentro del globo de palabras.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::P lay**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md)


 

 