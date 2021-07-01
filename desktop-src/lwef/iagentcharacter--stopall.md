---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120918"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter::StopAll

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Detiene todas las animaciones (solicitudes) y las quita de la cola de animación del carácter.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

Campo de bits que indica los tipos de solicitudes que se detienen (y quitan de la cola del carácter), que consta de lo siguiente:



| Valor                                                                                  |  Descripción                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **const unsigned long** **STOP TYPE ALL = \_ \_ 0xFFFFFFFF;**<br/>              | Detiene todas las solicitudes de animación, incluidas las solicitudes [**de preparación**](iagentcharacter--prepare.md) no en cola. |
| **const unsigned long** **STOP TYPE PLAY = \_ \_ 0x00000001;**<br/>             | Detiene todas las solicitudes de reproducción.                                                                                 |
| **const unsigned long** **STOP TYPE MOVE = \_ \_ 0x00000002;**<br/>             | Detiene todas [**las solicitudes**](https://www.bing.com/search?q=**Move**) move.                                               |
| **const unsigned long** **STOP TYPE SPEAK = \_ \_ 0x00000004;**<br/>            | Detiene todas las [**solicitudes speak.**](iagentcharacter--speak.md)                                              |
| **const unsigned long** **STOP TYPE PREPARE = \_ \_ 0x00000008;**<br/>          | Detiene todas las solicitudes [**de preparación en**](iagentcharacter--prepare.md) cola.                                   |
| **const unsigned long** **STOP TYPE \_ \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | Detiene todas las solicitudes de [**preparación que no están en**](iagentcharacter--prepare.md) cola.                               |
| **const unsigned long** **STOP TYPE VISIBLE = \_ \_ 0x00000020;**<br/>          | Detiene todas [**las solicitudes**](iagentcharacter--hide.md) Ocultar [**o**](iagentcharacter--show.md) Mostrar.       |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::Stop**](iagentcharacter--stop.md)


 

 





