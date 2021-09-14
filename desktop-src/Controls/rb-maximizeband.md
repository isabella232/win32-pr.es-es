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
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167313"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





