---
title: Propiedad Top (objeto Characters)
description: Obtenga información sobre la propiedad Top (objeto Characters). Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396350"
---
# <a name="top-property-characters-object"></a>Propiedad Top (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el borde superior del marco del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Valor_ *  \[  =  *superior*\]



| Parte    | Descripción                                             |
|---------|---------------------------------------------------------|
| *value* | Entero Long que especifica el borde superior del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **propiedad Top** siempre se expresa en píxeles, en relación con el origen de la pantalla (parte superior izquierda). La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.

Use el [**método MoveTo**](moveto-method.md) para cambiar la ubicación del carácter.

## <a name="see-also"></a>Consulte también

[**Left, propiedad**](left-property.md), [ **método MoveTo**](moveto-method.md)


 

 




