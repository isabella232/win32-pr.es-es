---
title: Mensaje de WM_HOTKEY (Winuser. h)
description: Se envía cuando el usuario presiona una tecla de acceso rápido registrada por la función RegisterHotKey. El mensaje se coloca en la parte superior de la cola de mensajes asociada al subproceso que registró la tecla de acceso rápido.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- Entrada de mouse y teclado de mensaje de WM_HOTKEY
topic_type:
- apiref
api_name:
- WM_HOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f09e81a964542a6a8166ae54a0df4d7127466c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422195"
---
# <a name="wm_hotkey-message"></a>Mensaje de Hotkey de WM \_

Se envía cuando el usuario presiona una tecla de acceso rápido registrada por la función [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) . El mensaje se coloca en la parte superior de la cola de mensajes asociada al subproceso que registró la tecla de acceso rápido.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El identificador de la tecla de acceso rápido que generó el mensaje. Si el mensaje se ha generado mediante una tecla de acceso rápido definida por el sistema, este parámetro tendrá uno de los valores siguientes.



| Value                                                                                                                                                                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_ SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | Se presionó la tecla de acceso rápido "ajustar escritorio".<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_ SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | Se presionó la tecla de acceso rápido "ventana de ajuste".<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica las teclas que se van a presionar en combinación con la clave especificada por la palabra de orden superior para generar el mensaje de **\_ Hotkey de WM** . Esta palabra puede ser uno o varios de los valores siguientes. La palabra de orden superior especifica el código de tecla virtual de la tecla de acceso rápido.



| Value                                                                                                                                                                                                               | Significado                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**Mod \_ ALT**</dt> <dt>0x0001</dt> </dl>             | Se ha mantenido presionada la tecla ALT.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**Mod \_**</dt> <dt>0X0002</dt> de control </dl> | Se ha mantenido presionada la tecla CTRL.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**Mod \_ SHIFT**</dt> <dt>0x0004</dt> </dl>       | Se ha mantenido presionada la tecla Mayús.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**Mod \_ WIN**</dt> <dt>0x0008</dt> </dl>             | Se ha mantenido la tecla WINDOWS. Estas claves se etiquetan con el logotipo de Windows. Las teclas de operación que implican la clave de Windows están reservadas para su uso por parte del sistema operativo.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

**WM \_ La tecla** de acceso rápido no está relacionada con las teclas de acceso rápido de [**WM \_ GETHOTKEY**](wm-gethotkey.md) y [**WM \_ SETHOTKEY**](wm-sethotkey.md) . El mensaje de **\_ Hotkey de WM** se envía para las teclas de acceso rápido genéricas mientras que los mensajes de **WM \_ SETHOTKEY** y **WM \_ GETHOTKEY** se relacionan con las teclas de acceso rápido de activación de la ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**GETHOTKEY de WM \_**](wm-gethotkey.md)
</dt> <dt>

[**SETHOTKEY de WM \_**](wm-sethotkey.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

