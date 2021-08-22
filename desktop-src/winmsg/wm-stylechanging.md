---
description: Se envía a una ventana cuando la función SetWindowLong está a punto de cambiar uno o varios de los estilos de la ventana.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: WM_STYLECHANGING mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26574f000c23c918bc0dfb14c5ddd0afcbc439939d6719b95da8024b4828f30b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705845"
---
# <a name="wm_stylechanging-message"></a>Mensaje \_ STYLECHANGING de WM

Se envía a una ventana cuando [**la función SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) está a punto de cambiar uno o varios de los estilos de la ventana.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si los estilos de la ventana o los estilos de ventana extendidos están cambiando. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                            | Significado                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <dt>**GWL \_ EXSTYLE**</dt> <dt>-20</dt> </dl> | Los estilos de ventana extendidos cambian.<br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <dt>**GWL \_ STYLE**</dt> <dt>-16</dt> </dl>       | Los estilos de ventana están cambiando.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contiene los nuevos estilos propuestos para la ventana. Una aplicación puede examinar los estilos y, si es necesario, cambiarlos.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[**ESTILO \_ WM MODIFICADO**](wm-stylechanged.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
