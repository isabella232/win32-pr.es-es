---
title: RB_SIZETORECT mensaje (Commctrl.h)
description: Intenta encontrar el mejor diseño de las bandas para el rectángulo especificado.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167246"
---
# <a name="rb_sizetorect-message"></a>Mensaje \_ SIZETORECT de RB

Intenta encontrar el mejor diseño de las bandas para el rectángulo especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que especifica el rectángulo al que se debe cambiar el tamaño del control rebar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se produjo un cambio de diseño o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Las bandas de rebar se organizarán y ajustarán según sea necesario para ajustarse al rectángulo. Las bandas que tienen el estilo VARIABLEHEIGHT de RBBS se cambiarán de tamaño de la forma más uniforme \_ posible para ajustarse al rectángulo. El alto de un rebar horizontal o el ancho de una barra vertical pueden cambiar, dependiendo del nuevo diseño.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

