---
description: Se envía cuando una aplicación solicita que se cree una ventana mediante una llamada a la función CreateWindowEx o CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Mensaje de WM_CREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706672"
---
# <a name="wm_create-message"></a>\_Crear mensaje de WM

Se envía cuando una aplicación solicita que se cree una ventana mediante una llamada a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . (El mensaje se envía antes de que se devuelva la función). El procedimiento de ventana de la ventana nueva recibe este mensaje después de crear la ventana, pero antes de que la ventana se vuelva visible.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contiene información sobre la ventana que se va a crear.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero para continuar con la creación de la ventana. Si la aplicación devuelve – 1, se destruye la ventana y la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) devuelve un identificador **nulo** .

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

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**NCCREATE de WM \_**](wm-nccreate.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
