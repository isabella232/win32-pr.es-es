---
title: Propiedad Pitch
description: Propiedad Pitch
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e346ea0fbb7ebb819d8f00b2fc6aab1ab95e72f391bddc696da18a49f0b2a09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475415"
---
# <a name="pitch-property"></a>Propiedad Pitch

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Descripción** 
</dt> <dd>

Devuelve un entero Long para la configuración de tono de salida de voz (TTS) del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Pitch_*

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta propiedad solo se aplica a los caracteres configurados para la salida de TTS. Si el carácter no admite la salida de TTS, esta propiedad devuelve cero (0).

Aunque la aplicación no puede escribir este valor, puede incluir etiquetas **Pit** (pitch) en el texto de salida que aumentará temporalmente el tono de una expresión determinada. Sin embargo, el uso **de la etiqueta Pit** para cambiar el tono no cambiará la configuración de la propiedad **Pitch.** Para más información, consulte [Etiquetas de salida de voz.](pit-tag.md)

 

 




