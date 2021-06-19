---
title: Propiedad Width (objeto Characters)
description: Obtenga información sobre la propiedad Width del objeto Characters, que devuelve o establece el ancho del marco para el carácter especificado.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395131"
---
# <a name="width-property-characters-object"></a>Propiedad Width (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el ancho del marco para el carácter especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis** 
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Valor de_ *  \[ =  *ancho*\]



| Parte    | Descripción                                                |
|---------|------------------------------------------------------------|
| *value* | Entero Long que especifica el ancho del marco del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [**propiedad Width**](width-property.md) siempre se expresa en píxeles. La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.

 

 




