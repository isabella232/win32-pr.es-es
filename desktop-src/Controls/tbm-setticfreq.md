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
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166410"
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

## <a name="remarks"></a>Observaciones

La barra de seguimiento debe tener el [**estilo \_ TBS AUTOTICKS**](trackbar-control-styles.md) para usar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





