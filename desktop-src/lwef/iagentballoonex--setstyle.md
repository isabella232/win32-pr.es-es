---
title: IAgentBalloonEx SetStyle
description: IAgentBalloonEx SetStyle
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d942cc8adaf454a7c5f1cd299581f917560c00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704815"
---
# <a name="iagentballoonexsetstyle"></a>IAgentBalloonEx:: SetStyle

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

Recupera la configuración de estilo de globo de palabras del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*
</dt> <dd>

Configuración de estilo para el globo de palabras, que puede ser una combinación de cualquiera de los valores siguientes:



| Value                                                                            | Descripción                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| constante de estilo de globo **corto sin signo de const** **\_ \_ = 0x00000001;**<br/>  | El globo es compatible con la salida.                        |
| **const unsigned short** **Balloon \_ style \_ SIZETOTEXT = 0x0000002;**<br/> | El alto del globo tiene el tamaño adecuado para la salida de texto. |
| tipo de globo **corto sin signo const** **\_ \_ Ocultar automáticamente = 0x00000004;**<br/>  | El globo se oculta automáticamente.                        |
| tipo de globo **corto sin signo const** **\_ \_ autopace = 0x00000008;**<br/>  | La salida de texto se acelera según la tasa de salida.          |



 

</dd> </dl>

Cuando se establece el bit de estilo de **globoon** , el globo de palabras aparece cuando se usa el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) , a menos que el usuario invalide su presentación en la hoja de propiedades del agente de Microsoft. Cuando no se establece, no aparece ningún globo.

Cuando se establece el bit de estilo **SizeToText** , el globo de palabras ajusta automáticamente el alto del globo al tamaño actual del texto especificado en el método [**Speak**](speak-method.md) o [**piénselo**](think-method.md) . Cuando no se establece, el alto del globo se basa en el valor de la propiedad número de líneas del globo. Este bit de estilo se establece en 1 y un intento de usar [**IAgentBalloonEx:: SetNumLines**](iagentballoonex--setnumlines.md) producirá un error.

Cuando se establece el bit de estilo de **ocultación** automática, el globo de palabras se oculta automáticamente tras un breve tiempo de espera. Cuando no se establece, el globo se muestra hasta una nueva llamada de [**voz**](speak-method.md) o de [**reflexión**](think-method.md) , el carácter está oculto o el usuario hace clic o arrastra el carácter.

Cuando se establece el bit de estilo **autopace** , el globo de palabras acelera la salida en función de la tasa de salida actual, por ejemplo, una palabra a la vez. Cuando la salida supera el tamaño del globo, el texto anterior se desplaza automáticamente. Cuando no se establece, todo el texto incluido en una instrucción [**Speak**](speak-method.md) o de [**reflexión**](think-method.md) se muestra a la vez.

La propiedad de estilo del globo se puede establecer incluso si el usuario ha deshabilitado la presentación del globo mediante la hoja de propiedades de Microsoft Agent.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los valores predeterminados para estos bits de estilo se basan en su configuración cuando el carácter se compila con el editor de caracteres del agente de Microsoft.

## <a name="see-also"></a>Consulte también

[**IAgentBalloonEx:: GetStyle**](iagentballoonex--getstyle.md)


 

 





