---
title: TB_SETTOOLTIPS mensaje (Commctrl.h)
description: Asocia un control de información sobre herramientas a una barra de herramientas.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- TB_SETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166557"
---
# <a name="tb_settooltips-message"></a>Mensaje \_ SETTOOLTIPS de TB

Asocia un control de información sobre herramientas a una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del control de información sobre herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los botones agregados a una barra de herramientas antes de enviar el **mensaje \_ SETTOOLTIPS** de TB no se registrarán con el control de información sobre herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





