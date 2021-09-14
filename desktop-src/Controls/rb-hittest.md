---
title: RB_HITTEST mensaje (Commctrl.h)
description: Determina qué parte de una banda de rebar se encuentra en un punto determinado de la pantalla, si existe una banda de rebar en ese momento.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167326"
---
# <a name="rb_hittest-message"></a>Mensaje \_ DE RB HITTEST

Determina qué parte de una banda de rebar se encuentra en un punto determinado de la pantalla, si existe una banda de rebar en ese momento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RBHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) Antes de enviar el mensaje, el **miembro pt** de esta estructura se debe inicializar hasta el punto en el que se va a comprobar la posición, en coordenadas de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero de la banda en el punto dado, o -1 si no había ninguna banda de rebar en el punto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





