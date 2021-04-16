---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714207"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter:: StopAll

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Detiene todas las animaciones (solicitudes) y las quita de la cola de animaciones del carácter.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

Un campo de bits que indica los tipos de solicitudes que se van a detener (y quitar de la cola del carácter), que se componen de lo siguiente:



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **const unsigned Long** **Stop \_ Type \_ All = 0xFFFFFFFF;**<br/>              | Detiene todas las solicitudes de animación, incluidas las solicitudes de [**preparación**](iagentcharacter--prepare.md) no en cola. |
| **const unsigned Long** **Stop \_ Type \_ Play = 0x00000001;**<br/>             | Detiene todas las solicitudes de reproducción.                                                                                 |
| **const unsigned Long** **Stop \_ Type \_ Move = 0x00000002;**<br/>             | Detiene todas las solicitudes de [**movimiento**](https://www.bing.com/search?q=**Move**) .                                               |
| **const unsigned Long** **Stop \_ Escriba \_ Speak = 0x00000004;**<br/>            | Detiene todas las solicitudes de [**voz**](iagentcharacter--speak.md) .                                              |
| **const unsigned Long** **Stop \_ Escriba \_ Prepare = 0x00000008;**<br/>          | Detiene todas las solicitudes de [**preparación**](iagentcharacter--prepare.md) en cola.                                   |
| **const unsigned Long** **Stop \_ Type \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | Detiene todas las solicitudes de [**preparación**](iagentcharacter--prepare.md) no en cola.                               |
| **const unsigned Long** **Stop \_ Type \_ visible = 0x00000020;**<br/>          | Detiene todas las solicitudes [**Hide**](iagentcharacter--hide.md) o [**Show**](iagentcharacter--show.md) .       |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: Stop**](iagentcharacter--stop.md)


 

 





