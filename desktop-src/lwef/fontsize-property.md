---
title: Propiedad FontSize (objeto Commands)
description: Obtenga información sobre la propiedad de objeto FontSize Commands. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068212"
---
# <a name="fontsize-property-commands-object"></a>Propiedad FontSize (objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el tamaño de fuente utilizado en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Commands.FontSize_ *  \[  =  *Points*\]



| Parte     | Descripción                                              |
|----------|----------------------------------------------------------|
| *Puntos* | Valor entero Long que especifica el tamaño de fuente en puntos. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **propiedad FontSize** define el tamaño de punto de la fuente utilizada para mostrar texto en el menú emergente del carácter. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente del menú para la configuración **de LanguageID** del carácter o, si no se establece, en la configuración de idioma predeterminada del usuario.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter ni a otros caracteres de la aplicación cliente.

 

 




