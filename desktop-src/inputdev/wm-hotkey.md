---
title: WM_HOTKEY mensaje (Winuser.h)
description: Se publica cuando el usuario presiona una tecla de acceso rápido registrada por la función RegisterHotKey. El mensaje se coloca en la parte superior de la cola de mensajes asociada al subproceso que registró la tecla de acceso activo.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- WM_HOTKEY entrada de teclado y mouse
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468824"
---
# <a name="wm_hotkey-message"></a>Mensaje \_ DE WM HOTKEY

Se publica cuando el usuario presiona una tecla de acceso rápido registrada por [**la función RegisterHotKey.**](/windows/win32/api/winuser/nf-winuser-registerhotkey) El mensaje se coloca en la parte superior de la cola de mensajes asociada al subproceso que registró la tecla de acceso activo.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la tecla de acceso que generó el mensaje. Si el mensaje se generó mediante una tecla de accesoso definida por el sistema, este parámetro será uno de los siguientes valores.



| Value                                                                                                                                                                                                                             | Significado                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_ SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | Se presionó la tecla de acceso rápido "Snap Desktop".<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_ SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | Se presionó la tecla de acceso rápido "snap window".<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica las teclas que se deben presionar en combinación con la clave especificada por la palabra de orden superior para generar el **mensaje WM \_ HOTKEY.** Esta palabra puede ser uno o varios de los valores siguientes. La palabra de orden superior especifica el código de clave virtual de la tecla de acceso.



| Value                                                                                                                                                                                                               | Significado                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**MOD \_ Alt**</dt> <dt>0x0001</dt> </dl>             | Se ha mantenido presionada cualquier tecla ALT.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**MOD \_ Control**</dt> <dt>0x0002</dt> </dl> | Se ha mantenido presionada la tecla CTRL.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**MOD \_ Mayús**</dt> <dt>0x0004</dt> </dl>       | Se ha mantenido o no la tecla MAYÚS.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**MOD \_ Win**</dt> <dt>0x0008</dt> </dl>             | Se ha mantenido o no la tecla WINDOWS. Estas claves se etiquetan con el logotipo Windows usuario. Las teclas de acceso rápido que implican Windows clave están reservadas para que las use el sistema operativo.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

**WM \_ HOTKEY no** está relacionado con las teclas de acceso rápido [**WM \_ GETHOTKEY**](wm-gethotkey.md) [**y WM \_ SETHOTKEY.**](wm-sethotkey.md) El **mensaje \_ WM HOTKEY se** envía para las teclas de acceso rápido genéricas, mientras que los mensajes WM **\_ SETHOTKEY** y **WM \_ GETHOTKEY** se relacionan con las teclas de acceso rápido de activación de ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GETHOTKEY**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SETHOTKEY**](wm-sethotkey.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

