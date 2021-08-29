---
title: TVM_GETLINECOLOR mensaje (Commctrl.h)
description: El mensaje GETLINECOLOR de TVM \_ obtiene el color de línea actual.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- TVM_GETLINECOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ed83649795ccbd9b41270272f5a8984ddf257c3f5881a0c0fb69232081974e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914005"
---
# <a name="tvm_getlinecolor-message"></a>Mensaje \_ GETLINECOLOR de TVM

El **mensaje \_ GETLINECOLOR de TVM** obtiene el color de línea actual.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de línea actual o el valor DEFAULT de CLR \_ si no se ha especificado ninguno.

## <a name="remarks"></a>Comentarios

Este mensaje solo recupera los colores de línea. Para recuperar los colores de "+" y "-" dentro de los botones, use el mensaje [**\_ GETTEXTCOLOR de TVM.**](tvm-gettextcolor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETLINECOLOR**](tvm-setlinecolor.md)
</dt> </dl>

 

 





