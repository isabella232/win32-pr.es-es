---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c91d4ebc4f55da6a0e102c30a8c2a16eab12beaf283ff4b5e023d15d3a17b05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693151"
---
# <a name="iagentcharactergetttspitch"></a>IAgentCharacter::GetTTSPitch

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

Recupera la configuración de tono de salida de TTS del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*
</dt> <dd>

Dirección de una variable que recibe la configuración de tono TTS actual del carácter en Hertz.

</dd> </dl>

Aunque la aplicación no puede escribir este valor, puede incluir etiquetas de tono en el texto de salida que aumentarán temporalmente el tono de una expresión determinada. Este método solo se aplica a los caracteres configurados para la salida de TTS. Si el motor de síntesis de voz (TTS) no está habilitado (o instalado) o el carácter no admite la salida de TTS, este método devuelve cero (0).

 

 




