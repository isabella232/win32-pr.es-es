---
title: Evento IdleComplete
description: Evento IdleComplete
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e678f49bcf0479b2095a97e4bf3ac95a62862ac90741cc47e592e0cac716591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114645"
---
# <a name="idlecomplete-event"></a>Evento IdleComplete

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el servidor finaliza el **estado idling** de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent** \_ IdleComplete* *  **(ByVal** *CharacterID))**



| Parte          | Descripción                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de idling como una cadena. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

El servidor envía este evento a todos los clientes del carácter.

### <a name="see-also"></a>Consulte también

[**Evento IdleStart**](idlestart-event.md)


 

 




