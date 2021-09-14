---
title: BM_GETCHECK mensaje (Winuser.h)
description: Obtiene el estado de comprobación de un botón de radio o una casilla. Puede enviar este mensaje explícitamente o usar la \_ macro Button GetCheck.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK controles de Windows mensaje
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174006"
---
# <a name="bm_getcheck-message"></a>Mensaje \_ GETCHECK de BM

Obtiene el estado de comprobación de un botón de radio o una casilla. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetCheck.**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto de un botón creado con el estilo [**BS \_ AUTOCHECKBOX**](button-styles.md), [**BS \_ AUTORADIOBUTTON,**](button-styles.md) [**BS \_ AUTO3STATE,**](button-styles.md) [**BS \_ CHECKBOX,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)o [**BS \_ 3STATE**](button-styles.md) puede ser uno de los siguientes.



| Código devuelto                                                                                       | Descripción                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ CHECKED**</dt> </dl>       | El botón está activado.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ INDETERMINATE**</dt> </dl> | El botón está atenuado, lo que indica un estado indeterminado (solo se aplica si el botón tiene el estilo [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE).**](button-styles.md)<br/> |
| <dl> <dt>**BST \_ UNCHECKED**</dt> </dl>     | El botón está desactivado<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Si el botón tiene un estilo distinto de los enumerados, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





