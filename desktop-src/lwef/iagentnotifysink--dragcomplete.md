---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63c24abd41f0509293ba2fafeb055f195a4d13ad354662e8d32d0fb1715e1fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477033"
---
# <a name="iagentnotifysinkdragcomplete"></a>IAgentNotifySink::D ragComplete

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Notifica a una aplicación cliente cuando el usuario deja de arrastrar un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter arrastrado.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Parámetro que indica el botón del mouse y el estado de la tecla modificadora. El parámetro puede devolver cualquier combinación de lo siguiente:



| Valor  | Descripción      |
|--------|------------------|
| 0x0001 | Botón izquierdo      |
| 0x0010 | Botón Central    |
| 0x0002 | Botón derecho     |
| 0x0004 | Mayús Key Down   |
| 0x0008 | Control de la tecla Abajo |
| 0x0020 | Alt tecla abajo     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada y del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> </dl>

 

 




