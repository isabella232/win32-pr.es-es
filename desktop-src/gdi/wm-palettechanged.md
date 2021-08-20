---
description: El mensaje PALETTECHANGED de WM se envía a todas las ventanas de nivel superior y superpuestas después de que la ventana con el foco del teclado haya realizado su paleta lógica, lo que cambia la paleta \_ del sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: WM_PALETTECHANGED mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb706452e357f2e322b1f4e2618f0fd59c5c4d9a6606c07d18fae7c3b346323e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977925"
---
# <a name="wm_palettechanged-message"></a>Mensaje \_ PALETTECHANGED de WM

El **mensaje \_ PALETTECHANGED de WM** se envía a todas las ventanas de nivel superior y superpuestas después de que la ventana con el foco del teclado haya realizado su paleta lógica, lo que cambia la paleta del sistema. Este mensaje habilita una ventana que usa una paleta de colores, pero que no tiene el foco del teclado para realizar su paleta lógica y actualizar su área cliente.

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

## <a name="remarks"></a>Comentarios

Este mensaje debe enviarse a todas las ventanas de nivel superior y superpuestas, incluida la que cambió la paleta del sistema. Si alguna ventana secundaria usa una paleta de colores, este mensaje también se debe pasar a ellas.

Para evitar la creación de un bucle infinito, una ventana que recibe este mensaje no debe realizar su paleta, a menos que determine que *wParam* no contiene su propio identificador de ventana.

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

[**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
