---
title: Mensaje de SBM_GETPOS (Winuser. h)
description: El \_ mensaje SBM GETPOS se envía para recuperar la posición actual del cuadro de desplazamiento de un control de barra de desplazamiento.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996805"
---
# <a name="sbm_getpos-message"></a>\_Mensaje GETPOS SBM

El mensaje **SBM \_ GETPOS** se envía para recuperar la posición actual del cuadro de desplazamiento de un control de barra de desplazamiento. La posición actual es un valor relativo que depende del intervalo de desplazamiento actual. Por ejemplo, si el intervalo de desplazamiento es de 0 a 100 y el cuadro de desplazamiento está en el centro de la barra, la posición actual es 50.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **GetScrollPos** funcione correctamente.

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

El valor devuelto es la posición actual del cuadro de desplazamiento en la barra de desplazamiento.

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

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SetRange**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

