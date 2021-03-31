---
title: IAgentCharacterEx creer
description: IAgentCharacterEx creer
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077656"
---
# <a name="iagentcharacterexthink"></a>IAgentCharacterEx:: cree

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

Muestra el globo de palabra pensamiento del carácter con el texto especificado.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Texto que se va a mostrar en el globo de pensamiento del carácter.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud de **reflexión** .

</dd> </dl>

Al igual que el método [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) , el método de **reflexión** es una solicitud en cola que muestra texto en un globo de palabras, con la excepción de que las ideas se muestran en un globo de pensamiento especial. El globo de pensamiento solo admite la etiqueta de control de voz de marcador (**\\ MRK**) y omite cualquier otra etiqueta de control de voz. A diferencia de **IAgentCharacter:: Speak**, el método de **reflexión** no cambia el estado de animación del carácter.

La configuración de [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon) también se aplica al estilo de apariencia del globo de pensamiento. Por ejemplo, la propiedad [**Enabled**](enabled-property.md) del globo también debe ser **true** para que el texto se muestre.

La separación de palabras automática del agente de Microsoft en el globo de palabras rompe las palabras mediante caracteres de espacio en blanco (por ejemplo, espacio y tabulación). Sin embargo, puede dividir una palabra en el globo también. En idiomas como el japonés, el chino y el tailandés, donde no se usan espacios para romper palabras, inserte un carácter de espacio de ancho cero de Unicode (0x200B) entre los caracteres para definir los saltos de palabra lógicos.

> [!Note]  
> Establezca el identificador de idioma del carácter (mediante [**IAgentCharacterEx:: SetLanguageID**](iagentcharacterex--setlanguageid.md) antes de usar el método [**IAgentCharacter:: Speak**](iagentcharacter--speak.md) para garantizar la presentación de texto adecuada en el globo de palabras.

 

## <a name="see-also"></a>Consulte también

[**IAgentBalloon:: GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx:: setStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md)


 

 