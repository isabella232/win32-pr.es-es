---
title: IAgentCharacter moveTo
description: IAgentCharacter moveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077627"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter:: moveTo

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Reproduce la animación de estado de **movimiento** asociada y mueve el marco de caracteres a la ubicación especificada.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente. Cuando la función devuelve, esta variable contiene el identificador de la solicitud.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

Coordenada x de la nueva posición en píxeles, con respecto al origen de la pantalla (superior izquierda). La ubicación de un carácter se basa en la esquina superior izquierda de su fotograma de animación.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*sí*
</dt> <dd>

Coordenada y de la nueva posición en píxeles, con respecto al origen de la pantalla (superior izquierda). La ubicación de un carácter se basa en la esquina superior izquierda de su fotograma de animación.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

Parámetro que especifica en milisegundos la rapidez con la que se mueve el marco del carácter. El valor recomendado es 1000. Si se especifica cero (0), se mueve el marco sin reproducir una animación.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud [**moveTo**](https://www.bing.com/search?q=**MoveTo**) .

</dd> </dl>

Al usar el protocolo HTTP para tener acceso a los datos de animación y de caracteres, utilice el método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantizar la disponibilidad de las animaciones de estado en **movimiento** antes de llamar a este método. Incluso si la animación no está cargada, el servidor todavía mueve el marco.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: SetPosition**](iagentcharacter--setposition.md)


 

 