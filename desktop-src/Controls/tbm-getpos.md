---
title: TBM_GETPOS mensaje (Commctrl.h)
description: Recupera la posición lógica actual del control deslizante en una barra de seguimiento. Las posiciones lógicas son los valores enteros del intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166505"
---
# <a name="tbm_getpos-message"></a>Mensaje \_ GETPOS de TBM

Recupera la posición lógica actual del control deslizante en una barra de seguimiento. Las posiciones lógicas son los valores enteros del intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica la posición lógica actual del control deslizante de la barra de seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ SETPOS**](tbm-setpos.md)
</dt> </dl>

 

 





