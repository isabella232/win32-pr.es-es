---
title: Propiedad ForeColor
description: Propiedad ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebfc7f0b64a43f7ccb9075426a75df9a777fbb8b1e5e94cb16e747e0681cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962765"
---
# <a name="forecolor-property"></a>Propiedad ForeColor

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve el color de primer plano que se muestra actualmente en la ventana de globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Balloon.ForeColor_*

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad ForeColor** devuelve un valor que especifica el color del texto en el globo de palabras. El intervalo válido para un color RGB normal es de 0 a 16 777 215 (&HFFFFFF). El byte alto de un número de este intervalo es igual a 0; los 3 bytes inferiores, de menos a más significativo, determinan la cantidad de rojo, verde y azul, respectivamente. Los componentes rojo, verde y azul se representan mediante un número comprendido entre 0 y 255 (&HFF).

 

 




