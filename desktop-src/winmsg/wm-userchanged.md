---
description: Se envía a todas las ventanas después de que el usuario haya iniciado o desactivado. Cuando el usuario inicia o cierra sesión, el sistema actualiza la configuración específica del usuario. El sistema envía este mensaje inmediatamente después de actualizar la configuración.
title: WM_USERCHANGED mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bb466e80070fe1be5cd7af7889fc5727c81f8caad89ad60c48c7a105b688fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705705"
---
# <a name="wm_userchanged-message"></a>Mensaje \_ USERCHANGED de WM

Se envía a todas las ventanas después de que el usuario haya iniciado o desactivado. Cuando el usuario inicia o cierra sesión, el sistema actualiza la configuración específica del usuario. El sistema envía este mensaje inmediatamente después de actualizar la configuración.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Este mensaje no se admite a Windows Vista.

 


```C++
#define WM_USERCHANGED                  0x0054
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

Tipo: **LRESULT**

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Visión general](windows.md)
</dt> </dl>

 

 
