---
title: Mensaje de RB_SETPALETTE (commctrl. h)
description: Establece la paleta actual del control rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996721"
---
# <a name="rb_setpalette-message"></a>Mensaje de SETPALETTE de RB \_

Establece la paleta actual del control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

**HPALETTE** que especifica la nueva paleta que usará el control rebar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **HPALETTE** que especifica la paleta anterior del control rebar.

## <a name="remarks"></a>Observaciones

Es responsabilidad de la aplicación que envía este mensaje eliminar el **HPALETTE** que se pasa en este mensaje (vea [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). El control rebar no eliminará un conjunto de **HPALETTE** con este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETPALETTE RB**](rb-getpalette.md)
</dt> </dl>

 

