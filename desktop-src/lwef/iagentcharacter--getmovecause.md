---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119690"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

Recupera la causa del último movimiento del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Dirección de una variable que recibe la causa del último movimiento del carácter y será una de las siguientes:



| Valor                                                               | Descripción                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | El carácter no se ha movido.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | El usuario arrastró el carácter.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | La aplicación movió el carácter.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Otra aplicación movió el carácter.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | El servidor movió el carácter para mantenerlo en pantalla después de un cambio de resolución de pantalla. |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentNotifySink::Move**](iagentnotifysink--move.md)


 

 





