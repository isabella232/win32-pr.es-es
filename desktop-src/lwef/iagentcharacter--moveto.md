---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea5a0e288e4b7d9782f1b463fdbcccf01b0da9314894be1a60c556392e25e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848545"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter::MoveTo

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Reproduce la animación **de estado Moving** asociada y mueve el marco de caracteres a la ubicación especificada.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente. Cuando la función devuelve un resultado, esta variable contiene el identificador de la solicitud.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x de la nueva posición en píxeles, con respecto al origen de la pantalla (parte superior izquierda). La ubicación de un carácter se basa en la esquina superior izquierda de su marco de animación.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada y de la nueva posición en píxeles, con respecto al origen de la pantalla (parte superior izquierda). La ubicación de un carácter se basa en la esquina superior izquierda de su marco de animación.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

Parámetro que especifica en milisegundos la rapidez con la que se mueve el marco del carácter. El valor recomendado es 1000. Si se especifica cero (0), se mueve el marco sin reproducir una animación.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador [**de solicitud MoveTo.**](https://www.bing.com/search?q=**MoveTo**)

</dd> </dl>

Cuando use el protocolo HTTP para acceder a los datos de  caracteres y animaciones, use el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad de las animaciones de estado móvil antes de llamar a este método. Incluso si no se carga la animación, el servidor sigue trasladando el fotograma.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md)


 

 