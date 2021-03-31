---
title: Propiedad height (objeto Characters)
description: Height (propiedad)
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800643"
---
# <a name="height-property-characters-object"></a>Propiedad height (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el alto del fotograma del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_")._ *  \[ =  *Valor* de alto\]



| Parte    | Descripción                                                 |
|---------|-------------------------------------------------------------|
| *value* | Entero largo que especifica el alto del marco del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **height** siempre se expresa en píxeles, con respecto a las coordenadas de pantalla (superior izquierda). La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, el alto del carácter se basa en las dimensiones externas del marco de animación rectangular que se usa cuando el carácter se compiló con el editor de caracteres del agente de Microsoft.

 

 




