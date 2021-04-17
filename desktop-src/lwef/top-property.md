---
title: Propiedad top (objeto Characters)
description: Propiedad Top
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef724c7052ad1d9ba5cb51ea46ccd7647723ed32
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714515"
---
# <a name="top-property-characters-object"></a>Propiedad top (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el borde superior del marco del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_")._ *  \[  =  *Valor* superior\]



| Parte    | Descripción                                             |
|---------|---------------------------------------------------------|
| *value* | Entero largo que especifica el borde superior del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **Top** siempre se expresa en píxeles, en relación con el origen de la pantalla (superior izquierda). La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular que se usa cuando el carácter se compiló con el editor de caracteres del agente de Microsoft.

Utilice el método [**moveTo**](moveto-method.md) para cambiar la ubicación del carácter.

## <a name="see-also"></a>Consulte también

[**Propiedad Left**](left-property.md), [ **método moveTo**](moveto-method.md)


 

 




