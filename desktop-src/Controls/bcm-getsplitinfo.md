---
title: Mensaje de BCM_GETSPLITINFO (commctrl. h)
description: Obtiene información de un control de botón de expansión. Envíe este mensaje explícitamente o mediante la \_ macro Button GetSplitInfo.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996468"
---
# <a name="bcm_getsplitinfo-message"></a>\_Mensaje GETSPLITINFO de BCM

Obtiene información de un control de botón de expansión. Envíe este mensaje explícitamente o mediante la macro [**Button \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Un puntero a una [**estructura \_ SPLITINFO de botón**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) para recibir información sobre el botón. El autor de la llamada es responsable de asignar la memoria para la estructura. Establezca el miembro de **máscara** de esta estructura para determinar la información que se va a recibir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Use este mensaje solo con los estilos de botón [**BS \_ SPLITBUTTON**](button-styles.md) y [**BS \_ DEFSPLITBUTTON**](button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Tipos de botón](button-types-and-styles.md)
</dt> </dl>

 

 





