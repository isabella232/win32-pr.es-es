---
title: Mensaje de RB_PUSHCHEVRON (commctrl. h)
description: Se envía a un control rebar para presionar mediante programación un botón de contenido adicional.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534660"
---
# <a name="rb_pushchevron-message"></a>Mensaje de PUSHCHEVRON de RB \_

Se envía a un control rebar para presionar mediante programación un botón de contenido adicional.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda cuyo cheurón se va a insertar.

</dd> <dt>

*lParam* 
</dt> <dd>

Un valor de 32 bits definido por la aplicación. Se devolverá a la aplicación como el miembro **lParamNM** de la estructura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) que se pasa con la notificación [ \_ CHEVRONPUSHED RBN](rbn-chevronpushed.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Cuando se envía este mensaje, el control rebar enviará a la aplicación un código de notificación [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) , que le pedirá que muestre el menú de comillas angulares.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





