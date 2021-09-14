---
title: RB_GETBARINFO mensaje (Commctrl.h)
description: Recupera información sobre el control rebar y la lista de imágenes que usa.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- RB_GETBARINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167377"
---
# <a name="rb_getbarinfo-message"></a>Mensaje \_ GETBARINFO de RB

Recupera información sobre el control rebar y la lista de imágenes que usa.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) que recibirá la información del control rebar. Debe establecer el **miembro cbSize** de esta estructura en **sizeof**(REBARINFO) antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





