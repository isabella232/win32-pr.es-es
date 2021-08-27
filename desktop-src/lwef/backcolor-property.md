---
title: Propiedad BackColor (características heredadas Windows entorno)
description: Propiedad BackColor
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f799e8b9e00a97770cd004e29df75da8345a6cc01531fce53079ea550402c68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114815"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>Propiedad BackColor (características heredadas Windows entorno)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve el color de fondo que se muestra actualmente en la ventana de globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Balloon.BackColor_*

</dd> </dl>

## <a name="remarks"></a>Comentarios

El intervalo válido para un color RGB normal es de 0 a 16 777 215 (&HFFFFFF). El byte alto de un número de este intervalo es igual a 0; los 3 bytes inferiores, de menos a más significativo, determinan la cantidad de rojo, verde y azul, respectivamente. Los componentes rojo, verde y azul se representan mediante un número comprendido entre 0 y 255 (&HFF).

 

 




