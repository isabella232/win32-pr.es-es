---
title: BM_SETCHECK mensaje (Winuser.h)
description: Establece el estado de comprobación de un botón de radio o una casilla. Puede enviar este mensaje explícitamente o mediante la macro Button \_ SetCheck.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- BM_SETCHECK controles de Windows mensaje
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 171515cb3c8498537bd0f9cc6d8c06017ff9d5d00f5505e193862f6cf9ebff76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674808"
---
# <a name="bm_setcheck-message"></a>Mensaje \_ DE BM SETCHECK

Establece el estado de comprobación de un botón de radio o una casilla. Puede enviar este mensaje explícitamente o mediante la macro [**Button \_ SetCheck.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estado de comprobación. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <dt>**BST \_ CHECKED**</dt> </dl>                   | Establece el estado del botón en activado.<br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <dt>**BST \_ INDETERMINATE**</dt> </dl> | Establece el estado del botón en atenuado, lo que indica un estado indeterminado. Use este valor solo si el botón tiene el estilo [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE.**](button-styles.md)<br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <dt>**BST \_ DESACTIVADO**</dt> </dl>             | Establece el estado del botón en desactivado.<br/>                                                                                                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve cero.

## <a name="remarks"></a>Observaciones

El **mensaje \_ BM SETCHECK** no tiene ningún efecto en los botones de inserción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**BM \_ GETCHECK**](bm-getcheck.md)
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





