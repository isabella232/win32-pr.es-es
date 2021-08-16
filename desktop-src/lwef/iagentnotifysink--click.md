---
title: Clic en IAgentNotifySink
description: Clic en IAgentNotifySink
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154b35d85b86d1bd835275e93e6ea4c397b01240910066debd826c3570f806fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477081"
---
# <a name="iagentnotifysinkclick"></a>IAgentNotifySink::Click

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Notifica a una aplicación cliente cuando el usuario hace clic en el icono de la barra de tareas de un carácter o carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter en el que se ha hecho clic.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Parámetro que indica el botón del mouse y el estado de la tecla modificadora. El parámetro puede devolver cualquier combinación de lo siguiente:



| Valor  | Descripción                                    |
|--------|------------------------------------------------|
| 0x0001 | Botón izquierdo                                    |
| 0x0010 | Botón Central                                  |
| 0x0002 | Botón derecho                                   |
| 0x0004 | Mayús Key Down                                 |
| 0x0008 | Tecla De control hacia abajo                               |
| 0x0020 | Tecla Alt hacia abajo                                   |
| 0x1000 | Evento producido en el icono de la barra de tareas del carácter |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x del puntero del mouse en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada y del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> </dl>

Este evento se envía al cliente activo de entrada del carácter. Si ninguno de los clientes del carácter es de entrada-activo, el servidor notifica al cliente activo del carácter. Si el carácter está visible, el servidor también activa esa entrada de cliente y envía [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md). Si el carácter está oculto, el carácter también se muestra automáticamente.

 

 




