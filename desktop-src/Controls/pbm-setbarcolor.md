---
title: PBM_SETBARCOLOR mensaje (Commctrl.h)
description: Establece el color de la barra de indicadores de progreso en el control de barra de progreso.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167766"
---
# <a name="pbm_setbarcolor-message"></a>Mensaje \_ SETBARCOLOR de PBM

Establece el color de la barra de indicadores de progreso en el control de barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **COLORREF que** especifica el nuevo color de la barra del indicador de progreso. Si se especifica el valor \_ DEFAULT de CLR, la barra de progreso usará su color de barra de indicador de progreso predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de la barra del indicador de progreso anterior o CLR DEFAULT si el color de la barra del \_ indicador de progreso es el color predeterminado.

## <a name="remarks"></a>Observaciones

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





