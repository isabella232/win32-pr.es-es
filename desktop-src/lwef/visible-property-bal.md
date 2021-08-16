---
title: Propiedad Visible (objeto Globo)
description: Obtenga información sobre la propiedad Visible del objeto Globo, que devuelve o establece el valor visible para el globo de palabras para el carácter especificado.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101d454f90e01ebcf31619b935d1b90512648baf33a11883b6b971c3178fb871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975485"
---
# <a name="visible-property-balloon-object"></a>Propiedad Visible (objeto Globo)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el valor visible para el globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Booleano Balloon.Visible* *  \[  =  \]



| Parte      | Descripción                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si la palabra globo está visible.<br/> **True** El globo está visible.<br/> **False** El globo está oculto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si sigue [](speak-method.md) una llamada a Speak o [**Think**](think-method.md) con una instrucción para intentar cambiar la propiedad del globo, es posible que no afecte al estado Visible del globo porque la llamada **Speak** o **Think** se pone en cola, pero la llamada que establece el estado visible del globo no. Por lo tanto, establezca este valor solo cuando no haya ninguna llamada **a Speak** o **Think** en la cola del carácter.

Si intenta establecer esta propiedad mientras el carácter habla, se mueve o se arrastra, el valor de la propiedad no tendrá efecto hasta que se complete la operación anterior.

Llamar a [**los métodos Speak**](speak-method.md) y [**Think**](think-method.md) hace que el globo sea visible automáticamente, estableciendo la [**propiedad Visible**](visible-property.md) en **True.** Si la propiedad AutoHide del globo del carácter está habilitada, el globo se oculta automáticamente después de que se habla el texto de salida. Al hacer clic o arrastrar un carácter que no está hablando actualmente, también se oculta automáticamente el globo incluso si su configuración Detección automática está deshabilitada. Puede cambiar la configuración de AutoHide del carácter mediante la propiedad [**Style del**](style-property.md) globo.

### <a name="see-also"></a>Consulte también

[**Propiedad Style**](style-property.md)


 

 





