---
title: Propiedad visible (objeto Characters)
description: Propiedad visible
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695812"
---
# <a name="visible-property-characters-object"></a>Propiedad visible (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve un valor booleano que indica si el carácter está visible.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica** 
</dt> <dd>

*agente ***. Caracteres (**"* CharacterID *" * *). Visible**



| Value | Descripción                            |
|-------|----------------------------------------|
| True  | Se muestra el carácter.            |
| False | El carácter está oculto (no es visible). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad indica si se muestra el fotograma del carácter. No significa necesariamente que haya una imagen en la pantalla. Por ejemplo, esta propiedad devuelve **true** incluso cuando el carácter se coloca fuera del área de visualización visible o cuando el marco de carácter actual no contiene ninguna imagen. La configuración de esta propiedad se aplica a todos los clientes del carácter.

Esta propiedad es de solo lectura. Para hacer que un carácter esté visible u oculto, use los métodos [**Mostrar**](show-method.md) u [**ocultar**](https://www.bing.com/search?q=**Hide**) .

 

 




