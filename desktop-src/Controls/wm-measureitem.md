---
title: WM_MEASUREITEM mensaje (Winuser.h)
description: Se envía a la ventana de propietario de un cuadro combinado, un cuadro de lista, un control de vista de lista o un elemento de menú cuando se crea el control o el menú.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165202"
---
# <a name="wm_measureitem-message"></a>Mensaje \_ MEASUREITEM de WM

Se envía a la ventana de propietario de un cuadro combinado, un cuadro de lista, un control de vista de lista o un elemento de menú cuando se crea el control o el menú.

Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el valor del miembro **CtlID** de la [**estructura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a la que apunta el *parámetro lParam.* Este valor identifica el control que envió el **mensaje \_ MEASUREITEM de WM.** Si el valor es cero, un menú envió el mensaje. Si el valor es distinto de cero, el mensaje lo envió un cuadro combinado o un cuadro de lista. Si el valor es distinto de cero y el valor del miembro **itemID** de **MEASUREITEMSTRUCT** al que *apunta lParam* es (UINT) 1, un campo de edición combinado envió el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) que contiene las dimensiones del elemento de menú o control dibujado por el propietario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver **TRUE**.

## <a name="remarks"></a>Observaciones

Cuando la ventana de propietario recibe el mensaje **\_ MEASUREITEM** de WM, el propietario rellena la estructura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a la que apunta el parámetro *lParam* del mensaje y devuelve; esto informa al sistema de las dimensiones del control. Si se crea un cuadro de lista o un cuadro combinado con el estilo [**LBS \_ OWNERDRAWVARIABLE**](list-box-styles.md) o [**CBS \_ OWNERDRAWVARIABLE,**](combo-box-styles.md) este mensaje se envía al propietario para cada elemento del control; de lo contrario, este mensaje se envía una vez.

El sistema envía el **mensaje \_ MEASUREITEM** de WM a la ventana de propietario de cuadros combinados y cuadros de lista creados con el estilo OWNERDRAWFIXED antes de enviar el [**mensaje WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) Como resultado, cuando el propietario recibe este mensaje, el sistema aún no ha determinado el alto y el ancho de la fuente utilizada en el control. Las llamadas de función y los cálculos que requieren estos valores deben producirse en la función principal de la aplicación o biblioteca.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

