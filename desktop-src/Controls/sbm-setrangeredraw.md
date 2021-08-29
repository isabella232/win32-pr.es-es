---
title: SBM_SETRANGEREDRAW mensaje (Winuser.h)
description: Una aplicación envía el mensaje SETRANGEREDRAW de SBM a un control de barra de desplazamiento para establecer los valores de posición mínimo y máximo y para \_ volver a dibujar el control.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- SBM_SETRANGEREDRAW controles de Windows mensaje
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70da860ac52e34a32ca72ae5c3cff36fe4a23feb7b0c78bdeac0294ff7d20df3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078519"
---
# <a name="sbm_setrangeredraw-message"></a>Mensaje \_ SETRANGEREDRAW de SBM

Una aplicación envía el mensaje **\_ SETRANGEREDRAW** de SBM a un control de barra de desplazamiento para establecer los valores de posición mínimo y máximo y para volver a dibujar el control.

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

**ComCtl32.dll versión 5.0:** si ha cambiado la posición del cuadro de desplazamiento, el valor devuelto es la posición anterior del cuadro de desplazamiento; de lo contrario, es cero.

**ComCtl32.dll versión 6.0:** la posición actual del cuadro de desplazamiento, independientemente de si ha cambiado.

## <a name="remarks"></a>Comentarios

Los valores de posición mínimo y máximo predeterminados son cero. La diferencia entre los valores especificados por los parámetros *wParam* y *lParam* no debe ser mayor que MAXLONG.

Si los valores de posición mínima y máxima son iguales, el control de barra de desplazamiento está oculto y, en efecto, deshabilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**SETRANGE de SBM \_**](sbm-setrange.md)
</dt> </dl>

 

 





