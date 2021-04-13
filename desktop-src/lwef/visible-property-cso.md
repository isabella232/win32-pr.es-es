---
title: Propiedad visible (objeto Commands)
description: Propiedad visible
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421853"
---
# <a name="visible-property-commands-object"></a>Propiedad visible (objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece un valor que determina si el título de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) aparece en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica** 
</dt> <dd>

*agente ***. Caracteres (**"* CharacterID *" * *). Commands. visible* *  \[  =  *Boolean*\]



| Parte      | Descripción                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) aparece en el menú emergente del carácter. <br/> **True** Aparece el título.<br/> **False** El título no aparece.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para que el título aparezca en el menú emergente del carácter cuando la aplicación no es el cliente de entrada-activo, esta propiedad debe establecerse en **true** y en la propiedad [**Caption**](caption-property.md) establecida para la colección de comandos. Además, esta propiedad debe establecerse en **true** para que los comandos de la colección aparezcan en el menú emergente cuando la aplicación sea de entrada-activa.

 

