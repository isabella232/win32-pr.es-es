---
title: LVM_GETUNICODEFORMAT mensaje (Commctrl.h)
description: Recupera la marca de formato de caracteres UNICODE para el control . Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetUnicodeFormat.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- LVM_GETUNICODEFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720a65baab8ec9c1ec3b311e49fe3672c97a0fba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061811"
---
# <a name="lvm_getunicodeformat-message"></a>Mensaje \_ GETUNICODEFORMAT de LVM

Recupera la marca de formato de caracteres UNICODE para el control . Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de formato Unicode del control. Si este valor es distinto de cero, el control usa caracteres Unicode. Si este valor es cero, el control usa caracteres ANSI.

## <a name="remarks"></a>Observaciones

Consulte los comentarios de [**CCM \_ GETUNICODEFORMAT para**](ccm-getunicodeformat.md) obtener una explicación de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LVM \_ SETUNICODEFORMAT**](lvm-setunicodeformat.md)
</dt> </dl>

 

 





