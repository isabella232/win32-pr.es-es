---
title: TBM_GETTHUMBRECT mensaje (Commctrl.h)
description: Recupera el tamaño y la posición del rectángulo delimitador para el control deslizante en una barra de seguimiento.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d2582ccfb5276f65cbf1187458774622e62f6dd87d8dcadd2e16a7447f769a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046365"
---
# <a name="tbm_getthumbrect-message"></a>Mensaje \_ GETTHUMBRECT de TBM

Recupera el tamaño y la posición del rectángulo delimitador para el control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) El mensaje rellena esta estructura con el rectángulo delimitador del control deslizante de la barra de seguimiento en coordenadas de cliente de la ventana de la barra de seguimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

