---
title: Mensaje de BM_GETSTATE (Winuser. h)
description: Recupera el estado de un botón o una casilla. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetState.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE controles de mensajes de Windows
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
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995985"
---
# <a name="bm_getstate-message"></a>\_Mensaje GETSTATE de BM

Recupera el estado de un botón o una casilla. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) .

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

El valor devuelto especifica el estado actual del botón. Es una combinación de los siguientes valores.



| Código devuelto                                                                                        | Descripción                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ comprobado**</dt> </dl>        | El botón está activado.<br/>                                                                                                                                                                                        |
| <dl> <dt>**BST \_ DROPDOWNPUSHED**</dt> </dl> | [Windows Vista](common-control-versions.md). El botón está en el estado desplegable. Solo se aplica si el botón tiene el estilo [**\_ desplegable TBSTYLE**](toolbar-control-and-button-styles.md) .<br/> |
| <dl> <dt>**enfoque de BST \_**</dt> </dl>          | El botón tiene el foco de teclado.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ activo**</dt> </dl>            | El botón está activo; es decir, el mouse se mantiene sobre él.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ indeterminado**</dt> </dl>  | El estado del botón es indeterminado. Solo se aplica si el botón tiene el estilo [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) .<br/>                    |
| <dl> <dt>**BST \_ insertado**</dt> </dl>         | El botón se muestra en el estado insertado.<br/>                                                                                                                                                                |
| <dl> <dt>**BST \_ DESactivado**</dt> </dl>      | Sin estado especial. Equivalente a cero.<br/>                                                                                                                                                                         |



 

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

[**\_GETCHECK BM**](bm-getcheck.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





