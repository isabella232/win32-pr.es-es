---
title: Mensaje EM_GETZOOM (RichEdit. h)
description: Obtiene la relación de zoom actual. La ración de zoom siempre está entre 1/64 y 64. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- EM_GETZOOM controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801370"
---
# <a name="em_getzoom-message"></a>\_Mensaje GETZOOM em

Obtiene la relación de zoom actual para un control de edición de varias líneas o un control Rich Edit. La ración de zoom siempre está entre 1/64 y 64.

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

El mensaje devuelve **true** si se procesa el mensaje, que será si *wParam* e *lParam* no son **null**.

## <a name="remarks"></a>Observaciones

**Editar:** Compatible con Windows 10 1809 y versiones posteriores. El control de edición debe tener el conjunto de estilo extendido **es \_ ex \_** para el que este mensaje tiene un efecto, vea [Edit control Extended Styles](edit-control-window-extended-styles.md). Para obtener información sobre el control de edición, vea [controles de edición](edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h/commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETZOOM em**](em-setzoom.md)
</dt> </dl>

 

 





