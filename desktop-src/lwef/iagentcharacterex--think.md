---
title: IAgentCharacterEx Think
description: IAgentCharacterEx Think
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a513a070104605df0cf3e0e722852a2b68d5845f4bcdb1ef6073954b3f9a18c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105443"
---
# <a name="iagentcharacterexthink"></a>IAgentCharacterEx::Think

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

Muestra el globo de palabras de reflexión del carácter con el texto especificado.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Texto que aparece en el globo de reflexión del carácter.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador **de solicitud think.**

</dd> </dl>

Al igual [**que el método IAgentCharacter::Speak,**](iagentcharacter--speak.md) el método **Think** es una solicitud en cola que muestra texto en un globo de palabras, salvo que las ideas se muestran en un globo de reflexión especial. El globo de reflexión solo admite la etiqueta de control de voz Bookmark **\\ (Mrk**) y omite cualquier otra etiqueta de control de voz. A **diferencia de IAgentCharacter::Speak,** el **método Think** no cambia el estado de animación del carácter.

La [**configuración de IAgentBalloon**](/windows/desktop/lwef/iagentballoon) también se aplica al estilo de apariencia del globo de reflexión. Por ejemplo, la propiedad Enabled del [**globo**](enabled-property.md) también debe ser **True** para que se muestre el texto.

La separación automática de palabras de Microsoft Agent en el globo de palabras interrumpe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio y tabulación). Sin embargo, también puede interrumpir una palabra para ajustarse al globo. En idiomas como japonés, chino y tailandés, donde los espacios no se usan para interrumpir palabras, inserte un carácter de espacio de ancho cero Unicode (0x200B) entre caracteres para definir saltos de palabras lógicos.

> [!Note]  
> Establezca el identificador de idioma del carácter (mediante [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) antes de usar el método [**IAgentCharacter::Speak**](iagentcharacter--speak.md) para garantizar la presentación adecuada del texto dentro del globo de palabras.

 

## <a name="see-also"></a>Consulte también

[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)


 

 