---
title: Propiedad Visible (objeto Characters)
description: Obtenga información sobre la propiedad Visible del objeto Characters, que devuelve un valor booleano que indica si el carácter está visible.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78cce163e7ddfa8af3bf9198cd08bbb42be127745ed419a2f487aac6a1b7f287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882236"
---
# <a name="visible-property-characters-object"></a>Propiedad Visible (objeto Characters)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve un valor booleano que indica si el carácter está visible.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Visible**



| Valor | Descripción                            |
|-------|----------------------------------------|
| True  | Se muestra el carácter .            |
| Falso | El carácter está oculto (no visible). |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta propiedad indica si se muestra el marco del carácter. No significa necesariamente que haya una imagen en la pantalla. Por ejemplo, esta propiedad devuelve **True** incluso cuando el carácter se coloca fuera del área de visualización visible o cuando el marco de caracteres actual no contiene imágenes. La configuración de esta propiedad se aplica a todos los clientes del carácter.

Esta propiedad es de solo lectura. Para que un carácter sea visible u oculto, use los [**métodos Show**](show-method.md) [**u Hide.**](https://www.bing.com/search?q=**Hide**)

 

 




