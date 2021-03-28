---
description: El mensaje de QUERYNEWPALETTE de WM \_ informa a una ventana de que está a punto de recibir el foco de teclado, lo que permite a la ventana tener la oportunidad de obtener su paleta lógica cuando recibe el foco.
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: Mensaje de WM_QUERYNEWPALETTE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985338"
---
# <a name="wm_querynewpalette-message"></a>Mensaje de QUERYNEWPALETTE de WM \_

El mensaje de **\_ QUERYNEWPALETTE de WM** informa a una ventana de que está a punto de recibir el foco de teclado, lo que permite a la ventana tener la oportunidad de obtener su paleta lógica cuando recibe el foco.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Si la ventana detecta su paleta lógica, debe devolver **true**; de lo contrario, debe devolver **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre colores](colors.md)
</dt> <dt>

[Mensajes de color](color-messages.md)
</dt> <dt>

[**PALETTECHANGED de WM \_**](wm-palettechanged.md)
</dt> <dt>

[**PALETTEISCHANGING de WM \_**](wm-paletteischanging.md)
</dt> </dl>

 

 
