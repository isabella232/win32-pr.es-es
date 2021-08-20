---
description: Se envía a un icono cuando el usuario solicita que la ventana se restaure a su tamaño y posición anteriores.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: WM_QUERYOPEN mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184b18c1cfb364a475aeb13fd197d804a5c73dec66b89a142ea0e674fed2c407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030871"
---
# <a name="wm_queryopen-message"></a>MENSAJE \_ WM QUERYOPEN

Se envía a un icono cuando el usuario solicita que la ventana se restaure a su tamaño y posición anteriores.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_QUERYOPEN                    0x0013
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

Si se puede abrir el icono, una aplicación que procesa este mensaje debe devolver **TRUE**; De lo contrario, debe devolver **FALSE** para evitar que se abra el icono.

## <a name="remarks"></a>Comentarios

De forma predeterminada, [**la función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve **TRUE.**

Al procesar este mensaje, la aplicación no debe realizar ninguna acción que pueda provocar un cambio de activación o foco (por ejemplo, crear un cuadro de diálogo).

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
