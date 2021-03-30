---
title: Mensaje de TBM_SETTICFREQ (commctrl. h)
description: Establece la frecuencia de intervalo para las marcas de graduación en una barra de aumento.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079122"
---
# <a name="tbm_setticfreq-message"></a>TBM \_ SETTICFREQ

Establece la frecuencia de intervalo para las marcas de graduación en una barra de aumento. Por ejemplo, si la frecuencia se establece en dos, se muestra una marca de graduación para cada incremento en el intervalo de la barra de aumento. El valor predeterminado de la frecuencia es uno; es decir, cada incremento del intervalo está asociado a una marca de graduación.

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

La barra de aumento debe tener el estilo de [**\_ marcas de graduación de TBS**](trackbar-control-styles.md) para utilizar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





