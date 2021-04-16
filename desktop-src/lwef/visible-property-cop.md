---
title: Propiedad visible (objeto Command)
description: Propiedad visible
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714505"
---
# <a name="visible-property-command-object"></a>Propiedad visible (objeto Command)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece si el [**comando**](/windows/desktop/lwef/the-command-object) está visible en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica** 
</dt> <dd>

*agente ***. Caracteres (**"* CharacterID *"**). Comandos (**"* name *" * *).* *  \[  =  *Booleano* visible\]



| Parte      | Descripción                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Una expresión booleana que especifica si el título del [**comando**](/windows/desktop/lwef/the-command-object)aparece en el menú emergente del carácter.<br/> **True** (valor predeterminado) aparece el título.<br/> **False** El título no aparece.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Establezca esta propiedad en **false** si desea incluir la entrada de voz para sus propias interfaces sin que aparezcan en el menú emergente del carácter. Si establece la propiedad [**título**](caption-property.md) de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en la cadena vacía (""), el texto del título no aparecerá en el menú emergente (por ejemplo, como una línea en blanco), independientemente de su configuración de propiedad [**visible**](visible-property.md) .

El valor de la propiedad [**visible**](visible-property.md) de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) primarios de un objeto [**Command**](/windows/desktop/lwef/the-command-object) no afecta al valor de la propiedad **visible** del **comando**.

 

