---
description: El mensaje WM PALETTEISCHANGING informa a las aplicaciones de que una \_ aplicación va a realizar su paleta lógica.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: WM_PALETTEISCHANGING mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0de17e7957e4b03c0a8fb942e7c0e4f94a3329e53cb039ce1d7f0a8c33aa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717685"
---
# <a name="wm_paletteischanging-message"></a>MENSAJE \_ DE WM PALETTEISCHANGING

El **mensaje \_ WM PALETTEISCHANGING** informa a las aplicaciones de que una aplicación va a realizar su paleta lógica.

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

Identificador de la ventana que va a realizar su paleta lógica.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

La aplicación que cambia su paleta no espera la confirmación de este mensaje antes de cambiar la paleta y enviar el [**mensaje \_ PALETTECHANGED de WM.**](wm-palettechanged.md) Como resultado, la paleta ya puede cambiarse en el momento en que una aplicación recibe este mensaje.

Si la aplicación omite o no puede procesar este mensaje y una segunda aplicación se da cuenta de su paleta mientras la primera usa índices de paleta, existe una gran posibilidad de que el usuario vea colores inesperados durante las operaciones de dibujo posteriores.

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

[**PALETA \_ WMCHANGED**](wm-palettechanged.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
