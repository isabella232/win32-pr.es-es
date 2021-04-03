---
title: Evento AgentPropertyChange
description: Evento AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075504"
---
# <a name="agentpropertychange-event"></a>Evento AgentPropertyChange

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando el usuario cambia una propiedad en la ventana Opciones de carácter avanzadas.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent. ** * * AgentPropertyChange*

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento indica que el usuario ha cambiado y aplicado cualquier propiedad incluida en la ventana opción de carácter avanzado.

En el código para controlar este evento, puede consultar los valores de propiedad específicos de los objetos [AudioOutput](the-audiooutput-object.md) o [SpeechInput](the-speechinput-object.md) .

### <a name="see-also"></a>Consulte también

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




