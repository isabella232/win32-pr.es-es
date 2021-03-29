---
title: Ocultar evento
description: Ocultar evento
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903516"
---
# <a name="hide-event"></a>Ocultar evento

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando se oculta un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent * * * \_ Hide (* *  **ByVal** *CharacterID*, **ByVal** *causa * * *)**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter oculto como una cadena.                                                                                                                                                                                                                                                                                                                                                               |
| *Causa*       | Devuelve un valor que indica la causa del carácter que se va a ocultar. 1 usuario ocultó el carácter seleccionando el comando en el menú emergente del icono de la barra de tareas del carácter o usando la entrada de voz.<br/> 3 la aplicación cliente ocultó el carácter.<br/> 5 otra aplicación cliente ocultó el carácter.<br/> 7 el usuario ocultó el carácter seleccionando el comando en el menú emergente del carácter.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El servidor envía este evento a todos los clientes del carácter. Para consultar el estado actual del carácter, utilice la propiedad [**visible**](visible-property.md) .

### <a name="see-also"></a>Consulte también

[**Mostrar evento**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





