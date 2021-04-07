---
title: Mostrar evento
description: Mostrar evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903287"
---
# <a name="show-event"></a>Mostrar evento

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando se muestra un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent * * * \_ Show (ByVal* *  *CharacterID*, **ByVal** *causa * * *)**



| Parte          | Descripción                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter que se muestra como una cadena.                                                                                                                                                                                                                          |
| *Causa*       | Devuelve un valor que indica la causa del carácter que se va a mostrar. 2 el usuario mostró el carácter (mediante el comando de menú o de voz).<br/> 4 la aplicación cliente mostró el carácter.<br/> 6 otra aplicación cliente mostró el carácter.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El servidor envía este evento a todos los clientes del carácter. Para consultar el estado actual del carácter, utilice la propiedad [**visible**](visible-property.md) .

### <a name="see-also"></a>Consulte también

[**Ocultar evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





