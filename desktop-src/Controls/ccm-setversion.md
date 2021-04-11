---
title: Mensaje de CCM_SETVERSION (commctrl. h)
description: Este mensaje se utiliza para informar al control de que está esperando un comportamiento asociado a una versión determinada.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079534"
---
# <a name="ccm_setversion-message"></a>\_Mensaje SETVERSION de CCM

Este mensaje se utiliza para informar al control de que está esperando un comportamiento asociado a una versión determinada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El número de versión.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la versión especificada en el mensaje **\_ SETVERSION de CCM** anterior. Si *wParam* se establece en un valor mayor que la versión del archivo dll actual, devuelve-1.

## <a name="remarks"></a>Observaciones

En algunos casos, es posible que un control se comporte de forma diferente, dependiendo de la versión. Esto se aplica principalmente a errores corregidos en versiones posteriores. El **mensaje \_ SETVERSION de CCM** le permite informar al control del comportamiento que se espera. Puede determinar qué versión ha especificado mediante el envío de un mensaje de [**\_ GETVERSION de CCM**](ccm-getversion.md) . Para obtener un ejemplo de cómo usar este mensaje, vea [dibujo personalizado con controles de List-View y Tree-View](custom-draw.md).

Si tiene instalada la versión 6 de ComCtl32.dll, independientemente del valor que establezca en *wParam*, el **mensaje \_ SETVERSION de CCM** devuelve la versión 6.

> [!Note]  
> Este mensaje solo establece el número de versión del control al que se envía.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





