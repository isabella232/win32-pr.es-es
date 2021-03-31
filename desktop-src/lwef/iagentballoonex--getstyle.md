---
title: IAgentBalloonEx GetStyle
description: IAgentBalloonEx GetStyle
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903665"
---
# <a name="iagentballoonexgetstyle"></a>IAgentBalloonEx:: GetStyle

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

Recupera la configuración de estilo de globo de palabras del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*
</dt> <dd>

Configuración de estilo para el globo de palabras, que puede ser una combinación de cualquiera de los valores siguientes:



| Value                                                                           | Descripción                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| constante de estilo de globo **corto sin signo de const** **\_ \_ = 0x00000001;**<br/> | El globo es compatible con la salida.                        |
| **const unsigned short** **Balloon \_ style \_ SIZETOTEXT = 0x0000002;**           | El alto del globo tiene el tamaño adecuado para la salida de texto. |
| tipo de globo **corto sin signo const** **\_ \_ Ocultar automáticamente = 0x00000004;**            | El globo se oculta automáticamente.                        |
| tipo de globo **corto sin signo const** **\_ \_ autopace = 0x00000008;**            | La salida de texto se acelera según la tasa de salida.          |



 

</dd> </dl>

Cuando se establece el bit de estilo de **globoon** , el globo de palabras aparece cuando se usa el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) , a menos que el usuario invalide su presentación a través de la hoja de propiedades del agente de Microsoft. Cuando no se establece, no aparece ningún globo.

Cuando se establece el bit de estilo **SizeToText** , el globo de palabras ajusta automáticamente el alto del globo al tamaño actual del texto especificado en el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) . Cuando no se establece, el alto del globo se basa en el valor de la propiedad número de líneas del globo. Este bit de estilo se establece en 1 y un intento de usar [**IAgentBalloonEx:: SetNumLines**](iagentballoonex--setnumlines.md) producirá un error.

Cuando se establece el bit de estilo de **ocultación** automática, el globo de palabras se oculta automáticamente después de un tiempo de espera corto. Cuando no se establece, el globo se muestra hasta una nueva llamada de [**voz**](speak-method.md) o de [**reflexión**](think-method.md) , el carácter está oculto o el usuario hace clic o arrastra el carácter.

Cuando se establece el bit de estilo **autopace** , el globo de palabras acelera la salida en función de la tasa de salida actual, por ejemplo, una palabra a la vez. Cuando la salida supera el tamaño del globo, el texto anterior se desplaza automáticamente. Cuando no se establece, todo el texto incluido en una instrucción [**Speak**](speak-method.md) o de [**reflexión**](think-method.md) se muestra a la vez.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los valores predeterminados para estos bits de estilo se basan en la configuración cuando el carácter se compila mediante el editor de caracteres del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloonEx:: SetStyle**](iagentballoonex--setstyle.md)


 

 





