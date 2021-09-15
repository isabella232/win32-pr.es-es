---
title: Propiedad Visible (objeto Command)
description: Obtenga información sobre la propiedad Visible del objeto Command, que devuelve o establece si el comando está visible en el menú emergente del carácter.
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4efec1ad8a97d6412a560a81836273b93ebf2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568704"
---
# <a name="visible-property-command-object"></a>Propiedad Visible (objeto Command)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si el [**comando**](/windows/desktop/lwef/the-command-object) está visible en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Commands(**"* name *"**). Booleano* *  \[  =  *visible*\]



| Parte      | Descripción                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si [**el**](/windows/desktop/lwef/the-command-object)título del comando aparece en el menú emergente del carácter.<br/> **True** (valor predeterminado) Aparece el título.<br/> **False** El título no aparece.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Establezca esta propiedad en **False** cuando quiera incluir la entrada de voz para sus propias interfaces sin que aparezcan en el menú emergente del carácter. Si establece [](/windows/desktop/lwef/the-command-object) la propiedad [**Caption**](caption-property.md) de un objeto Command en la cadena vacía (""), el texto del título no aparecerá en el menú emergente (por ejemplo, como una línea en blanco), independientemente de su valor de propiedad [**Visible.**](visible-property.md)

El [**valor de**](visible-property.md) la propiedad Visible de la colección [**Commands**](/windows/desktop/lwef/the-command-object) primaria de un objeto [**Command**](/windows/desktop/lwef/the-commands-collection-object) no afecta al valor de propiedad **Visible** del **comando**.

 

