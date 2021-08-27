---
title: CB_GETEXTENDEDUI mensaje (Winuser.h)
description: Determina si un cuadro combinado tiene la interfaz de usuario predeterminada o la interfaz de usuario extendida.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05201b0986b114e97523716edacc6fe391908d3ed2841d36bf7578a6455f42a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089225"
---
# <a name="cb_getextendedui-message"></a>Mensaje \_ GETEXTENDEDUI de CB

Determina si un cuadro combinado tiene la interfaz de usuario predeterminada o la interfaz de usuario extendida.

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

Si el cuadro combinado tiene la interfaz de usuario extendida, el valor devuelto es **TRUE**; de lo contrario, es **FALSE.**

## <a name="remarks"></a>Comentarios

De forma predeterminada, la tecla F4 abre o cierra la lista y la FLECHA ABAJO cambia la selección actual. En un cuadro combinado con la interfaz de usuario extendida, la tecla F4 está deshabilitada y al presionar la tecla FLECHA ABAJO se abre la lista desplegable.

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

[**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





