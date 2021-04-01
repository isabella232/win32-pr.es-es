---
title: Mensaje de SBM_GETRANGE (Winuser. h)
description: El \_ mensaje SBM GETRANGE se envía para recuperar los valores de posición mínimo y máximo del control de barra de desplazamiento.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- SBM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996804"
---
# <a name="sbm_getrange-message"></a>\_Mensaje GETRANGE SBM

El mensaje **SBM \_ GETRANGE** se envía para recuperar los valores de posición mínimo y máximo del control de barra de desplazamiento.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **GetScrollRange** funcione correctamente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una variable que recibe la posición de desplazamiento mínima.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una variable que recibe la posición de desplazamiento máxima.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

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

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SetRange**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

