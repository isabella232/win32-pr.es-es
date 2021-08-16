---
title: Propiedad Top (objeto Characters)
description: Obtenga información sobre la propiedad Top (objeto Characters). Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bdc753bc287e1289b2a75633081c7b325d698a7fbe92ba495cc93662485d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474492"
---
# <a name="top-property-characters-object"></a>Propiedad Top (objeto Characters)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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

## <a name="remarks"></a>Comentarios

La **propiedad Top** siempre se expresa en píxeles, en relación con el origen de la pantalla (parte superior izquierda). La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.

Use el [**método MoveTo**](moveto-method.md) para cambiar la ubicación del carácter.

## <a name="see-also"></a>Consulte también

[**Propiedad Left**](left-property.md), [ **método MoveTo**](moveto-method.md)


 

 




