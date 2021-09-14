---
title: TBM_GETTICPOS mensaje (Commctrl.h)
description: Recupera la posición física actual de una marca de graduación en una barra de seguimiento.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166478"
---
# <a name="tbm_getticpos-message"></a>Mensaje \_ GETTICPOS de TBM

Recupera la posición física actual de una marca de graduación en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero que identifica una marca de graduación. Las posiciones de la primera y la última marca de graduación no están disponibles directamente a través de este mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la distancia, en coordenadas de cliente, desde la izquierda o la parte superior del área cliente de la barra de seguimiento hasta la marca de graduación especificada. El valor devuelto es la coordenada x de la marca de graduación de una barra de seguimiento horizontal o la coordenada Y de una barra de seguimiento vertical. Si *wParam* no es un índice válido, el valor devuelto es -1.

## <a name="remarks"></a>Observaciones

Dado que la primera y la última marca de graduación no están disponibles a través de este mensaje, los índices válidos se desplazan desde su posición de tic en la barra de seguimiento. Si la diferencia entre [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) y [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) es menor que dos, no hay ningún índice válido y se producirá un error en este mensaje.

A continuación se muestra la relación entre los tics de una barra de seguimiento, los tics disponibles a través de este mensaje y sus índices de base cero.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





