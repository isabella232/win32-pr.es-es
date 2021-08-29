---
title: TCM_GETIMAGELIST mensaje (Commctrl.h)
description: Recupera la lista de imágenes asociada a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetImageList.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- TCM_GETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a8c91e5e88397ed436ae14c3500aadd6e450a14d168d1f6bb874c12b24da69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104895"
---
# <a name="tcm_getimagelist-message"></a>Mensaje \_ GETIMAGELIST de TCM

Recupera la lista de imágenes asociada a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes si se realiza correctamente o NULL en **caso** contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





