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
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062180"
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

## <a name="remarks"></a>Observaciones

Puede activar la separación de línea avanzada mediante el envío [**del mensaje EM \_ SETTYPOGRAPHYOPTIONS.**](em-settypographyoptions.md) El control de edición enriquecido también puede desactivar automáticamente la separación de línea avanzada y normal si es necesario para determinados idiomas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



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

 

 





