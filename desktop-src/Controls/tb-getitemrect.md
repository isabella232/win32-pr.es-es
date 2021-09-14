---
title: TB_GETITEMRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador de un botón de una barra de herramientas.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166794"
---
# <a name="tb_getitemrect-message"></a>Mensaje \_ DE TB GETITEMRECT

Recupera el rectángulo delimitador de un botón de una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del botón para el que se va a recuperar información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibe las coordenadas de cliente del rectángulo delimitador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Observaciones

Este mensaje no recupera el rectángulo delimitador para los botones cuyo estado se establece en el [**valor TBSTATE \_ HIDDEN.**](toolbar-button-states.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

