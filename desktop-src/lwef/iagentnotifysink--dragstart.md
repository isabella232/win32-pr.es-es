---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031e78319beb0f62ddb0ea340fca0cd7ed88c0a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357122"
---
# <a name="iagentnotifysinkdragstart"></a>IAgentNotifySink::D ragStart

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Notifica a una aplicación cliente cuando el usuario comienza a arrastrar un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter arrastrado.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Un parámetro que indica el botón del mouse y el estado de la tecla modificadora. El parámetro puede devolver cualquier combinación de lo siguiente:



|        |                  |
|--------|------------------|
| 0x0001 | Botón izquierdo      |
| 0x0010 | Botón central    |
| 0x0002 | Botón derecho     |
| 0x0004 | Tecla Mayús abajo   |
| 0x0008 | Tecla control abajo |
| 0x0020 | Tecla Alt abajo     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

Coordenada x del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*sí*
</dt> <dd>

Coordenada y del puntero del mouse en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> </dl>

 

 




