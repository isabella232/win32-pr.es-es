---
title: TB_GETRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador de un botón de barra de herramientas especificado.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- TB_GETRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166773"
---
# <a name="tb_getrect-message"></a>Mensaje \_ GETRECT de TB

Recupera el rectángulo delimitador de un botón de barra de herramientas especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando del botón.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que recibirá la información del rectángulo delimitador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Este mensaje no recupera el rectángulo delimitador para los botones cuyo estado se establece en el [**valor TBSTATE \_ HIDDEN.**](toolbar-button-states.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

