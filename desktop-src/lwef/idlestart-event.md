---
title: Evento IdleStart
description: Evento IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714175"
---
# <a name="idlestart-event"></a>Evento IdleStart

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando el servidor establece un carácter en el estado de **ralentí** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent * * * \_ IdleStart* *  **(ByVal** *CharacterID ** * *)*



| Parte          | Descripción                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de ralentí como una cadena. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El servidor envía este evento a todos los clientes del carácter.

### <a name="see-also"></a>Consulte también

[**Evento IdleComplete**](idlecomplete-event.md)


 

 




