---
title: Mensaje de TBM_GETTICPOS (commctrl. h)
description: Recupera la posición física actual de una marca de graduación en una barra de aumento.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658199"
---
# <a name="tbm_getticpos-message"></a>TBM \_ GETTICPOS

Recupera la posición física actual de una marca de graduación en una barra de aumento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero que identifica una marca de graduación. Las posiciones de las marcas de graduación primera y última no están directamente disponibles a través de este mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la distancia, en coordenadas de cliente, desde el lado izquierdo o superior del área de cliente de la barra de aumento hasta la marca de graduación especificada. El valor devuelto es la coordenada x de la marca de graduación de una barra de desplazamiento horizontal o la coordenada y de una barra de desplazamiento vertical. Si *wParam* no es un índice válido, el valor devuelto es-1.

## <a name="remarks"></a>Observaciones

Dado que la primera y la última marca de graduación no están disponibles a través de este mensaje, los índices válidos se desplazan desde su posición de paso en la barra de desplazamiento. Si la diferencia entre [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) y [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) es inferior a dos, no hay ningún índice válido y se producirá un error en este mensaje.

A continuación se muestra la relación entre las marcas de paso de una barra de aumento, los pasos disponibles a través de este mensaje y sus índices basados en cero.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





