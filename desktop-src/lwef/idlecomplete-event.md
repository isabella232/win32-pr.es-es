---
title: Evento IdleComplete
description: Evento IdleComplete
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104074983"
---
# <a name="idlecomplete-event"></a>Evento IdleComplete

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando el servidor finaliza el estado de **ralentí** de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent * * * \_ IdleComplete* *  **(ByVal** *CharacterID ** * *)*



| Parte          | Descripción                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de ralentí como una cadena. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El servidor envía este evento a todos los clientes del carácter.

### <a name="see-also"></a>Consulte también

[**Evento IdleStart**](idlestart-event.md)


 

 




