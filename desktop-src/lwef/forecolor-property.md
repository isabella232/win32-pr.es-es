---
title: Propiedad ForeColor
description: Propiedad ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903218"
---
# <a name="forecolor-property"></a>Propiedad ForeColor

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve el color de primer plano que se muestra actualmente en la ventana de globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Balloon. ForeColor**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **ForeColor** devuelve un valor que especifica el color del texto del globo de palabras. El intervalo válido para un color RGB normal es de 0 a 16.777.215 (&HFFFFFF). El byte alto de un número de este intervalo es igual a 0; los 3 bytes inferiores, desde menos hasta el byte más significativo, determinan la cantidad de rojo, verde y azul, respectivamente. Los componentes rojo, verde y azul se representan mediante un número comprendido entre 0 y 255 (&HFF).

 

 




