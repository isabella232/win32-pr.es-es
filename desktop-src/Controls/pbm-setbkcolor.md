---
title: PBM_SETBKCOLOR mensaje (Commctrl.h)
description: Establece el color de fondo en la barra de progreso.
ms.assetid: e28af958-babb-4c2e-9202-89b608c22f8e
keywords:
- PBM_SETBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ddfaf84695221cf998275d76a9d2d67773150da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167761"
---
# <a name="pbm_setbkcolor-message"></a>Mensaje \_ SETBKCOLOR de PBM

Establece el color de fondo en la barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valor COLORREF** que especifica el nuevo color de fondo. Especifique el valor DEFAULT de CLR \_ para que la barra de progreso use su color de fondo predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de fondo anterior o CLR \_ DEFAULT si el color de fondo es el predeterminado.

## <a name="remarks"></a>Observaciones

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





