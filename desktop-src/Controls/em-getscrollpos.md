---
title: EM_GETSCROLLPOS mensaje (Richedit.h)
description: Obtiene la posición de desplazamiento actual del control de edición.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42bde137096ae3c13582017f91b82c1eb9100097bb76f0d1babb91fa47b52196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800035"
---
# <a name="em_getscrollpos-message"></a>Mensaje \_ EM GETSCROLLPOS

Obtiene la posición de desplazamiento actual del control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT.**](/previous-versions//dd162805(v=vs.85)) Después de **llamar a EM \_ GETSCROLLPOS**, estos parámetros contienen un punto en el espacio de texto virtual del documento, expresado en píxeles. Este punto será el que se encuentra actualmente en la esquina superior izquierda de la ventana de control de edición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve 1.

## <a name="remarks"></a>Comentarios

Los valores devueltos en la [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) son valores de 16 bits (incluso en los campos de 32 bits).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

