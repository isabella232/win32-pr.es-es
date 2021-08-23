---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff1811e7b7ee323ef57e21dbeea4e6ea9d33dc8bc735327ec9ba5afc2ce299b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609785"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter::StopAll

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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
| **const unsigned long** **STOP TYPE ALL = \_ \_ 0xFFFFFFFF;**<br/>              | Detiene todas las solicitudes de animación, incluidas las solicitudes [**de preparación que**](iagentcharacter--prepare.md) no están en cola. |
| **const unsigned long** **STOP TYPE PLAY = \_ \_ 0x00000001;**<br/>             | Detiene todas las solicitudes de reproducción.                                                                                 |
| **const unsigned long** **STOP TYPE MOVE = \_ \_ 0x00000002;**<br/>             | Detiene todas [**las solicitudes**](https://www.bing.com/search?q=**Move**) move.                                               |
| **const unsigned long** **STOP TYPE SPEAK = \_ \_ 0x00000004;**<br/>            | Detiene todas las [**solicitudes speak.**](iagentcharacter--speak.md)                                              |
| **const unsigned long** **STOP TYPE PREPARE = \_ \_ 0x00000008;**<br/>          | Detiene todas las solicitudes [**de preparación en**](iagentcharacter--prepare.md) cola.                                   |
| **const unsigned long** **STOP TYPE \_ \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | Detiene todas las solicitudes de preparación que no [**están en**](iagentcharacter--prepare.md) cola.                               |
| **const unsigned long** **STOP TYPE VISIBLE = \_ \_ 0x00000020;**<br/>          | Detiene todas [**las solicitudes Ocultar**](iagentcharacter--hide.md) o Mostrar. [](iagentcharacter--show.md)       |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::Stop**](iagentcharacter--stop.md)


 

 





