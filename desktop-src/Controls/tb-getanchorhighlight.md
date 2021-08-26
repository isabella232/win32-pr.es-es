---
title: TB_GETANCHORHIGHLIGHT mensaje (Commctrl.h)
description: Recupera la configuración de resaltado de delimitador para una barra de herramientas.
ms.assetid: 167d481c-8684-40eb-9323-cfa238be3643
keywords:
- TB_GETANCHORHIGHLIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eadee4fd029cfe8ffb43960070538cf6574ca3bb178829f65af1ddc0753b9ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919085"
---
# <a name="tb_getanchorhighlight-message"></a>Mensaje \_ DE TB GETANCHORHIGHLIGHT

Recupera la configuración de resaltado de delimitador para una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si se ha establecido el resaltado de delimitadores. Si este valor es distinto de cero, se habilita el resaltado de delimitadores. Si este valor es cero, se deshabilita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TB \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)
</dt> </dl>

 

 





