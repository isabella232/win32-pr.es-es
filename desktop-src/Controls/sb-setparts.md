---
title: SB_SETPARTS mensaje (Commctrl.h)
description: Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167121"
---
# <a name="sb_setparts-message"></a>Mensaje \_ SB SETPARTS

Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de partes que se deben establecer (no puede ser mayor que 256).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de enteros. El número de elementos se especifica en *wParam*. Cada elemento especifica la posición, en coordenadas de cliente, del borde derecho de la parte correspondiente. Si un elemento es -1, el borde derecho de la parte correspondiente se extiende al borde de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





