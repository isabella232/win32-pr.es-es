---
description: El mensaje de PALETTECHANGED de WM \_ se envía a todas las ventanas de nivel superior y superpuestas después de que la ventana con el foco de teclado haya realizado su paleta lógica, lo que cambia la paleta del sistema.
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: Mensaje de WM_PALETTECHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813016"
---
# <a name="wm_palettechanged-message"></a>Mensaje de PALETTECHANGED de WM \_

El mensaje de **\_ PALETTECHANGED de WM** se envía a todas las ventanas de nivel superior y superpuestas después de que la ventana con el foco de teclado haya realizado su paleta lógica, lo que cambia la paleta del sistema. Este mensaje habilita una ventana que usa una paleta de colores, pero no tiene el foco de teclado para obtener su paleta lógica y actualizar su área cliente.

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

Identificador de la ventana que provocó el cambio de la paleta del sistema.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje debe enviarse a todas las ventanas superpuestas y de nivel superior, incluida la que cambió la paleta del sistema. Si alguna de las ventanas secundarias usa una paleta de colores, este mensaje también se debe pasar a ellos.

Para evitar la creación de un bucle infinito, una ventana que reciba este mensaje no debe obtener su paleta, a menos que determine que *wParam* no contiene su propio identificador de ventana.

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

[**PALETTEISCHANGING de WM \_**](wm-paletteischanging.md)
</dt> <dt>

[**QUERYNEWPALETTE de WM \_**](wm-querynewpalette.md)
</dt> </dl>

 

 
