---
title: BM_GETSTATE mensaje (Winuser.h)
description: Recupera el estado de un botón o una casilla. Puede enviar este mensaje explícitamente o usar la \_ macro Button GetState.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd44921c61477e26cd5570fcbaa6f96a4e61f96ee22ad1c705bf553788d8cfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674845"
---
# <a name="bm_getstate-message"></a>Mensaje \_ GETSTATE de BM

Recupera el estado de un botón o una casilla. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetState.**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)

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

El valor devuelto especifica el estado actual del botón. Es una combinación de los siguientes valores.



| Código devuelto                                                                                        | Descripción                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ CHECKED**</dt> </dl>        | El botón está activado.<br/>                                                                                                                                                                                        |
| <dl> <dt>**LISTA DESPLEGABLE \_ BSTPUSHED**</dt> </dl> | [Windows Vista](common-control-versions.md). El botón está en estado desplegable. Solo se aplica si el botón tiene el [**estilo DE LISTA \_ DESPLEGABLE TBSTYLE.**](toolbar-control-and-button-styles.md)<br/> |
| <dl> <dt>**BST \_ FOCUS**</dt> </dl>          | El botón tiene el foco del teclado.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ HOT**</dt> </dl>            | El botón está en caliente; es decir, el mouse se mantiene sobre él.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ INDETERMINATE**</dt> </dl>  | El estado del botón es indeterminado. Solo se aplica si el botón tiene el [**estilo BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE.**](button-styles.md)<br/>                    |
| <dl> <dt>**BST \_ PUSHED**</dt> </dl>         | El botón se muestra en estado presionado.<br/>                                                                                                                                                                |
| <dl> <dt>**BST \_ UNCHECKED**</dt> </dl>      | Ningún estado especial. Equivalente a cero.<br/>                                                                                                                                                                         |



 

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

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





