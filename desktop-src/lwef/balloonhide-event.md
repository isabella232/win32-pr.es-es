---
title: Evento BalloonHide
description: Evento BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269300"
---
# <a name="balloonhide-event"></a>Evento BalloonHide

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando se oculta el globo de palabras de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent* \_ **BalloonHide** **(ByVal** *CharacterID ** * *)*



| Parte          | Descripción                                                       |
|---------------|-------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter asociado al globo de palabras. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El servidor envía este evento solo a los clientes del carácter (aplicaciones que han cargado el carácter) que usa el globo de palabras.

### <a name="see-also"></a>Consulte también

[**Evento BalloonShow**](balloonshow-event.md)


 

 




