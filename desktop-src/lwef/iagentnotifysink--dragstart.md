---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360722"
---
# <a name="iagentnotifysinkdragstart"></a>IAgentNotifySink::D ragStart

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

Notifica a una aplicación cliente cuando el usuario empieza a arrastrar un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter arrastrado.

</dd> <dt>

<span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*
</dt> <dd>

Parámetro que indica el botón del mouse y el estado de la tecla modificadora. El parámetro puede devolver cualquier combinación de lo siguiente:



| Value  | Descripción      |
|--------|------------------|
| 0x0001 | Botón izquierdo      |
| 0x0010 | Botón Central    |
| 0x0002 | Botón derecho     |
| 0x0004 | Mayús Key Down   |
| 0x0008 | Tecla De control hacia abajo |
| 0x0020 | Tecla Alt hacia abajo     |



 

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x del puntero del mouse en píxeles, en relación con el origen de la pantalla (esquina superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada y del puntero del mouse en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> </dl>

 

 




