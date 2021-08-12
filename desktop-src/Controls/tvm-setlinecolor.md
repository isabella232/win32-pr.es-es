---
title: TVM_SETLINECOLOR mensaje (Commctrl.h)
description: El mensaje SETLINECOLOR de TVM \_ establece el color de línea actual.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af66e7a711611ff5e59ec0d68b58a24fb39399245437b0e5d81840c1c38b2d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669525"
---
# <a name="tvm_setlinecolor-message"></a>Mensaje \_ SETLINECOLOR de TVM

El **mensaje \_ SETLINECOLOR de TVM** establece el color de línea actual.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo color de línea. Use el valor DEFAULT de CLR \_ para restaurar los colores predeterminados del sistema.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de línea anterior.

## <a name="remarks"></a>Observaciones

Este mensaje solo cambia los colores de línea. Para cambiar los colores de "+" y "-" dentro de los botones, use el mensaje [**\_ SETTEXTCOLOR de TVM.**](tvm-settextcolor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





