---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419206"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

Recupera la causa del último movimiento del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Dirección de una variable que recibe la causa del último movimiento del carácter y será uno de los siguientes:



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | No se ha despasado el carácter.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | El usuario arrastró el carácter.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | La aplicación ha cambiado el carácter.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Otra aplicación ha cambiado el carácter.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | El servidor ha quitado el carácter para mantenerlo en la pantalla después de un cambio en la resolución de pantalla. |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentNotifySink:: Move**](iagentnotifysink--move.md)


 

 





