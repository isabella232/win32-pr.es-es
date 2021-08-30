---
title: SBM_SETRANGE mensaje (Winuser.h)
description: El mensaje SETRANGE de SBM se envía para establecer los valores de posición mínimo y máximo \_ para el control de barra de desplazamiento.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- SBM_SETRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfac02c2a902e890b56e1d14d9ec4b300257e340340d72c6cf80e17488afe3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914325"
---
# <a name="sbm_setrange-message"></a>Mensaje \_ SETRANGE de SBM

El **mensaje \_ SETRANGE de SBM** se envía para establecer los valores de posición mínimo y máximo para el control de barra de desplazamiento.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben usar la [**función SetScrollRange.**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la **función SetScrollRange** funcione correctamente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica la posición de desplazamiento mínima.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica la posición de desplazamiento máxima.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**ComCtl32.dll versión 5.0:** si la posición del cuadro de desplazamiento ha cambiado, el valor devuelto es la posición anterior del cuadro de desplazamiento; de lo contrario, es cero.

**ComCtl32.dll versión 6.0:** la posición actual del cuadro de desplazamiento, independientemente de si ha cambiado.

## <a name="remarks"></a>Comentarios

Los valores de posición mínimo y máximo predeterminados son cero. La diferencia entre los valores especificados por los *parámetros wParam* e *lParam* no debe ser mayor que MAXLONG.

Si los valores de posición mínima y máxima son iguales, el control de barra de desplazamiento está oculto y, en efecto, deshabilitado.

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

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SETPOS de SBM \_**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

