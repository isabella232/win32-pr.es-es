---
title: Mensaje EM_SETSCROLLPOS (RichEdit. h)
description: Desplaza el contenido de un control Rich Edit al punto especificado.
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492449"
---
# <a name="em_setscrollpos-message"></a>\_Mensaje SETSCROLLPOS em

Desplaza el contenido de un control Rich Edit al punto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que especifica un punto en el espacio de texto virtual del documento, expresado en píxeles. El documento se desplazará hasta que este punto se encuentre en la esquina superior izquierda de la ventana Editar control. Si desea cambiar la vista de forma que la esquina superior izquierda de la vista tenga dos líneas hacia abajo y un carácter en el borde izquierdo. Pasaría un punto de (7, 22).

El control Rich Edit comprueba las coordenadas x e y, y las ajusta si es necesario, para que se muestre una línea completa en la parte superior. También garantiza que el texto nunca se desplaza completamente fuera del rectángulo de la vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETSCROLLPOS em**](em-getscrollpos.md)
</dt> </dl>

 

