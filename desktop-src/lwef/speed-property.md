---
title: Propiedad Speed
description: Propiedad Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704623"
---
# <a name="speed-property"></a>Propiedad Speed

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve un entero largo que especifica la velocidad actual de la salida de voz del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Rápidas**

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve el valor actual de la velocidad de salida de habla para el carácter. En el caso de los caracteres que usan la salida de TTS, la propiedad devuelve el valor de salida de TTS real para el carácter. Si TTS no está habilitado o el carácter no admite la salida de TTS, el valor refleja la configuración de usuario para la velocidad de salida.

Aunque la aplicación no puede escribir este valor, puede incluir etiquetas **SPD** (Speed) en el texto de salida que acelerarán temporalmente la salida de un utterance determinado. Sin embargo, el uso de la etiqueta **SPD** para cambiar la salida de voz del carácter no afecta al valor de la propiedad **Speed** . Para obtener más información, consulte [etiquetas de salida de voz](microsoft-agent-speech-output-tags.md).

 

 




