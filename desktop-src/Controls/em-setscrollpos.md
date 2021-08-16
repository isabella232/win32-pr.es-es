---
title: EM_SETSCROLLPOS mensaje (Richedit.h)
description: Desplaza el contenido de un control de edición enriquecido hasta el punto especificado.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d86609c1b3f4b04ade24e5ea2f3343c367bbad0a52b8e07be7c18b2282536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412340"
---
# <a name="em_setscrollpos-message"></a>Mensaje \_ EM SETSCROLLPOS

Desplaza el contenido de un control de edición enriquecido hasta el punto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) que especifica un punto en el espacio de texto virtual del documento, expresado en píxeles. El documento se desplazará hasta que este punto se encuentra en la esquina superior izquierda de la ventana de control de edición. Si desea cambiar la vista de forma que la esquina superior izquierda de la vista esté dos líneas hacia abajo y un carácter en el borde izquierdo. Se pasará un punto de (7, 22).

El control rich edit comprueba las coordenadas x e y las ajusta si es necesario, para que se muestre una línea completa en la parte superior. También garantiza que el texto nunca se desplace completamente fuera del rectángulo de la vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> </dl>

 

