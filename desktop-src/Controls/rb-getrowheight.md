---
title: Mensaje de RB_GETROWHEIGHT (commctrl. h)
description: Recupera el alto de una fila especificada en un control rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905400"
---
# <a name="rb_getrowheight-message"></a>Mensaje de GETROWHEIGHT de RB \_

Recupera el alto de una fila especificada en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de una banda. Se recuperará el alto de la fila que contiene la banda especificada.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **uint** que representa el alto de la fila, en píxeles.

## <a name="remarks"></a>Observaciones

Para recuperar el número de filas de un control rebar, utilice el mensaje de [**\_ ingetrowcount de RB**](rb-getrowcount.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





