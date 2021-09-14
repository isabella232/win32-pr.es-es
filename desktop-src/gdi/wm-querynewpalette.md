---
description: El mensaje WM QUERYNEWPALETTE informa a una ventana de que está a punto de recibir el foco del teclado, lo que ofrece a la ventana la oportunidad de realizar su paleta lógica cuando recibe \_ el foco.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: WM_QUERYNEWPALETTE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269519"
---
# <a name="wm_querynewpalette-message"></a>WM \_ QUERYNEWPALETTE message

El **mensaje \_ WM QUERYNEWPALETTE** informa a una ventana de que está a punto de recibir el foco del teclado, lo que ofrece a la ventana la oportunidad de realizar su paleta lógica cuando recibe el foco.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la ventana se da cuenta de su paleta lógica, debe devolver **TRUE**; de lo contrario, debe devolver **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general sobre colores](colors.md)
</dt> <dt>

[Mensajes de color](color-messages.md)
</dt> <dt>

[**PALETA \_ WMCHANGED**](wm-palettechanged.md)
</dt> <dt>

[**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md)
</dt> </dl>

 

 
