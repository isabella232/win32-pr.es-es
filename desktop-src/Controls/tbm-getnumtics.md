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
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166518"
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

Si no [se establece ninguna](trackbar-control-styles.md) marca de graduación, devuelve 2 para los tics inicial y final. Si [**se establece \_ TBS NOTICKS,**](trackbar-control-styles.md) devuelve cero. De lo contrario, toma la diferencia entre el intervalo mínimo y máximo, divide por la frecuencia de paso y agrega 2.

## <a name="remarks"></a>Observaciones

El **mensaje \_ GETNUMTICS** de TBM cuenta todas las marcas de graduación, incluidas la primera y la última marca de graduación creadas por la barra de seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





