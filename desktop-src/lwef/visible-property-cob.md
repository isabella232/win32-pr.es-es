---
title: Propiedad Visible (objeto Characters)
description: Obtenga información sobre la propiedad Visible del objeto Characters, que devuelve un valor booleano que indica si el carácter está visible.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396310"
---
# <a name="visible-property-characters-object"></a>Propiedad Visible (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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
| False | El carácter está oculto (no visible). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad indica si se muestra el marco del carácter. No significa necesariamente que haya una imagen en la pantalla. Por ejemplo, esta propiedad devuelve **True** incluso cuando el carácter se coloca fuera del área de visualización visible o cuando el marco de caracteres actual no contiene imágenes. La configuración de esta propiedad se aplica a todos los clientes del carácter.

Esta propiedad es de solo lectura. Para que un carácter sea visible u oculto, use los [**métodos Show**](show-method.md) [**u Hide.**](https://www.bing.com/search?q=**Hide**)

 

 




