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
ms.openlocfilehash: ec41ac5255059b8d40f3a4c2e9b666815b9094fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062070"
---
# <a name="em_setscrollpos-message"></a>Mensaje \_ EM SETSCROLLPOS

Desplaza el contenido de un control de edición enriquecido hasta el punto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) que especifica un punto en el espacio de texto virtual del documento, expresado en píxeles. El documento se desplazará hasta que este punto se encuentra en la esquina superior izquierda de la ventana de control de edición. Si desea cambiar la vista de forma que la esquina superior izquierda de la vista tenga dos líneas hacia abajo y un carácter en el borde izquierdo. Se pasa un punto de (7, 22).

El control rich edit comprueba las coordenadas x e y las ajusta si es necesario, para que se muestre una línea completa en la parte superior. También garantiza que el texto nunca se desplace completamente fuera del rectángulo de vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> </dl>

 

