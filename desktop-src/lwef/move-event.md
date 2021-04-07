---
title: Evento de movimiento
description: Evento de movimiento
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903506"
---
# <a name="move-event"></a>Evento de movimiento

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando se mueve un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent* \_ **Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *causa * * *)**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter que se ha despasado.                                                                                                                                                                                                                                                                                                   |
| *X*           | Devuelve la coordenada x (en píxeles) del borde superior de la nueva ubicación del marco de caracteres como un entero.                                                                                                                                                                                                                                         |
| *S*           | Devuelve la coordenada y (en píxeles) del borde izquierdo de la nueva ubicación del marco de caracteres como un entero.                                                                                                                                                                                                                                        |
| *Causa*       | Devuelve un valor que indica lo que ha provocado el movimiento del carácter. 1 el usuario arrastró el carácter.<br/> 2 la aplicación cliente ha cambiado el carácter.<br/> 3 otra aplicación cliente ha cambiado el carácter.<br/> 4 el servidor del agente ha quitado el carácter para mantenerlo en la pantalla después de un cambio en la resolución de pantalla.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento se produce cuando el usuario o una aplicación cambian la posición del carácter. Las coordenadas son relevantes en la esquina superior izquierda de la pantalla. Este evento solo se envía a los clientes del carácter (aplicaciones que han cargado el carácter).

**Vea también**

[**Propiedad MoveCause**](movecause-property.md), [ **evento size**](size-event.md)

 

 





