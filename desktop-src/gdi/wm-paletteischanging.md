---
description: El mensaje de PALETTEISCHANGING de WM \_ informa a las aplicaciones de que una aplicación va a obtener su paleta lógica.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Mensaje de WM_PALETTEISCHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815526"
---
# <a name="wm_paletteischanging-message"></a>Mensaje de PALETTEISCHANGING de WM \_

El mensaje de **\_ PALETTEISCHANGING de WM** informa a las aplicaciones de que una aplicación va a obtener su paleta lógica.

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

Identificador de la ventana que va a obtener su paleta lógica.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

La aplicación que cambia su paleta no espera la confirmación de este mensaje antes de cambiar la paleta y enviar el mensaje de [**\_ PALETTECHANGED de WM**](wm-palettechanged.md) . Como resultado, es posible que la paleta ya haya cambiado en el momento en que una aplicación recibe este mensaje.

Si la aplicación pasa por alto o no puede procesar este mensaje y una segunda aplicación detecta su paleta mientras que la primera usa índices de paleta, existe la posibilidad de que el usuario vea colores inesperados durante las operaciones de dibujo posteriores.

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

[**QUERYNEWPALETTE de WM \_**](wm-querynewpalette.md)
</dt> </dl>

 

 
