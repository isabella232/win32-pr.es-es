---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695482"
---
# <a name="iagentcharactergetttspitch"></a>IAgentCharacter::GetTTSPitch

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

Recupera la configuración del tono de salida de TTS del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*
</dt> <dd>

Dirección de una variable que recibe la configuración de tono de TTS actual del carácter en hercios.

</dd> </dl>

Aunque la aplicación no puede escribir este valor, puede incluir etiquetas de paso en el texto de salida que aumentarán temporalmente el paso de un utterance determinado. Este método solo se aplica a los caracteres configurados para la salida de TTS. Si el motor de síntesis de voz (TTS) no está habilitado (o instalado) o el carácter no admite la salida de TTS, este método devuelve cero (0).

 

 




