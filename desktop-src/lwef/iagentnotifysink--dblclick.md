---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88193f228f94d24384e6bf2b874e9208d67f3e9c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120928"
---
# <a name="iagentnotifysinkdblclick"></a>IAgentNotifySink::D blClick

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

Notifica a una aplicación cliente cuando el usuario hace doble clic en un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter con doble clic.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Parámetro que indica el botón del mouse y el estado de la tecla modificadora. El parámetro puede devolver cualquier combinación de lo siguiente:



| Valor  | Descripción                               |
|--------|------------------------------------------------|
| 0x0001 | Botón izquierdo                                    |
| 0x0010 | Botón Central                                  |
| 0x0002 | Botón derecho                                   |
| 0x0004 | Mayús Key Down                                 |
| 0x0008 | Control de la tecla Abajo                               |
| 0x0020 | Alt tecla abajo                                   |
| 0x1000 | Evento en el icono de la barra de tareas del carácter |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada y del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> </dl>

Este evento se envía al cliente activo de entrada del carácter. Si ninguno de los clientes del carácter está activo de entrada, el servidor notifica al cliente activo del carácter. Si el carácter está visible, el servidor también activa esa entrada de cliente y envía [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md). Si el carácter está oculto, el carácter también se muestra automáticamente.

 

 




