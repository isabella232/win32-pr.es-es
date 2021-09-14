---
title: RB_PUSHCHEVRON mensaje (Commctrl.h)
description: Se envía a un control rebar para insertar mediante programación un botón de contenido adicional.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167297"
---
# <a name="rb_pushchevron-message"></a>Mensaje \_ PUSHCHEVRON de RB

Se envía a un control rebar para insertar mediante programación un botón de contenido adicional.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda cuyo botón de contenido adicional se va a insertar.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor de 32 bits definido por la aplicación. Se volverá a pasar a la aplicación como miembro **lParamNM** de la estructura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) que se pasa con la notificación [ \_ RBN CHEVRONPUSHED.](rbn-chevronpushed.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Cuando se envía este mensaje, el control rebar enviará a la aplicación un código de notificación [ \_ RBN CHEVRONPUSHED,](rbn-chevronpushed.md) en el que se le pedirá que muestre el menú de contenido adicional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





