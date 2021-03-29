---
description: Se envía a una ventana cuando la ventana está a punto de ocultarse o mostrarse.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Mensaje de WM_SHOWWINDOW (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360713"
---
# <a name="wm_showwindow-message"></a>Mensaje de WM \_ SHOWWINDOW

Se envía a una ventana cuando la ventana está a punto de ocultarse o mostrarse.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si se muestra una ventana. Si *wParam* es **true**, se muestra la ventana. Si *wParam* es **false**, se oculta la ventana.

</dd> <dt>

*lParam* 
</dt> <dd>

Estado de la ventana que se va a mostrar. Si *lParam* es cero, el mensaje se envió debido a una llamada a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) ; de lo contrario, *lParam* es uno de los valores siguientes.



| Value                                                                                                                                                                                                                         | Significado                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <dt>**SW \_ OTHERUNZOOM**</dt> <dt>4</dt> </dl>       | La ventana se está descubriendo porque se restauró o se minimizó una ventana de maximizar.<br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <dt>**SW \_ OTHERZOOM**</dt> <dt>2</dt> </dl>             | La ventana está en el ámbito de otra ventana que se ha maximizado.<br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <dt>**SW \_ PARENTCLOSING**</dt> <dt>1</dt> </dl> | La ventana propietaria de la ventana se está minimizando.<br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <dt>**SW \_ PARENTOPENING**</dt> <dt>3</dt> </dl> | La ventana propietaria de la ventana se está restaurando.<br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oculta o muestra la ventana, tal como se especifica en el mensaje. Si una ventana tiene el [**estilo \_ visible de WS**](window-styles.md) cuando se crea, la ventana recibe este mensaje después de crearlo, pero antes de que se muestre. Una ventana también recibe este mensaje cuando la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) o [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) cambia su estado de visibilidad.

El **mensaje \_ SHOWWINDOW de WM** no se envía en las siguientes circunstancias:

-   Cuando se crea una ventana superpuesta de nivel superior con el estilo [**WS \_ Maximize**](window-styles.md) o **WS \_ miniMIZE** .
-   Cuando se especifica la marca **SW \_ SHOWNORMAL** en la llamada a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .

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

[**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
