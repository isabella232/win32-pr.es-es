---
title: LM_GETIDEALHEIGHT mensaje (Commctrl.h)
description: 'LM_GETIDEALHEIGHT mensaje: recupera el alto preferido de un vínculo para el ancho actual del control.'
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- LM_GETIDEALHEIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0cd4b56da08baefe36d9ce1d669c4dbc4939883005c1cd45e59760566b468b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920445"
---
# <a name="lm_getidealheight-message"></a>Mensaje \_ GETIDEALHEIGHT de LM

Recupera el alto preferido de un vínculo para el ancho actual del control.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Entero que representa el alto preferido del texto del vínculo, en píxeles.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





