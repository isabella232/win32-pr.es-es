---
title: Ocultar evento
description: Ocultar evento
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02974d1d66a22eab24c93fc5c9d29b9c2d0e604082fef9f4f0583ebcf7354576
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062065"
---
# <a name="hide-event"></a>Ocultar evento

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando se oculta un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent** \_ Hide(* *  **ByVal** *CharacterID*, **ByVal** *Cause...))**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter oculto como una cadena.                                                                                                                                                                                                                                                                                                                                                               |
| *Causa*       | Devuelve un valor que indica lo que hizo que el carácter se ocultara. 1 El usuario ocultó el carácter seleccionando el comando en el menú emergente del icono de la barra de tareas del carácter o usando la entrada de voz.<br/> 3 La aplicación cliente ocultó el carácter.<br/> 5 Otra aplicación cliente ocultó el carácter.<br/> 7 El usuario ocultó el carácter seleccionando el comando en el menú emergente del carácter.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

El servidor envía este evento a todos los clientes del carácter. Para consultar el estado actual del carácter, use la [**propiedad Visible.**](visible-property.md)

### <a name="see-also"></a>Consulte también

[**Mostrar evento**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





