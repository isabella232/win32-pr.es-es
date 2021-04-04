---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076410"
---
# <a name="iagentcharacterplay"></a>IAgentCharacter::P establecer

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Reproduce la animación especificada.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente. Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*
</dt> <dd>

Nombre de una animación.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud **IAgentCharacter::P** .

</dd> </dl>

El nombre de una animación se define cuando el carácter se compila con el editor de caracteres del agente de Microsoft. Antes de reproducir la animación especificada, el servidor intenta reproducir la animación de **retorno** de la animación anterior (si se ha asignado alguna).

Cuando los datos de animación de un carácter se almacenan en el equipo local del usuario, puede utilizar el método **IAgentCharacter::P establecer** y especificar el nombre de la animación. Al usar el protocolo HTTP para tener acceso a los datos de animación, use el método [**Prepare**](iagentcharacter--prepare.md) para garantizar la disponibilidad de la animación antes de llamar a este método.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::P redondear**](iagentcharacter--prepare.md)


 

 




