---
title: TBM_GETNUMTICS mensaje (Commctrl.h)
description: Recupera el número de marcas de graduación de una barra de seguimiento.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- TBM_GETNUMTICS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d247dd49db4223cd61de3684bc2ea92d6d00c843416d4f9d5a8650e6eb8b85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046555"
---
# <a name="tbm_getnumtics-message"></a>Mensaje \_ GETNUMTICS de TBM

Recupera el número de marcas de graduación de una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si no [se establece](trackbar-control-styles.md) ninguna marca de graduación, devuelve 2 para los tics inicial y final. Si [**se establece \_ TBS NOTICKS,**](trackbar-control-styles.md) devuelve cero. De lo contrario, toma la diferencia entre el intervalo mínimo y máximo, divide por la frecuencia de tic y agrega 2.

## <a name="remarks"></a>Comentarios

El **mensaje \_ GETNUMTICS** de TBM cuenta todas las marcas de graduación, incluidas la primera y la última marca de graduación creadas por la barra de seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





