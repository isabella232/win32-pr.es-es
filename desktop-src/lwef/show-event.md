---
title: Mostrar evento
description: Mostrar evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b126c7726f8b8ed3ce1e83162cf41ad3223700630167448ff8a7655817a0604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975745"
---
# <a name="show-event"></a>Mostrar evento

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando se muestra un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent** \_ Show (ByVal* *  *CharacterID*, **ByVal** *Cause...))**



| Parte          | Descripción                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter que se muestra como una cadena.                                                                                                                                                                                                                          |
| *Causa*       | Devuelve un valor que indica lo que hizo que se mostrara el carácter. 2 El usuario mostró el carácter (mediante el comando de menú o voz).<br/> 4 La aplicación cliente mostró el carácter.<br/> 6 Otra aplicación cliente mostró el carácter.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

El servidor envía este evento a todos los clientes del carácter. Para consultar el estado actual del carácter, use la [**propiedad**](visible-property.md) Visible.

### <a name="see-also"></a>Consulte también

[**Ocultar evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)


 

 





