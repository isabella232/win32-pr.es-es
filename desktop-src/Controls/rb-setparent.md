---
title: RB_SETPARENT mensaje (Commctrl.h)
description: Establece la ventana primaria de un control rebar.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- RB_SETPARENT controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167277"
---
# <a name="rb_setparent-message"></a>Mensaje \_ SETPARENT de RB

Establece la ventana primaria de un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana primaria que se va a establecer.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la ventana primaria anterior o **NULL** si no hay ningún elemento primario anterior.

## <a name="remarks"></a>Observaciones

El control rebar envía mensajes de notificación a la ventana que especifique con este mensaje. Este mensaje no cambia realmente el elemento primario del control rebar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





