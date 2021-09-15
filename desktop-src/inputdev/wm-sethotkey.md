---
title: WM_SETHOTKEY mensaje (Winuser.h)
description: Se envía a una ventana para asociar una tecla de acceso activa a la ventana. Cuando el usuario presiona la tecla de acceso activo, el sistema activa la ventana.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- WM_SETHOTKEY entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572893"
---
# <a name="wm_sethotkey-message"></a>Mensaje \_ SETHOTKEY de WM

Se envía a una ventana para asociar una tecla de acceso activa a la ventana. Cuando el usuario presiona la tecla de acceso activo, el sistema activa la ventana.


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo especifica el código de clave virtual que se asociará a la ventana.

La palabra de orden superior puede ser uno o varios de los valores siguientes de CommCtrl.h.

Si *se establece wParam* en **NULL,** se quita la tecla de acceso activa asociada a una ventana.



| Value                                                                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <dt>**HOTKEYF \_ Alt**</dt> <dt>0x04</dt> </dl>             | tecla ALT<br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <dt>**HOTKEYF \_ Control**</dt> <dt>0x02</dt> </dl> | Tecla CTRL<br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <dt>**HOTKEYF \_ Ext**</dt> <dt>0x08</dt> </dl>             | Clave extendida<br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <dt>**HOTKEYF \_ Mayús**</dt> <dt>0x01</dt> </dl>       | Tecla MAYÚS<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es uno de los siguientes.



| Valor devuelto                                                                  | Descripción                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>-1</dt> </dl> | La función no es correcta; la tecla de acceso no es válida.<br/>                        |
| <dl> <dt>0</dt> </dl>  | La función no es correcta; la ventana no es válida.<br/>                         |
| <dl> <dt>1</dt> </dl>  | La función se realiza correctamente y ninguna otra ventana tiene la misma clave activa.<br/>        |
| <dl> <dt>2</dt> </dl>  | La función se realiza correctamente, pero otra ventana ya tiene la misma clave activa.<br/> |



 

## <a name="remarks"></a>Observaciones

No se puede asociar una tecla de acceso activa a una ventana secundaria.

**VK \_ ESCAPE,** **VK \_ SPACE y** **VK \_ TAB** son teclas de acceso rápido no válidas.

Cuando el usuario presiona la tecla de acceso rápido, el sistema genera un mensaje [**\_ SYSCOMMAND wm**](/windows/desktop/menurc/wm-syscommand) con *wParam* igual a **SC \_ HOTKEY** y *lParam* igual al identificador de la ventana. Si este mensaje se pasa a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), el sistema llevará el último elemento emergente activo de la ventana (si existe) o la propia ventana (si no hay ninguna ventana emergente) al primer plano.

Una ventana solo puede tener una tecla de acceso activa. Si la ventana ya tiene asociada una tecla de acceso activa, la nueva tecla de acceso activa reemplaza a la antigua. Si más de una ventana tiene la misma tecla de acceso rápido, la ventana activada por la tecla de acceso rápido es aleatoria.

Estas teclas de acceso rápido no están relacionadas con las teclas de acceso rápido establecidas [**por RegisterHotKey.**](/windows/win32/api/winuser/nf-winuser-registerhotkey)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GETHOTKEY**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

