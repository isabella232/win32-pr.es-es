---
title: IAgentCharacterEx Listen
description: IAgentCharacterEx Listen
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ee221de03fe0a0e908e1fc3c10f05d48c26dd9fd264edd20ee2e4d78d73fb91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105503"
---
# <a name="iagentcharacterexlisten"></a>IAgentCharacterEx::Listen

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

Activa o desactiva el modo de escucha (entrada de reconocimiento de voz).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*
</dt> <dd>

Marca de modo de escucha. Si este parámetro es **True**, el modo de escucha está activado; si **es False,** el modo de escucha está desactivado.

</dd> </dl>

Establecer este método en **True habilita** el modo de escucha (activa el reconocimiento de voz) durante un período de tiempo fijo. Aunque no puede establecer el valor del tiempo de espera, puede desactivar el modo de escucha antes de que expire el tiempo de espera. Además, si el modo de escucha ya está en porque usted (u otro cliente) estableció correctamente el método en **True** antes de que expire el tiempo de espera, el método se realiza correctamente y restablece el tiempo de espera. Sin embargo, si el modo de escucha ya está on porque el usuario presiona la tecla Listening, el método se realiza correctamente, pero el tiempo de espera se omite y el modo de escucha finaliza en función de la interacción del usuario con la clave de escucha.

Este método solo se realizará correctamente cuando lo llame el cliente activo de entrada. Por lo tanto, se producirá un error en el método si el cliente no es el cliente activo del carácter superior. El método también producirá un error si intenta establecer el método en **False** y el usuario presiona la tecla Listening. También puede producir un error si no hay ningún motor de voz compatible disponible que coincida con la configuración del identificador de idioma del carácter o si el usuario ha deshabilitado la entrada de voz mediante la hoja de propiedades de Microsoft Agent. Sin embargo, el método no producirá un error si el dispositivo de audio está ocupado.

Cuando se establece correctamente este método en **True,** el servidor desencadena el [**evento IAgentNotifySinkEx::ListeningState.**](iagentnotifysinkex--listeningstate.md) El servidor también envía **IAgentNotifySinkEx::ListeningState** cuando se completa el tiempo de espera del modo de escucha o cuando se establece [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) en **False.**

Este método no llama automáticamente a [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md) y reproduce una animación de estado de escucha del carácter como se produce cuando el usuario presiona la tecla Listening. Esto le permite usar el evento [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) para determinar si desea detener la animación actual y reproducir su propia animación adecuada. Sin embargo, una vez que se detecta una expresión de usuario, el servidor llama automáticamente a **IAgentCharacter::StopAll** y reproduce una animación de estado de audiencia.

## <a name="see-also"></a>Consulte también

[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




