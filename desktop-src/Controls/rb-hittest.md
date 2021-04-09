---
title: Mensaje de RB_HITTEST (commctrl. h)
description: Determina qué parte de una banda rebar se encuentra en un punto determinado de la pantalla, si existe una banda rebar en ese punto.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- RB_HITTEST controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078929"
---
# <a name="rb_hittest-message"></a>Mensaje de RB \_ HITTEST

Determina qué parte de una banda rebar se encuentra en un punto determinado de la pantalla, si existe una banda rebar en ese punto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) . Antes de enviar el mensaje, el miembro **PT** de esta estructura se debe inicializar en el punto en el que se realizará la prueba de posicionamiento, en coordenadas de cliente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de base cero de la banda en el punto especificado, o-1 si no hay ninguna banda rebar en el punto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





