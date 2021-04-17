---
title: Mensaje de WM_MENUDRAG (Winuser. h)
description: Se envía al propietario de un menú de arrastrar y colocar cuando el usuario arrastra un elemento de menú.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714650"
---
# <a name="wm_menudrag-message"></a>Mensaje de MENUDRAG de WM \_

Se envía al propietario de un menú de arrastrar y colocar cuando el usuario arrastra un elemento de menú.


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Posición del elemento donde comenzó la operación de arrastre.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del menú que contiene el elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación debe devolver uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                   | Descripción                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**MND \_ CONTINUAR**</dt> <dt>0</dt> </dl> | El menú debe permanecer activo. Si se suelta el mouse, debe omitirse.<br/> |
| <dl> <dt>**MND \_ ENDMENU**</dt> <dt>1</dt> </dl>  | El menú debe finalizar.<br/>                                                      |



 

## <a name="remarks"></a>Observaciones

La aplicación puede llamar a la función [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) en respuesta a este mensaje.

Para crear un menú de arrastrar y colocar, llame a [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) con **mns \_ DRAGDROP**.

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

[**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

**Vista**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

