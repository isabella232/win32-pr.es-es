---
title: Mensaje de RB_SIZETORECT (commctrl. h)
description: Intenta encontrar el mejor diseño de las bandas del rectángulo especificado.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151143"
---
# <a name="rb_sizetorect-message"></a>Mensaje de SIZETORECT de RB \_

Intenta encontrar el mejor diseño de las bandas del rectángulo especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica el rectángulo al que se debe ajustar el tamaño del control rebar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se ha producido un cambio de diseño o cero en caso contrario.

## <a name="remarks"></a>Observaciones

Las bandas rebar se organizarán y ajustarán según sea necesario para ajustarse al rectángulo. Se cambiará el tamaño de las bandas que tengan el estilo RBBS VARIABLEHEIGHT de la \_ manera más uniforme posible para ajustar el rectángulo. El alto de un rebar horizontal o el ancho de un rebar vertical puede cambiar en función del nuevo diseño.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

