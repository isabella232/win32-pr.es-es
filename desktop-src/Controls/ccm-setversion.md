---
title: CCM_SETVERSION mensaje (Commctrl.h)
description: Este mensaje se usa para informar al control de que espera un comportamiento asociado a una versión determinada.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION controles de Windows mensaje
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063372"
---
# <a name="ccm_setversion-message"></a>Mensaje \_ SETVERSION de CCM

Este mensaje se usa para informar al control de que espera un comportamiento asociado a una versión determinada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El número de versión.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la versión especificada en el mensaje **\_ SETVERSION de CCM** anterior. Si *wParam se* establece en un valor mayor que la versión del archivo DLL actual, devuelve -1.

## <a name="remarks"></a>Observaciones

En algunos casos, un control puede comportarse de forma diferente, dependiendo de la versión. Esto se aplica principalmente a los errores corregidos en versiones posteriores. El **mensaje \_ SETVERSION de CCM** permite informar al control de qué comportamiento se espera. Puede determinar qué versión ha especificado mediante el envío de un [**mensaje \_ GETVERSION de CCM.**](ccm-getversion.md) Para obtener un ejemplo de cómo usar este mensaje, vea [Custom Draw With List-View and Tree-View Controls](custom-draw.md).

Si ha instalado ComCtl32.dll versión 6, independientemente del valor que establezca en *wParam,* el mensaje **\_ SETVERSION** de CCM devuelve la versión 6.

> [!Note]  
> Este mensaje solo establece el número de versión del control al que se envía.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





