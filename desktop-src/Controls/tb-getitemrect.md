---
title: Mensaje de TB_GETITEMRECT (commctrl. h)
description: Recupera el rectángulo delimitador de un botón de una barra de herramientas.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905453"
---
# <a name="tb_getitemrect-message"></a>\_Mensaje GETITEMRECT TB

Recupera el rectángulo delimitador de un botón de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del botón para el que se va a recuperar información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe las coordenadas de cliente del rectángulo delimitador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje no recupera el rectángulo delimitador de los botones cuyo estado está establecido en el valor [**\_ oculto TBSTATE**](toolbar-button-states.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

