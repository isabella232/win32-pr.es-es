---
title: Mensaje de SB_GETPARTS (commctrl. h)
description: Recupera un recuento de los elementos de una ventana de estado. El mensaje también recupera la coordenada del borde derecho del número especificado de partes.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SB_GETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee0f33331c579490cf66a38b9ce6655215ae673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534833"
---
# <a name="sb_getparts-message"></a>\_Mensaje GETPARTS de SB

Recupera un recuento de los elementos de una ventana de estado. El mensaje también recupera la coordenada del borde derecho del número especificado de partes.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de elementos para los que se van a recuperar las coordenadas. Si este parámetro es mayor que el número de partes de la ventana, el mensaje solo recupera las coordenadas de los elementos existentes.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros que tiene el mismo número de elementos que las partes especificadas por *wParam*. Cada elemento de la matriz recibe la coordenada del cliente del borde derecho del elemento correspondiente. Si un elemento se establece en-1, la posición del borde derecho de esa parte se extiende hasta el borde derecho de la ventana. Para recuperar el número actual de partes, establezca este parámetro en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de partes de la ventana.

## <a name="remarks"></a>Observaciones

Este mensaje siempre devuelve el número de partes de la barra de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





