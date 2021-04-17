---
title: Mensaje de BM_SETSTATE (Winuser. h)
description: Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera insertado. Puede enviar este mensaje explícitamente o usar la macro de botón \_ SetState.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656499"
---
# <a name="bm_setstate-message"></a>Mensaje de BM \_ SETSTATE

Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera insertado. Puede enviar este mensaje explícitamente o usar la macro de [**botón \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un **booleano** que especifica si el botón está resaltado. Un valor de **true** resalta el botón. Un valor **false** quita cualquier resaltado.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve cero.

## <a name="remarks"></a>Observaciones

El resaltado solo afecta a la apariencia de un botón. No tiene ningún efecto en el estado de activación de un botón de radio o casilla.

Un botón se resalta automáticamente cuando el usuario coloca el cursor sobre él y presiona y mantiene presionado el botón primario del mouse. El resaltado se quita cuando el usuario suelta el botón del mouse.

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

 

 





