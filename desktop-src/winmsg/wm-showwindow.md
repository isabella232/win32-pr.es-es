---
description: Se envía a una ventana cuando la ventana está a punto de ocultarse o mostrarse.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: WM_SHOWWINDOW mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251654"
---
# <a name="wm_showwindow-message"></a>Mensaje \_ DE WM SHOWWINDOW

Se envía a una ventana cuando la ventana está a punto de ocultarse o mostrarse.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si se muestra una ventana. Si *wParam* es **TRUE,** se muestra la ventana. Si *wParam* es **FALSE,** la ventana se está ocultando.

</dd> <dt>

*lParam* 
</dt> <dd>

Estado de la ventana que se muestra. Si *lParam* es cero, el mensaje se envió debido a una llamada a la [**función ShowWindow;**](/windows/win32/api/winuser/nf-winuser-showwindow) de lo contrario, *lParam* es uno de los valores siguientes.



| Value                                                                                                                                                                                                                         | Significado                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <dt>**SW \_ OTHERUNZOOM**</dt> <dt>4</dt> </dl>       | La ventana se está desvelando porque se restauró o minimizó una ventana de maximizar.<br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <dt>**SW \_ OTHERZOOM**</dt> <dt>2</dt> </dl>             | La ventana está siendo cubierta por otra ventana que se ha maximizado.<br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <dt>**SW \_ PARÉNTESIS**</dt> <dt>1</dt> </dl> | La ventana de propietario de la ventana se está minimizando.<br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <dt>**SW \_ PARENTOPENING**</dt> <dt>3</dt> </dl> | La ventana de propietario de la ventana se está restaurando.<br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oculta o muestra la ventana, tal y como especifica el mensaje. Si una ventana tiene el estilo VISIBLE de [**WS \_**](window-styles.md) cuando se crea, la ventana recibe este mensaje después de crearla, pero antes de que se muestre. Una ventana también recibe este mensaje cuando la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) o [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) cambia su estado de visibilidad.

El **mensaje \_ WM SHOWWINDOW** no se envía en las siguientes circunstancias:

-   Cuando se crea una ventana superpuesta de nivel superior con el estilo [**WS \_ MAXIMIZE**](window-styles.md) o **WS \_ MINIMIZE.**
-   Cuando se **especifica la marca SW \_ SHOWNORMAL** en la llamada a la [**función ShowWindow.**](/windows/win32/api/winuser/nf-winuser-showwindow)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
