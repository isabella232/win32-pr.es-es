---
title: TBM_GETCHANNELRECT mensaje (Commctrl.h)
description: Recupera el tamaño y la posición del rectángulo delimitador para el canal de una barra de seguimiento.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- TBM_GETCHANNELRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166529"
---
# <a name="tbm_getchannelrect-message"></a>Mensaje \_ GETCHANNELRECT de TBM

Recupera el tamaño y la posición del rectángulo delimitador para el canal de una barra de seguimiento. (El canal es el área sobre la que se mueve el control deslizante. Contiene el resaltado cuando se selecciona un intervalo).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) El mensaje rellena esta estructura con el rectángulo delimitador del canal, en coordenadas de cliente de la ventana de la barra de seguimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

