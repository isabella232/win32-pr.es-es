---
title: Mensaje de WM_MOUSEACTIVATE (Winuser. h)
description: Se envía cuando el cursor está en una ventana inactiva y el usuario presiona un botón del mouse. La ventana primaria recibe este mensaje solo si la ventana secundaria lo pasa a la función DefWindowProc.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- Entrada de mouse y teclado de mensaje de WM_MOUSEACTIVATE
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150154"
---
# <a name="wm_mouseactivate-message"></a>Mensaje de MOUSEACTIVATE de WM \_

Se envía cuando el cursor está en una ventana inactiva y el usuario presiona un botón del mouse. La ventana primaria recibe este mensaje solo si la ventana secundaria lo pasa a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana primaria de nivel superior de la ventana que se va a activar.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica el valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado del procesamiento del mensaje [**\_ NCHITTEST de WM**](wm-nchittest.md) . Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.

La palabra de orden superior especifica el identificador del mensaje de mouse que se genera cuando el usuario presionó un botón del mouse. El mensaje del mouse se descarta o se envía a la ventana, dependiendo del valor devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto especifica si se debe activar la ventana y si se debe descartar el identificador del mensaje del mouse. Debe ser uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                          | Descripción                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**MA \_ ACTIVAR**</dt> <dt>1</dt> </dl>         | Activa la ventana y no descarta el mensaje del mouse.<br/>         |
| <dl> <dt>**MA \_ ACTIVATEANDEAT**</dt> <dt>2</dt> </dl>   | Activa la ventana y descarta el mensaje del mouse.<br/>                 |
| <dl> <dt>**MA \_ Noactivate**</dt> <dt>3</dt> </dl>       | No activa la ventana y no descarta el mensaje del mouse.<br/> |
| <dl> <dt>**MA \_ NOACTIVATEANDEAT**</dt> <dt>4</dt> </dl> | No activa la ventana, pero descarta el mensaje del mouse.<br/>         |



 

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria de una ventana secundaria antes de que se produzca cualquier procesamiento. La ventana primaria determina si se debe activar la ventana secundaria. Si activa la ventana secundaria, la ventana primaria debe devolver **MA \_ noactivate** o **MA \_ NOACTIVATEANDEAT** para evitar que el sistema procese el mensaje más allá.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**NCHITTEST de WM \_**](wm-nchittest.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> </dl>

 

