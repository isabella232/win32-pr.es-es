---
title: Propiedad de paso
description: Propiedad de paso
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419155"
---
# <a name="pitch-property"></a>Propiedad de paso

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Denominación** 
</dt> <dd>

Devuelve un entero largo para la configuración de tono de salida de voz (TTS) del carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Espacia**

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad solo se aplica a los caracteres configurados para la salida de TTS. Si el carácter no admite la salida de TTS, esta propiedad devuelve cero (0).

Aunque la aplicación no puede escribir este valor, puede incluir etiquetas **Pit** (Brea) en el texto de salida que aumentarán temporalmente el paso de un utterance determinado. Sin embargo, el uso de la etiqueta **Pit** para cambiar el paso no cambiará el valor de la propiedad de **paso** . Para obtener más información, consulte [etiquetas de salida de voz](pit-tag.md).

 

 




