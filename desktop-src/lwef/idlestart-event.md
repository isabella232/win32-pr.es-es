---
title: Evento IdleStart
description: Evento IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81458d4c88bc5db4ae4231ecb4ca47f456700917f42d6ccdfe5a6013bc288849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716055"
---
# <a name="idlestart-event"></a>Evento IdleStart

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el servidor establece un carácter en el **estado Idling.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent: \_ IdleStart* *  **(ByVal** *CharacterID"))**



| Parte          | Descripción                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter de idling como una cadena. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

El servidor envía este evento a todos los clientes del carácter.

### <a name="see-also"></a>Consulte también

[**Evento IdleComplete**](idlecomplete-event.md)


 

 




