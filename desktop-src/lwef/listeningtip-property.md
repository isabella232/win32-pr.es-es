---
title: Propiedad ListeningTip
description: Propiedad ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695446"
---
# <a name="listeningtip-property"></a>Propiedad ListeningTip

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve un valor booleano que indica la configuración del usuario actual para la sugerencia de escucha.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintáctica** 
</dt> <dd>

*agente * * *. SpeechInput.ListeningTip**



| Value     | Descripción                    |
|-----------|--------------------------------|
| **True**  | La sugerencia de escucha está habilitada.  |
| **False** | La sugerencia de escucha está deshabilitada. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **ListeningTip** indica si está habilitada la opción Mostrar sugerencia de escucha en la hoja de propiedades del agente de Microsoft (opciones avanzadas de caracteres). Cuando **ListeningTip** devuelve **true** y la entrada de voz está habilitada, el servidor muestra la ventana de sugerencia cuando el usuario presiona la tecla de escucha.

## <a name="see-also"></a>Consulte también

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




