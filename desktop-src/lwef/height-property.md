---
title: Propiedad Height (objeto Characters)
description: Obtenga información sobre la propiedad Height del objeto Characters. Microsoft Agent está en desuso a partir Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ecd8e48b63a426ec8508f3838ec9f9dc24ebd6289f9482ab796bb22e388e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693411"
---
# <a name="height-property-characters-object"></a>Propiedad Height (objeto Characters)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el alto del marco del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Valor de_ *  \[ =  *alto*\]



| Parte    | Descripción                                                 |
|---------|-------------------------------------------------------------|
| *value* | Entero Long que especifica el alto del marco del carácter. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad Height** siempre se expresa en píxeles, en relación con las coordenadas de pantalla (esquina superior izquierda). La configuración de esta propiedad se aplica a todos los clientes del carácter.

Aunque el carácter aparece en una ventana de región con forma irregular, el alto del carácter se basa en las dimensiones externas del marco de animación rectangular utilizado cuando el carácter se compiló con el Editor de caracteres de Microsoft Agent.

 

 




