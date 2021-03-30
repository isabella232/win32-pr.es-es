---
title: Mensaje de BM_GETCHECK (Winuser. h)
description: Obtiene el estado de activación de un botón de radio o casilla. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetCheck.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150982"
---
# <a name="bm_getcheck-message"></a>\_Mensaje GETCHECK de BM

Obtiene el estado de activación de un botón de radio o casilla. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto de un botón creado con el estilo [**BS \_ autocheckbox**](button-styles.md), [**BS \_ autoradiobutton**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), la [**\_ casilla**](button-styles.md)BS, el [**\_ RADIOBUTTON de BS**](button-styles.md)o [**BS \_ 3STATE**](button-styles.md) puede ser uno de los siguientes.



| Código devuelto                                                                                       | Descripción                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ comprobado**</dt> </dl>       | Está activado.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ indeterminado**</dt> </dl> | El botón está atenuado, lo que indica un estado indeterminado (solo se aplica si el botón tiene el estilo [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) ).<br/> |
| <dl> <dt>**BST \_ DESactivado**</dt> </dl>     | El botón está desactivado<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

Si el botón tiene un estilo distinto de los enumerados, el valor devuelto es cero.

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

[**\_GETSTATE BM**](bm-getstate.md)
</dt> <dt>

[**\_SETCHECK BM**](bm-setcheck.md)
</dt> </dl>

 

 





