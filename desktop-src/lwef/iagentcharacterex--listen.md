---
title: IAgentCharacterEx escucha
description: IAgentCharacterEx escucha
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357277"
---
# <a name="iagentcharacterexlisten"></a>IAgentCharacterEx:: Listen

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

Activa o desactiva el modo de escucha (entrada de reconocimiento de voz).

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*
</dt> <dd>

Marca de modo de escucha. Si este parámetro es **true**, el modo de escucha está activado; Si es **false**, el modo de escucha está desactivado.

</dd> </dl>

Al establecer este método en **true** , se habilita el modo de escucha (activa el reconocimiento de voz) durante un período de tiempo fijo. Aunque no se puede establecer el valor del tiempo de espera, puede desactivar el modo de escucha antes de que expire el tiempo de espera. Además, si el modo de escucha ya está activado porque usted (u otro cliente) estableció correctamente el método en **true** antes de que expire el tiempo de espera, el método se ejecuta correctamente y restablece el tiempo de espera. Sin embargo, si el modo de escucha ya está activado porque el usuario está presionando la clave de escucha, el método se ejecuta correctamente, pero el tiempo de espera se omite y el modo de escucha finaliza en función de la interacción del usuario con la clave de escucha.

Este método se realizará correctamente solo cuando lo llame el cliente de entrada y de actividad. Por lo tanto, se producirá un error en el método si el cliente no es el cliente activo del carácter más alto. También se producirá un error en el método si intenta establecer el método en **false** y el usuario está presionando la clave de escucha. También puede producir un error si no hay ningún motor de voz compatible disponible que coincida con el valor de ID. de idioma del carácter o el usuario ha deshabilitado la entrada de voz mediante la hoja de propiedades del agente de Microsoft. Sin embargo, el método no generará un error si el dispositivo de audio está ocupado.

Cuando se establece correctamente este método en **true**, el servidor desencadena el evento [**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md) . El servidor también envía **IAgentNotifySinkEx:: ListeningState** cuando se completa el tiempo de espera del modo de escucha o cuando se establece [**IAgentCharacterEx:: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) en **false**.

Este método no llama automáticamente a [**IAgentCharacter:: stopAll**](iagentcharacter--stopall.md) y reproduce una animación de estado de escucha del carácter como ocurre cuando el usuario presiona la tecla de escucha. Esto le permite usar el evento [**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md) para determinar si desea detener la animación actual y reproducir su propia animación adecuada. Sin embargo, una vez que se detecta un utterance de usuario, el servidor llama automáticamente a **IAgentCharacter:: stopAll** y reproduce una animación del estado de la audición.

## <a name="see-also"></a>Consulte también

[**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




