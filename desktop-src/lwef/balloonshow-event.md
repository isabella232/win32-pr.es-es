---
title: Evento BalloonShow
description: Evento BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418966"
---
# <a name="balloonshow-event"></a>Evento BalloonShow

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando se muestra el globo de palabras de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent* \_ **BalloonShow** **(ByVal** *CharacterID ** * *)*



| Parte          | Descripción                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter asociado al globo de palabras. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El servidor envía este evento solo a los clientes del carácter (aplicaciones que han cargado el carácter) que usa el globo de palabras.

### <a name="see-also"></a>Consulte también

[**Evento BalloonHide**](balloonhide-event.md)


 

 




