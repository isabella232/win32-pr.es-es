---
title: EM_GETTYPOGRAPHYOPTIONS mensaje (Richedit.h)
description: Devuelve el estado actual de las opciones de tipografía de un control de edición enriquecido.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d575550e2c239ee5b689deb5874a9803c581151b54100ab227a24d4f29941973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831176"
---
# <a name="em_gettypographyoptions-message"></a>Mensaje \_ EM GETTYPOGRAPHYOPTIONS

Devuelve el estado actual de las opciones de tipografía de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve las opciones de tipografía actuales. Para obtener una lista de opciones, [**vea EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).

## <a name="remarks"></a>Comentarios

Puede activar la separación de línea avanzada mediante el envío [**del mensaje EM \_ SETTYPOGRAPHYOPTIONS.**](em-settypographyoptions.md) El control de edición enriquecido también puede desactivar automáticamente la separación de línea avanzada y normal si es necesario para determinados idiomas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de los controles rich edit](about-rich-edit-controls.md)
</dt> </dl>

 

 





