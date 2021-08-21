---
title: Propiedad Speed
description: Propiedad Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaca342dde91965ab381f95671a39c4ba9fdcae040835f09867b3fabf5899a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745957"
---
# <a name="speed-property"></a>Propiedad Speed

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve un entero Long que especifica la velocidad actual de la salida de voz del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Velocidad_*

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve la configuración de velocidad de salida de habla actual para el carácter. Para los caracteres que usan la salida de TTS, la propiedad devuelve el valor de salida de TTS real para el carácter. Si TTS no está habilitado o el carácter no admite la salida de TTS, la configuración refleja la configuración del usuario para la velocidad de salida.

Aunque la aplicación no puede escribir este valor, puede incluir etiquetas **Spd** (velocidad) en el texto de salida que acelerarán temporalmente la salida de una expresión determinada. Sin embargo, el uso **de la etiqueta Spd** para cambiar la salida hablada del carácter no afecta al valor **de la propiedad Speed.** Para más información, consulte [Etiquetas de salida de voz.](microsoft-agent-speech-output-tags.md)

 

 




