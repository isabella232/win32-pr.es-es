---
title: Mensaje de RB_SETPARENT (commctrl. h)
description: Establece la ventana primaria de un control rebar.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- RB_SETPARENT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905417"
---
# <a name="rb_setparent-message"></a>Mensaje de el SETPARENT de RB \_

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

Devuelve el identificador de la ventana primaria anterior o **null** si no hay ningún elemento primario anterior.

## <a name="remarks"></a>Observaciones

El control rebar envía mensajes de notificación a la ventana que se especifica con este mensaje. En realidad, este mensaje no cambia el elemento primario del control rebar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





