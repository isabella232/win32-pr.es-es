---
title: Mensaje de WM_MEASUREITEM (Winuser. h)
description: Se envía a la ventana propietaria de un cuadro combinado, un cuadro de lista, un control de vista de lista o un elemento de menú cuando se crea el control o el menú.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905396"
---
# <a name="wm_measureitem-message"></a>Mensaje de MEASUREITEM de WM \_

Se envía a la ventana propietaria de un cuadro combinado, un cuadro de lista, un control de vista de lista o un elemento de menú cuando se crea el control o el menú.

Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el valor del miembro **CtlID** de la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) señalada por el parámetro *lParam* . Este valor identifica el control que envió el mensaje de **\_ MEASUREITEM de WM** . Si el valor es cero, un menú envió el mensaje. Si el valor es distinto de cero, el mensaje se envió mediante un cuadro combinado o un cuadro de lista. Si el valor es distinto de cero y el valor del miembro **itemID** de **measureitemstruct (** al que apunta *lParam* es (uint) 1, el mensaje se envió mediante un campo de edición combinado.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contiene las dimensiones del elemento de menú o control dibujado por el propietario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **true**.

## <a name="remarks"></a>Observaciones

Cuando la ventana propietaria recibe el mensaje de **\_ MEASUREITEM de WM** , el propietario rellena la estructura [**measureitemstruct (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) señalada por el parámetro *lParam* del mensaje y devuelve; esto informa al sistema de las dimensiones del control. Si se crea un cuadro de lista o un cuadro combinado con el estilo [**lb \_ OwnerDrawVariable**](list-box-styles.md) o [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , este mensaje se envía al propietario de cada elemento del control; de lo contrario, este mensaje se envía una vez.

El sistema envía el mensaje de **WM \_ MEASUREITEM** a la ventana propietaria de cuadros combinados y cuadros de lista creados con el estilo OWNERDRAWFIXED antes de enviar el mensaje de [**\_ INITDIALOG de WM**](/windows/desktop/dlgbox/wm-initdialog) . Como resultado, cuando el propietario recibe este mensaje, el sistema no ha determinado aún el alto y el ancho de la fuente utilizada en el control. las llamadas de función y los cálculos que requieren estos valores deben aparecer en la función Main de la aplicación o biblioteca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**MEASUREITEMSTRUCT (**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**INITDIALOG de WM \_**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

