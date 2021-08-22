---
title: TBM_SETTICFREQ mensaje (Commctrl.h)
description: Establece la frecuencia de intervalo de las marcas de graduación en una barra de seguimiento.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c1b3e029abc8027d8708da31698f44db85ec78e427ba9461f0a71a740fb05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078019"
---
# <a name="tbm_setticfreq-message"></a>Mensaje \_ TBM SETTICFREQ

Establece la frecuencia de intervalo de las marcas de graduación en una barra de seguimiento. Por ejemplo, si la frecuencia se establece en dos, se muestra una marca de graduación para cada otro incremento en el intervalo de la barra de seguimiento. El valor predeterminado para la frecuencia es uno; Es decir, cada incremento del intervalo está asociado a una marca de graduación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Frecuencia de las marcas de graduación.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La barra de seguimiento debe tener el [**estilo \_ TBS AUTOTICKS**](trackbar-control-styles.md) para usar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





