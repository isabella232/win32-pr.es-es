---
title: Propiedad FontName (objeto Commands)
description: Obtenga información sobre la propiedad de objeto FontName Commands. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068261"
---
# <a name="fontname-property-commands-object"></a>Propiedad FontName (objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece la fuente utilizada en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Caracteres("**_CharacterID_*_"). Commands.FontName_ *  \[  =  *Font*\]



| Parte   | Descripción                                      |
|--------|--------------------------------------------------|
| *Fuente* | Valor de cadena correspondiente al nombre de la fuente. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **propiedad FontName** define la fuente utilizada para mostrar texto en el menú emergente del carácter. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente del menú para la configuración **de LanguageID** del carácter o, si no se establece, en la configuración del identificador de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 




