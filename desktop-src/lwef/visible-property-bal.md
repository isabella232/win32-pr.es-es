---
title: Propiedad Visible (objeto De globo)
description: Obtenga información sobre la propiedad Visible del objeto Globo, que devuelve o establece la configuración visible para el globo de palabras para el carácter especificado.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac587fa649f2a8ccb5ea83ddc077050a8548d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396330"
---
# <a name="visible-property-balloon-object"></a>Propiedad Visible (objeto De globo)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece la configuración visible para el globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Booleano Balloon.Visible* *  \[  =  \]



| Parte      | Descripción                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el globo de palabras está visible.<br/> **True** El globo está visible.<br/> **False** El globo está oculto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si sigue [](speak-method.md) una llamada a Speak o [**Think**](think-method.md) con una instrucción para intentar cambiar la propiedad del  globo, es posible que no afecte al estado Visible del globo porque la llamada Speak o **Think** se pone en cola, pero la llamada que establece el estado visible del globo no. Por lo tanto, establezca este valor solo cuando no haya llamadas **speak** o **think** en la cola del carácter.

Si intenta establecer esta propiedad mientras el carácter habla, se mueve o se arrastra, la configuración de la propiedad no tiene efecto hasta que se completa la operación anterior.

Llamar a [**los métodos Speak**](speak-method.md) y [**Think**](think-method.md) automáticamente hace que el globo sea visible, estableciendo la [**propiedad Visible**](visible-property.md) en **True.** Si la propiedad AutoHide del globo del carácter está habilitada, el globo se oculta automáticamente después de que se hable el texto de salida. Al hacer clic o arrastrar un carácter que no está hablando actualmente, también se oculta automáticamente el globo aunque su configuración Detección automática esté deshabilitada. Puede cambiar la configuración de AutoHide del carácter mediante la propiedad [**Style del**](style-property.md) globo.

### <a name="see-also"></a>Consulte también

[**Propiedad Style**](style-property.md)


 

 





