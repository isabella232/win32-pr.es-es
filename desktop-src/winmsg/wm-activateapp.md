---
description: Se envía cuando una ventana que pertenece a una aplicación diferente de la ventana activa está a punto de activarse. El mensaje se envía a la aplicación cuya ventana se está activando y a la aplicación cuya ventana se está desactivando.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: WM_ACTIVATEAPP mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466731"
---
# <a name="wm_activateapp-message"></a>Mensaje \_ DE WM ACTIVATEAPP

Se envía cuando una ventana que pertenece a una aplicación diferente de la ventana activa está a punto de activarse. El mensaje se envía a la aplicación cuya ventana se está activando y a la aplicación cuya ventana se está desactivando.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si la ventana se está activando o desactivando. Este parámetro es **TRUE si** se está activando la ventana; es **FALSE si** se está desactivando la ventana.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de subproceso. Si el *parámetro wParam* es **TRUE,** *lParam* es el identificador del subproceso propietario de la ventana que se está desactivando. Si *wParam es* **FALSE,** *lParam es* el identificador del subproceso propietario de la ventana que se está activando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

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

[**WM \_ ACTIVATE**](../inputdev/wm-activate.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
