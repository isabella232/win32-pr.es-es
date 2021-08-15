---
description: Se envía a una ventana después de que la función SetWindowLong haya cambiado uno o varios de los estilos de la ventana.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: WM_STYLECHANGED mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc84d3df087cb8667367830998675903a83f633eba4797e64125269d0c937c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705945"
---
# <a name="wm_stylechanged-message"></a>Mensaje \_ STYLECHANGED de WM

Se envía a una ventana después [**de que la función SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) haya cambiado uno o varios de los estilos de la ventana.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si los estilos de la ventana o los estilos de ventana extendidos han cambiado. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                            | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt> </dl> | Los estilos de ventana extendidos han cambiado.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STYLE**</dt> <dt>-16</dt> </dl>       | Los estilos de ventana han cambiado.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contiene los nuevos estilos de la ventana. Una aplicación puede examinar los estilos, pero no puede cambiarlos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**INTERCAMBIO \_ DE ESTILOS WM**](wm-stylechanging.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
