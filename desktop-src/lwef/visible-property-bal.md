---
title: Propiedad visible (objeto Balloon)
description: Propiedad visible
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba58993a3328a4c99dbe7da43b43460f6048bf57
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078673"
---
# <a name="visible-property-balloon-object"></a>Propiedad visible (objeto Balloon)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el valor visible para el globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica** 
</dt> <dd>

*agente ***. Caracteres (**"* CharacterID *" * *). Balloon. visible* *  \[  =  *booleano*\]



| Parte      | Descripción                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Una expresión booleana que especifica si el globo de palabras está visible.<br/> **True** El globo está visible.<br/> **False** El globo está oculto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si sigue una llamada de [**hablar**](speak-method.md) o de [**reflexión**](think-method.md) con una instrucción para intentar cambiar la propiedad del globo, es posible que no afecte al estado visible del globo porque la llamada de **Speak** o **pensar** se pone en cola, pero la llamada que establece el estado visible del globo no. Por lo tanto, solo se establece este valor cuando no hay llamadas de **voz** o de **reflexión** en la cola del carácter.

Si intenta establecer esta propiedad mientras el carácter está hablando, moviendo o arrastrando, el valor de la propiedad no surtirá efecto hasta que se complete la operación anterior.

Llamar a los métodos [**Speak**](speak-method.md) y [**piénselo**](think-method.md) hace que el globo sea visible automáticamente, estableciendo la propiedad [**visible**](visible-property.md) en **true**. Si la propiedad AutoHide de globos del carácter está habilitada, el globo se oculta automáticamente una vez que se habla del texto de salida. Al hacer clic o arrastrar un carácter que no está hablando en ese momento, también se oculta automáticamente el globo incluso si su configuración de ocultación automática está deshabilitada. Puede cambiar la configuración de autoocultar del carácter mediante la propiedad de [**estilo**](style-property.md) del globo.

### <a name="see-also"></a>Consulte también

[**Propiedad de estilo**](style-property.md)


 

 





