---
title: IAgentBalloonEx SetStyle
description: IAgentBalloonEx SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3961bf5f32aad10c662d9dc2943f32b60fad485621b5adce32e2036e6d2d4275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478545"
---
# <a name="iagentballoonexsetstyle"></a>IAgentBalloonEx::SetStyle

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

Recupera la configuración de estilo de globo de palabras del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*
</dt> <dd>

Configuración de estilo para el globo de palabras, que puede ser una combinación de cualquiera de los valores siguientes:



| Valor                                                                            | Descripción                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| **const unsigned short** **BALLOON STYLE \_ \_ BALLOONON = 0x00000001;**<br/>  | El globo se admite para la salida.                        |
| **const unsigned short** **BALLOON STYLE \_ \_ SIZETOTEXT = 0x0000002;**<br/> | El alto del globo tiene el tamaño para dar cabida a la salida de texto. |
| **const unsigned short** **BALLOON STYLE \_ \_ AUTOHIDE = 0x00000004;**<br/>  | El globo se oculta automáticamente.                        |
| **const unsigned short** **BALLOON STYLE \_ \_ AUTOPACE = 0x00000008;**<br/>  | La salida de texto se acelera en función de la velocidad de salida.          |



 

</dd> </dl>

Cuando se establece el bit de estilo **BalloonOn,** la palabra globo aparece cuando se usa el método [**Speak**](speak-method.md) o [**Think,**](think-method.md) a menos que el usuario invalide su presentación en la hoja de propiedades de Microsoft Agent. Cuando no se establece, no aparece ningún globo.

Cuando se establece el bit **de estilo SizeToText,** el globo de palabras ajusta automáticamente el tamaño del globo al tamaño actual del texto especificado en el método [**Speak**](speak-method.md) o [**Think.**](think-method.md) Cuando no se establece, el alto del globo se basa en el valor de propiedad número de líneas del globo. Este bit de estilo se establece en 1 y un intento de usar [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) producirá un error.

Cuando se establece el bit de estilo **AutoHide,** la palabra globo se oculta automáticamente después de un breve tiempo de espera. Cuando no se establece, el globo se muestra hasta una nueva llamada [**a Speak**](speak-method.md) o [**Think,**](think-method.md) el carácter está oculto o el usuario hace clic o arrastra el carácter.

Cuando se establece el bit de estilo **AutoPace,** la palabra globo marca el ritmo de la salida en función de la velocidad de salida actual, por ejemplo, una palabra a la vez. Cuando la salida supera el tamaño del globo, el texto anterior se desplaza automáticamente. Cuando no se establece, todo el texto incluido en una instrucción [**Speak**](speak-method.md) o [**Think**](think-method.md) se muestra a la vez.

La propiedad de estilo del globo se puede establecer incluso si el usuario ha deshabilitado la presentación del globo mediante la hoja de propiedades de Microsoft Agent.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los valores predeterminados de estos bits de estilo se basan en su configuración cuando el carácter se compila con el Editor de caracteres de Microsoft Agent.

## <a name="see-also"></a>Consulte también

[**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md)


 

 





