---
title: Mensaje de TBM_SETPOS (commctrl. h)
description: Establece la posición lógica actual del control deslizante en una barra de desplazamiento.
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e8da6e8e231a26b216ca8f9314d59474384857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997139"
---
# <a name="tbm_setpos-message"></a>TBM \_ SETPOS

Establece la posición lógica actual del control deslizante en una barra de desplazamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar el marcador. Si este parámetro es **true**, el mensaje vuelve a dibujar el control con el control deslizante en la posición especificada por *lParam*. Si este parámetro es **false**, el mensaje no vuelve a dibujar el control deslizante en la nueva posición. Tenga en cuenta que el mensaje establece el valor de la posición del control deslizante (tal y como lo devuelve el mensaje [**\_ GETPOS de TBM**](tbm-getpos.md) ), independientemente del parámetro *wParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Nueva posición lógica del control deslizante. Las posiciones lógicas válidas son los valores enteros en el intervalo de la barra de desplazamiento mínimo al máximo. Si este valor está fuera del intervalo máximo y mínimo del control, la posición se establece en el valor máximo o mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





