---
title: RB_MAXIMIZEBAND mensaje (Commctrl.h)
description: Cambia el tamaño de una banda de un control rebar a su tamaño ideal o mayor.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef02fbe9611c09d1932907c8218ffd169d3e18d10e0b07faa2b63d50058af1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770095"
---
# <a name="rb_maximizeband-message"></a>Mensaje \_ MAXIMIZEBAND de RB

Cambia el tamaño de una banda de un control rebar a su tamaño ideal o mayor.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda que se va a maximizar.

</dd> <dt>

*lParam* 
</dt> <dd>

Indica si se debe usar el ancho ideal de la banda cuando se maximiza la banda. Si este valor es distinto de cero, se usará el ancho ideal. Si este valor es cero, la banda se hará lo más grande posible.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





