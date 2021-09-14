---
title: EM_SHOWBALLOONTIP mensaje (Commctrl.h)
description: El mensaje EM \_ SHOWBALLOONTIP muestra una sugerencia de globo asociada a un control de edición.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- EM_SHOWBALLOONTIP controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062052"
---
# <a name="em_showballoontip-message"></a>Mensaje \_ EM SHOWBALLOONTIP

El **mensaje EM \_ SHOWBALLOONTIP** muestra una sugerencia de globo asociada a un control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) que contiene información sobre la sugerencia de globo que se mostrará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **TRUE.** De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[**Edición \_ de ShowBalloonTip**](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





