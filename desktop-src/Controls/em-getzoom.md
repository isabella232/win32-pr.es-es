---
title: EM_GETZOOM mensaje (Richedit.h)
description: Obtiene la relación de zoom actual. La proporción de zoom siempre está entre 1/64 y 64. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- EM_GETZOOM controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062174"
---
# <a name="em_getzoom-message"></a>Mensaje \_ DE EM GETZOOM

Obtiene la relación de zoom actual para un control de edición multilínea o un control de edición enriquecido. La proporción de zoom siempre está entre 1/64 y 64.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Recibe el numerador de la relación de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Recibe el denominador de la relación de zoom.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El mensaje devuelve **TRUE** si se procesa el mensaje, que será si *wParam* y *lParam* no son **NULL.**

## <a name="remarks"></a>Observaciones

**Editar:** Compatible con Windows 10 1809 y versiones posteriores. El control de edición debe tener el estilo extendido **\_ ES EX \_ ZOOMABLE;** para que este mensaje tenga efecto, vea [Editar estilos extendidos de control.](edit-control-window-extended-styles.md) Para obtener información sobre el control de edición, vea [Editar controles](edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>Richedit.h/Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ SETZOOM**](em-setzoom.md)
</dt> </dl>

 

 





