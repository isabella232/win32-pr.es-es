---
description: Asocia un nuevo icono grande o pequeño a una ventana. El sistema muestra el icono grande en el cuadro de diálogo ALT + TAB y el icono pequeño en el título de la ventana.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Mensaje de WM_SETICON (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276846"
---
# <a name="wm_seticon-message"></a>Mensaje de SETICON de WM \_

Asocia un nuevo icono grande o pequeño a una ventana. El sistema muestra el icono grande en el cuadro de diálogo ALT + TAB y el icono pequeño en el título de la ventana.


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de icono que se va a establecer. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                       | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Icono \_ de BIG**</dt> <dt>1</dt> </dl>       | Establezca el icono grande para la ventana.<br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Icono \_ de PEQUEÑO**</dt> <dt>0</dt> </dl> | Establezca el icono pequeño de la ventana.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para el nuevo icono grande o pequeño. Si este parámetro es **null**, se quita el icono indicado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

El valor devuelto es un identificador del icono grande o pequeño anterior, dependiendo del valor de *wParam*. Es **null** si la ventana no tenía previamente ningún icono del tipo indicado por *wParam*.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve un identificador al icono grande o pequeño anterior asociado a la ventana, dependiendo del valor de *wParam*.

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

[**GETICON de WM \_**](wm-geticon.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
