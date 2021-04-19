---
title: Propiedad fontSize (objeto Commands)
description: Propiedad fontSize
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105720209"
---
# <a name="fontsize-property-commands-object"></a>Propiedad fontSize (objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el tamaño de fuente utilizado en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*Caracteres Agent. ***("**_CharacterID_*_"). Commands. FontSize_( *  \[  =  *puntos* )\]



| Parte     | Descripción                                              |
|----------|----------------------------------------------------------|
| *Cima* | Valor entero largo que especifica el tamaño de fuente en puntos. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **FontSize** define el tamaño en puntos de la fuente utilizada para mostrar texto en el menú emergente del carácter. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente de menú para la configuración de **LanguageID** del carácter, o bien, si no está establecida, la configuración de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 




