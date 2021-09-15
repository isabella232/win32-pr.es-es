---
title: IAgentNotifySink Move
description: IAgentNotifySink Move
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359152"
---
# <a name="iagentnotifysinkmove"></a>IAgentNotifySink::Move

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

Notifica a una aplicación cliente cuando se ha movido el carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter que se ha movido.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x de la nueva posición en píxeles, con respecto al origen de la pantalla (parte superior izquierda). La ubicación de un carácter se basa en la esquina superior izquierda de su marco de animación.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada y de la nueva posición en píxeles, en relación con el origen de la pantalla (esquina superior izquierda). La ubicación de un carácter se basa en la esquina superior izquierda de su marco de animación.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La causa del movimiento de caracteres. El parámetro puede ser uno de los siguientes:



| Value                                                          | Descripción                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | No se ha movido el carácter.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | El usuario arrastró el carácter.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | La aplicación movió el carácter.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Otra aplicación movió el carácter.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | El servidor movió el carácter para mantenerlo en pantalla después de un cambio en la resolución de pantalla. |



 

</dd> </dl>

Este evento se envía a todos los clientes del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)


 

 





