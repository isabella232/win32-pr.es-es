---
title: EM_GETZOOM mensaje (Richedit.h)
description: Obtiene la relación de zoom actual. La relación de zoom siempre está entre 1/64 y 64. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
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
ms.openlocfilehash: 874feba3022571a69f816a94bc5f56cb29a94929c47a2a8d408b1c8fac7b26ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438115"
---
# <a name="em_getzoom-message"></a>Mensaje \_ EM GETZOOM

Obtiene la relación de zoom actual para un control de edición multilínea o un control de edición enriquecido. La relación de zoom siempre está entre 1/64 y 64.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Recibe el numerador de la proporción de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Recibe el denominador de la relación de zoom.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El mensaje devuelve **TRUE** si se procesa el mensaje, que será si *wParam* y *lParam* no son **NULL.**

## <a name="remarks"></a>Observaciones

**Editar:** Compatible con Windows 10 1809 y versiones posteriores. El control de edición debe tener el estilo extendido **ES \_ EX \_ ZOOMABLE** establecido; para que este mensaje suba efecto, vea [Editar estilos extendidos de control](edit-control-window-extended-styles.md). Para obtener información sobre el control de edición, vea [Editar controles](edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h/Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETZOOM**](em-setzoom.md)
</dt> </dl>

 

 





