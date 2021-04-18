---
title: Mensaje EM_GETSCROLLPOS (RichEdit. h)
description: Obtiene la posición de desplazamiento actual del control de edición.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS controles de mensajes de Windows
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
ms.openlocfilehash: 70458abca94e483f8e202f13ecaed3df04a68366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490378"
---
# <a name="em_getscrollpos-message"></a>\_Mensaje GETSCROLLPOS em

Obtiene la posición de desplazamiento actual del control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) . Después de llamar a **em \_ GETSCROLLPOS**, este parámetro contiene un punto en el espacio de texto virtual del documento, expresado en píxeles. Este punto será el punto que se encuentra actualmente en la esquina superior izquierda de la ventana Editar control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje siempre devuelve 1.

## <a name="remarks"></a>Observaciones

Los valores devueltos en la estructura [**Point**](/previous-versions//dd162805(v=vs.85)) son valores de 16 bits (incluso en los campos anchos de 32 bits).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETSCROLLPOS em**](em-setscrollpos.md)
</dt> </dl>

 

