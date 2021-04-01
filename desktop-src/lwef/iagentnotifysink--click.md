---
title: IAgentNotifySink clic
description: IAgentNotifySink clic
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d1dccd838152503c603d158f043a0279d4b5c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075916"
---
# <a name="iagentnotifysinkclick"></a>IAgentNotifySink:: click

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Notifica a una aplicación cliente cuando el usuario hace clic en el icono de la barra de tareas de un carácter o un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter en el que se hizo clic.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Un parámetro que indica el botón del mouse y el estado de la tecla modificadora. El parámetro puede devolver cualquier combinación de lo siguiente:



|        |                                                |
|--------|------------------------------------------------|
| 0x0001 | Botón izquierdo                                    |
| 0x0010 | Botón central                                  |
| 0x0002 | Botón derecho                                   |
| 0x0004 | Tecla Mayús abajo                                 |
| 0x0008 | Tecla control abajo                               |
| 0x0020 | Tecla Alt abajo                                   |
| 0x1000 | Evento producido en el icono de la barra de tareas del carácter |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

Coordenada x del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*sí*
</dt> <dd>

Coordenada y del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> </dl>

Este evento se envía al cliente de entrada-activo del carácter. Si ninguno de los clientes del carácter es de entrada-activo, el servidor notifica al cliente activo del carácter. Si el carácter está visible, el servidor también hace que la entrada del cliente esté activa y envía [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md). Si el carácter está oculto, el carácter también se muestra automáticamente.

 

 




