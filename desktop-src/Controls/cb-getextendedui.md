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
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062544"
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

## <a name="remarks"></a>Observaciones

De forma predeterminada, la tecla F4 abre o cierra la lista y la FLECHA ABAJO cambia la selección actual. En un cuadro combinado con la interfaz de usuario extendida, la tecla F4 está deshabilitada y al presionar la tecla FLECHA ABAJO se abre la lista desplegable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





