---
title: SB_SETBKCOLOR mensaje (Commctrl.h)
description: Establece el color de fondo en una barra de estado.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- SB_SETBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167126"
---
# <a name="sb_setbkcolor-message"></a>Mensaje \_ SB SETBKCOLOR

Establece el color de fondo en una barra de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valor COLORREF**](/windows/desktop/gdi/colorref) que especifica el nuevo color de fondo. Especifique el valor DEFAULT de CLR \_ para que la barra de estado use su color de fondo predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de fondo anterior o CLR \_ DEFAULT si el color de fondo es el predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

