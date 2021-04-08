---
title: Propiedad width (objeto Characters)
description: Width (propiedad)
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078722"
---
# <a name="width-property-characters-object"></a>Propiedad width (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el ancho del marco para el carácter especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica** 
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_")._ *  \[ =  *Valor* de ancho\]



| Parte    | Descripción                                                |
|---------|------------------------------------------------------------|
| *value* | Entero largo que especifica el ancho del marco del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad [**ancho**](width-property.md) siempre se expresa en píxeles. La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, la ubicación del carácter se basa en las dimensiones externas del marco de animación rectangular que se usa cuando el carácter se compiló con el editor de caracteres del agente de Microsoft.

 

 




