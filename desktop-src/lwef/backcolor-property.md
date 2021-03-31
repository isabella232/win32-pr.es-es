---
title: BackColor (propiedad, características heredadas del entorno de Windows)
description: BackColor (propiedad)
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800890"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>BackColor (propiedad, características heredadas del entorno de Windows)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve el color de fondo que se muestra actualmente en la ventana de globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("**_CharacterID_*_"). Balloon. BackColor_*

</dd> </dl>

## <a name="remarks"></a>Observaciones

El intervalo válido para un color RGB normal es de 0 a 16.777.215 (&HFFFFFF). El byte alto de un número de este intervalo es igual a 0; los 3 bytes inferiores, desde menos hasta el byte más significativo, determinan la cantidad de rojo, verde y azul, respectivamente. Los componentes rojo, verde y azul se representan mediante un número comprendido entre 0 y 255 (&HFF).

 

 




