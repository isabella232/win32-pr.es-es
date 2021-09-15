---
description: El mensaje WM PALETTECHANGED se envía a todas las ventanas de nivel superior y superpuestas después de que la ventana con el foco de teclado haya realizado su paleta lógica, lo que cambia la \_ paleta del sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: WM_PALETTECHANGED mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474310"
---
# <a name="wm_palettechanged-message"></a>Mensaje \_ PALETTECHANGED de WM

El **mensaje \_ WM PALETTECHANGED** se envía a todas las ventanas de nivel superior y superpuestas después de que la ventana con el foco de teclado haya realizado su paleta lógica, lo que cambia la paleta del sistema. Este mensaje habilita una ventana que usa una paleta de colores, pero que no tiene el foco del teclado para realizar su paleta lógica y actualizar su área cliente.

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

Identificador de la ventana que hizo que la paleta del sistema cambiara.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje debe enviarse a todas las ventanas de nivel superior y superpuestas, incluida la que cambió la paleta del sistema. Si alguna ventana secundaria usa una paleta de colores, este mensaje también se debe pasar a ellas.

Para evitar la creación de un bucle infinito, una ventana que recibe este mensaje no debe darse cuenta de su paleta, a menos que determine que *wParam* no contiene su propio identificador de ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre colores](colors.md)
</dt> <dt>

[Mensajes de color](color-messages.md)
</dt> <dt>

[**PALETA \_ WMISCHANGING**](wm-paletteischanging.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
