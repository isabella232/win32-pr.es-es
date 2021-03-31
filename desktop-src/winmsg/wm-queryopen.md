---
description: Se envía a un icono cuando el usuario solicita que la ventana se restaure a su tamaño y posición anteriores.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Mensaje de WM_QUERYOPEN (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082669"
---
# <a name="wm_queryopen-message"></a>Mensaje de QUERYOPEN de WM \_

Se envía a un icono cuando el usuario solicita que la ventana se restaure a su tamaño y posición anteriores.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Si se puede abrir el icono, una aplicación que procese este mensaje debe devolver **true**; de lo contrario, debería devolver **false** para evitar que se abra el icono.

## <a name="remarks"></a>Observaciones

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve **true**.

Al procesar este mensaje, la aplicación no debe realizar ninguna acción que provoque un cambio de activación o foco (por ejemplo, crear un cuadro de diálogo).

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
