---
title: RB_SETBARINFO mensaje (Commctrl.h)
description: Establece las características de un control rebar.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- RB_SETBARINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b360bc0b4d14963619aad8f769634d7dd0ad17e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167286"
---
# <a name="rb_setbarinfo-message"></a>Mensaje \_ SETBARINFO de RB

Establece las características de un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) que contiene la información que se va a establecer. Debe establecer el **miembro cbSize** de esta estructura en **sizeof**(REBARINFO) antes de enviar este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





