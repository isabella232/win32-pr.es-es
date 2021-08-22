---
title: IAgentNotifySink Move
description: IAgentNotifySink Move
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f32df3058a5b5c8e0a4e02a98f9a97afdbff56f349a63fceb5d70a9001391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105189"
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

Coordenada y de la nueva posición en píxeles, con respecto al origen de la pantalla (parte superior izquierda). La ubicación de un carácter se basa en la esquina superior izquierda de su marco de animación.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La causa del movimiento de caracteres. El parámetro puede ser uno de los siguientes:



| Valor                                                          | Descripción                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | El carácter no se ha movido.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | El usuario arrastró el carácter.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | La aplicación movió el carácter.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Otra aplicación movió el carácter.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | El servidor movió el carácter para mantenerlo en pantalla después de un cambio de resolución de pantalla. |



 

</dd> </dl>

Este evento se envía a todos los clientes del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)


 

 





