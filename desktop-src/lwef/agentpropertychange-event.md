---
title: Evento AgentPropertyChange
description: Evento AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accafc89fbcd9f29dd7327cc4561c0375f773abe01077bab7cbfa24653f6106d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752696"
---
# <a name="agentpropertychange-event"></a>Evento AgentPropertyChange

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el usuario cambia una propiedad en la ventana Opciones avanzadas de caracteres.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent.**AgentPropertyChange**

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento indica cuándo el usuario ha cambiado y aplicado cualquier propiedad incluida en la ventana Opción avanzada de caracteres.

En el código para controlar este evento, puede consultar la configuración de propiedad específica de los objetos [AudioOutput](the-audiooutput-object.md) [o SpeechInput.](the-speechinput-object.md)

### <a name="see-also"></a>Consulte también

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




