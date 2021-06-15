---
title: Propiedad FontSize (objeto Balloon)
description: Obtenga información sobre la propiedad de objeto FontSize Balloon. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068223"
---
# <a name="fontsize-property-balloon-object"></a>Propiedad FontSize (objeto Balloon)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el tamaño de fuente admitido para el globo de palabras para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.:Characters* *  **("**_CharacterID_*_"). Puntos Balloon.FontSize_* \[  =  \]



| Parte     | Descripción                                              |
|----------|----------------------------------------------------------|
| *Puntos* | Valor entero Long que especifica el tamaño de fuente en puntos. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [**propiedad FontSize**](fontsize-property.md) devuelve un valor entero Long que especifica el tamaño de fuente actual en puntos. El valor máximo de **FontSize** es 2160 puntos.

El valor predeterminado de la configuración de fuente del globo de palabras de un carácter se establece en el Editor de caracteres de Microsoft Agent. Además, el usuario puede invalidar la configuración de fuente de todos los caracteres de la hoja de propiedades de Microsoft Agent.

 

 




