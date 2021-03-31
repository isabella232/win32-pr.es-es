---
title: Ocultar IAgentCharacter
description: Ocultar IAgentCharacter
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077675"
---
# <a name="iagentcharacterhide"></a>IAgentCharacter:: Hide

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

Oculta el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente. Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

**Ocultar** marca de animación de estado. Si este parámetro es **true**, la animación de **ocultación** no se reproduce antes de que se oculte el marco de caracteres; Si **es false**, la animación se reproduce.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud de **ocultación** .

</dd> </dl>

El servidor pone en cola la animación asociada al método **Hide** en la cola del carácter. Esto le permite usarlo para ocultar el carácter después de una secuencia de otras animaciones. Puede reproducir la acción inmediatamente mediante el método [**Stop**](iagentcharacter--stop.md) antes de llamar al método **Hide** .

Al usar el protocolo HTTP para tener acceso a los datos de animación y de caracteres, utilice el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad de la animación de **ocultación** de estado antes de llamar a este método.

Ocultar un carácter también puede producir el desencadenamiento del evento [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md) de otro carácter visible.

Los caracteres ocultos no pueden tener acceso al canal de audio. El servidor devolverá un estado de error en el evento [**RequestComplete**](iagentnotifysink--requestcomplete.md) si genera una solicitud de animación y el carácter está oculto.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: show**](iagentcharacter--show.md)


 

 