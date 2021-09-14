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
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165621"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 





