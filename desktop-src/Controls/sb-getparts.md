---
title: SB_GETPARTS mensaje (Commctrl.h)
description: Recupera un recuento de las partes de una ventana de estado. El mensaje también recupera la coordenada del borde derecho del número de partes especificado.
ms.assetid: 2535f490-4d6b-468a-b13c-096941e61bf4
keywords:
- SB_GETPARTS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167157"
---
# <a name="sb_getparts-message"></a>Mensaje \_ SB GETPARTS

Recupera un recuento de las partes de una ventana de estado. El mensaje también recupera la coordenada del borde derecho del número de partes especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de partes para las que se recuperarán las coordenadas. Si este parámetro es mayor que el número de partes de la ventana, el mensaje recupera las coordenadas solo para las partes existentes.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros que tiene el mismo número de elementos que las partes especificadas por *wParam*. Cada elemento de la matriz recibe la coordenada de cliente del borde derecho de la parte correspondiente. Si un elemento se establece en -1, la posición del borde derecho de esa parte se extiende al borde derecho de la ventana. Para recuperar el número actual de partes, establezca este parámetro en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos de la ventana.

## <a name="remarks"></a>Observaciones

Este mensaje siempre devuelve el número de partes de la barra de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





