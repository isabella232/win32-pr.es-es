---
description: Se envía cuando se va a activar una ventana que pertenece a una aplicación diferente de la ventana activa. El mensaje se envía a la aplicación cuya ventana se está activando y a la aplicación cuya ventana se está desactivando.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Mensaje de WM_ACTIVATEAPP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706679"
---
# <a name="wm_activateapp-message"></a>Mensaje de ACTIVATEAPP de WM \_

Se envía cuando se va a activar una ventana que pertenece a una aplicación diferente de la ventana activa. El mensaje se envía a la aplicación cuya ventana se está activando y a la aplicación cuya ventana se está desactivando.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si la ventana se está activando o desactivando. Este parámetro es **true** si la ventana se está activando; es **false** si la ventana se está desactivando.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de subproceso. Si el parámetro *wParam* es **true**, *lParam* es el identificador del subproceso que posee la ventana que se va a desactivar. Si *wParam* es **false**, *lParam* es el identificador del subproceso que posee la ventana que se está activando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

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

[**activación de WM \_**](../inputdev/wm-activate.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
