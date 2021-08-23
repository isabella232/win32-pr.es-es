---
title: Propiedad ListeningTip
description: Propiedad ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a743eb26d1e2b57d106e72d77c3774938ffe7e56ca4ba4147001d74bb99f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665445"
---
# <a name="listeningtip-property"></a>Propiedad ListeningTip

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve un valor booleano que indica la configuración actual del usuario para la sugerencia de escucha.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxis** 
</dt> <dd>

*agent,. SpeechInput.ListeningTip**



| Value     | Descripción                    |
|-----------|--------------------------------|
| **True**  | La sugerencia de escucha está habilitada.  |
| **False** | La sugerencia de escucha está deshabilitada. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **propiedad ListeningTip** indica si la opción Mostrar sugerencia de escucha de la hoja de propiedades de Microsoft Agent (Opciones avanzadas de caracteres) está habilitada. Cuando **ListeningTip** devuelve **True y** la entrada de voz está habilitada, el servidor muestra la ventana de sugerencias cuando el usuario presiona la tecla Listening.

## <a name="see-also"></a>Consulte también

[**Evento AgentPropertyChange**](agentpropertychange-event.md)


 

 




